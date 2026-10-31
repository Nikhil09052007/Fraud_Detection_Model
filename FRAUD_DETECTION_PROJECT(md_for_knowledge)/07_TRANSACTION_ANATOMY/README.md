# 07 — Events and fields

## Why this chapter matters

This chapter answers: **What is one row, what does each field measure, and what was knowable when the row was created?** It sits inside a larger fraud-detection system, so read the concepts as connected parts of one payment story rather than as isolated vocabulary. The aim is to understand what is happening in the real world before deciding what a dataset or model can support.

## Concepts in this chapter

- [Customer and Account](Customer_and_Account.md) — Identifiers linking the transaction to a specific customer and account, enabling all account-level historical and behavioral features.
- [Device](Device.md) — Information about the device used to initiate the transaction — device ID, type, OS, browser fingerprint.
- [IP and Network](IP_and_Network.md) — The IP address and network characteristics (VPN/proxy use, ISP, ASN) from which the transaction was initiated.
- [Location](Location.md) — The geographic location associated with the transaction — from GPS, IP geolocation, or billing address — compared against a customer's usual locations.
- [Merchant](Merchant.md) — The merchant identifier and category involved in the transaction — used to assess merchant risk and detect unusual merchant patterns for a customer.
- [Payment Method](Payment_Method.md) — How the payment was made — credit card, debit card, bank transfer, digital wallet — each with different fraud risk profiles.
- [Timestamp](Timestamp.md) — The exact date and time a transaction occurred — used to derive time-based features and to enforce correct temporal ordering for training/evaluation.
- [Transaction Amount](Transaction_Amount.md) — The monetary value of the transaction — one of the single strongest raw signals in fraud detection, especially relative to a customer's typical spend.
- [Transaction History](Transaction_History.md) — The sequence of a customer's past transactions, which forms the baseline against which the current transaction's normalcy is judged.

## The analytical lens

For each field, record its unit, grain, source, missingness meaning, and availability time. Verify whether a column describes the transaction itself or information learned later. Keep three layers separate throughout the chapter:

- **Reality:** what the customer, merchant, attacker, bank, or payment system actually did.
- **Evidence:** what was recorded, by whom, and at what time.
- **Decision:** what action is justified by that evidence, given uncertainty and cost.

Moving from one layer to the next requires assumptions. Write them down rather than treating them as facts. Ask what legitimate explanation could produce the same observation and what evidence could distinguish the possibilities.

## Work through one example

A transaction row may combine amount, time, merchant, payment instrument, device, and network observations. An identifier can join records without meaning the underlying values are stable or globally unique.

For each article, try this short exercise: explain the concept in plain language; identify the relevant entity and event; name the observable evidence; note when that evidence becomes available; and connect it to a decision or downstream analysis. Then explain one limitation.

## Common misunderstanding

Assuming a column name fully defines its meaning or that a null always means “no.” In practice, a single field, event, or model score is rarely enough to establish intent. The goal is not to eliminate uncertainty by confident language. It is to make the uncertainty visible and collect the evidence needed for a responsible decision.

## Checkpoint before moving on

Choose five fields and write a data dictionary entry for each: definition, unit, source, as-of time, and one ambiguity.

You are ready to continue when you can answer the chapter question with a concrete example and explain what is known, what is inferred, and what is still unknown.

## Navigation

Previous: [06 HOW FRAUD HAPPENS](../06_HOW_FRAUD_HAPPENS/README.md) · Next: [08 FRAUD AS DATA](../08_FRAUD_AS_DATA/README.md)
