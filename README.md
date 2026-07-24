# Monoova (monoova)

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
