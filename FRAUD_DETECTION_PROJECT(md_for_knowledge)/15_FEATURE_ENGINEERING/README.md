# 15 — Behavior encoded as inputs

## Why this chapter matters

This chapter answers: **How can raw observations be transformed into useful signals without losing meaning or using future information?** It sits inside a larger fraud-detection system, so read the concepts as connected parts of one payment story rather than as isolated vocabulary. The aim is to understand what is happening in the real world before deciding what a dataset or model can support.

## Concepts in this chapter

- [Behavioral Risk Signals](Behavioral_Risk_Signals.md) — Higher-level, often composite features combining multiple raw signals into a single risk indicator — e.g. a 'suspicious session score' combining device, velocity, and location anomalies.
- [Customer Behavior Features](Customer_Behavior_Features.md) — Features summarizing a customer's historical patterns — average transaction amount, typical merchants, usual times — used to detect deviation.
- [Device Features](Device_Features.md) — Features derived from device fingerprinting — is this device new, how many accounts has this device been used on, device risk score.
- [Location Features](Location_Features.md) — Features derived from geographic data — distance from home location, distance from last transaction, country risk score, IP/billing mismatch.
- [Time Based Features](Time_Based_Features.md) — Features derived from the transaction timestamp — hour of day, day of week, time since last transaction, time since account creation.
- [Transaction Level Features](Transaction_Level_Features.md) — Features derived purely from the current transaction's own fields — amount, time, merchant category, payment method — without referencing history.
- [Velocity Features](Velocity_Features.md) — Counts or sums of activity within recent time windows — e.g. transactions in the last 1hr/24hr, total amount spent in the last 24hr.
- [What is Feature Engineering](What_is_Feature_Engineering.md) — The process of transforming raw data into input variables (features) that better expose the underlying patterns a model needs to learn to distinguish fraud from legitimate activity.

## The analytical lens

For each engineered feature, document formula, entity, time window, missing-history behavior, fit data, and online equivalent. Compare a simple baseline before adding complexity. Keep three layers separate throughout the chapter:

- **Reality:** what the customer, merchant, attacker, bank, or payment system actually did.
- **Evidence:** what was recorded, by whom, and at what time.
- **Decision:** what action is justified by that evidence, given uncertainty and cost.

Moving from one layer to the next requires assumptions. Write them down rather than treating them as facts. Ask what legitimate explanation could produce the same observation and what evidence could distinguish the possibilities.

## Work through one example

A sequence of card purchases can produce counts in prior one-hour windows, time since the previous event, and a deviation from prior spending. The current transaction must not count itself in its own history.

For each article, try this short exercise: explain the concept in plain language; identify the relevant entity and event; name the observable evidence; note when that evidence becomes available; and connect it to a decision or downstream analysis. Then explain one limitation.

## Common misunderstanding

Building a feature that is unavailable at scoring time, leaks the current label, or cannot be reproduced online. In practice, a single field, event, or model score is rarely enough to establish intent. The goal is not to eliminate uncertainty by confident language. It is to make the uncertainty visible and collect the evidence needed for a responsible decision.

## Checkpoint before moving on

Design one velocity feature and specify exactly which past events it uses, how ties are handled, and what its first-event value means.

You are ready to continue when you can answer the chapter question with a concrete example and explain what is known, what is inferred, and what is still unknown.

## Navigation

Previous: [14 DATA UNDERSTANDING](../14_DATA_UNDERSTANDING/README.md) · Next: [16 DATA LEAKAGE AND TIME](../16_DATA_LEAKAGE_AND_TIME/README.md)
