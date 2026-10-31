# How Payment Entities Interact

A full payment flow: Customer → Merchant → Gateway → Processor → Card Network → Issuing Bank (approves/declines) → back down the chain to the merchant, in usually under a second.

## Key Points

- Each hop can add its own fraud check
- Latency at each hop matters — real-time fraud detection must fit within this window
- Data available to your model depends on which entity you are in this chain

## Example

A customer taps their card → gateway captures details → processor routes to Visa → Visa routes to the issuing bank → issuing bank scores the transaction and returns approve/decline → response flows back to the terminal, all within ~1-2 seconds.

## Understand How Payment Entities Interact

### Put the idea in context

Distinguish the message path from the money path. For each actor, ask what it can observe, when it observes it, and which action it can take. Apply **How Payment Entities Interact** to an actual payment or investigation as a way to organize evidence. A concept describes one part of the system; it does not, by itself, establish that a customer committed fraud or that a model should take a particular action.

### Think like a data scientist

1. **Name the unit.** Are you reasoning about a person, account, device, transaction, merchant, or sequence of events? Keep the unit consistent when you count and compare.
2. **Place it on the timeline.** What happened, when was it recorded, and when could a decision-maker first know it? Keep later investigation outcomes separate from prediction-time evidence.
3. **Separate observation from interpretation.** A field is a measurement or proxy. State what it directly records before inferring behavior or intent.
4. **Choose a comparison.** Ask what normal or expected means for this unit, time period, and context. A raw value rarely explains risk by itself.
5. **Connect evidence to an action.** Say what decision this information could change, who bears the cost of an error, and what additional evidence would change your conclusion.

### Worked example

A shopper submits a checkout request. The gateway packages the request, a processor routes it, the card network carries it to the issuer, and the issuer approves or declines against its records. The merchant, acquirer, and issuer may see different fields and have different responsibilities. When applying **How Payment Entities Interact**, state what is directly known, what is inferred, and what remains uncertain. Then identify the smallest additional observation that would make the interpretation more reliable.

### Common reasoning trap

Assuming every party sees the same data or can reverse every outcome. Another useful check is to ask whether the same observation could arise from a legitimate customer, a measurement problem, or a change in how the system collects data. If so, the concept should guide investigation or comparison rather than act as a verdict.

### Check your understanding

Sketch the authorization message path and the later settlement path. Mark where a fraud score could be added and who could act on it.

Try explaining the answer aloud without using the page’s technical vocabulary. If you cannot say what is observed, when it is known, and what decision it informs, revisit the definition and example.

### Continue the learning path

Use the [chapter guide](README.md) to connect this idea to the other concepts in **actors and responsibility**. The chapter’s central question is: **Which parties send instructions, move funds, authorize the payment, and keep the records?**
