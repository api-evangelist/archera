# Archera

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

Archera is a cloud financial operations (FinOps) platform that helps organizations reduce cloud spend by 20-30% through intelligent commitment management and insured, short-term cloud commitments across AWS, Azure, and Google Cloud. Its Guaranteed Commitments (Guaranteed Savings Plans, Guaranteed Reserved Instances, and Guaranteed Committed Use Discounts) provide flexible terms as short as 30 days with risk protection for unused capacity. The Archera Public API exposes commitment plans, commitments, exchanges, metrics, resources, orgs, and uploads over a REST v1 interface authenticated with an API key or OAuth 2.0 (Authorization Code + PKCE), and Archera operates a hosted remote MCP server so AI assistants can query cloud cost data and optimization recommendations directly. A Partner API supports onboarding customers and creating marketplace offers via AWS CPPO, Microsoft MPO, and Google MCPO.

**Areas:** Company · Developer Tools · FinOps · Cloud Cost Management · Cloud Commitments · Cost Optimization · MCP · AWS · Microsoft Azure · Google Cloud · Reserved Instances

## Archera on APIs.io

Everything profiled for Archera is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/archera/](https://apis.io/providers/archera/)** — or go straight to one of the APIs or properties below.

### APIs (10)

- [Archera Partner API](https://apis.io/apis/archera/archera-partner-api/) — Partner API for onboarding customers, managing their optimization strategies, and creating marketplace offers through AWS CPPO, Microsoft MPO / ISV-to-CSP…
- [Archera Commitment Plans API](https://apis.io/apis/archera/archera-commitment-plans-api/) — API for managing commitment plans
- [Archera Commitments API](https://apis.io/apis/archera/archera-commitments-api/) — API for retrieving and analyzing cloud commitment inventory, including Reserved Instances, Savings Plans, and Azure Reserved VM Instances. Provides access…
- [Archera Exchanges API](https://apis.io/apis/archera/archera-exchanges-api/) — API for commitment exchange recommendations
- [Archera Metrics API](https://apis.io/apis/archera/archera-metrics-api/) — High level metrics to track commitment performance.
- [Archera Orgs API](https://apis.io/apis/archera/archera-orgs-api/) — Endpoints for organizations accessible to the authenticated user
- [Archera Resources API](https://apis.io/apis/archera/archera-resources-api/) — API for retrieving and analyzing infrastructure resources
- [Archera Uploads API](https://apis.io/apis/archera/archera-uploads-api/) — API for uploading billing files for savings analysis
- [Archera Well-Known API](https://apis.io/apis/archera/archera-well-known-api/) — OAuth 2.0 discovery endpoints (JWKS and Authorization Server Metadata)
- [Archera O Auth API](https://apis.io/apis/archera/archera-oauth-api/) — OAuth 2.0 authorization endpoints for third-party integrations

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [archera](https://apis.io/servers/archera/archera/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Archera Agentic Access](https://apis.io/agentic-access/archera/archera-agentic-access/)

#### Collections (9)

Postman and Open Collection request collections.

- [Archera.ai Commitment Plans API](https://apis.io/collections/archera/open-archera-commitment-plans-api/)
- [Archera.ai Commitment Plans Commitments API](https://apis.io/collections/archera/open-archera-commitments-api/)
- [Archera.ai Commitment Plans Exchanges API](https://apis.io/collections/archera/open-archera-exchanges-api/)
- [Archera.ai Commitment Plans Metrics API](https://apis.io/collections/archera/open-archera-metrics-api/)
- [Archera.ai Commitment Plans OAuth API](https://apis.io/collections/archera/open-archera-oauth-api/)
- [Archera.ai Commitment Plans Orgs API](https://apis.io/collections/archera/open-archera-orgs-api/)
- [Archera.ai Commitment Plans Resources API](https://apis.io/collections/archera/open-archera-resources-api/)
- [Archera.ai Commitment Plans Uploads API](https://apis.io/collections/archera/open-archera-uploads-api/)
- [Archera.ai Commitment Plans Well-Known API](https://apis.io/collections/archera/open-archera-well-known-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Archera Openapi Overlay](https://apis.io/overlays/archera/archera-openapi-overlay/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Archera Authentication](https://apis.io/security/archera/archera-authentication/)
- [Archera Domain Security](https://apis.io/security/archera/archera-domain-security/)
- [Archera Trust Center](https://apis.io/security/archera/archera-trust-center/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Archera Scopes](https://apis.io/scopes/archera/archera-scopes/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://archera.ai)
- [Documentation](https://docs.archera.ai)
- [Getting started](https://docs.archera.ai/getting-started/how-to-sign-up-with-archera)
- [API reference](https://docs.archera.ai/api-reference)
- [Pricing](https://www.archera.ai/pricing)
- [Sign up](https://app.archera.ai/signup)
- [Support](https://help.archera.ai)
- [Blog](https://www.archera.ai/blog)
- [Compliance](https://www.archera.ai/trust)
- [Terms of service](https://www.archera.ai/terms)
- [Privacy policy](https://www.archera.ai/privacy)

## API Evangelist rating

**Kin Score 44.2** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 75.0 |
| Contract quality | 40.1 |
| Contract governance | 18.2 |
| Operational transparency | 0.0 |
| Developer ergonomics | 54.2 |
| Access clarity | 53.9 |

**Agent readiness 50.5** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | verified |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | — |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 39.2** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/archera/](https://apis.io/providers/archera/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Archera: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/archera/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
