# 03 — Events and stages

## Why this chapter matters

This chapter answers: **At what stage is the payment, and what does its current status actually mean?** It sits inside a larger fraud-detection system, so read the concepts as connected parts of one payment story rather than as isolated vocabulary. The aim is to understand what is happening in the real world before deciding what a dataset or model can support.

## Concepts in this chapter

- [Approval and Decline](Approval_and_Decline.md) — The binary (or ternary, with 'review') outcome of authorization. An approval lets the transaction proceed; a decline stops it immediately.
- [Authentication](Authentication.md) — Verifying that the person initiating the transaction is who they claim to be — via PIN, OTP, biometrics, or 3-D Secure.
- [Authentication vs Authorization](Authentication_vs_Authorization.md) — Authentication proves identity ('who are you'); authorization decides permission ('can this transaction go through'). Both can independently fail even when the other succeeds.
- [Authorization](Authorization.md) — The step where the issuing bank checks funds/credit availability and fraud risk, then approves or declines the transaction in real time.
- [Clearing](Clearing.md) — The process, after authorization, of exchanging transaction details between banks to confirm and prepare for the actual movement of funds.
- [Complete Payment Lifecycle](Complete_Payment_Lifecycle.md) — End to end: Initiation → Authentication → Authorization → Approval/Decline → Clearing → Settlement.
- [Payment Initiation](Payment_Initiation.md) — The moment a customer starts a payment — swiping a card, clicking 'pay now', or authorizing a transfer. This is where transaction data first gets captured.
- [Settlement](Settlement.md) — The actual movement of funds between banks that finalizes the transaction — money leaves the customer's account and lands, net of fees, in the merchant's.

## The analytical lens

Use a timeline and event timestamps. Keep authentication, authorization, clearing, settlement, reversal, and dispute as distinct events; late evidence must not be used as if it existed at decision time. Keep three layers separate throughout the chapter:

- **Reality:** what the customer, merchant, attacker, bank, or payment system actually did.
- **Evidence:** what was recorded, by whom, and at what time.
- **Decision:** what action is justified by that evidence, given uncertainty and cost.

Moving from one layer to the next requires assumptions. Write them down rather than treating them as facts. Ask what legitimate explanation could produce the same observation and what evidence could distinguish the possibilities.

## Work through one example

A card authorization may be approved now, cleared later, and settled after that. Approval means the issuer accepted the authorization request at that moment; it does not prove the transaction is genuine or guarantee final settlement.

For each article, try this short exercise: explain the concept in plain language; identify the relevant entity and event; name the observable evidence; note when that evidence becomes available; and connect it to a decision or downstream analysis. Then explain one limitation.

## Common misunderstanding

Treating an approval as final truth or a chargeback as immediate proof of intentional fraud. In practice, a single field, event, or model score is rarely enough to establish intent. The goal is not to eliminate uncertainty by confident language. It is to make the uncertainty visible and collect the evidence needed for a responsible decision.

## Checkpoint before moving on

Place authorization, clearing, settlement, and possible dispute on a timeline. For each, write what is known and what remains unknown.

You are ready to continue when you can answer the chapter question with a concrete example and explain what is known, what is inferred, and what is still unknown.

## Navigation

Previous: [02 PAYMENT ECOSYSTEM](../02_PAYMENT_ECOSYSTEM/README.md) · Next: [04 FINANCIAL FRAUD](../04_FINANCIAL_FRAUD/README.md)
