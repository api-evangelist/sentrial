---
name: Record a tool call or decision event
description: Emit a single Sentrial event (tool call, LLM decision, state change, or error) inside an existing agent session.
api: openapi/sentrial-openapi.yml
operations: [createEvent]
---

# Record a tool call or decision event

Use this to log one event against a session you already opened (see `sentrial-track-agent-session`).

## Auth
- `POST https://api.sentrial.com/api/sdk/events`, header `Authorization: Bearer sentrial_live_...`, JSON body.

## Call
`createEvent` — required `sessionId` (the `sess_...` id) and `eventType`.
- `tool_call`: set `toolName`, `toolInput` (object), `toolOutput` (object), optional `reasoning`, `estimatedCost`.
- `llm_decision`: set `reasoning`, `alternativesConsidered` (array), `confidence` (0.0–1.0), optional `estimatedCost`.
- `state_change` / `error`: set `reasoning` and any relevant fields.

Response returns `id` (prefix `evt_`), `sessionId`, `eventType`, `createdAt`.

## Rules
- A `404` means the `sessionId` is wrong or the session does not exist — open one first.
- `400` means a required field is missing or `eventType` is not one of the four allowed values.
- Keep `confidence` within 0.0–1.0. Costs are USD numbers.
