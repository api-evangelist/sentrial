# Sentrial

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

Sentrial is an observability platform for AI agents, backed by Y Combinator. It tracks every agent session, tool call, and LLM interaction, then automatically detects issues, diagnoses root causes, and helps teams fix them in code. Developers instrument agents with the Sentrial Python or TypeScript SDK (one-line integrations for LangChain, CrewAI, AutoGen, Mastra, the Vercel AI SDK, and the Claude Agent SDK), by sending OpenTelemetry traces, or by calling the REST ingestion API (https://api.sentrial.com) directly to create sessions and record events. A `sentrial` CLI ships with the SDK for local setup, scriptable session/event inspection, diagnosis, and CI regression gates.

**Areas:** Company · AI Agents · Observability · Monitoring · LLM · Developer Tools · Tracing

## Sentrial on APIs.io

Everything profiled for Sentrial is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/sentrial/](https://apis.io/providers/sentrial/)** — or go straight to one of the APIs or properties below.

### APIs (2)

- [Sentrial Events API](https://apis.io/apis/sentrial/sentrial-events-api/) — Track events within agent sessions.
- [Sentrial Sessions API](https://apis.io/apis/sentrial/sentrial-sessions-api/) — Create and manage agent sessions.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [sentrial](https://apis.io/servers/sentrial/sentrial/)

#### Collections (2)

Postman and Open Collection request collections.

- [Sentrial SDK Events API](https://apis.io/collections/sentrial/open-sentrial-events-api/)
- [Sentrial SDK Events Sessions API](https://apis.io/collections/sentrial/open-sentrial-sessions-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Sentrial Openapi Overlay](https://apis.io/overlays/sentrial/sentrial-openapi-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Sentrial Authentication](https://apis.io/security/sentrial/sentrial-authentication/)
- [Sentrial Domain Security](https://apis.io/security/sentrial/sentrial-domain-security/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.sentrial.com/)
- [Documentation](https://www.sentrial.com/docs)
- [Getting started](https://www.sentrial.com/docs/quickstart)
- [API reference](https://www.sentrial.com/docs/api/sessions)
- [Sign up](https://sentrial.com/signup)
- [Blog](https://www.sentrial.com/blog)
- [Terms of service](https://www.sentrial.com/terms)
- [Privacy policy](https://www.sentrial.com/privacy)
- [GitHub](https://github.com/sentrialdev)

## API Evangelist rating

**Kin Score 22.9** — emerging · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 14.3 |
| Contract governance | 4.5 |
| Operational transparency | 2.6 |
| Developer ergonomics | 58.9 |
| Access clarity | 0.0 |

**Agent readiness 24.3** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | verified |
| Rate Limit Signal | — |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 15.5** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/sentrial/](https://apis.io/providers/sentrial/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Sentrial: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/sentrial/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
