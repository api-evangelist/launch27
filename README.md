# Launch27

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

Launch27 is a booking and scheduling platform for cleaning service businesses (maid services), offering online booking, customer/employee/team management, recurring scheduling, payments, and marketing tools. Launch27 was acquired by Fullsteam Operations in 2019 and continues to operate today as an actively sold, independently branded product; Vonigo (a broader field service management platform for home service businesses) is a sister brand under the same Fullsteam Operations portfolio, acquired separately in 2022 - Launch27 is not a Vonigo product line, though the two are frequently compared as Fullsteam-owned competitors in the same space. Launch27 publishes a real, actively used REST API (currently v2.1, with a deprecated v2.0) documented in a public Bitbucket wiki linked from the Launch27 marketing site footer, rather than in first-party developer docs at docs.launch27.com. The API is multi-tenant, meaning every client account gets its own subdomain (e.g. https://acme.launch27.com), and covers booking creation/management for non-logged-in and logged-in customers, booking-form helper data (services, spots, frequencies, custom fields, price estimation), booking policies, and account settings.

**Areas:** Field Service · Home Services · Cleaning Services · Booking · Scheduling · Fullsteam · Vonigo · Real-Time

## Launch27 on APIs.io

Everything profiled for Launch27 is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/launch27/](https://apis.io/providers/launch27/)** — or go straight to one of the APIs or properties below.

### APIs (6)

- [Launch27 Account API](https://apis.io/apis/launch27/launch27-account-api/) — Account/tenant settings and configuration.
- [Launch27 Authentication API](https://apis.io/apis/launch27/launch27-authentication-api/) — Login and JWT bearer token issuance.
- [Launch27 Booking Helpers API](https://apis.io/apis/launch27/launch27-booking-helpers-api/) — Supporting data for building and pricing a booking form.
- [Launch27 Customer Bookings API](https://apis.io/apis/launch27/launch27-customer-bookings-api/) — Authenticated customer-portal booking CRUD.
- [Launch27 Guest Booking API](https://apis.io/apis/launch27/launch27-guest-booking-api/) — Booking creation for non-logged-in customers.
- [Launch27 Policy API](https://apis.io/apis/launch27/launch27-policy-api/) — Booking, reschedule, cancellation, and location policies.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Launch27 Account Notification Channel (WebSocket, minimally documented)](https://apis.io/asyncapis/launch27/launch27-asyncapi/)

#### Event channels (1)

Individual events and webhooks the provider emits.

- [subscribe](https://apis.io/channels/launch27/subscribe/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Launch27 Agentic Access](https://apis.io/agentic-access/launch27/launch27-agentic-access/)

#### Collections (7)

Postman and Open Collection request collections.

- [Launch27 API](https://apis.io/collections/launch27/open-launch27/)
- [Launch27 Account API](https://apis.io/collections/launch27/open-launch27-account-api/)
- [Launch27 Account Authentication API](https://apis.io/collections/launch27/open-launch27-authentication-api/)
- [Launch27 Account Booking Helpers API](https://apis.io/collections/launch27/open-launch27-booking-helpers-api/)
- [Launch27 Account Customer Bookings API](https://apis.io/collections/launch27/open-launch27-customer-bookings-api/)
- [Launch27 Account Guest Booking API](https://apis.io/collections/launch27/open-launch27-guest-booking-api/)
- [Launch27 Account Policy API](https://apis.io/collections/launch27/open-launch27-policy-api/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [Launch27 — asyncapi rules](https://apis.io/rules/launch27/launch27-asyncapi-spectral-rules/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Launch27 Authentication](https://apis.io/security/launch27/launch27-authentication/)
- [Launch27 Domain Security](https://apis.io/security/launch27/launch27-domain-security/)
- [Launch27 Vulnerability Disclosure](https://apis.io/security/launch27/launch27-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Launch27 Plans Pricing](https://apis.io/plans/launch27/launch27-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Launch27 Rate Limits](https://apis.io/rate-limits/launch27/launch27-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Launch27 Finops](https://apis.io/finops/launch27/launch27-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.launch27.com)
- [Documentation](https://docs.launch27.com)
- [API reference](https://bitbucket.org/awoo23/api-2.0/wiki/Home)
- [Blog](https://launch27.com/feed/)

## API Evangelist rating

**Kin Score 30.3** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 66.1 |
| Contract quality | 54.6 |
| Contract governance | 11.4 |
| Operational transparency | 7.9 |
| Developer ergonomics | 32.1 |
| Access clarity | 7.9 |

**Agent readiness 20.7** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | derived (partial credit) |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 17.6** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/launch27/](https://apis.io/providers/launch27/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Launch27: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/launch27/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
