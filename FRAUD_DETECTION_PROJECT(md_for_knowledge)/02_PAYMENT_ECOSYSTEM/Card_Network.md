# Card Network

The rail that connects issuing and acquiring banks — e.g. Visa, Mastercard — routing authorization requests and enforcing network rules.

## Key Points

- Doesn't hold customer money — purely routes and governs transactions
- Sets interchange fees and fraud liability rules
- Runs its own network-level fraud scoring in parallel to issuers

## Understand Card Network

### Put the idea in context

Distinguish the message path from the money path. For each actor, ask what it can observe, when it observes it, and which action it can take. Apply **Card Network** to an actual payment or investigation as a way to organize evidence. A concept describes one part of the system; it does not, by itself, establish that a customer committed fraud or that a model should take a particular action.

### Think like a data scientist

1. **Name the unit.** Are you reasoning about a person, account, device, transaction, merchant, or sequence of events? Keep the unit consistent when you count and compare.
2. **Place it on the timeline.** What happened, when was it recorded, and when could a decision-maker first know it? Keep later investigation outcomes separate from prediction-time evidence.
3. **Separate observation from interpretation.** A field is a measurement or proxy. State what it directly records before inferring behavior or intent.
4. **Choose a comparison.** Ask what normal or expected means for this unit, time period, and context. A raw value rarely explains risk by itself.
5. **Connect evidence to an action.** Say what decision this information could change, who bears the cost of an error, and what additional evidence would change your conclusion.

### Worked example

A shopper submits a checkout request. The gateway packages the request, a processor routes it, the card network carries it to the issuer, and the issuer approves or declines against its records. The merchant, acquirer, and issuer may see different fields and have different responsibilities. When applying **Card Network**, state what is directly known, what is inferred, and what remains uncertain. Then identify the smallest additional observation that would make the interpretation more reliable.

### Common reasoning trap

Assuming every party sees the same data or can reverse every outcome. Another useful check is to ask whether the same observation could arise from a legitimate customer, a measurement problem, or a change in how the system collects data. If so, the concept should guide investigation or comparison rather than act as a verdict.

### Check your understanding

Sketch the authorization message path and the later settlement path. Mark where a fraud score could be added and who could act on it.

Try explaining the answer aloud without using the page’s technical vocabulary. If you cannot say what is observed, when it is known, and what decision it informs, revisit the definition and example.

### Continue the learning path

Use the [chapter guide](README.md) to connect this idea to the other concepts in **actors and responsibility**. The chapter’s central question is: **Which parties send instructions, move funds, authorize the payment, and keep the records?**
