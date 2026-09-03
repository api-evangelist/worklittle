---
name: Search jobs and apply on Worklittle
description: Find roles in the market-wide index, read details, and submit an application — inside quota and billing guardrails.
api: openapi/worklittle-jobs-api-openapi.yml
operations: ["GET /jobs", "GET /jobs/{id}", "POST /jobs/{id}/apply", "POST /jobs/apply"]
generated: '2026-09-03'
method: generated
---

# Search jobs and apply on Worklittle

Auth: `Authorization: Bearer sk-wl-api01-...` (scopes `jobs:read`, `jobs:apply`). MCP equivalents: `search_jobs`, `get_job_details`, `submit_job_application`, `apply_for_job`.

1. **Search** `GET /jobs` with `q`/`title` (title-substring match — company names do NOT belong in this field; negatives use a leading dash: `software engineer, -senior`), `company` for employer slugs (`-slug` excludes), `limit`, `cursor`. Rows in `data[]` are snippets; page with `meta.next_cursor`. The free quota is 1,000 jobs returned per UTC month — keep `limit` small and cache.
2. **Detail** `GET /jobs/{id}` with the row's `job_id`. Raw `description_text` and cached AI never bill; `?summary=true` triggers first-time AI generation (100 free/org/day, then tokens).
3. **Apply — hosted jobs**: `POST /jobs/{id}/apply` ($0.01 per successful submit; read `application_fields` from the detail first). Only employer-posted Worklittle jobs accept this — scraped-index listings with an external `apply_url` do not.
4. **Apply — Apply with AI**: `POST /jobs/apply` starts an AI session that fills the employer's real application (~$0.01–$0.03 in tokens). You can take control or stop before submit.

Errors arrive as `{"error":{code,message,documentation_url}}`. On `429 RATE_LIMITED` honor `Retry-After: 60`; on `QUOTA_EXCEEDED` stop until the UTC month resets. `402 PAYMENT_REQUIRED` means billing — do not retry. No idempotency keys exist: never blind-retry a paid apply after a timeout without checking `GET /jobs/applied` first.
