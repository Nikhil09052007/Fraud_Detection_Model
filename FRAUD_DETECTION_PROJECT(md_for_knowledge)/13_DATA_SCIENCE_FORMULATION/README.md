# 13 — Business question to prediction

## Why this chapter matters

This chapter answers: **What exact event is predicted, for which entity, using information available at what prediction point and horizon?** It sits inside a larger fraud-detection system, so read the concepts as connected parts of one payment story rather than as isolated vocabulary. The aim is to understand what is happening in the real world before deciding what a dataset or model can support.

## Concepts in this chapter

- [Business to ML Problem](Business_to_ML_Problem.md) — The translation step: 'reduce fraud losses while minimizing false declines' becomes 'predict the probability that a given transaction is fraudulent, using only information available at the time of authorization'.
- [Features](Features.md) — The input variables the model uses to make its prediction — derived from transaction, customer, device, and behavioral data.
- [Labels](Labels.md) — The historical ground-truth values of the target variable across the training dataset — the 'answer key' the model learns from.
- [Prediction Horizon](Prediction_Horizon.md) — The window of time over which the outcome (fraud confirmation) is observed and used to assign the label — e.g. 'fraudulent if charged back within 90 days'.
- [Prediction Point](Prediction_Point.md) — The exact moment in time at which the model must make its prediction — for fraud, this is the instant of transaction authorization.
- [Target Variable](Target_Variable.md) — The specific column the model is trained to predict — typically a binary `is_fraud` flag derived from confirmed chargebacks or investigator confirmation.
- [What Are We Predicting](What_Are_We_Predicting.md) — In this repo's core formulation: the probability that a given transaction, at the moment of authorization, is fraudulent.

## The analytical lens

Specify unit, prediction timestamp, target definition, horizon, label maturation, action, and split strategy. Then check every proposed input against the as-of time. Keep three layers separate throughout the chapter:

- **Reality:** what the customer, merchant, attacker, bank, or payment system actually did.
- **Evidence:** what was recorded, by whom, and at what time.
- **Decision:** what action is justified by that evidence, given uncertainty and cost.

Moving from one layer to the next requires assumptions. Write them down rather than treating them as facts. Ask what legitimate explanation could produce the same observation and what evidence could distinguish the possibilities.

## Work through one example

For a transaction-level model, the unit may be one authorization request and the target may be confirmed unauthorized fraud within a defined follow-up period. A chargeback days later cannot be a feature at authorization time.

For each article, try this short exercise: explain the concept in plain language; identify the relevant entity and event; name the observable evidence; note when that evidence becomes available; and connect it to a decision or downstream analysis. Then explain one limitation.

## Common misunderstanding

Writing “predict fraud” without deciding what counts as fraud, when prediction happens, or how action follows. In practice, a single field, event, or model score is rarely enough to establish intent. The goal is not to eliminate uncertainty by confident language. It is to make the uncertainty visible and collect the evidence needed for a responsible decision.

## Checkpoint before moving on

Complete the sentence: At time T, using fields available by T, predict outcome Y within H for unit U, so actor A can take action D.

You are ready to continue when you can answer the chapter question with a concrete example and explain what is known, what is inferred, and what is still unknown.

## Navigation

Previous: [12 BUSINESS PROBLEM](../12_BUSINESS_PROBLEM/README.md) · Next: [14 DATA UNDERSTANDING](../14_DATA_UNDERSTANDING/README.md)
