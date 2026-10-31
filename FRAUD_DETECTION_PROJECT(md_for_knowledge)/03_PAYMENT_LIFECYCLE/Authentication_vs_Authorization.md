# Authentication vs Authorization

Authentication proves identity ('who are you'); authorization decides permission ('can this transaction go through'). Both can independently fail even when the other succeeds.

## Key Points

- Authentication answers identity; authorization answers eligibility/risk
- A well-authenticated user can still be declined for authorization reasons (insufficient funds, risk score)
- Fraud models mostly operate at the authorization stage

## Understand Authentication vs Authorization

### Put the idea in context

Use a timeline and event timestamps. Keep authentication, authorization, clearing, settlement, reversal, and dispute as distinct events; late evidence must not be used as if it existed at decision time. Apply **Authentication vs Authorization** to an actual payment or investigation as a way to organize evidence. A concept describes one part of the system; it does not, by itself, establish that a customer committed fraud or that a model should take a particular action.

### Think like a data scientist

1. **Name the unit.** Are you reasoning about a person, account, device, transaction, merchant, or sequence of events? Keep the unit consistent when you count and compare.
2. **Place it on the timeline.** What happened, when was it recorded, and when could a decision-maker first know it? Keep later investigation outcomes separate from prediction-time evidence.
3. **Separate observation from interpretation.** A field is a measurement or proxy. State what it directly records before inferring behavior or intent.
4. **Choose a comparison.** Ask what normal or expected means for this unit, time period, and context. A raw value rarely explains risk by itself.
5. **Connect evidence to an action.** Say what decision this information could change, who bears the cost of an error, and what additional evidence would change your conclusion.

### Worked example

A card authorization may be approved now, cleared later, and settled after that. Approval means the issuer accepted the authorization request at that moment; it does not prove the transaction is genuine or guarantee final settlement. When applying **Authentication vs Authorization**, state what is directly known, what is inferred, and what remains uncertain. Then identify the smallest additional observation that would make the interpretation more reliable.

### Common reasoning trap

Treating an approval as final truth or a chargeback as immediate proof of intentional fraud. Another useful check is to ask whether the same observation could arise from a legitimate customer, a measurement problem, or a change in how the system collects data. If so, the concept should guide investigation or comparison rather than act as a verdict.

### Check your understanding

Place authorization, clearing, settlement, and possible dispute on a timeline. For each, write what is known and what remains unknown.

Try explaining the answer aloud without using the page’s technical vocabulary. If you cannot say what is observed, when it is known, and what decision it informs, revisit the definition and example.

### Continue the learning path

Use the [chapter guide](README.md) to connect this idea to the other concepts in **events and stages**. The chapter’s central question is: **At what stage is the payment, and what does its current status actually mean?**
