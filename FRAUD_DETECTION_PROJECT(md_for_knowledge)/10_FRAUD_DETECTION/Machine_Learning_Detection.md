# Machine Learning Detection

Using models trained on historical labeled data to learn complex, non-obvious patterns that separate fraud from legitimate activity, generalizing beyond hand-written rules.

## Key Points

- Can combine hundreds of weak features into one strong prediction
- Requires quality labeled data, careful feature engineering, and ongoing retraining
- The primary technique this entire repo builds toward

## Understand Machine Learning Detection

### Put the idea in context

Evaluate each control by the evidence it uses, latency, coverage, false-positive burden, and action path. Look for defense in depth rather than a single perfect detector. Apply **Machine Learning Detection** to an actual payment or investigation as a way to organize evidence. A concept describes one part of the system; it does not, by itself, establish that a customer committed fraud or that a model should take a particular action.

### Think like a data scientist

1. **Name the unit.** Are you reasoning about a person, account, device, transaction, merchant, or sequence of events? Keep the unit consistent when you count and compare.
2. **Place it on the timeline.** What happened, when was it recorded, and when could a decision-maker first know it? Keep later investigation outcomes separate from prediction-time evidence.
3. **Separate observation from interpretation.** A field is a measurement or proxy. State what it directly records before inferring behavior or intent.
4. **Choose a comparison.** Ask what normal or expected means for this unit, time period, and context. A raw value rarely explains risk by itself.
5. **Connect evidence to an action.** Say what decision this information could change, who bears the cost of an error, and what additional evidence would change your conclusion.

### Worked example

A simple rule can stop a known compromised card immediately, while a model ranks less obvious cases and an analyst reviews ambiguous ones. The system should also handle outages and allow legitimate customers to recover. When applying **Machine Learning Detection**, state what is directly known, what is inferred, and what remains uncertain. Then identify the smallest additional observation that would make the interpretation more reliable.

### Common reasoning trap

Assuming machine learning replaces rules, investigations, or operational design. Another useful check is to ask whether the same observation could arise from a legitimate customer, a measurement problem, or a change in how the system collects data. If so, the concept should guide investigation or comparison rather than act as a verdict.

### Check your understanding

Choose an attack pattern and design a rule, a model signal, a review action, and a safe fallback. Explain what each contributes.

Try explaining the answer aloud without using the page’s technical vocabulary. If you cannot say what is observed, when it is known, and what decision it informs, revisit the definition and example.

### Continue the learning path

Use the [chapter guide](README.md) to connect this idea to the other concepts in **controls work as a system**. The chapter’s central question is: **How should rules, models, analysts, and customer challenges combine to reduce loss without excessive friction?**
