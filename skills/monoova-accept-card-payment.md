---
name: Accept a tokenised card payment
description: Create a client session for the browser Card SDK, charge the tokenised card via the Card Payments API, confirm the transaction, and refund if needed.
api: openapi/monoova-cc.yml
operations: [generate-clientSession, createPayment, get-transaction-by-id, request-refund-transaction]
---

# Accept a card payment

Take a card payment with reduced PCI scope using Monoova's browser Card SDK plus
the Card Payments API.

## Auth
Mint a 24h Bearer token from `oauth-v1/token` (POST
/au/security/oauth-v1/Token) via HTTP Basic, then send it as a Bearer token.
Base URL `https://api.monoova.com` (sandbox `https://sand-api.monoova.com`).

## Steps
1. **Create a client session** — `generate-clientSession` (POST
   /au/card/ccm/CreditCardTransaction/token) to initialise the browser Card SDK
   (components/monoova-components.yml). The SDK tokenises the card client-side so
   raw PAN never reaches your server.
2. **Charge** — `createPayment` (POST
   /au/card/ccm/CreditCardTransaction/payment) with the payment method token and
   a unique client reference.
3. **Confirm** — `get-transaction-by-id`
   (/au/card/ccm/CreditCardTransaction/{clientTransactionUniqueReference}) or
   consume the `PaymentStatusNotification` webhook.
4. **Refund (optional)** — `request-refund-transaction` (POST
   /au/card/ccm/CreditCardTransactionAsync/refund); poll async status.

## Notes
Errors use the `{ traceId, errors[] }` envelope with CCM_* codes
(errors/monoova-problem-types.yml).
