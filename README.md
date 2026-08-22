# Launch27 (launch27)

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

Launch27 is a booking and scheduling platform for cleaning service businesses (maid services), offering online booking, customer/employee/team management, recurring scheduling, payments, and marketing tools.

## Ownership and operating status

Launch27 was acquired by **Fullsteam Operations** in 2019 and continues to operate today as an actively sold, independently branded product - the pricing page, free trial signup, and support channels are all live and current. **Vonigo**, a broader field service management platform for home service businesses, is a **sister brand** under the same Fullsteam Operations portfolio, acquired separately in 2022. Launch27 is not a Vonigo product line or white-label of Vonigo; the two are frequently compared as Fullsteam-owned competitors serving overlapping markets (cleaning/home services), and no public source indicates the two products have been merged or that Launch27 has been folded into Vonigo's technology.

## Access model

Launch27 publishes a real, actively used REST API. It is **not** documented at the first-party `docs.launch27.com` knowledge base (which covers end-user/admin features, integrations, and FAQs). Instead, the actual API reference is a public **Bitbucket wiki** linked directly from the footer of launch27.com ("Launch27 API"): [https://bitbucket.org/awoo23/api-2.0/wiki/Home](https://bitbucket.org/awoo23/api-2.0/wiki/Home). It documents the current **v2.1** API plus a deprecated **v2.0**.

The API is **multi-tenant**: every Launch27 client account is issued its own subdomain (e.g. `https://acme.launch27.com`, or `https://acme-sandbox.l27.co` for sandbox), and all API calls are scoped to that tenant. Authentication is via a JWT bearer token returned from a `/login` call (legacy `email:token` header auth was retired March 1, 2023). No self-serve API key/developer-portal signup exists independent of a paying Launch27 account; the API exists primarily to power Launch27's own embeddable booking widgets and customer self-service portal, and is used by integration platforms (Zapier, Pipedream, Latenode) and third-party API catalogs (API Tracker) as an integration surface.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/launch27/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/launch27/refs/heads/main/apis.yml)

## Tags

- Field Service Management
- Home Services
- Cleaning Services
- Booking
- Scheduling
- Fullsteam
- Vonigo

## Timestamps

- **Created:** 2026-07-04
- **Modified:** 2026-07-04

## APIs

### Launch27 Authentication API

Authenticate a Launch27 customer or staff user and return a JWT (bearer token) used for subsequent authenticated requests. Legacy email:token header authentication was retired March 1, 2023 in favor of JWT.

- **Human URL:** [https://bitbucket.org/awoo23/api-2.0/wiki/Login](https://bitbucket.org/awoo23/api-2.0/wiki/Login)
- **Base URL:** `https://{tenant}.launch27.com/v1`

#### Properties

- [Documentation](https://bitbucket.org/awoo23/api-2.0/wiki/Home)
- [API Reference](https://bitbucket.org/awoo23/api-2.0/wiki/General_notes)
- [OpenAPI](openapi/launch27-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/launch27.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/launch27.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Launch27 Account Settings API

Read a client account's configuration - branding, currency, country and states, enabled feature flags (multi-location, gift cards, tips, sales tax, SMS reminders, mobile app, etc.), locale/date preferences, accepted payment methods, and the default location. Some fields (Stripe public key, team permissions, alerts, admin id, and a `wss://` pubsub notification URL) are only present for authenticated staff/team requests.

- **Human URL:** [https://bitbucket.org/awoo23/api-2.0/wiki/Get_settings](https://bitbucket.org/awoo23/api-2.0/wiki/Get_settings)
- **Base URL:** `https://{tenant}.launch27.com/v1`

#### Properties

- [API Reference](https://bitbucket.org/awoo23/api-2.0/wiki/Get_settings)
- [OpenAPI](openapi/launch27-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [AsyncAPI](asyncapi/launch27-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/v2.6.0)
- [Postman Collection](collections/launch27.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### Launch27 Booking Helpers API

Supporting data needed to build and price a booking form - the booking form's field/heading/appearance setup, configured services/extras/pricing parameters, available date/time spots (grid or list, for new bookings or reschedules), location resolution by address, recurring frequencies (with discounts), custom fields, next recurring service date for a frequency, and detailed price/discount/tax estimation.

- **Human URL:** [https://bitbucket.org/awoo23/api-2.0/wiki/Services_for_booking](https://bitbucket.org/awoo23/api-2.0/wiki/Services_for_booking)
- **Base URL:** `https://{tenant}.launch27.com/v1`

#### Properties

- [Documentation](https://bitbucket.org/awoo23/api-2.0/wiki/Booking_form_setup)
- [API Reference](https://bitbucket.org/awoo23/api-2.0/wiki/Price_estimation_for_booking)
- [OpenAPI](openapi/launch27-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/launch27.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/launch27.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Launch27 Booking Policies API

Read the account's new-booking lead-time policy, reschedule lead-time policy, late-cancellation fee/percentage and reason-required policy, and multi-location "prevent booking if no matching location" policy. These policies are also enforced (not just described) by the Booking Helpers API's spots endpoint.

- **Human URL:** [https://bitbucket.org/awoo23/api-2.0/wiki/New_booking_policy](https://bitbucket.org/awoo23/api-2.0/wiki/New_booking_policy)
- **Base URL:** `https://{tenant}.launch27.com/v1`

#### Properties

- [API Reference](https://bitbucket.org/awoo23/api-2.0/wiki/New_booking_policy)
- [API Reference](https://bitbucket.org/awoo23/api-2.0/wiki/Booking_cancellation_policy)
- [OpenAPI](openapi/launch27-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Launch27 Guest Booking API

Create a new booking as a first-time, non-logged-in customer - submits customer details, address, service date/arrival window, selected services/extras/pricing parameters, discount code, tip, custom field answers, and payment method (cash, check, PayPal, or a Stripe.js token) in a single call, used to power embeddable/white-label booking widgets.

- **Human URL:** [https://bitbucket.org/awoo23/api-2.0/wiki/Create_booking_as_non-logged-in](https://bitbucket.org/awoo23/api-2.0/wiki/Create_booking_as_non-logged-in)
- **Base URL:** `https://{tenant}.launch27.com/v1`

#### Properties

- [API Reference](https://bitbucket.org/awoo23/api-2.0/wiki/Create_booking_as_non-logged-in)
- [OpenAPI](openapi/launch27-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/launch27.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### Launch27 Customer Bookings API

Authenticated customer-portal operations on a logged-in customer's own bookings - list (with date range, free-text, completed/feedback filters, paging), count, get a single booking's full detail, create a new booking (including "book this again" from a prior booking), update/reschedule an existing booking, and cancel a booking (handling late-cancellation confirmation and recurring-series options).

- **Human URL:** [https://bitbucket.org/awoo23/api-2.0/wiki/Get_bookings_for_customer](https://bitbucket.org/awoo23/api-2.0/wiki/Get_bookings_for_customer)
- **Base URL:** `https://{tenant}.launch27.com/v1`

#### Properties

- [API Reference](https://bitbucket.org/awoo23/api-2.0/wiki/Get_bookings_for_customer)
- [API Reference](https://bitbucket.org/awoo23/api-2.0/wiki/Create_booking_for_customer)
- [OpenAPI](openapi/launch27-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/launch27.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/launch27.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/launch-27)
- [Website](https://www.launch27.com)
- [Documentation](https://docs.launch27.com)
- [API Reference](https://bitbucket.org/awoo23/api-2.0/wiki/Home)
- [Plans](plans/launch27-plans-pricing.yml)
- [Rate Limits](rate-limits/launch27-rate-limits.yml)
- [Fin Ops](finops/launch27-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
