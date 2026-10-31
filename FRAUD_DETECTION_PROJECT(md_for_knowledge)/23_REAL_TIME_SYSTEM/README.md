# 23 — Reliable components and contracts

## Why this chapter matters

This chapter answers: **How do events, features, models, and policies connect while meeting latency, availability, and audit needs?** It sits inside a larger fraud-detection system, so read the concepts as connected parts of one payment story rather than as isolated vocabulary. The aim is to understand what is happening in the real world before deciding what a dataset or model can support.

## Concepts in this chapter

- [API](API.md) — The interface through which upstream systems (payment gateway, processor) send transaction data and receive a fraud decision, typically a low-latency synchronous request-response API.
- [Data Ingestion](Data_Ingestion.md) — The layer that receives incoming transaction events (and related data like login/device events) and makes them available to the rest of the system.
- [Decision Service](Decision_Service.md) — The component implementing Section 21's Decision Engine logic in the live system — combining model scores and business rules into a final action, exposed via the API.
- [End to End System](End_to_End_System.md) — The complete architecture in action: Ingestion → Feature Pipeline → Model Serving → Decision Service → API response, all within the real-time latency budget, continuously fed by monitoring and retraining loops.
- [Feature Pipeline](Feature_Pipeline.md) — The system that computes and serves the features a model needs, both offline (for training) and online (for real-time scoring), ideally from the same underlying logic to avoid train/serve skew.
- [Model Serving](Model_Serving.md) — The infrastructure that hosts the trained model and returns predictions on demand, optimized for low latency and high throughput.
- [System Architecture](System_Architecture.md) — The overall design of how components — ingestion, features, model, decision service — connect and communicate to deliver a fraud decision within the authorization window.

## The analytical lens

Define input/output contracts, versions, timeouts, retries, idempotency, monitoring, access control, and rollback. Trace one request end to end. Keep three layers separate throughout the chapter:

- **Reality:** what the customer, merchant, attacker, bank, or payment system actually did.
- **Evidence:** what was recorded, by whom, and at what time.
- **Decision:** what action is justified by that evidence, given uncertainty and cost.

Moving from one layer to the next requires assumptions. Write them down rather than treating them as facts. Ask what legitimate explanation could produce the same observation and what evidence could distinguish the possibilities.

## Work through one example

A transaction service may call an API, retrieve recent account aggregates, score a model, apply policy, and return a response. A missing feature store or model timeout requires a defined fallback rather than an accidental approval.

For each article, try this short exercise: explain the concept in plain language; identify the relevant entity and event; name the observable evidence; note when that evidence becomes available; and connect it to a decision or downstream analysis. Then explain one limitation.

## Common misunderstanding

Focusing on model accuracy while ignoring broken inputs, latency, deployments, and operational recovery. In practice, a single field, event, or model score is rarely enough to establish intent. The goal is not to eliminate uncertainty by confident language. It is to make the uncertainty visible and collect the evidence needed for a responsible decision.

## Checkpoint before moving on

Draw one request path and annotate each component’s contract, failure mode, owner, and latency budget.

You are ready to continue when you can answer the chapter question with a concrete example and explain what is known, what is inferred, and what is still unknown.

## Navigation

Previous: [22 EXPLAINABILITY](../22_EXPLAINABILITY/README.md) · Next: [24 MONITORING](../24_MONITORING/README.md)
