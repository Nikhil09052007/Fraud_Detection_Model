# Temporal Data Splitting

Splitting training and test data by time (e.g. train on Jan-Oct, test on Nov-Dec) rather than randomly, to accurately simulate how the model will actually be used in production.

## Key Points

- The correct default splitting strategy for essentially all fraud detection problems
- Prevents both train/test leakage and gives a realistic estimate of future performance

## Understand Temporal Data Splitting

### Put the idea in context

Assign every feature and label an availability time. Split chronologically, fit preprocessing only on the training period, and simulate the intended prediction boundary. Apply **Temporal Data Splitting** to an actual payment or investigation as a way to organize evidence. A concept describes one part of the system; it does not, by itself, establish that a customer committed fraud or that a model should take a particular action.

### Think like a data scientist

1. **Name the unit.** Are you reasoning about a person, account, device, transaction, merchant, or sequence of events? Keep the unit consistent when you count and compare.
2. **Place it on the timeline.** What happened, when was it recorded, and when could a decision-maker first know it? Keep later investigation outcomes separate from prediction-time evidence.
3. **Separate observation from interpretation.** A field is a measurement or proxy. State what it directly records before inferring behavior or intent.
4. **Choose a comparison.** Ask what normal or expected means for this unit, time period, and context. A raw value rarely explains risk by itself.
5. **Connect evidence to an action.** Say what decision this information could change, who bears the cost of an error, and what additional evidence would change your conclusion.

### Worked example

A later investigation result may be strongly correlated with fraud, but it did not exist when an authorization decision was made. Randomly splitting neighboring events can also let future patterns inform past evaluation. When applying **Temporal Data Splitting**, state what is directly known, what is inferred, and what remains uncertain. Then identify the smallest additional observation that would make the interpretation more reliable.

### Common reasoning trap

Thinking leakage is only the target column appearing directly among inputs. Future aggregates and selection effects can leak too. Another useful check is to ask whether the same observation could arise from a legitimate customer, a measurement problem, or a change in how the system collects data. If so, the concept should guide investigation or comparison rather than act as a verdict.

### Check your understanding

For every model input, answer “available by prediction time?” If not, remove it or redefine the decision point.

Try explaining the answer aloud without using the page’s technical vocabulary. If you cannot say what is observed, when it is known, and what decision it informs, revisit the definition and example.

### Continue the learning path

Use the [chapter guide](README.md) to connect this idea to the other concepts in **information must respect the clock**. The chapter’s central question is: **Would this value have been known at the exact moment the model makes its prediction?**
