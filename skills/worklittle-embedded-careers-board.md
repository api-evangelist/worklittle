---
name: Build an embedded careers board
description: Serve a custom employer careers site from the public Job Boards API, with ETag caching and webhook-driven revalidation.
api: openapi/worklittle-job-boards-api-openapi.yml
operations: ["GET /job-boards/{company}", "GET /job-boards/{company}/board", "GET /job-boards/{company}/jobs", "GET /job-boards/{company}/jobs/{idOrSlug}", "GET /job-boards/{company}/jobs/{idOrSlug}/json-ld", "POST /job-boards/{company}/jobs/{idOrSlug}/apply"]
generated: '2026-09-03'
method: generated
---

# Build an embedded careers board

No key needed — the public board surface is CORS `*` with per-IP limits (120/min reads, 20/min applies). A Bearer key raises GET limits.

1. `GET /job-boards/{company}/board` returns the organization profile plus the job list in one call; filter with `q`, `department`, `workplace_type`, `employment_type`, `location`, and add `include=facets` for filter counts.
2. Honor `ETag`/`304 Not Modified` on profile and board routes — poll cheaply.
3. Render detail from `GET /job-boards/{company}/jobs/{idOrSlug}` and embed the output of `.../json-ld` (Google JobPosting structured data) so roles index into Google Jobs.
4. Accept applications with `POST .../apply`; `.../parse-resume` pre-fills fields from an uploaded resume (20/min per IP).
5. For instant freshness instead of polling, register a webhook (`POST /webhooks`, scope `webhooks:manage`) for `job.published`, `job.updated`, `job.closed` — payloads carry `slug`, `organization.slug`, `public_visible`, `accepting_applicants` exactly for careers-page cache revalidation.
