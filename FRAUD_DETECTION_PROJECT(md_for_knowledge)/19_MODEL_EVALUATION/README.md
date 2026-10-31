# 19 — Evidence for model usefulness

## Why this chapter matters

This chapter answers: **Does the model rank fraud well, behave acceptably at an operating threshold, and generalize to a later period?** It sits inside a larger fraud-detection system, so read the concepts as connected parts of one payment story rather than as isolated vocabulary. The aim is to understand what is happening in the real world before deciding what a dataset or model can support.

## Concepts in this chapter

- [Accuracy](Accuracy.md) — The fraction of all predictions that were correct — misleadingly high and largely uninformative on imbalanced fraud data (see Section 18).
- [Confusion Matrix](Confusion_Matrix.md) — A table breaking down predictions into true positives, true negatives, false positives, and false negatives — the foundation all other classification metrics are built from.
- [Cost Based Evaluation](Cost_Based_Evaluation.md) — Evaluating model performance in actual monetary terms — dollars of fraud prevented minus dollars lost to false declines and review costs — rather than abstract statistical metrics alone.
- [F1 Score](F1_Score.md) — The harmonic mean of precision and recall, providing a single balanced metric when both false positives and false negatives matter.
- [False Positive and Negative](False_Positive_and_Negative.md) — A false positive is a legitimate transaction wrongly flagged as fraud (a false decline); a false negative is fraud that slipped through undetected — the two 'wrong' outcomes, each with different costs.
- [PR AUC](PR_AUC.md) — The area under the precision-recall curve — generally the preferred single-number summary metric for highly imbalanced fraud problems over ROC AUC.
- [Precision](Precision.md) — Of all transactions flagged as fraud, the fraction that were actually fraud (TP / (TP + FP)) — high precision means few false alarms.
- [Precision Recall Curve](Precision_Recall_Curve.md) — A plot of precision vs recall across all possible classification thresholds — more informative than ROC on imbalanced data because it focuses on the minority (fraud) class directly.
- [Recall](Recall.md) — Of all actual fraud, the fraction correctly caught (TP / (TP + FN)) — also called sensitivity or true positive rate. High recall means little fraud slips through.
- [ROC AUC](ROC_AUC.md) — The area under the Receiver Operating Characteristic curve, measuring how well the model ranks fraud above non-fraud across all thresholds, in terms of true positive rate vs false positive rate.
- [Threshold Evaluation](Threshold_Evaluation.md) — Explicitly evaluating model performance at specific, business-relevant thresholds rather than only via threshold-independent summary metrics.
- [True Positive and Negative](True_Positive_and_Negative.md) — A true positive is fraud correctly flagged as fraud; a true negative is a legitimate transaction correctly allowed through — the two 'correct' outcomes.

## The analytical lens

Inspect PR-AUC, recall, precision, false-positive rate, calibration, threshold curves, segment performance, temporal stability, and cost assumptions. Reserve data for final evaluation. Keep three layers separate throughout the chapter:

- **Reality:** what the customer, merchant, attacker, bank, or payment system actually did.
- **Evidence:** what was recorded, by whom, and at what time.
- **Decision:** what action is justified by that evidence, given uncertainty and cost.

Moving from one layer to the next requires assumptions. Write them down rather than treating them as facts. Ask what legitimate explanation could produce the same observation and what evidence could distinguish the possibilities.

## Work through one example

A high ROC-AUC can coexist with a low precision when fraud is rare. A threshold can catch more fraud but flood a review team. A single validation window may not represent future attacks.

For each article, try this short exercise: explain the concept in plain language; identify the relevant entity and event; name the observable evidence; note when that evidence becomes available; and connect it to a decision or downstream analysis. Then explain one limitation.

## Common misunderstanding

Choosing one metric in isolation or tuning and reporting on the same set as if it were untouched. In practice, a single field, event, or model score is rarely enough to establish intent. The goal is not to eliminate uncertainty by confident language. It is to make the uncertainty visible and collect the evidence needed for a responsible decision.

## Checkpoint before moving on

Given two models, compare them at equal review capacity and explain which errors and customer outcomes differ.

You are ready to continue when you can answer the chapter question with a concrete example and explain what is known, what is inferred, and what is still unknown.

## Navigation

Previous: [18 CLASS IMBALANCE](../18_CLASS_IMBALANCE/README.md) · Next: [20 RISK SCORING](../20_RISK_SCORING/README.md)
