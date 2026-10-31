# Model Retraining

The process of periodically (or triggered by drift detection) retraining the model on fresh data to keep pace with evolving fraud patterns.

## Key Points

- Cadence depends on how fast fraud patterns evolve in your specific business — can range from weekly to quarterly
- Should follow the same leakage-safe practices (Section 16) as the original training process

## Understand Model Retraining

### Put the idea in context

Monitor data quality, feature and score drift, matured-label metrics, action rates, review capacity, and customer outcomes. Investigate causes before retraining. Apply **Model Retraining** to an actual payment or investigation as a way to organize evidence. A concept describes one part of the system; it does not, by itself, establish that a customer committed fraud or that a model should take a particular action.

### Think like a data scientist

1. **Name the unit.** Are you reasoning about a person, account, device, transaction, merchant, or sequence of events? Keep the unit consistent when you count and compare.
2. **Place it on the timeline.** What happened, when was it recorded, and when could a decision-maker first know it? Keep later investigation outcomes separate from prediction-time evidence.
3. **Separate observation from interpretation.** A field is a measurement or proxy. State what it directly records before inferring behavior or intent.
4. **Choose a comparison.** Ask what normal or expected means for this unit, time period, and context. A raw value rarely explains risk by itself.
5. **Connect evidence to an action.** Say what decision this information could change, who bears the cost of an error, and what additional evidence would change your conclusion.

### Worked example

A shift in score distribution can come from a new customer mix, a broken feature pipeline, or changed attacker behavior. Mature labels are needed before outcome metrics can be trusted. When applying **Model Retraining**, state what is directly known, what is inferred, and what remains uncertain. Then identify the smallest additional observation that would make the interpretation more reliable.

### Common reasoning trap

Treating drift as proof of model failure or retraining automatically on unstable labels. Another useful check is to ask whether the same observation could arise from a legitimate customer, a measurement problem, or a change in how the system collects data. If so, the concept should guide investigation or comparison rather than act as a verdict.

### Check your understanding

For one alert, name at least three possible causes and the evidence needed to distinguish them.

Try explaining the answer aloud without using the page’s technical vocabulary. If you cannot say what is observed, when it is known, and what decision it informs, revisit the definition and example.

### Continue the learning path

Use the [chapter guide](README.md) to connect this idea to the other concepts in **performance changes over time**. The chapter’s central question is: **Which signals reveal input change, model degradation, label delay, policy burden, or customer harm?**
