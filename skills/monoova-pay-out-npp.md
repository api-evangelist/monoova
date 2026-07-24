---
name: Make a real-time outbound payment (NPP/Osko)
description: Validate and execute an outbound AUD payment from a Monoova account across NPP, direct entry, or BPAY, then confirm settlement status.
api: openapi/monoova-payments.yml
operations: [TransactionValidate, TransactionExecute, TransactionStatusByUid]
---

# Make an outbound payment

Send AUD out of a Monoova mAccount across the appropriate rail (real-time
NPP/Osko, direct credit, or BPAY) using the Payments API.

## Auth
HTTP Basic with the API key as username. Base URL `https://api.mpay.com.au`
(sandbox `https://api.m-pay.com.au`).

## Steps
1. **Validate** — `TransactionValidate` to pre-check the disbursement (account /
   BSB / PayID resolution, limits) before moving money.
2. **Execute** — `TransactionExecute` to move the funds; supply a unique client
   reference so retries do not double-pay (there is no idempotency-key header).
3. **Confirm** — `TransactionStatusByUid` to poll settlement status, or rely on
   the `NppPaymentStatus` webhook (asyncapi/monoova-webhooks.yml).

## Notes
On a failed real-time payment, the response carries an NPP reject reason code —
see errors/monoova-decline-codes.yml (R0xx). All values are reproducible in the
sandbox via the cents-suffix trigger (sandbox/monoova-sandbox.yml).
