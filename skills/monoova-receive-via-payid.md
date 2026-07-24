---
name: Receive real-time funds into a virtual account via PayID
description: Provision a Monoova mAccount, register a PayID against it, subscribe to receive-payment webhooks, and reconcile inbound NPP funds.
api: openapi/monoova-payments.yml
operations: [MAccountCreate, ReceivablesRegisterPayID, SubscriptionsCreate, ReceivablesReceivePaymentWebhook, MAccountGetFinancials]
---

# Receive real-time funds via PayID

Use the Monoova Payments API to stand up a virtual account that can receive
real-time NPP/Osko payments addressed by PayID.

## Auth
HTTP Basic — supply your API key as the username, leave the password blank
(Monoova supplies a password only for OneShotSecurityToken flows). Base URL
`https://api.mpay.com.au` (sandbox `https://api.m-pay.com.au`).

## Steps
1. **Create a virtual account** — `MAccountCreate` to provision an mAccount that
   will hold received funds.
2. **Register a PayID** — `ReceivablesRegisterPayID` to attach a PayID (email or
   phone alias) to the mAccount so payers can address funds to it.
3. **Subscribe to notifications** — `SubscriptionsCreate` with your callback URL
   for the receive-payment event; Monoova will POST to your endpoint
   (`ReceivablesReceivePaymentWebhook` shape) when funds arrive.
4. **Reconcile** — on webhook receipt, confirm balance with
   `MAccountGetFinancials`. Note the error envelope is `{ traceId, errors[] }`,
   not RFC 9457 (see errors/monoova-problem-types.yml).

## Sandbox
Sign up free at https://sandbox.monoova.com/. There is no idempotency-key
header; use your own unique client references to de-dup.
