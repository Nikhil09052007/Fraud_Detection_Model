# 26 — Connect the full loop

## Why this chapter matters

This chapter answers: **How does a real financial event become data, a prediction, a decision, an outcome, and new evidence?** It sits inside a larger fraud-detection system, so read the concepts as connected parts of one payment story rather than as isolated vocabulary. The aim is to understand what is happening in the real world before deciding what a dataset or model can support.

## Concepts in this chapter

- [Connecting All Concepts](Connecting_All_Concepts.md) — A map of how core ideas recur and connect across sections — e.g. 'Normal vs Abnormal Behavior' (09) becomes 'Feature Engineering' (15), which must respect 'Data Leakage and Time' (16), gets evaluated via 'Model…
- [Data Scientist Perspective](Data_Scientist_Perspective.md) — How a data scientist should think about this whole system day to day: business problem first, careful problem formulation, leakage-free features, rigorous imbalance-aware evaluation, and honest communication of…
- [End to End Fraud System](End_to_End_Fraud_System.md) — The full journey: real-world money and transactions (01-03) → fraud and how it happens (04-06) → transaction data (07-09) → detection approaches and business context (10-12) → ML formulation and features (13-16) →…
- [Interview Mental Model](Interview_Mental_Model.md) — A structured way to answer 'design a fraud detection system' in an interview: (1) clarify the business goal and constraints, (2) define the ML problem precisely, (3) discuss data and features, being explicit about…
- [System Limitations](System_Limitations.md) — No fraud system is perfect: labels are noisy and delayed (08), some information is fundamentally unobservable (08), fraud is adversarial and adapts (04, 24), and every threshold is a tradeoff, not a solution (12, 19).

## The analytical lens

Trace ideas backward to their assumptions and forward to their consequences. Every model choice should connect to a business need, data evidence, and an operational action. Keep three layers separate throughout the chapter:

- **Reality:** what the customer, merchant, attacker, bank, or payment system actually did.
- **Evidence:** what was recorded, by whom, and at what time.
- **Decision:** what action is justified by that evidence, given uncertainty and cost.

Moving from one layer to the next requires assumptions. Write them down rather than treating them as facts. Ask what legitimate explanation could produce the same observation and what evidence could distinguish the possibilities.

## Work through one example

Start with payment behavior, define the prediction point, gather only available evidence, build a model, evaluate errors, choose a policy, then observe customer and loss outcomes. New labels and attack patterns feed the next version.

For each article, try this short exercise: explain the concept in plain language; identify the relevant entity and event; name the observable evidence; note when that evidence becomes available; and connect it to a decision or downstream analysis. Then explain one limitation.

## Common misunderstanding

Treating data science as a one-time training run rather than an iterative system with feedback and constraints. In practice, a single field, event, or model score is rarely enough to establish intent. The goal is not to eliminate uncertainty by confident language. It is to make the uncertainty visible and collect the evidence needed for a responsible decision.

## Checkpoint before moving on

Explain the complete project using one example transaction, including where uncertainty, latency, labels, and customer costs enter.

You are ready to continue when you can answer the chapter question with a concrete example and explain what is known, what is inferred, and what is still unknown.

## Navigation

Previous: [25 BUSINESS EVALUATION](../25_BUSINESS_EVALUATION/README.md)
