# Data Ingestion

The layer that receives incoming transaction events (and related data like login/device events) and makes them available to the rest of the system.

## Key Points

- Often built on streaming platforms (e.g. Kafka) for scalability and low latency
- Must handle both the real-time path (scoring) and the batch/historical path (retraining, monitoring)

## Understand Data Ingestion

### Put the idea in context

Define input/output contracts, versions, timeouts, retries, idempotency, monitoring, access control, and rollback. Trace one request end to end. Apply **Data Ingestion** to an actual payment or investigation as a way to organize evidence. A concept describes one part of the system; it does not, by itself, establish that a customer committed fraud or that a model should take a particular action.

### Think like a data scientist

1. **Name the unit.** Are you reasoning about a person, account, device, transaction, merchant, or sequence of events? Keep the unit consistent when you count and compare.
2. **Place it on the timeline.** What happened, when was it recorded, and when could a decision-maker first know it? Keep later investigation outcomes separate from prediction-time evidence.
3. **Separate observation from interpretation.** A field is a measurement or proxy. State what it directly records before inferring behavior or intent.
4. **Choose a comparison.** Ask what normal or expected means for this unit, time period, and context. A raw value rarely explains risk by itself.
5. **Connect evidence to an action.** Say what decision this information could change, who bears the cost of an error, and what additional evidence would change your conclusion.

### Worked example

A transaction service may call an API, retrieve recent account aggregates, score a model, apply policy, and return a response. A missing feature store or model timeout requires a defined fallback rather than an accidental approval. When applying **Data Ingestion**, state what is directly known, what is inferred, and what remains uncertain. Then identify the smallest additional observation that would make the interpretation more reliable.

### Common reasoning trap

Focusing on model accuracy while ignoring broken inputs, latency, deployments, and operational recovery. Another useful check is to ask whether the same observation could arise from a legitimate customer, a measurement problem, or a change in how the system collects data. If so, the concept should guide investigation or comparison rather than act as a verdict.

### Check your understanding

Draw one request path and annotate each component’s contract, failure mode, owner, and latency budget.

Try explaining the answer aloud without using the page’s technical vocabulary. If you cannot say what is observed, when it is known, and what decision it informs, revisit the definition and example.

### Continue the learning path

Use the [chapter guide](README.md) to connect this idea to the other concepts in **reliable components and contracts**. The chapter’s central question is: **How do events, features, models, and policies connect while meeting latency, availability, and audit needs?**
