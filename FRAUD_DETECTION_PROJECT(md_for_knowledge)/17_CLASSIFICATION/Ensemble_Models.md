# Ensemble Models

Models that combine many individual models (typically decision trees) to produce a stronger, more robust prediction — e.g. Random Forest, XGBoost, LightGBM.

## Key Points

- The dominant model family in real-world fraud detection due to strong performance on tabular data
- Gradient boosted trees (XGBoost/LightGBM) are the most common production choice

## Understand Ensemble Models

### Put the idea in context

Separate ranking, probability calibration, and threshold policy. Compare models using ranking metrics, then select actions against explicit operating objectives. Apply **Ensemble Models** to an actual payment or investigation as a way to organize evidence. A concept describes one part of the system; it does not, by itself, establish that a customer committed fraud or that a model should take a particular action.

### Think like a data scientist

1. **Name the unit.** Are you reasoning about a person, account, device, transaction, merchant, or sequence of events? Keep the unit consistent when you count and compare.
2. **Place it on the timeline.** What happened, when was it recorded, and when could a decision-maker first know it? Keep later investigation outcomes separate from prediction-time evidence.
3. **Separate observation from interpretation.** A field is a measurement or proxy. State what it directly records before inferring behavior or intent.
4. **Choose a comparison.** Ask what normal or expected means for this unit, time period, and context. A raw value rarely explains risk by itself.
5. **Connect evidence to an action.** Say what decision this information could change, who bears the cost of an error, and what additional evidence would change your conclusion.

### Worked example

A classifier may assign 0.12 to a transaction. That number can rank it above many peers; whether it means a 12% chance depends on calibration and population stability. The business action depends on costs and capacity. When applying **Ensemble Models**, state what is directly known, what is inferred, and what remains uncertain. Then identify the smallest additional observation that would make the interpretation more reliable.

### Common reasoning trap

Treating 0.5 as a natural threshold or reading every model score as a calibrated probability. Another useful check is to ask whether the same observation could arise from a legitimate customer, a measurement problem, or a change in how the system collects data. If so, the concept should guide investigation or comparison rather than act as a verdict.

### Check your understanding

Explain what a score of 0.12 means for ranking, calibration, and action separately.

Try explaining the answer aloud without using the page’s technical vocabulary. If you cannot say what is observed, when it is known, and what decision it informs, revisit the definition and example.

### Continue the learning path

Use the [chapter guide](README.md) to connect this idea to the other concepts in **score is not action**. The chapter’s central question is: **What score is predicted, how should it be interpreted, and what threshold maps it to an action?**
