# 12 — Losses and customer friction

## Why this chapter matters

This chapter answers: **What harm is the business trying to reduce, and what harm can the intervention create?** It sits inside a larger fraud-detection system, so read the concepts as connected parts of one payment story rather than as isolated vocabulary. The aim is to understand what is happening in the real world before deciding what a dataset or model can support.

## Concepts in this chapter

- [Business Tradeoffs](Business_Tradeoffs.md) — The central tension in fraud detection: catching more fraud (recall) generally means blocking more legitimate transactions (false declines) and costs more to operate — there is no free lunch.
- [Customer Experience](Customer_Experience.md) — The friction (or lack thereof) a legitimate customer experiences during a transaction — extra authentication steps, declines, or delays — driven by the fraud system's decisions.
- [False Declines](False_Declines.md) — Legitimate transactions incorrectly blocked as fraud — a hidden but often larger cost than fraud loss itself, since it drives away good customers.
- [Fraud Loss](Fraud_Loss.md) — The direct monetary loss when fraud goes undetected — the transaction amount, plus associated chargeback fees and operational costs.
- [Fraud Prevention Cost](Fraud_Prevention_Cost.md) — The total investment in fraud prevention infrastructure — data systems, models, engineering, analysts, and third-party tools.
- [Manual Review Cost](Manual_Review_Cost.md) — The operational cost (analyst time, tooling, delay) of routing uncertain transactions to human review instead of an automated decision.
- [Why Companies Care About Fraud](Why_Companies_Care_About_Fraud.md) — Fraud directly costs money (losses, fees, chargebacks), damages customer trust, invites regulatory scrutiny, and can even threaten a company's ability to keep processing payments.

## The analytical lens

Name all affected parties and outcomes before selecting a metric. Estimate the costs of missed fraud, false declines, review, and friction using realistic assumptions. Keep three layers separate throughout the chapter:

- **Reality:** what the customer, merchant, attacker, bank, or payment system actually did.
- **Evidence:** what was recorded, by whom, and at what time.
- **Decision:** what action is justified by that evidence, given uncertainty and cost.

Moving from one layer to the next requires assumptions. Write them down rather than treating them as facts. Ask what legitimate explanation could produce the same observation and what evidence could distinguish the possibilities.

## Work through one example

Blocking one fraudulent payment may prevent a loss, but blocking a legitimate customer can cause abandonment, support calls, and lost trust. Sending a case to review also consumes staff time and delays the customer.

For each article, try this short exercise: explain the concept in plain language; identify the relevant entity and event; name the observable evidence; note when that evidence becomes available; and connect it to a decision or downstream analysis. Then explain one limitation.

## Common misunderstanding

Optimizing fraud recall alone while ignoring legitimate-customer impact and operating cost. In practice, a single field, event, or model score is rarely enough to establish intent. The goal is not to eliminate uncertainty by confident language. It is to make the uncertainty visible and collect the evidence needed for a responsible decision.

## Checkpoint before moving on

Write a decision objective with at least three costs. State whose costs are included and which are not measurable yet.

You are ready to continue when you can answer the chapter question with a concrete example and explain what is known, what is inferred, and what is still unknown.

## Navigation

Previous: [11 REAL TIME FRAUD DETECTION](../11_REAL_TIME_FRAUD_DETECTION/README.md) · Next: [13 DATA SCIENCE FORMULATION](../13_DATA_SCIENCE_FORMULATION/README.md)
