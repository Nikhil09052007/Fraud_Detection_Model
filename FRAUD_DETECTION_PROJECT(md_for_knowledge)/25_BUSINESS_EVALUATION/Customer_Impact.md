# Customer Impact

The effect of the fraud system on legitimate customers — false decline rate, added friction (step-up authentication), and resulting complaints or churn.

## Key Points

- Often measured via false decline rate, customer complaints, and churn correlated with fraud-system friction
- The counterweight to Fraud_Prevented — both must be reported together for an honest picture

## Understand Customer Impact

### Put the idea in context

Separate offline metrics from realized outcomes. Include loss avoided, false declines, review cost, customer impact, control overlap, and measurement uncertainty. Apply **Customer Impact** to an actual payment or investigation as a way to organize evidence. A concept describes one part of the system; it does not, by itself, establish that a customer committed fraud or that a model should take a particular action.

### Think like a data scientist

1. **Name the unit.** Are you reasoning about a person, account, device, transaction, merchant, or sequence of events? Keep the unit consistent when you count and compare.
2. **Place it on the timeline.** What happened, when was it recorded, and when could a decision-maker first know it? Keep later investigation outcomes separate from prediction-time evidence.
3. **Separate observation from interpretation.** A field is a measurement or proxy. State what it directly records before inferring behavior or intent.
4. **Choose a comparison.** Ask what normal or expected means for this unit, time period, and context. A raw value rarely explains risk by itself.
5. **Connect evidence to an action.** Say what decision this information could change, who bears the cost of an error, and what additional evidence would change your conclusion.

### Worked example

Fraud captured is not automatically fraud prevented: some cases would have been stopped by other controls, and some blocked purchases might have been legitimate. Compare outcomes against a credible baseline. When applying **Customer Impact**, state what is directly known, what is inferred, and what remains uncertain. Then identify the smallest additional observation that would make the interpretation more reliable.

### Common reasoning trap

Calling prevented fraud equal to every fraud prediction, or reporting ROI without a counterfactual. Another useful check is to ask whether the same observation could arise from a legitimate customer, a measurement problem, or a change in how the system collects data. If so, the concept should guide investigation or comparison rather than act as a verdict.

### Check your understanding

Build a business scorecard and identify which values are measured, estimated, or unknown.

Try explaining the answer aloud without using the page’s technical vocabulary. If you cannot say what is observed, when it is known, and what decision it informs, revisit the definition and example.

### Continue the learning path

Use the [chapter guide](README.md) to connect this idea to the other concepts in **measure realized impact**. The chapter’s central question is: **Did the system reduce losses enough to justify declines, review operations, customer friction, and implementation cost?**
