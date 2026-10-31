# 24 — Performance changes over time

## Why this chapter matters

This chapter answers: **Which signals reveal input change, model degradation, label delay, policy burden, or customer harm?** It sits inside a larger fraud-detection system, so read the concepts as connected parts of one payment story rather than as isolated vocabulary. The aim is to understand what is happening in the real world before deciding what a dataset or model can support.

## Concepts in this chapter

- [Concept Drift](Concept_Drift.md) — When the actual relationship between features and the fraud label changes over time — e.g. a feature that used to strongly indicate fraud stops being predictive as fraudsters adapt.
- [Data Drift](Data_Drift.md) — When the statistical properties of input features change over time relative to what the model was trained on — e.g. a new payment method becoming popular shifts the payment-method feature distribution.
- [False Positive Monitoring](False_Positive_Monitoring.md) — Tracking the rate of legitimate transactions incorrectly flagged or blocked, since this directly drives customer complaints and revenue loss.
- [Fraud Rate Monitoring](Fraud_Rate_Monitoring.md) — Tracking the overall rate of confirmed fraud over time, segmented by relevant dimensions (merchant, region, payment method), to spot emerging attack patterns.
- [Model Performance Monitoring](Model_Performance_Monitoring.md) — Continuously tracking live model metrics (precision, recall, score distributions) against expectations, using delayed-but-eventually-available true labels.
- [Model Retraining](Model_Retraining.md) — The process of periodically (or triggered by drift detection) retraining the model on fresh data to keep pace with evolving fraud patterns.
- [Why Monitoring is Necessary](Why_Monitoring_is_Necessary.md) — Fraud patterns actively evolve as fraudsters adapt to evade detection, and underlying data can shift for unrelated reasons — without monitoring, model quality silently degrades until losses spike.

## The analytical lens

Monitor data quality, feature and score drift, matured-label metrics, action rates, review capacity, and customer outcomes. Investigate causes before retraining. Keep three layers separate throughout the chapter:

- **Reality:** what the customer, merchant, attacker, bank, or payment system actually did.
- **Evidence:** what was recorded, by whom, and at what time.
- **Decision:** what action is justified by that evidence, given uncertainty and cost.

Moving from one layer to the next requires assumptions. Write them down rather than treating them as facts. Ask what legitimate explanation could produce the same observation and what evidence could distinguish the possibilities.

## Work through one example

A shift in score distribution can come from a new customer mix, a broken feature pipeline, or changed attacker behavior. Mature labels are needed before outcome metrics can be trusted.

For each article, try this short exercise: explain the concept in plain language; identify the relevant entity and event; name the observable evidence; note when that evidence becomes available; and connect it to a decision or downstream analysis. Then explain one limitation.

## Common misunderstanding

Treating drift as proof of model failure or retraining automatically on unstable labels. In practice, a single field, event, or model score is rarely enough to establish intent. The goal is not to eliminate uncertainty by confident language. It is to make the uncertainty visible and collect the evidence needed for a responsible decision.

## Checkpoint before moving on

For one alert, name at least three possible causes and the evidence needed to distinguish them.

You are ready to continue when you can answer the chapter question with a concrete example and explain what is known, what is inferred, and what is still unknown.

## Navigation

Previous: [23 REAL TIME SYSTEM](../23_REAL_TIME_SYSTEM/README.md) · Next: [25 BUSINESS EVALUATION](../25_BUSINESS_EVALUATION/README.md)
