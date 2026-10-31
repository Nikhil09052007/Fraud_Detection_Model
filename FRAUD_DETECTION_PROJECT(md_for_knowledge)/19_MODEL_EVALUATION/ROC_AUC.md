# ROC AUC

The area under the Receiver Operating Characteristic curve, measuring how well the model ranks fraud above non-fraud across all thresholds, in terms of true positive rate vs false positive rate.

## Key Points

- Threshold-independent — summarizes overall ranking ability
- Can be overly optimistic on highly imbalanced data since it's diluted by the large true-negative population — PR-AUC is often preferred for fraud

## Understand ROC AUC

### Put the idea in context

Inspect PR-AUC, recall, precision, false-positive rate, calibration, threshold curves, segment performance, temporal stability, and cost assumptions. Reserve data for final evaluation. Apply **ROC AUC** to an actual payment or investigation as a way to organize evidence. A concept describes one part of the system; it does not, by itself, establish that a customer committed fraud or that a model should take a particular action.

### Think like a data scientist

1. **Name the unit.** Are you reasoning about a person, account, device, transaction, merchant, or sequence of events? Keep the unit consistent when you count and compare.
2. **Place it on the timeline.** What happened, when was it recorded, and when could a decision-maker first know it? Keep later investigation outcomes separate from prediction-time evidence.
3. **Separate observation from interpretation.** A field is a measurement or proxy. State what it directly records before inferring behavior or intent.
4. **Choose a comparison.** Ask what normal or expected means for this unit, time period, and context. A raw value rarely explains risk by itself.
5. **Connect evidence to an action.** Say what decision this information could change, who bears the cost of an error, and what additional evidence would change your conclusion.

### Worked example

A high ROC-AUC can coexist with a low precision when fraud is rare. A threshold can catch more fraud but flood a review team. A single validation window may not represent future attacks. When applying **ROC AUC**, state what is directly known, what is inferred, and what remains uncertain. Then identify the smallest additional observation that would make the interpretation more reliable.

### Common reasoning trap

Choosing one metric in isolation or tuning and reporting on the same set as if it were untouched. Another useful check is to ask whether the same observation could arise from a legitimate customer, a measurement problem, or a change in how the system collects data. If so, the concept should guide investigation or comparison rather than act as a verdict.

### Check your understanding

Given two models, compare them at equal review capacity and explain which errors and customer outcomes differ.

Try explaining the answer aloud without using the page’s technical vocabulary. If you cannot say what is observed, when it is known, and what decision it informs, revisit the definition and example.

### Continue the learning path

Use the [chapter guide](README.md) to connect this idea to the other concepts in **evidence for model usefulness**. The chapter’s central question is: **Does the model rank fraud well, behave acceptably at an operating threshold, and generalize to a later period?**
