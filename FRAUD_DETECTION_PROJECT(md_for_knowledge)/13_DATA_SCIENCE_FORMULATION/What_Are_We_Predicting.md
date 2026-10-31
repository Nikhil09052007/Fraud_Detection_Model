# What Are We Predicting?

In this repo's core formulation: the probability that a given transaction, at the moment of authorization, is fraudulent.

## Key Points

- Precisely scoped — not 'is this customer a fraudster' (a different, harder problem) but 'is this transaction fraudulent'
- Scope changes (per-transaction vs per-customer vs per-session) lead to very different systems

## Understand What Are We Predicting

### Put the idea in context

Specify unit, prediction timestamp, target definition, horizon, label maturation, action, and split strategy. Then check every proposed input against the as-of time. Apply **What Are We Predicting** to an actual payment or investigation as a way to organize evidence. A concept describes one part of the system; it does not, by itself, establish that a customer committed fraud or that a model should take a particular action.

### Think like a data scientist

1. **Name the unit.** Are you reasoning about a person, account, device, transaction, merchant, or sequence of events? Keep the unit consistent when you count and compare.
2. **Place it on the timeline.** What happened, when was it recorded, and when could a decision-maker first know it? Keep later investigation outcomes separate from prediction-time evidence.
3. **Separate observation from interpretation.** A field is a measurement or proxy. State what it directly records before inferring behavior or intent.
4. **Choose a comparison.** Ask what normal or expected means for this unit, time period, and context. A raw value rarely explains risk by itself.
5. **Connect evidence to an action.** Say what decision this information could change, who bears the cost of an error, and what additional evidence would change your conclusion.

### Worked example

For a transaction-level model, the unit may be one authorization request and the target may be confirmed unauthorized fraud within a defined follow-up period. A chargeback days later cannot be a feature at authorization time. When applying **What Are We Predicting**, state what is directly known, what is inferred, and what remains uncertain. Then identify the smallest additional observation that would make the interpretation more reliable.

### Common reasoning trap

Writing “predict fraud” without deciding what counts as fraud, when prediction happens, or how action follows. Another useful check is to ask whether the same observation could arise from a legitimate customer, a measurement problem, or a change in how the system collects data. If so, the concept should guide investigation or comparison rather than act as a verdict.

### Check your understanding

Complete the sentence: At time T, using fields available by T, predict outcome Y within H for unit U, so actor A can take action D.

Try explaining the answer aloud without using the page’s technical vocabulary. If you cannot say what is observed, when it is known, and what decision it informs, revisit the definition and example.

### Continue the learning path

Use the [chapter guide](README.md) to connect this idea to the other concepts in **business question to prediction**. The chapter’s central question is: **What exact event is predicted, for which entity, using information available at what prediction point and horizon?**
