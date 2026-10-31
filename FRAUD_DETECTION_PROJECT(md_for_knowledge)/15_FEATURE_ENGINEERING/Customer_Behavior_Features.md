# Customer Behavior Features

Features summarizing a customer's historical patterns — average transaction amount, typical merchants, usual times — used to detect deviation.

## Key Points

- Usually the most predictive feature category in fraud models
- Require careful, leakage-free rolling aggregation (only using data before the current transaction)

## Understand Customer Behavior Features

### Put the idea in context

For each engineered feature, document formula, entity, time window, missing-history behavior, fit data, and online equivalent. Compare a simple baseline before adding complexity. Apply **Customer Behavior Features** to an actual payment or investigation as a way to organize evidence. A concept describes one part of the system; it does not, by itself, establish that a customer committed fraud or that a model should take a particular action.

### Think like a data scientist

1. **Name the unit.** Are you reasoning about a person, account, device, transaction, merchant, or sequence of events? Keep the unit consistent when you count and compare.
2. **Place it on the timeline.** What happened, when was it recorded, and when could a decision-maker first know it? Keep later investigation outcomes separate from prediction-time evidence.
3. **Separate observation from interpretation.** A field is a measurement or proxy. State what it directly records before inferring behavior or intent.
4. **Choose a comparison.** Ask what normal or expected means for this unit, time period, and context. A raw value rarely explains risk by itself.
5. **Connect evidence to an action.** Say what decision this information could change, who bears the cost of an error, and what additional evidence would change your conclusion.

### Worked example

A sequence of card purchases can produce counts in prior one-hour windows, time since the previous event, and a deviation from prior spending. The current transaction must not count itself in its own history. When applying **Customer Behavior Features**, state what is directly known, what is inferred, and what remains uncertain. Then identify the smallest additional observation that would make the interpretation more reliable.

### Common reasoning trap

Building a feature that is unavailable at scoring time, leaks the current label, or cannot be reproduced online. Another useful check is to ask whether the same observation could arise from a legitimate customer, a measurement problem, or a change in how the system collects data. If so, the concept should guide investigation or comparison rather than act as a verdict.

### Check your understanding

Design one velocity feature and specify exactly which past events it uses, how ties are handled, and what its first-event value means.

Try explaining the answer aloud without using the page’s technical vocabulary. If you cannot say what is observed, when it is known, and what decision it informs, revisit the definition and example.

### Continue the learning path

Use the [chapter guide](README.md) to connect this idea to the other concepts in **behavior encoded as inputs**. The chapter’s central question is: **How can raw observations be transformed into useful signals without losing meaning or using future information?**
