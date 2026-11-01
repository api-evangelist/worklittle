# Worklittle

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

Worklittle is a workforce-intelligence platform covering job discovery, auto-apply, embedded careers boards, ATS sync and sourcing over one API. It splits into two halves: Jobs, the market-wide index plus candidate-facing apply and document tools including commute search on a geocoded job map, and Business, an employer hiring workspace with postings, an ATS pipeline, employees, HR documents and webhooks. The public contract is a $ref-based OpenAPI 3.1 document served from docs.worklittle.com/openapi/openapi.yaml resolving to 47 paths across jobs, platform and job-board surfaces on api.worklittle.com, with bearer sk-wl-api01 authentication plus an OAuth 2.0 authorization server (RFC 8414, PKCE, dynamic registration) backing MCP Connect. Worklittle operates a live remote MCP server at mcp.worklittle.com (101 documented tools, 13 anonymously introspectable), ships first-party TypeScript and Python SDKs and a CLI on npm, PyPI and Homebrew, and publishes a 99KB llms.txt plus a docs agent manifest.

**Areas:** Job Search · Applicant Tracking · Recruiting · Workforce Intelligence · Job Board · Webhook · MCP

## Worklittle on APIs.io

Everything profiled for Worklittle is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/worklittle/](https://apis.io/providers/worklittle/)** — or go straight to one of the APIs or properties below.

### APIs (16)

- [Worklittle Job Boards API](https://apis.io/apis/worklittle/worklittle-job-boards-api/) — The Job Boards API from Worklittle — 8 operation(s) for job boards.
- [Worklittle Jobs API](https://apis.io/apis/worklittle/worklittle-jobs-api/) — The consumer Jobs surface of the Worklittle API — 9 operations for market-wide job search, job detail, map clusters, suggestions, company search, market…
- [Worklittle Agent Documents API](https://apis.io/apis/worklittle/worklittle-agent-documents-api/) — The agent-documents API from Worklittle — 4 operation(s) for agent-documents.
- [Worklittle Apply API](https://apis.io/apis/worklittle/worklittle-apply-api/) — The apply API from Worklittle — 5 operation(s) for apply.
- [Worklittle Attendance API](https://apis.io/apis/worklittle/worklittle-attendance-api/) — The attendance API from Worklittle — 1 operation(s) for attendance.
- [Worklittle Billing API](https://apis.io/apis/worklittle/worklittle-billing-api/) — The billing API from Worklittle — 1 operation(s) for billing.
- [Worklittle Candidates API](https://apis.io/apis/worklittle/worklittle-candidates-api/) — The candidates API from Worklittle — 3 operation(s) for candidates.
- [Worklittle Documents API](https://apis.io/apis/worklittle/worklittle-documents-api/) — The documents API from Worklittle — 1 operation(s) for documents.
- [Worklittle Email Offers API](https://apis.io/apis/worklittle/worklittle-email-offers-api/) — The email-offers API from Worklittle — 3 operation(s) for email-offers.
- [Worklittle Employees API](https://apis.io/apis/worklittle/worklittle-employees-api/) — The employees API from Worklittle — 2 operation(s) for employees.
- [Worklittle Employer Jobs API](https://apis.io/apis/worklittle/worklittle-employer-jobs-api/) — The employer-jobs API from Worklittle — 1 operation(s) for employer-jobs.
- [Worklittle Job Listings API](https://apis.io/apis/worklittle/worklittle-job-listings-api/) — The job-listings API from Worklittle — 2 operation(s) for job-listings.
- [Worklittle Organization API](https://apis.io/apis/worklittle/worklittle-organization-api/) — The organization API from Worklittle — 2 operation(s) for organization.
- [Worklittle People API](https://apis.io/apis/worklittle/worklittle-people-api/) — The people API from Worklittle — 3 operation(s) for people.
- [Worklittle Surveys API](https://apis.io/apis/worklittle/worklittle-surveys-api/) — The surveys API from Worklittle — 2 operation(s) for surveys.
- [Worklittle Webhooks API](https://apis.io/apis/worklittle/worklittle-webhooks-api/) — The webhooks API from Worklittle — 2 operation(s) for webhooks.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Worklittle Webhooks](https://apis.io/asyncapis/worklittle/worklittle-webhooks/)

#### MCP servers (2)

Model Context Protocol servers that expose the API to agents.

- [Moved to /providers/worklittle/](https://apis.io/servers/worklittle/mcp/)
- [worklittle](https://apis.io/servers/worklittle/worklittle/)

#### Agent skills (13)

Agent skills built on the API.

- [apply-with-ai](https://apis.io/agent-skills/worklittle/apply-with-ai/)
- [candidates](https://apis.io/agent-skills/worklittle/candidates/)
- [capability-map](https://apis.io/agent-skills/worklittle/capability-map/)
- [employees](https://apis.io/agent-skills/worklittle/employees/)
- [job-alerts](https://apis.io/agent-skills/worklittle/job-alerts/)
- [job-search](https://apis.io/agent-skills/worklittle/job-search/)
- [market-stats](https://apis.io/agent-skills/worklittle/market-stats/)
- [mcp-install](https://apis.io/agent-skills/worklittle/mcp-install/)
- [people-search](https://apis.io/agent-skills/worklittle/people-search/)
- [post-a-job](https://apis.io/agent-skills/worklittle/post-a-job/)
- [resume-cover-letter](https://apis.io/agent-skills/worklittle/resume-cover-letter/)
- [worklittle-best-practices](https://apis.io/agent-skills/worklittle/worklittle-best-practices/)
- [worklittle-docs](https://apis.io/agent-skills/worklittle/worklittle-docs/)

#### Overlays (2)

OpenAPI overlays, including conversational phrasing for each operation.

- [Worklittle Jobs Api Overlay](https://apis.io/overlays/worklittle/worklittle-jobs-api-overlay/)
- [Worklittle Platform Api Overlay](https://apis.io/overlays/worklittle/worklittle-platform-api-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Worklittle Authentication](https://apis.io/security/worklittle/worklittle-authentication/)
- [Worklittle Domain Security](https://apis.io/security/worklittle/worklittle-domain-security/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Worklittle Scopes](https://apis.io/scopes/worklittle/worklittle-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Worklittle Plans Pricing](https://apis.io/plans/worklittle/worklittle-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Worklittle Rate Limits](https://apis.io/rate-limits/worklittle/worklittle-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://worklittle.com)
- [Documentation](https://docs.worklittle.com)
- [Getting started](https://docs.worklittle.com/jobs/get-started/overview)
- [Pricing](https://docs.worklittle.com/jobs/get-started/pricing)
- [Sign up](https://worklittle.com/login)
- [Support](https://docs.worklittle.com/help/privacy-safety/contact-support)
- [Terms of service](https://worklittle.com/terms-of-use)
- [Privacy policy](https://worklittle.com/privacy)
- [GitHub](https://github.com/worklittle)
- [Status](https://docs.worklittle.com/business/resources/status)

## API Evangelist rating

**Kin Score 53.1** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 80.0 |
| Contract quality | 52.4 |
| Contract governance | 4.5 |
| Operational transparency | 57.9 |
| Developer ergonomics | 42.9 |
| Access clarity | 65.8 |

**Agent readiness 52.5** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | verified |
| Auth Clarity | served (partial credit) |
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
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | — |

**Regulatory alignment 34.3** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/worklittle/](https://apis.io/providers/worklittle/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Worklittle: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/worklittle/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
