# 22 — A reason is not a cause

## Why this chapter matters

This chapter answers: **What did the model use for this prediction, and what can an explanation legitimately tell a human?** It sits inside a larger fraud-detection system, so read the concepts as connected parts of one payment story rather than as isolated vocabulary. The aim is to understand what is happening in the real world before deciding what a dataset or model can support.

## Concepts in this chapter

- [Explaining a Fraud Decision](Explaining_a_Fraud_Decision.md) — Putting explainability into practice: translating a SHAP-based local explanation into a clear, human-readable reason an analyst or customer can understand — e.g. 'flagged due to unusual location and a new device'.
- [Feature Importance](Feature_Importance.md) — A global explanation technique ranking which features contribute most to a model's predictions overall, across the full dataset.
- [Global vs Local Explanations](Global_vs_Local_Explanations.md) — Global explanations describe what drives the model's behavior overall, across the whole population; local explanations describe why one specific transaction received its specific score.
- [SHAP](SHAP.md) — A game-theory-based technique that attributes each individual prediction to specific contributions from each feature, providing both accurate local and aggregable global explanations.
- [Why Explainability Matters](Why_Explainability_Matters.md) — Explaining why a transaction was flagged supports regulatory compliance, builds analyst trust, helps customers understand declines, and helps data scientists debug and improve the model.

## The analytical lens

Check global and local explanations, correlated inputs, background population, stability, and data provenance. Present a model reason alongside case evidence and uncertainty. Keep three layers separate throughout the chapter:

- **Reality:** what the customer, merchant, attacker, bank, or payment system actually did.
- **Evidence:** what was recorded, by whom, and at what time.
- **Decision:** what action is justified by that evidence, given uncertainty and cost.

Moving from one layer to the next requires assumptions. Write them down rather than treating them as facts. Ask what legitimate explanation could produce the same observation and what evidence could distinguish the possibilities.

## Work through one example

An attribution may show that unusual velocity pushed a score upward. It does not prove the transaction is fraudulent, establish why the customer acted, or show that changing the feature would change real-world fraud.

For each article, try this short exercise: explain the concept in plain language; identify the relevant entity and event; name the observable evidence; note when that evidence becomes available; and connect it to a decision or downstream analysis. Then explain one limitation.

## Common misunderstanding

Treating feature importance as causal evidence or presenting an attribution as proof of intent. In practice, a single field, event, or model score is rarely enough to establish intent. The goal is not to eliminate uncertainty by confident language. It is to make the uncertainty visible and collect the evidence needed for a responsible decision.

## Checkpoint before moving on

Explain one decision without jargon, then list what the explanation does not establish.

You are ready to continue when you can answer the chapter question with a concrete example and explain what is known, what is inferred, and what is still unknown.

## Navigation

Previous: [21 DECISION ENGINE](../21_DECISION_ENGINE/README.md) · Next: [23 REAL TIME SYSTEM](../23_REAL_TIME_SYSTEM/README.md)
