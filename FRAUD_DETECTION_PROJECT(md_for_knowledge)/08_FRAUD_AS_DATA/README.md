# 08 — Reality becomes a dataset

## Why this chapter matters

This chapter answers: **Which parts of the real event are observed, inferred, delayed, missing, or never recorded?** It sits inside a larger fraud-detection system, so read the concepts as connected parts of one payment story rather than as isolated vocabulary. The aim is to understand what is happening in the real world before deciding what a dataset or model can support.

## Concepts in this chapter

- [Behavioral Data](Behavioral_Data.md) — Data capturing patterns of behavior over time — login frequency, typical spend, typical merchants, typical times — rather than single events.
- [Customer Data](Customer_Data.md) — Static and semi-static information about the customer — account age, demographics, KYC status, historical risk flags.
- [Fraud Label](Fraud_Label.md) — The target variable — a 0/1 flag on each transaction or account indicating whether it was fraudulent, usually derived from confirmed chargebacks, customer disputes, or investigator confirmation.
- [Observable vs Unobservable Information](Observable_vs_Unobservable_Information.md) — Observable information is what your system actually captures (amount, device, location); unobservable information is real but invisible to your data (fraudster's true intent, offline context).
- [Real World to Data](Real_World_to_Data.md) — The process of translating a real financial event into structured data — transaction tables, customer profiles, device logs — that a model can consume.
- [Transaction Data](Transaction_Data.md) — Structured records of each transaction — amount, time, merchant, device, location — forming the primary dataset for fraud modeling.

## The analytical lens

Treat each column as a measurement with a collection process. Ask what creates a value, what causes it to be absent, and how labels were produced. Keep three layers separate throughout the chapter:

- **Reality:** what the customer, merchant, attacker, bank, or payment system actually did.
- **Evidence:** what was recorded, by whom, and at what time.
- **Decision:** what action is justified by that evidence, given uncertainty and cost.

Moving from one layer to the next requires assumptions. Write them down rather than treating them as facts. Ask what legitimate explanation could produce the same observation and what evidence could distinguish the possibilities.

## Work through one example

The data may contain an IP address and device identifier, but neither proves who operated the device. Fraud labels may be assigned only after a dispute and investigation, so recent rows can be unlabeled rather than legitimate.

For each article, try this short exercise: explain the concept in plain language; identify the relevant entity and event; name the observable evidence; note when that evidence becomes available; and connect it to a decision or downstream analysis. Then explain one limitation.

## Common misunderstanding

Confusing a proxy with the underlying fact or interpreting every missing label as a negative. In practice, a single field, event, or model score is rarely enough to establish intent. The goal is not to eliminate uncertainty by confident language. It is to make the uncertainty visible and collect the evidence needed for a responsible decision.

## Checkpoint before moving on

For one field and the target, draw the path from real-world event to stored value. Identify missingness and delay at each step.

You are ready to continue when you can answer the chapter question with a concrete example and explain what is known, what is inferred, and what is still unknown.

## Navigation

Previous: [07 TRANSACTION ANATOMY](../07_TRANSACTION_ANATOMY/README.md) · Next: [09 NORMAL VS ABNORMAL BEHAVIOR](../09_NORMAL_VS_ABNORMAL_BEHAVIOR/README.md)
