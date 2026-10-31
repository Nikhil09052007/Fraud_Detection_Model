# 25 — Measure realized impact

## Why this chapter matters

This chapter answers: **Did the system reduce losses enough to justify declines, review operations, customer friction, and implementation cost?** It sits inside a larger fraud-detection system, so read the concepts as connected parts of one payment story rather than as isolated vocabulary. The aim is to understand what is happening in the real world before deciding what a dataset or model can support.

## Concepts in this chapter

- [Business Success Metrics](Business_Success_Metrics.md) — The full dashboard of metrics — fraud rate, false decline rate, review queue size, model ROI — that together define whether the fraud system is succeeding, tracked over time and by segment.
- [Customer Impact](Customer_Impact.md) — The effect of the fraud system on legitimate customers — false decline rate, added friction (step-up authentication), and resulting complaints or churn.
- [Financial Loss](Financial_Loss.md) — The total realized cost of fraud that was NOT prevented — including the transaction amount, chargeback fees, and any associated recovery costs.
- [Fraud Prevented](Fraud_Prevented.md) — The estimated dollar value of fraud stopped by the system — typically the transaction amounts of correctly blocked/flagged fraudulent transactions.
- [Model ROI](Model_ROI.md) — The overall return on investment of the fraud model and system — value delivered (fraud prevented, minus false-decline cost) versus total cost (infrastructure, engineering, review operations).
- [Review Operations](Review_Operations.md) — Metrics about the manual review process itself — queue size, average review time, analyst accuracy, and cost per review.

## The analytical lens

Separate offline metrics from realized outcomes. Include loss avoided, false declines, review cost, customer impact, control overlap, and measurement uncertainty. Keep three layers separate throughout the chapter:

- **Reality:** what the customer, merchant, attacker, bank, or payment system actually did.
- **Evidence:** what was recorded, by whom, and at what time.
- **Decision:** what action is justified by that evidence, given uncertainty and cost.

Moving from one layer to the next requires assumptions. Write them down rather than treating them as facts. Ask what legitimate explanation could produce the same observation and what evidence could distinguish the possibilities.

## Work through one example

Fraud captured is not automatically fraud prevented: some cases would have been stopped by other controls, and some blocked purchases might have been legitimate. Compare outcomes against a credible baseline.

For each article, try this short exercise: explain the concept in plain language; identify the relevant entity and event; name the observable evidence; note when that evidence becomes available; and connect it to a decision or downstream analysis. Then explain one limitation.

## Common misunderstanding

Calling prevented fraud equal to every fraud prediction, or reporting ROI without a counterfactual. In practice, a single field, event, or model score is rarely enough to establish intent. The goal is not to eliminate uncertainty by confident language. It is to make the uncertainty visible and collect the evidence needed for a responsible decision.

## Checkpoint before moving on

Build a business scorecard and identify which values are measured, estimated, or unknown.

You are ready to continue when you can answer the chapter question with a concrete example and explain what is known, what is inferred, and what is still unknown.

## Navigation

Previous: [24 MONITORING](../24_MONITORING/README.md) · Next: [26 COMPLETE MENTAL MODEL](../26_COMPLETE_MENTAL_MODEL/README.md)
