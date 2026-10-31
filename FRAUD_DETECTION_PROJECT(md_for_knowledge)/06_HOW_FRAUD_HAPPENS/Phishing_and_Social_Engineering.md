# Phishing and Social Engineering

Techniques that trick victims into voluntarily giving up credentials or authorizing fraudulent transactions, exploiting trust rather than technical vulnerabilities.

## Key Points

- Fake emails, texts, or calls impersonating trusted entities
- Often the first step in an account takeover chain
- Hard to detect purely from transaction data — needs behavioral/session context

## Understand Phishing and Social Engineering

### Put the idea in context

Model the attack as a sequence. For every stage, distinguish what happened in the real world from what a system logs, and note the time lag between them. Apply **Phishing and Social Engineering** to an actual payment or investigation as a way to organize evidence. A concept describes one part of the system; it does not, by itself, establish that a customer committed fraud or that a model should take a particular action.

### Think like a data scientist

1. **Name the unit.** Are you reasoning about a person, account, device, transaction, merchant, or sequence of events? Keep the unit consistent when you count and compare.
2. **Place it on the timeline.** What happened, when was it recorded, and when could a decision-maker first know it? Keep later investigation outcomes separate from prediction-time evidence.
3. **Separate observation from interpretation.** A field is a measurement or proxy. State what it directly records before inferring behavior or intent.
4. **Choose a comparison.** Ask what normal or expected means for this unit, time period, and context. A raw value rarely explains risk by itself.
5. **Connect evidence to an action.** Say what decision this information could change, who bears the cost of an error, and what additional evidence would change your conclusion.

### Worked example

An attacker obtains credentials through phishing, tests whether they work, then makes rapid purchases or cashes out. A transaction table may show the testing and spending pattern but not the phishing message or who controlled the device. When applying **Phishing and Social Engineering**, state what is directly known, what is inferred, and what remains uncertain. Then identify the smallest additional observation that would make the interpretation more reliable.

### Common reasoning trap

Expecting one transaction or one model feature to reveal the whole attack. Another useful check is to ask whether the same observation could arise from a legitimate customer, a measurement problem, or a change in how the system collects data. If so, the concept should guide investigation or comparison rather than act as a verdict.

### Check your understanding

Draw the attack chain. Mark one prevention point, one detection point, the evidence available at each point, and a possible false alarm.

Try explaining the answer aloud without using the page’s technical vocabulary. If you cannot say what is observed, when it is known, and what decision it informs, revisit the definition and example.

### Continue the learning path

Use the [chapter guide](README.md) to connect this idea to the other concepts in **attack chains and evidence**. The chapter’s central question is: **How does an attacker move from opportunity to attempted payment, and where could controls interrupt the chain?**
