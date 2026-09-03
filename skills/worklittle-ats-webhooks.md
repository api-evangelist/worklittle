---
name: Sync hiring events with webhooks
description: Register, verify, and operate Worklittle webhooks for ATS/HRIS sync without polling.
api: openapi/worklittle-platform-api-openapi.yml
operations: ["GET /business/webhooks", "GET /business/webhooks/{id}"]
generated: '2026-09-03'
method: generated
---

# Sync hiring events with webhooks

Auth: Bearer key with `webhooks:manage`. Management is `POST/GET /webhooks`, `PATCH/DELETE /webhooks/:id`, `POST /webhooks/:id/secret` (rotate), `POST /webhooks/:id/test`, and `GET /webhook-deliveries` — or MCP tools `create_webhook`, `list_webhooks`, `test_webhook`, `list_webhook_deliveries`.

1. Register an HTTPS endpoint and subscribe to event types (`candidate.application_submitted`, `candidate.stage_changed`, `job.published`, `offer.created`, `survey.response_submitted`, … or `"*"`).
2. **Verify every delivery**: compute HMAC-SHA256 over `timestamp.rawBody` with the endpoint secret and timing-safe-compare against `Worklittle-Webhook-Signature` (`v1=` prefix stripped). Read the RAW body before JSON parsing. Reject timestamps older than a few minutes.
3. Dedupe on `Worklittle-Webhook-Id`; `created_at` is Unix seconds.
4. Respond 2xx fast and do heavy work asynchronously — failed deliveries retry with backoff; inspect `GET /webhook-deliveries?endpoint_id=` when debugging.
5. Send `webhook.test` via `POST /webhooks/:id/test` before going live, and rotate secrets with `POST /webhooks/:id/secret` on any suspicion of leak.
