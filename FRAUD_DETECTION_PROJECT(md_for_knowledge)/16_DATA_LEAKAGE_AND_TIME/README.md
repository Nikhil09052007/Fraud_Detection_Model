# 16 — Information must respect the clock

## Why this chapter matters

This chapter answers: **Would this value have been known at the exact moment the model makes its prediction?** It sits inside a larger fraud-detection system, so read the concepts as connected parts of one payment story rather than as isolated vocabulary. The aim is to understand what is happening in the real world before deciding what a dataset or model can support.

## Concepts in this chapter

- [Future Information](Future_Information.md) — Any data generated after the prediction point — e.g. whether a chargeback eventually occurred, or the customer's transactions the following week — that must never be used as a feature.
- [Information Available at Prediction](Information_Available_at_Prediction.md) — The complete set of data that genuinely existed and was accessible at prediction time — the only valid basis for features.
- [Label Leakage](Label_Leakage.md) — A specific, severe form of leakage where the feature itself is derived from or highly correlated with the label-generating process — e.g. using 'was this transaction disputed' as a feature to predict fraud.
- [Prediction Time](Prediction_Time.md) — The exact timestamp at which the model makes its prediction — synonymous with the Prediction Point from Section 13 — the hard boundary for what data is valid to use.
- [Temporal Data Splitting](Temporal_Data_Splitting.md) — Splitting training and test data by time (e.g. train on Jan-Oct, test on Nov-Dec) rather than randomly, to accurately simulate how the model will actually be used in production.
- [Train Test Leakage](Train_Test_Leakage.md) — When information from the test set influences the training process — e.g. computing a global average using the full dataset before splitting, or randomly (not temporally) splitting time-ordered fraud data.
- [What is Data Leakage](What_is_Data_Leakage.md) — When information that would not actually be available at prediction time is accidentally included in training features, causing the model to learn from 'answers' it won't have access to in production.

## The analytical lens

Assign every feature and label an availability time. Split chronologically, fit preprocessing only on the training period, and simulate the intended prediction boundary. Keep three layers separate throughout the chapter:

- **Reality:** what the customer, merchant, attacker, bank, or payment system actually did.
- **Evidence:** what was recorded, by whom, and at what time.
- **Decision:** what action is justified by that evidence, given uncertainty and cost.

Moving from one layer to the next requires assumptions. Write them down rather than treating them as facts. Ask what legitimate explanation could produce the same observation and what evidence could distinguish the possibilities.

## Work through one example

A later investigation result may be strongly correlated with fraud, but it did not exist when an authorization decision was made. Randomly splitting neighboring events can also let future patterns inform past evaluation.

For each article, try this short exercise: explain the concept in plain language; identify the relevant entity and event; name the observable evidence; note when that evidence becomes available; and connect it to a decision or downstream analysis. Then explain one limitation.

## Common misunderstanding

Thinking leakage is only the target column appearing directly among inputs. Future aggregates and selection effects can leak too. In practice, a single field, event, or model score is rarely enough to establish intent. The goal is not to eliminate uncertainty by confident language. It is to make the uncertainty visible and collect the evidence needed for a responsible decision.

## Checkpoint before moving on

For every model input, answer “available by prediction time?” If not, remove it or redefine the decision point.

You are ready to continue when you can answer the chapter question with a concrete example and explain what is known, what is inferred, and what is still unknown.

## Navigation

Previous: [15 FEATURE ENGINEERING](../15_FEATURE_ENGINEERING/README.md) · Next: [17 CLASSIFICATION](../17_CLASSIFICATION/README.md)
