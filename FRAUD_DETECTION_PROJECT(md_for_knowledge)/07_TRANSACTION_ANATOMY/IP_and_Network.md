# IP and Network

The IP address and network characteristics (VPN/proxy use, ISP, ASN) from which the transaction was initiated.

## Key Points

- IP geolocation can be compared against billing/shipping address for mismatches
- VPN/proxy/Tor usage is a common risk flag
- Shared IPs across many accounts can indicate fraud rings

## Understand IP and Network

### Put the idea in context

For each field, record its unit, grain, source, missingness meaning, and availability time. Verify whether a column describes the transaction itself or information learned later. Apply **IP and Network** to an actual payment or investigation as a way to organize evidence. A concept describes one part of the system; it does not, by itself, establish that a customer committed fraud or that a model should take a particular action.

### Think like a data scientist

1. **Name the unit.** Are you reasoning about a person, account, device, transaction, merchant, or sequence of events? Keep the unit consistent when you count and compare.
2. **Place it on the timeline.** What happened, when was it recorded, and when could a decision-maker first know it? Keep later investigation outcomes separate from prediction-time evidence.
3. **Separate observation from interpretation.** A field is a measurement or proxy. State what it directly records before inferring behavior or intent.
4. **Choose a comparison.** Ask what normal or expected means for this unit, time period, and context. A raw value rarely explains risk by itself.
5. **Connect evidence to an action.** Say what decision this information could change, who bears the cost of an error, and what additional evidence would change your conclusion.

### Worked example

A transaction row may combine amount, time, merchant, payment instrument, device, and network observations. An identifier can join records without meaning the underlying values are stable or globally unique. When applying **IP and Network**, state what is directly known, what is inferred, and what remains uncertain. Then identify the smallest additional observation that would make the interpretation more reliable.

### Common reasoning trap

Assuming a column name fully defines its meaning or that a null always means “no.” Another useful check is to ask whether the same observation could arise from a legitimate customer, a measurement problem, or a change in how the system collects data. If so, the concept should guide investigation or comparison rather than act as a verdict.

### Check your understanding

Choose five fields and write a data dictionary entry for each: definition, unit, source, as-of time, and one ambiguity.

Try explaining the answer aloud without using the page’s technical vocabulary. If you cannot say what is observed, when it is known, and what decision it informs, revisit the definition and example.

### Continue the learning path

Use the [chapter guide](README.md) to connect this idea to the other concepts in **events and fields**. The chapter’s central question is: **What is one row, what does each field measure, and what was knowable when the row was created?**
