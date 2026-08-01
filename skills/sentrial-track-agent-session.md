---
name: Track an agent session end-to-end
description: Open a Sentrial session, record the tool calls and decisions your agent makes, then close the session with final metrics so Sentrial can detect and diagnose issues.
api: openapi/sentrial-openapi.yml
operations: [createSession, createEvent, updateSession]
---

# Track an agent session end-to-end

Use this when instrumenting an AI agent run with Sentrial's ingestion API.

## Auth
- Base URL: `https://api.sentrial.com`
- Every request: header `Authorization: Bearer sentrial_live_...` (create keys in Settings -> API Keys; read from `SENTRIAL_API_KEY`, never hard-code).
- All bodies are `application/json`.

## Steps
1. **Open the session** — `createSession` (`POST /api/sdk/sessions`). Required: `name`, `agentName`, `userId`. Optional `metadata` object. Keep the returned `id` (prefix `sess_`) for every later call.
2. **Record each event** — `createEvent` (`POST /api/sdk/events`) with `sessionId` set to that `id`. Set `eventType` to one of `tool_call`, `llm_decision`, `state_change`, `error`. For `tool_call` include `toolName`, `toolInput`, `toolOutput`; for `llm_decision` include `reasoning`, `alternativesConsidered`, `confidence`. Add `estimatedCost` where known.
3. **Close the session** — `updateSession` (`PATCH /api/sdk/sessions/{id}`). Set `status` to `completed` or `failed`, `success` bool, and roll up `estimatedCost`, `durationMs`, `promptTokens`, `completionTokens`, `totalTokens`, and any `customMetrics`.

## Rules
- Identifiers are opaque prefixed strings (`sess_`, `evt_`) — pass them back verbatim.
- There is no documented idempotency key; do not blind-retry a create on an ambiguous response — check before re-posting.
- Errors are `{ "error", "message" }`: `400` bad/missing fields, `401` bad key, `403` no permission, `404` unknown `sessionId`, `500` retryable. See `errors/sentrial-error-codes.yml`.
- If you already emit OpenTelemetry traces, prefer OTel ingestion over manual event posting (see `conventions/`).
