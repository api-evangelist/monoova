---
name: Create a PayTo agreement and debit against it
description: Establish an NPP PayTo payment agreement (mandate), wait for payer approval, then initiate a payment instruction against the active mandate.
api: openapi/monoova-payto.yml
operations: [post-paymentagreement, get-paymentagreement-id, post-paymentinstruction, get-paymentinstruction-paymentinitiationid]
---

# PayTo: create a mandate and debit

Use the PayTo API to set up a mandated debit agreement and collect against it.

## Auth
Mint a short-lived (24h) Bearer token from `oauth-v1/token` (POST
/au/security/oauth-v1/Token) using HTTP Basic (mAccount number as username, API
key as password), then send `Authorization: Bearer <token>`. Base URL
`https://api.monoova.com` (sandbox `https://sand-api.monoova.com`).

## Steps
1. **Create the agreement** — `post-paymentagreement` (POST
   /au/payto/pam-v1/PaymentAgreement) with the payer PayID/BSB, amount or
   maxAmount, and frequency.
2. **Await approval** — poll `get-paymentagreement-id` until status is `Active`
   (states: InProgress → Created → Active; also Paused/Cancelled/Rejected/
   Expired), or consume the `PaymentAgreementNotification` webhook.
3. **Initiate a payment** — `post-paymentinstruction` (POST
   /au/payto/pas-v1/paymentInstruction) against the active agreement.
4. **Confirm** — `get-paymentinstruction-paymentinitiationid` for the final
   status (ACSC settled / RJCT rejected).

## Notes
Rejections carry an R0xx / M0xx reason code (errors/monoova-decline-codes.yml).
In the sandbox the amount's cents drive the simulated reason code
(sandbox/monoova-sandbox.yml).
