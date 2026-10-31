# Why Real-Time Matters

Once a transaction is authorized and funds move, reversing fraud becomes far harder and costlier — chargebacks, disputes, and recovery efforts are expensive and often unsuccessful.

## Key Points

- Blocking fraud before authorization is dramatically cheaper than recovering it after
- The entire system must fit its decision inside the payment authorization window (often under 1-2 seconds)

## Understand Why Real Time Matters

### Put the idea in context

Trace arrival, feature lookup, scoring, policy, and response. Measure latency at each stage and specify behavior for missing, delayed, or unavailable dependencies. Apply **Why Real Time Matters** to an actual payment or investigation as a way to organize evidence. A concept describes one part of the system; it does not, by itself, establish that a customer committed fraud or that a model should take a particular action.

### Think like a data scientist

1. **Name the unit.** Are you reasoning about a person, account, device, transaction, merchant, or sequence of events? Keep the unit consistent when you count and compare.
2. **Place it on the timeline.** What happened, when was it recorded, and when could a decision-maker first know it? Keep later investigation outcomes separate from prediction-time evidence.
3. **Separate observation from interpretation.** A field is a measurement or proxy. State what it directly records before inferring behavior or intent.
4. **Choose a comparison.** Ask what normal or expected means for this unit, time period, and context. A raw value rarely explains risk by itself.
5. **Connect evidence to an action.** Say what decision this information could change, who bears the cost of an error, and what additional evidence would change your conclusion.

### Worked example

A checkout request arrives and must be scored in milliseconds. Account history may be available from a fast feature store, while a batch report from yesterday is too stale for an immediate decision. When applying **Why Real Time Matters**, state what is directly known, what is inferred, and what remains uncertain. Then identify the smallest additional observation that would make the interpretation more reliable.

### Common reasoning trap

Calling a process real time merely because it runs automatically, or ignoring stale state and tail latency. Another useful check is to ask whether the same observation could arise from a legitimate customer, a measurement problem, or a change in how the system collects data. If so, the concept should guide investigation or comparison rather than act as a verdict.

### Check your understanding

Set a response deadline. Allocate it across feature retrieval, model scoring, and decisioning, then define the timeout behavior.

Try explaining the answer aloud without using the page’s technical vocabulary. If you cannot say what is observed, when it is known, and what decision it informs, revisit the definition and example.

### Continue the learning path

Use the [chapter guide](README.md) to connect this idea to the other concepts in **decision under a time budget**. The chapter’s central question is: **What can be computed before the payment response deadline, and how fresh and reliable are those inputs?**
