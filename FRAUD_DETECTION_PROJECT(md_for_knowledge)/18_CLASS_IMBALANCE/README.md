# 18 — Rare outcomes change evaluation

## Why this chapter matters

This chapter answers: **How do low fraud prevalence, sampling, weighting, and resampling alter training and decision metrics?** It sits inside a larger fraud-detection system, so read the concepts as connected parts of one payment story rather than as isolated vocabulary. The aim is to understand what is happening in the real world before deciding what a dataset or model can support.

## Concepts in this chapter

- [Class Weights](Class_Weights.md) — Assigning a higher loss penalty to misclassifying the minority (fraud) class during training, without altering the actual data — an alternative to resampling.
- [Cost Sensitive Learning](Cost_Sensitive_Learning.md) — Training approaches that directly incorporate the differing real-world costs of false positives (false declines) vs false negatives (missed fraud) into the model's optimization objective.
- [Resampling](Resampling.md) — Techniques that adjust the class balance of training data — oversampling the minority (fraud) class, undersampling the majority (legitimate) class, or both.
- [SMOTE](SMOTE.md) — An oversampling method that generates synthetic minority-class examples by interpolating between existing fraud examples and their nearest neighbors, rather than simply duplicating them.
- [What is Class Imbalance](What_is_Class_Imbalance.md) — When the classes in a classification problem are not represented equally — in fraud, legitimate transactions vastly outnumber fraudulent ones.
- [Why Accuracy Can Fail](Why_Accuracy_Can_Fail.md) — With 99.9% legitimate transactions, a model that always predicts 'not fraud' achieves 99.9% accuracy while catching zero fraud — making accuracy a meaningless metric here.
- [Why Fraud Data is Imbalanced](Why_Fraud_Data_is_Imbalanced.md) — Fraud is inherently rare because most transactions are legitimate — this reflects reality, not a data collection flaw, and shouldn't be 'fixed' away entirely.

## The analytical lens

Track the real base rate. Apply resampling only within training folds, and evaluate on untouched data at its natural prevalence. Inspect precision, recall, and review volume. Keep three layers separate throughout the chapter:

- **Reality:** what the customer, merchant, attacker, bank, or payment system actually did.
- **Evidence:** what was recorded, by whom, and at what time.
- **Decision:** what action is justified by that evidence, given uncertainty and cost.

Moving from one layer to the next requires assumptions. Write them down rather than treating them as facts. Ask what legitimate explanation could produce the same observation and what evidence could distinguish the possibilities.

## Work through one example

If 1 in 100 transactions is fraud, a model that flags 10% of all events has a different operational burden than one that flags 1%. A balanced training sample does not make fraud common in production.

For each article, try this short exercise: explain the concept in plain language; identify the relevant entity and event; name the observable evidence; note when that evidence becomes available; and connect it to a decision or downstream analysis. Then explain one limitation.

## Common misunderstanding

Using accuracy or a balanced evaluation set to claim production performance. In practice, a single field, event, or model score is rarely enough to establish intent. The goal is not to eliminate uncertainty by confident language. It is to make the uncertainty visible and collect the evidence needed for a responsible decision.

## Checkpoint before moving on

Calculate how many false alarms arise when precision is applied to a million events at the real fraud prevalence.

You are ready to continue when you can answer the chapter question with a concrete example and explain what is known, what is inferred, and what is still unknown.

## Navigation

Previous: [17 CLASSIFICATION](../17_CLASSIFICATION/README.md) · Next: [19 MODEL EVALUATION](../19_MODEL_EVALUATION/README.md)
