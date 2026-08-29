---
name: crawl4ai-bulk-crawl-job
description: >-
  Run a large Crawl4AI Cloud crawl as an async job — submit up to 10,000 URLs,
  poll to completion, page through the NDJSON results, and retry only what failed.
  Use when a scrape list is too big for a single batch call.
api: Crawl4AI Cloud API
base_url: https://gate.crawl4ai.com
generated: '2026-08-29'
method: generated
source: >-
  https://gate.crawl4ai.com/docs and https://gate.crawl4ai.com/llms.txt. Crawl4AI
  publishes no OpenAPI for this surface, so steps cite METHOD + PATH verbatim from
  the docs rather than operationIds — there are none to cite.
operations:
  - 'POST /scrape/jobs'
  - 'GET /scrape/jobs/{id}'
  - 'GET /scrape/jobs/{id}/results'
  - 'POST /scrape/jobs/{id}/retry'
  - 'POST /scrape/batch'
---

# Bulk crawl with Crawl4AI Cloud

Pick the right surface first. Up to ~50 URLs, use `POST /scrape/batch` and read the
NDJSON stream as it lands. Above that, and up to 10,000, use the job API below.

## 1. Authenticate

Every call needs `Authorization: Bearer sk_live_...` (`x-api-key` also works).
An unauthenticated call returns **401 with an empty body** — there is no error
message to read, so check the status, not the payload.

## 2. Submit the job

```
POST /scrape/jobs
{"urls": ["https://a.com", "https://b.com"], "format": "md"}
-> {"job_id": "j_...", "status": "pending"}
```

Any `/scrape` field — `format`, `proxy`, `country`, `parse` — applies to every URL
in the job. Choose `proxy` deliberately: `off` costs 1x per page, `on`
(residential) 5x, `crawl4ai` (Web-Unlocker) 10x.

**Before you submit, know that this cannot be undone.** The gate job surface
publishes submit, status, results and retry — and no cancel. A 10,000-URL job you
did not mean to send will run to completion and bill for it. Size the list with
`POST /v1/map` on the v1 API if you need to see a domain's URLs first.

## 3. Poll

```
GET /scrape/jobs/{id}          -> status + counts
GET /scrape/jobs/{id}?full=1   -> per-URL detail
```

Poll on an interval (the provider's own example sleeps 2s) until `status` is
`done`. There is no webhook on this surface — `webhook_url` exists on the v1 API
and the self-hosted server, not here.

## 4. Read the results

```
GET /scrape/jobs/{id}/results?after=N
```

NDJSON, 500 lines per page, one line per URL: `{"url":"...","ok":true,"result":{...}}`.
Advance `after` by the number of lines you consumed. Consume the stream line by
line rather than buffering the whole page.

## 5. Retry only the failures

```
POST /scrape/jobs/{id}/retry
```

Re-runs just the URLs that failed. Each retry is billable and is itself
irreversible.

## Error handling

There is **no idempotency key** on this API. If a submit call times out you cannot
safely re-send it — poll `GET /scrape/jobs/{id}` with the id you have, or list
what exists, before submitting again.

| Status | Do |
|---|---|
| 401 | Key missing or invalid. Body is empty; fix the header. |
| 429 | Wait `X-RateLimit-Reset` **seconds** (not a timestamp), then retry. |
| 503 | Retry after 5s, max 3 attempts. |
| 504 | Page too slow — narrow the list or accept the failure and retry it. |
| 5xx | Retry once after 2s. |

Every response carries `X-RateLimit-Limit`, `X-RateLimit-Remaining` and
`X-RateLimit-Reset`; read them rather than guessing a backoff.

## Cost control

Repeated URLs are served from a shared archive, and every result carries which
engine served it and whether it came from cache. Do not set `bypass_cache` on a
bulk job unless freshness is the point — it turns every cached hit into a paid fetch.
