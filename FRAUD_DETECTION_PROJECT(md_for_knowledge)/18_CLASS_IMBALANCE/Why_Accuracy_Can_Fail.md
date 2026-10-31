# Why Accuracy Can Fail

With 99.9% legitimate transactions, a model that always predicts 'not fraud' achieves 99.9% accuracy while catching zero fraud — making accuracy a meaningless metric here.

## Key Points

- A stark illustration of why Section 19 emphasizes precision, recall, and PR-AUC over accuracy
- This is the single most common beginner mistake in fraud modeling

## Understand Why Accuracy Can Fail

### Put the idea in context

Track the real base rate. Apply resampling only within training folds, and evaluate on untouched data at its natural prevalence. Inspect precision, recall, and review volume. Apply **Why Accuracy Can Fail** to an actual payment or investigation as a way to organize evidence. A concept describes one part of the system; it does not, by itself, establish that a customer committed fraud or that a model should take a particular action.

### Think like a data scientist

1. **Name the unit.** Are you reasoning about a person, account, device, transaction, merchant, or sequence of events? Keep the unit consistent when you count and compare.
2. **Place it on the timeline.** What happened, when was it recorded, and when could a decision-maker first know it? Keep later investigation outcomes separate from prediction-time evidence.
3. **Separate observation from interpretation.** A field is a measurement or proxy. State what it directly records before inferring behavior or intent.
4. **Choose a comparison.** Ask what normal or expected means for this unit, time period, and context. A raw value rarely explains risk by itself.
5. **Connect evidence to an action.** Say what decision this information could change, who bears the cost of an error, and what additional evidence would change your conclusion.

### Worked example

If 1 in 100 transactions is fraud, a model that flags 10% of all events has a different operational burden than one that flags 1%. A balanced training sample does not make fraud common in production. When applying **Why Accuracy Can Fail**, state what is directly known, what is inferred, and what remains uncertain. Then identify the smallest additional observation that would make the interpretation more reliable.

### Common reasoning trap

Using accuracy or a balanced evaluation set to claim production performance. Another useful check is to ask whether the same observation could arise from a legitimate customer, a measurement problem, or a change in how the system collects data. If so, the concept should guide investigation or comparison rather than act as a verdict.

### Check your understanding

Calculate how many false alarms arise when precision is applied to a million events at the real fraud prevalence.

Try explaining the answer aloud without using the page’s technical vocabulary. If you cannot say what is observed, when it is known, and what decision it informs, revisit the definition and example.

### Continue the learning path

Use the [chapter guide](README.md) to connect this idea to the other concepts in **rare outcomes change evaluation**. The chapter’s central question is: **How do low fraud prevalence, sampling, weighting, and resampling alter training and decision metrics?**
