# Numerical Data

Continuous or discrete numeric columns — amount, account age, transaction count — that often need scaling or transformation before modeling.

## Key Points

- Check for outliers, skew, and scale differences across features
- Tree-based models are relatively robust to scale; linear models are not

## Understand Numerical Data

### Put the idea in context

Check schema, key uniqueness, duplicates, missingness, distributions, time coverage, target prevalence, and train/test differences. Validate findings against how the data was collected. Apply **Numerical Data** to an actual payment or investigation as a way to organize evidence. A concept describes one part of the system; it does not, by itself, establish that a customer committed fraud or that a model should take a particular action.

### Think like a data scientist

1. **Name the unit.** Are you reasoning about a person, account, device, transaction, merchant, or sequence of events? Keep the unit consistent when you count and compare.
2. **Place it on the timeline.** What happened, when was it recorded, and when could a decision-maker first know it? Keep later investigation outcomes separate from prediction-time evidence.
3. **Separate observation from interpretation.** A field is a measurement or proxy. State what it directly records before inferring behavior or intent.
4. **Choose a comparison.** Ask what normal or expected means for this unit, time period, and context. A raw value rarely explains risk by itself.
5. **Connect evidence to an action.** Say what decision this information could change, who bears the cost of an error, and what additional evidence would change your conclusion.

### Worked example

A feature can appear useful because it is missing for a particular device population or because the train and test periods differ. Data profiling reveals such patterns before they become unexplained model behavior. When applying **Numerical Data**, state what is directly known, what is inferred, and what remains uncertain. Then identify the smallest additional observation that would make the interpretation more reliable.

### Common reasoning trap

Treating a successful notebook run as proof that the data is valid or representative. Another useful check is to ask whether the same observation could arise from a legitimate customer, a measurement problem, or a change in how the system collects data. If so, the concept should guide investigation or comparison rather than act as a verdict.

### Check your understanding

Summarize one field’s distribution, missingness, time trend, and association with the label. Give at least one alternative explanation.

Try explaining the answer aloud without using the page’s technical vocabulary. If you cannot say what is observed, when it is known, and what decision it informs, revisit the definition and example.

### Continue the learning path

Use the [chapter guide](README.md) to connect this idea to the other concepts in **evidence before modeling**. The chapter’s central question is: **What are the dataset’s rows, columns, coverage, quality issues, distributions, and collection limits?**
