# Card Not Present (CNP) Fraud

Fraud where only card details (number, expiry, CVV) are used — typical of online/e-commerce transactions, without the physical card present.

## Key Points

- The dominant fraud type in e-commerce
- Enabled by data breaches, phishing, and card testing
- Harder to catch since there's no physical verification possible

## Understand Card Not Present Fraud

### Put the idea in context

Describe an attack with several labels instead of forcing it into one exclusive category. Identify the attack objective and the observable evidence each label would imply. Apply **Card Not Present Fraud** to an actual payment or investigation as a way to organize evidence. A concept describes one part of the system; it does not, by itself, establish that a customer committed fraud or that a model should take a particular action.

### Think like a data scientist

1. **Name the unit.** Are you reasoning about a person, account, device, transaction, merchant, or sequence of events? Keep the unit consistent when you count and compare.
2. **Place it on the timeline.** What happened, when was it recorded, and when could a decision-maker first know it? Keep later investigation outcomes separate from prediction-time evidence.
3. **Separate observation from interpretation.** A field is a measurement or proxy. State what it directly records before inferring behavior or intent.
4. **Choose a comparison.** Ask what normal or expected means for this unit, time period, and context. A raw value rarely explains risk by itself.
5. **Connect evidence to an action.** Say what decision this information could change, who bears the cost of an error, and what additional evidence would change your conclusion.

### Worked example

A stolen card used online is card-not-present payment fraud and may also be part of an account-takeover campaign. Typologies can overlap because they describe different dimensions: the target, method, channel, or lifecycle stage. When applying **Card Not Present Fraud**, state what is directly known, what is inferred, and what remains uncertain. Then identify the smallest additional observation that would make the interpretation more reliable.

### Common reasoning trap

Treating fraud types as mutually exclusive classes or assuming one feature identifies an entire attack. Another useful check is to ask whether the same observation could arise from a legitimate customer, a measurement problem, or a change in how the system collects data. If so, the concept should guide investigation or comparison rather than act as a verdict.

### Check your understanding

Describe one scenario by target, method, channel, and stage. Which parts can transaction data reveal, and which require investigation?

Try explaining the answer aloud without using the page’s technical vocabulary. If you cannot say what is observed, when it is known, and what decision it informs, revisit the definition and example.

### Continue the learning path

Use the [chapter guide](README.md) to connect this idea to the other concepts in **fraud typologies**. The chapter’s central question is: **Which asset, identity, account, channel, and stage is being attacked?**
