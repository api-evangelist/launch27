# Launch27 (launch27)

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
