# 09 — Behavior depends on context

## Why this chapter matters

This chapter answers: **Compared with which customer baseline, peer group, time window, and sequence is an event unusual?** It sits inside a larger fraud-detection system, so read the concepts as connected parts of one payment story rather than as isolated vocabulary. The aim is to understand what is happening in the real world before deciding what a dataset or model can support.

## Concepts in this chapter

- [Abnormal Behavior](Abnormal_Behavior.md) — Activity that deviates meaningfully from an entity's established normal pattern — the core signal fraud models look for.
- [Behavioral Deviation](Behavioral_Deviation.md) — A quantified measure of how far a new event is from an entity's normal baseline — e.g. amount is 5 standard deviations above average spend.
- [Multiple Signals](Multiple_Signals.md) — The principle that no single abnormal signal alone is usually enough — fraud risk emerges from the combination and co-occurrence of multiple deviations.
- [New Device](New_Device.md) — A transaction or login originating from a device not previously associated with the account.
- [New Merchant](New_Merchant.md) — A transaction with a merchant the customer has never transacted with before.
- [Normal Behavior](Normal_Behavior.md) — The typical, expected pattern of activity for a given customer, account, device, or merchant — the baseline against which new activity is judged.
- [Transaction Velocity](Transaction_Velocity.md) — The rate of transactions over a time window — e.g. number of transactions in the last hour/day — a classic and powerful fraud signal.
- [Unusual Amount](Unusual_Amount.md) — A transaction amount that's significantly higher (or sometimes lower) than the customer's typical spend.
- [Unusual Location](Unusual_Location.md) — A transaction occurring in a geographic location the customer doesn't normally transact from, especially combined with impossible travel time from their last known location.
- [Unusual Time](Unusual_Time.md) — A transaction occurring at a time of day or day of week atypical for that customer's normal activity pattern.

## The analytical lens

Define the comparison group before calling something abnormal. Combine signals, measure how long the baseline is observed, and test whether a deviation changes risk after accounting for context. Keep three layers separate throughout the chapter:

- **Reality:** what the customer, merchant, attacker, bank, or payment system actually did.
- **Evidence:** what was recorded, by whom, and at what time.
- **Decision:** what action is justified by that evidence, given uncertainty and cost.

Moving from one layer to the next requires assumptions. Write them down rather than treating them as facts. Ask what legitimate explanation could produce the same observation and what evidence could distinguish the possibilities.

## Work through one example

A high amount may be normal for a business account but unusual for a customer who normally makes small local purchases. A new device may be common after a phone upgrade and risky when paired with a new location and rapid spending.

For each article, try this short exercise: explain the concept in plain language; identify the relevant entity and event; name the observable evidence; note when that evidence becomes available; and connect it to a decision or downstream analysis. Then explain one limitation.

## Common misunderstanding

Equating unusual with fraudulent, or using population-wide averages as every customer’s normal behavior. In practice, a single field, event, or model score is rarely enough to establish intent. The goal is not to eliminate uncertainty by confident language. It is to make the uncertainty visible and collect the evidence needed for a responsible decision.

## Checkpoint before moving on

Compare the same transaction against its customer history and a peer group. Which signals are informative, and what could explain them legitimately?

You are ready to continue when you can answer the chapter question with a concrete example and explain what is known, what is inferred, and what is still unknown.

## Navigation

Previous: [08 FRAUD AS DATA](../08_FRAUD_AS_DATA/README.md) · Next: [10 FRAUD DETECTION](../10_FRAUD_DETECTION/README.md)
