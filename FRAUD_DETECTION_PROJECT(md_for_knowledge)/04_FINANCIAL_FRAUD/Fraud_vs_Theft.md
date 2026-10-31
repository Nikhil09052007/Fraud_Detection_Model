# Fraud vs Theft

Theft is the physical or direct taking of an asset (e.g. stealing a wallet); fraud is deception used to obtain something, often without direct physical taking.

## Key Points

- Theft can enable fraud (a stolen card enables fraudulent transactions)
- Fraud is about deceit; theft is about unauthorized taking
- A fraud model cares about the transaction pattern, not how the credential was obtained

## Understand Fraud vs Theft

### Put the idea in context

Separate underlying intent from the evidence available in a dataset. Ask who adjudicates the label, when it matures, and which legitimate outcomes can look similar. Apply **Fraud vs Theft** to an actual payment or investigation as a way to organize evidence. A concept describes one part of the system; it does not, by itself, establish that a customer committed fraud or that a model should take a particular action.

### Think like a data scientist

1. **Name the unit.** Are you reasoning about a person, account, device, transaction, merchant, or sequence of events? Keep the unit consistent when you count and compare.
2. **Place it on the timeline.** What happened, when was it recorded, and when could a decision-maker first know it? Keep later investigation outcomes separate from prediction-time evidence.
3. **Separate observation from interpretation.** A field is a measurement or proxy. State what it directly records before inferring behavior or intent.
4. **Choose a comparison.** Ask what normal or expected means for this unit, time period, and context. A raw value rarely explains risk by itself.
5. **Connect evidence to an action.** Say what decision this information could change, who bears the cost of an error, and what additional evidence would change your conclusion.

### Worked example

A cardholder disputes a purchase weeks after it was approved. The dispute is an observable outcome; it might indicate stolen-card fraud, a merchant mistake, a family member’s purchase, or friendly fraud. The label needs a clear adjudication rule. When applying **Fraud vs Theft**, state what is directly known, what is inferred, and what remains uncertain. Then identify the smallest additional observation that would make the interpretation more reliable.

### Common reasoning trap

Equating theft, default, dispute, loss, and fraud. These overlap in some cases but answer different questions. Another useful check is to ask whether the same observation could arise from a legitimate customer, a measurement problem, or a change in how the system collects data. If so, the concept should guide investigation or comparison rather than act as a verdict.

### Check your understanding

Take a disputed transaction and list at least two explanations. What extra evidence would distinguish them, and when would it become available?

Try explaining the answer aloud without using the page’s technical vocabulary. If you cannot say what is observed, when it is known, and what decision it informs, revisit the definition and example.

### Continue the learning path

Use the [chapter guide](README.md) to connect this idea to the other concepts in **intent, event, and outcome**. The chapter’s central question is: **What behavior is unauthorized or deceptive, and what evidence can establish that classification?**
