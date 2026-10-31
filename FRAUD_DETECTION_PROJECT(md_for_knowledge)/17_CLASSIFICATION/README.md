# 17 — Score is not action

## Why this chapter matters

This chapter answers: **What score is predicted, how should it be interpreted, and what threshold maps it to an action?** It sits inside a larger fraud-detection system, so read the concepts as connected parts of one payment story rather than as isolated vocabulary. The aim is to understand what is happening in the real world before deciding what a dataset or model can support.

## Concepts in this chapter

- [Binary Classification](Binary_Classification.md) — A classification problem with exactly two possible outcomes — fraud or not fraud — the standard framing for transaction-level fraud detection.
- [Classification Problem](Classification_Problem.md) — A supervised learning task where the model predicts a discrete category (e.g. fraud/not fraud) rather than a continuous value.
- [Classification Threshold](Classification_Threshold.md) — The cutoff probability above which a transaction is classified as fraud (e.g. score > 0.7 = block). Adjusting this threshold directly trades off precision and recall.
- [Decision Trees](Decision_Trees.md) — A model that splits data into branches based on feature thresholds, learning non-linear decision boundaries and interactions naturally.
- [Ensemble Models](Ensemble_Models.md) — Models that combine many individual models (typically decision trees) to produce a stronger, more robust prediction — e.g. Random Forest, XGBoost, LightGBM.
- [Logistic Regression](Logistic_Regression.md) — A simple, interpretable linear model that estimates the probability of the positive class using a weighted sum of features passed through a sigmoid function.
- [Probability Prediction](Probability_Prediction.md) — Most fraud models output a continuous probability (0 to 1) of fraud, rather than a hard 0/1 label directly, which then feeds into risk scoring.

## The analytical lens

Separate ranking, probability calibration, and threshold policy. Compare models using ranking metrics, then select actions against explicit operating objectives. Keep three layers separate throughout the chapter:

- **Reality:** what the customer, merchant, attacker, bank, or payment system actually did.
- **Evidence:** what was recorded, by whom, and at what time.
- **Decision:** what action is justified by that evidence, given uncertainty and cost.

Moving from one layer to the next requires assumptions. Write them down rather than treating them as facts. Ask what legitimate explanation could produce the same observation and what evidence could distinguish the possibilities.

## Work through one example

A classifier may assign 0.12 to a transaction. That number can rank it above many peers; whether it means a 12% chance depends on calibration and population stability. The business action depends on costs and capacity.

For each article, try this short exercise: explain the concept in plain language; identify the relevant entity and event; name the observable evidence; note when that evidence becomes available; and connect it to a decision or downstream analysis. Then explain one limitation.

## Common misunderstanding

Treating 0.5 as a natural threshold or reading every model score as a calibrated probability. In practice, a single field, event, or model score is rarely enough to establish intent. The goal is not to eliminate uncertainty by confident language. It is to make the uncertainty visible and collect the evidence needed for a responsible decision.

## Checkpoint before moving on

Explain what a score of 0.12 means for ranking, calibration, and action separately.

You are ready to continue when you can answer the chapter question with a concrete example and explain what is known, what is inferred, and what is still unknown.

## Navigation

Previous: [16 DATA LEAKAGE AND TIME](../16_DATA_LEAKAGE_AND_TIME/README.md) · Next: [18 CLASS IMBALANCE](../18_CLASS_IMBALANCE/README.md)
