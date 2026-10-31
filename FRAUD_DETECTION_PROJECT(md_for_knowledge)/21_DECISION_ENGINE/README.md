# 21 — Policy translates risk into action

## Why this chapter matters

This chapter answers: **What action is taken at each score, who bears its cost, and what happens at boundaries or failures?** It sits inside a larger fraud-detection system, so read the concepts as connected parts of one payment story rather than as isolated vocabulary. The aim is to understand what is happening in the real world before deciding what a dataset or model can support.

## Concepts in this chapter

- [Approval](Approval.md) — The decision to let a transaction proceed — typically for low risk-score transactions below the review/block thresholds.
- [Blocking](Blocking.md) — Declining a transaction outright due to high assessed risk, typically for scores above a defined threshold.
- [Business Rules](Business_Rules.md) — Explicit, hand-written logic layered on top of (or ahead of) the model — e.g. 'always block transactions from sanctioned countries' — for cases requiring certainty or compliance, not probability.
- [Decision Thresholds](Decision_Thresholds.md) — The specific risk score cutoffs that separate approve, review, and block outcomes — directly derived from the threshold evaluation work in Section 19.
- [Manual Review](Manual_Review.md) — Routing a transaction to a human analyst instead of an automated approve/decline, typically for scores in an uncertain middle band.
- [Model plus Rules](Model_plus_Rules.md) — The standard production pattern: business rules handle known hard cases and compliance requirements, while the ML model handles the nuanced, probabilistic majority of decisions — combined into one final decision.
- [What is a Decision Engine](What_is_a_Decision_Engine.md) — The component of a fraud system responsible for converting risk scores and business rules into a final action on each transaction, in real time.

## The analytical lens

Map score ranges to actions, set constraints, quantify outcomes, and design overrides. Compare policies on a later sample and monitor action rates after launch. Keep three layers separate throughout the chapter:

- **Reality:** what the customer, merchant, attacker, bank, or payment system actually did.
- **Evidence:** what was recorded, by whom, and at what time.
- **Decision:** what action is justified by that evidence, given uncertainty and cost.

Moving from one layer to the next requires assumptions. Write them down rather than treating them as facts. Ask what legitimate explanation could produce the same observation and what evidence could distinguish the possibilities.

## Work through one example

Low risk may be approved, ambiguous cases reviewed, and high risk declined or challenged. A review policy needs a capacity limit, prioritization rule, and handling for model outages.

For each article, try this short exercise: explain the concept in plain language; identify the relevant entity and event; name the observable evidence; note when that evidence becomes available; and connect it to a decision or downstream analysis. Then explain one limitation.

## Common misunderstanding

Confusing a model threshold with the full decision policy. In practice, a single field, event, or model score is rarely enough to establish intent. The goal is not to eliminate uncertainty by confident language. It is to make the uncertainty visible and collect the evidence needed for a responsible decision.

## Checkpoint before moving on

Create an approve/review/decline table with thresholds, expected volume, owner, cost, and fallback.

You are ready to continue when you can answer the chapter question with a concrete example and explain what is known, what is inferred, and what is still unknown.

## Navigation

Previous: [20 RISK SCORING](../20_RISK_SCORING/README.md) · Next: [22 EXPLAINABILITY](../22_EXPLAINABILITY/README.md)
