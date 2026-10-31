# 20 — Prediction becomes a risk estimate

## Why this chapter matters

This chapter answers: **What does the score represent, how calibrated is it, and how should bands be interpreted?** It sits inside a larger fraud-detection system, so read the concepts as connected parts of one payment story rather than as isolated vocabulary. The aim is to understand what is happening in the real world before deciding what a dataset or model can support.

## Concepts in this chapter

- [Probability vs Risk](Probability_vs_Risk.md) — A model's output probability is a statistical estimate of fraud likelihood; 'risk' additionally incorporates the potential impact (e.g. transaction amount, customer value) — two transactions with equal fraud…
- [Risk Bands](Risk_Bands.md) — Grouping continuous risk scores into discrete tiers (e.g. Low, Medium, High, Critical) that map to different business actions.
- [Risk Score](Risk_Score.md) — A single number (often 0-100 or 0-1000) summarizing a transaction's overall fraud risk, typically derived from the model's probability output, sometimes combined with amount/impact.
- [Score Calibration](Score_Calibration.md) — Ensuring that a model's output probability actually matches real-world frequency — e.g. among all transactions scored at 0.7, roughly 70% should truly be fraud.
- [Translating Model Output to Risk](Translating_Model_Output_to_Risk.md) — The end-to-end process: raw model probability → calibration → combination with impact/amount → risk score → risk band, ready for the decision engine to act on.

## The analytical lens

State whether the score is a probability, rank, or points scale. Check calibration and segment stability before attaching verbal meanings or costs. Keep three layers separate throughout the chapter:

- **Reality:** what the customer, merchant, attacker, bank, or payment system actually did.
- **Evidence:** what was recorded, by whom, and at what time.
- **Decision:** what action is justified by that evidence, given uncertainty and cost.

Moving from one layer to the next requires assumptions. Write them down rather than treating them as facts. Ask what legitimate explanation could produce the same observation and what evidence could distinguish the possibilities.

## Work through one example

A score of 80 on a 0–100 scale may be a rescaled model output rather than an 80% probability. Bands can help route work, but their observed fraud rates depend on data and calibration.

For each article, try this short exercise: explain the concept in plain language; identify the relevant entity and event; name the observable evidence; note when that evidence becomes available; and connect it to a decision or downstream analysis. Then explain one limitation.

## Common misunderstanding

Assuming a prettier scale makes predictions more accurate or probabilities calibrated. In practice, a single field, event, or model score is rarely enough to establish intent. The goal is not to eliminate uncertainty by confident language. It is to make the uncertainty visible and collect the evidence needed for a responsible decision.

## Checkpoint before moving on

For each band, report volume, observed fraud rate, label maturity, and uncertainty; then say what action the band supports.

You are ready to continue when you can answer the chapter question with a concrete example and explain what is known, what is inferred, and what is still unknown.

## Navigation

Previous: [19 MODEL EVALUATION](../19_MODEL_EVALUATION/README.md) · Next: [21 DECISION ENGINE](../21_DECISION_ENGINE/README.md)
