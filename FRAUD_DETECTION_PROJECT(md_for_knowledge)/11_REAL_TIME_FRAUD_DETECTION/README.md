# 11 — Decision under a time budget

## Why this chapter matters

This chapter answers: **What can be computed before the payment response deadline, and how fresh and reliable are those inputs?** It sits inside a larger fraud-detection system, so read the concepts as connected parts of one payment story rather than as isolated vocabulary. The aim is to understand what is happening in the real world before deciding what a dataset or model can support.

## Concepts in this chapter

- [End to End Real Time Flow](End_to_End_Real_Time_Flow.md) — Transaction Arrival → Feature Generation → Model Scoring → Decision → Response, all within the payment authorization window.
- [Real Time Decision](Real_Time_Decision.md) — Converting the risk score into an actual action — approve, decline, or step-up/review — using thresholds and business rules.
- [Real Time Feature Generation](Real_Time_Feature_Generation.md) — Computing the features a model needs (velocity, deviation from average, device recognition) on the fly, at the moment of the transaction, using low-latency data stores.
- [Real Time Scoring](Real_Time_Scoring.md) — Passing the generated features through the trained model to produce a risk score, within the live transaction flow.
- [Transaction Arrival](Transaction_Arrival.md) — The moment a transaction request enters the fraud detection system, triggering the real-time scoring pipeline.
- [Why Real Time Matters](Why_Real_Time_Matters.md) — Once a transaction is authorized and funds move, reversing fraud becomes far harder and costlier — chargebacks, disputes, and recovery efforts are expensive and often unsuccessful.

## The analytical lens

Trace arrival, feature lookup, scoring, policy, and response. Measure latency at each stage and specify behavior for missing, delayed, or unavailable dependencies. Keep three layers separate throughout the chapter:

- **Reality:** what the customer, merchant, attacker, bank, or payment system actually did.
- **Evidence:** what was recorded, by whom, and at what time.
- **Decision:** what action is justified by that evidence, given uncertainty and cost.

Moving from one layer to the next requires assumptions. Write them down rather than treating them as facts. Ask what legitimate explanation could produce the same observation and what evidence could distinguish the possibilities.

## Work through one example

A checkout request arrives and must be scored in milliseconds. Account history may be available from a fast feature store, while a batch report from yesterday is too stale for an immediate decision.

For each article, try this short exercise: explain the concept in plain language; identify the relevant entity and event; name the observable evidence; note when that evidence becomes available; and connect it to a decision or downstream analysis. Then explain one limitation.

## Common misunderstanding

Calling a process real time merely because it runs automatically, or ignoring stale state and tail latency. In practice, a single field, event, or model score is rarely enough to establish intent. The goal is not to eliminate uncertainty by confident language. It is to make the uncertainty visible and collect the evidence needed for a responsible decision.

## Checkpoint before moving on

Set a response deadline. Allocate it across feature retrieval, model scoring, and decisioning, then define the timeout behavior.

You are ready to continue when you can answer the chapter question with a concrete example and explain what is known, what is inferred, and what is still unknown.

## Navigation

Previous: [10 FRAUD DETECTION](../10_FRAUD_DETECTION/README.md) · Next: [12 BUSINESS PROBLEM](../12_BUSINESS_PROBLEM/README.md)
