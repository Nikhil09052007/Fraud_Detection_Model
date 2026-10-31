# Normal Behavior

The typical, expected pattern of activity for a given customer, account, device, or merchant — the baseline against which new activity is judged.

## Key Points

- Established from historical data, usually via rolling averages or typical ranges
- Different for every entity — normal for one customer may be abnormal for another

## Understand Normal Behavior

### Put the idea in context

Define the comparison group before calling something abnormal. Combine signals, measure how long the baseline is observed, and test whether a deviation changes risk after accounting for context. Apply **Normal Behavior** to an actual payment or investigation as a way to organize evidence. A concept describes one part of the system; it does not, by itself, establish that a customer committed fraud or that a model should take a particular action.

### Think like a data scientist

1. **Name the unit.** Are you reasoning about a person, account, device, transaction, merchant, or sequence of events? Keep the unit consistent when you count and compare.
2. **Place it on the timeline.** What happened, when was it recorded, and when could a decision-maker first know it? Keep later investigation outcomes separate from prediction-time evidence.
3. **Separate observation from interpretation.** A field is a measurement or proxy. State what it directly records before inferring behavior or intent.
4. **Choose a comparison.** Ask what normal or expected means for this unit, time period, and context. A raw value rarely explains risk by itself.
5. **Connect evidence to an action.** Say what decision this information could change, who bears the cost of an error, and what additional evidence would change your conclusion.

### Worked example

A high amount may be normal for a business account but unusual for a customer who normally makes small local purchases. A new device may be common after a phone upgrade and risky when paired with a new location and rapid spending. When applying **Normal Behavior**, state what is directly known, what is inferred, and what remains uncertain. Then identify the smallest additional observation that would make the interpretation more reliable.

### Common reasoning trap

Equating unusual with fraudulent, or using population-wide averages as every customer’s normal behavior. Another useful check is to ask whether the same observation could arise from a legitimate customer, a measurement problem, or a change in how the system collects data. If so, the concept should guide investigation or comparison rather than act as a verdict.

### Check your understanding

Compare the same transaction against its customer history and a peer group. Which signals are informative, and what could explain them legitimately?

Try explaining the answer aloud without using the page’s technical vocabulary. If you cannot say what is observed, when it is known, and what decision it informs, revisit the definition and example.

### Continue the learning path

Use the [chapter guide](README.md) to connect this idea to the other concepts in **behavior depends on context**. The chapter’s central question is: **Compared with which customer baseline, peer group, time window, and sequence is an event unusual?**
