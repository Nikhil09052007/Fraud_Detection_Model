# What is Fintech?

Fintech (financial technology) refers to companies that use technology to deliver financial services — payments, lending, banking — often faster or more accessibly than traditional banks, frequently by partnering with or building on top of banking infrastructure.

## Key Points

- Examples: payment processors, digital wallets, neobanks, buy-now-pay-later providers
- Fintechs often generate the transaction and behavioral data fraud models are trained on
- Fraud risk is often higher in fintech due to faster onboarding and thinner friction

## Understand What is Fintech

### Put the idea in context

Translate the story into entities and relationships before choosing columns. Ask who owns each record, what balance or obligation changes, and who can correct an error. Apply **What is Fintech** to an actual payment or investigation as a way to organize evidence. A concept describes one part of the system; it does not, by itself, establish that a customer committed fraud or that a model should take a particular action.

### Think like a data scientist

1. **Name the unit.** Are you reasoning about a person, account, device, transaction, merchant, or sequence of events? Keep the unit consistent when you count and compare.
2. **Place it on the timeline.** What happened, when was it recorded, and when could a decision-maker first know it? Keep later investigation outcomes separate from prediction-time evidence.
3. **Separate observation from interpretation.** A field is a measurement or proxy. State what it directly records before inferring behavior or intent.
4. **Choose a comparison.** Ask what normal or expected means for this unit, time period, and context. A raw value rarely explains risk by itself.
5. **Connect evidence to an action.** Say what decision this information could change, who bears the cost of an error, and what additional evidence would change your conclusion.

### Worked example

A customer pays a merchant with a card. Separate the customer, the account that funds the purchase, the card that identifies the payment route, and the merchant receiving it. One person can have several accounts and instruments; a mismatch is a question to investigate, not proof of fraud. When applying **What is Fintech**, state what is directly known, what is inferred, and what remains uncertain. Then identify the smallest additional observation that would make the interpretation more reliable.

### Common reasoning trap

Treating a card number, account, customer, and transaction as if they were the same thing. Another useful check is to ask whether the same observation could arise from a legitimate customer, a measurement problem, or a change in how the system collects data. If so, the concept should guide investigation or comparison rather than act as a verdict.

### Check your understanding

Draw one payment and label the payer, funding account, instrument, merchant, and institutions. State which records each party would hold.

Try explaining the answer aloud without using the page’s technical vocabulary. If you cannot say what is observed, when it is known, and what decision it informs, revisit the definition and example.

### Continue the learning path

Use the [chapter guide](README.md) to connect this idea to the other concepts in **foundation: money and records**. The chapter’s central question is: **What is actually happening when value moves, and which person, account, institution, or merchant is involved?**
