# Risk Score

A single number (often 0-100 or 0-1000) summarizing a transaction's overall fraud risk, typically derived from the model's probability output, sometimes combined with amount/impact.

## Key Points

- Should be interpretable and stable enough for business teams (not just data scientists) to reason about
- Feeds directly into the decision engine's thresholds and rules

## Understand Risk Score

### Put the idea in context

State whether the score is a probability, rank, or points scale. Check calibration and segment stability before attaching verbal meanings or costs. Apply **Risk Score** to an actual payment or investigation as a way to organize evidence. A concept describes one part of the system; it does not, by itself, establish that a customer committed fraud or that a model should take a particular action.

### Think like a data scientist

1. **Name the unit.** Are you reasoning about a person, account, device, transaction, merchant, or sequence of events? Keep the unit consistent when you count and compare.
2. **Place it on the timeline.** What happened, when was it recorded, and when could a decision-maker first know it? Keep later investigation outcomes separate from prediction-time evidence.
3. **Separate observation from interpretation.** A field is a measurement or proxy. State what it directly records before inferring behavior or intent.
4. **Choose a comparison.** Ask what normal or expected means for this unit, time period, and context. A raw value rarely explains risk by itself.
5. **Connect evidence to an action.** Say what decision this information could change, who bears the cost of an error, and what additional evidence would change your conclusion.

### Worked example

A score of 80 on a 0–100 scale may be a rescaled model output rather than an 80% probability. Bands can help route work, but their observed fraud rates depend on data and calibration. When applying **Risk Score**, state what is directly known, what is inferred, and what remains uncertain. Then identify the smallest additional observation that would make the interpretation more reliable.

### Common reasoning trap

Assuming a prettier scale makes predictions more accurate or probabilities calibrated. Another useful check is to ask whether the same observation could arise from a legitimate customer, a measurement problem, or a change in how the system collects data. If so, the concept should guide investigation or comparison rather than act as a verdict.

### Check your understanding

For each band, report volume, observed fraud rate, label maturity, and uncertainty; then say what action the band supports.

Try explaining the answer aloud without using the page’s technical vocabulary. If you cannot say what is observed, when it is known, and what decision it informs, revisit the definition and example.

### Continue the learning path

Use the [chapter guide](README.md) to connect this idea to the other concepts in **prediction becomes a risk estimate**. The chapter’s central question is: **What does the score represent, how calibrated is it, and how should bands be interpreted?**
