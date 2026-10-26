# Monoova (monoova)

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

Monoova is an Australian payments platform that lets businesses receive, manage, and pay funds in AUD across every domestic rail through a single set of RESTful JSON APIs. Operated by Monoova Global Payments Pty Ltd (AFSL 421414) and enrolled with AUSTRAC, it connects directly to the New Payments Platform — real-time account-to-account transfers via NPP/Osko, PayID addressing, and PayTo mandated debits — alongside BPAY, direct entry, card acquiring, and Apple Pay / Google Pay. Its Automatcher reconciliation engine, virtual mAccount/mWallet hierarchies, Confirmation of Payee, account verification, payment tokenisation, and webhook-driven reporting serve fintechs, marketplaces, payroll, lending, remittance, and SaaS businesses (customers include Wise, Nium, Finder, and Sharesies).

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/monoova/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/monoova/refs/heads/main/apis.yml)

## Tags

- Payments
- Australia
- Real-Time Payments
- NPP
- PayTo
- PayID
- Account-to-Account
- BPAY
- Card Payments
- Money Movement
- Virtual Accounts
- Cross-Border

## Timestamps

- **Created:** 2026-07-24
- **Modified:** 2026-07-24

## APIs

### Monoova Payments API

Core Payments API (v5.29) to receive, manage, and pay AUD across all Australian payment rails — real-time transfers via NPP/Osko, direct credit and direct debit, BPAY, card payments, and PayID — plus the Automatcher receivables engine, virtual mAccount/mWallet hierarchies, ledger accounts, reconciliation and financial reporting, account verification, payment tokenisation, and webhooks. Authenticated with HTTP Basic auth (API key as the username).

- **Human URL:** [https://developer.monoova.com/overview](https://developer.monoova.com/overview)
- **Base URL:** `https://api.mpay.com.au` (sandbox `https://api.m-pay.com.au`)

#### Properties

- [OpenAPI](openapi/monoova-payments.yml)
- [Documentation](https://developer.monoova.com/overview)
- [API Reference](https://api-docs.monoova.com/)

### Monoova PayTo API

PayTo API (v1) for the New Payments Platform's mandated account-to-account debit service — create and manage payment agreements (mandates), initiate payments, handle mandate/payment status lifecycles, and receive notifications and webhooks. Authenticated with short-lived (24h) Bearer tokens obtained via HTTP Basic auth.

- **Human URL:** [https://developer.monoova.com/payto](https://developer.monoova.com/payto)
- **Base URL:** `https://api.monoova.com` (sandbox `https://sand-api.monoova.com`)

#### Properties

- [OpenAPI](openapi/monoova-payto.yml)
- [Documentation](https://developer.monoova.com/payto)
- [API Reference](https://api-docs.monoova.com/)

### Monoova Card Payments API

Card Payments API (v1) for accepting card payments, including tokenised card flows and webhook notifications for payment events. Authenticated with short-lived (24h) Bearer tokens obtained via HTTP Basic auth.

- **Human URL:** [https://developer.monoova.com/card-payments](https://developer.monoova.com/card-payments)
- **Base URL:** `https://api.monoova.com` (sandbox `https://sand-api.monoova.com`)

#### Properties

- [OpenAPI](openapi/monoova-cc.yml)
- [Documentation](https://developer.monoova.com/card-payments)
- [API Reference](https://api-docs.monoova.com/)

## Common Properties

- [Website](https://www.monoova.com/)
- [Developer Portal](https://developer.monoova.com/)
- [API Reference](https://api-docs.monoova.com/)
- [Getting Started](https://developer.monoova.com/getting-started)
- [Authentication](https://developer.monoova.com/authentication)
- [Postman](https://www.postman.com/monoova/monoova-api)
- [Status Page](https://monoova.statuspage.io)
- [Blog](https://www.monoova.com/blog)
- [GitHub Organization](https://github.com/monoova)
- [LinkedIn](https://www.linkedin.com/company/monoova)
- [Sign Up (Sandbox)](https://sandbox.monoova.com/)
- [Support](https://www.monoova.com/contact)
- [Terms of Use](https://www.monoova.com/terms-of-use)
- [Privacy Policy](https://www.monoova.com/privacy-policy)
- [Security](https://www.monoova.com/security)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
