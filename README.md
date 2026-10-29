# Crawl4AI

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Crawl4AI is an open-source, Apache-2.0 web crawler and scraper built to turn any URL into clean, LLM-ready data — Markdown, typed JSON, screenshots, PDFs, or a map of every URL on a domain. Operated by CONTEXT4AI PTE LTD of Singapore and created by Hossein Tohidi (@unclecode), the project pairs a 79,000-star Python library and self-hostable Docker API server with a hosted Cloud API at gate.crawl4ai.com that serves scrape, search, answer, extract and bulk-job endpoints from three regions, plus a live remote MCP server that exposes the same capabilities to agents as five native tools. Self-hosting is free and unmetered; the hosted tier is free at 5,000 searches and 1,000 scrapes a month.

**Areas:** AI Automation · Web Crawling · Web Scraping · Data Extraction · Search · LLM Tooling · Agents · MCP · Open Source

## Crawl4AI on APIs.io

Everything profiled for Crawl4AI is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/crawl4ai/](https://apis.io/providers/crawl4ai/)** — or go straight to one of the APIs or properties below.

### APIs (4)

- [Crawl4AI Cloud API](https://apis.io/apis/crawl4ai/crawl4ai/) — The hosted Crawl4AI API. One key, plain JSON, one fast endpoint per job: POST /scrape turns a URL into clean Markdown or HTML, GET /search runs a…
- [Crawl4AI Cloud v1 API](https://apis.io/apis/crawl4ai/crawl4ai-v1/) — The versioned Crawl4AI cloud surface the first-party Cloud SDKs and the Claude Code plugin call. Covers POST /v1/markdown, /v1/screenshot (screenshot and…
- [Crawl4AI Self-Hosted API](https://apis.io/apis/crawl4ai/crawl4ai-docker/) — The Apache-2.0 API server that ships inside the crawl4ai project and the unclecode/crawl4ai Docker image, serving on port 11235 on infrastructure the…
- [Crawl4AI Crawl API](https://apis.io/apis/crawl4ai/crawl4ai-crawl-api/) — The Crawl API from Crawl4AI — 2 operation(s) for crawl.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Crawl4Ai Webhooks](https://apis.io/asyncapis/crawl4ai/crawl4ai-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [Crawl4AI Cloud MCP Server](https://apis.io/servers/crawl4ai/crawl4ai-cloud-mcp-server/)

#### Overlays (2)

OpenAPI overlays, including conversational phrasing for each operation.

- [Crawl4Ai Crawl Api Phrasing Overlay](https://apis.io/overlays/crawl4ai/crawl4ai-crawl-api-phrasing-overlay/)
- [Crawl4Ai Platform Gateway Overlay](https://apis.io/overlays/crawl4ai/crawl4ai-platform-gateway-overlay/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Crawl4Ai Authentication](https://apis.io/security/crawl4ai/crawl4ai-authentication/)
- [Crawl4Ai Domain Security](https://apis.io/security/crawl4ai/crawl4ai-domain-security/)
- [Crawl4Ai Vulnerability Disclosure](https://apis.io/security/crawl4ai/crawl4ai-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Crawl4Ai Plans Pricing](https://apis.io/plans/crawl4ai/crawl4ai-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Crawl4Ai Rate Limits](https://apis.io/rate-limits/crawl4ai/crawl4ai-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Crawl4Ai Finops](https://apis.io/finops/crawl4ai/crawl4ai-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://crawl4ai.com)
- [Documentation](https://docs.crawl4ai.com)
- [Getting started](https://docs.crawl4ai.com/core/quickstart/)
- [API reference](https://gate.crawl4ai.com/docs)
- [Pricing](https://gate.crawl4ai.com/#pricing)
- [Sign up](https://gate.crawl4ai.com/dashboard/)
- [Support](https://discord.gg/jP8KfhDhyN)
- [Blog](https://docs.crawl4ai.com/blog/)
- [Terms of service](https://gate.crawl4ai.com/legal/#terms)
- [Privacy policy](https://gate.crawl4ai.com/legal/#privacy)
- [GitHub](https://github.com/unclecode)
- [Status](https://unclecode.github.io/crawl4ai-status/)

## API Evangelist rating

**Kin Score 67.1** — exemplar · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 75.0 |
| Contract quality | 47.3 |
| Contract governance | 18.2 |
| Operational transparency | 97.4 |
| Developer ergonomics | 85.7 |
| Access clarity | 71.1 |

**Agent readiness 38.7** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | verified |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | yes |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | distinct |

**Regulatory alignment 30.4** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/crawl4ai/](https://apis.io/providers/crawl4ai/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Crawl4AI: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/crawl4ai/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
