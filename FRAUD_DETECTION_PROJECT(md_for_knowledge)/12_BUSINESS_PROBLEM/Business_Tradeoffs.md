# Business Tradeoffs

The central tension in fraud detection: catching more fraud (recall) generally means blocking more legitimate transactions (false declines) and costs more to operate — there is no free lunch.

## Key Points

- Fraud loss vs. false declines vs. review cost vs. system cost — these all move together
- The 'right' operating point (threshold) is a business decision, informed by, but not purely dictated by, the model
- This tradeoff reappears formally in Section 19 (Model Evaluation) and Section 21 (Decision Engine)

## Understand Business Tradeoffs

### Put the idea in context

Name all affected parties and outcomes before selecting a metric. Estimate the costs of missed fraud, false declines, review, and friction using realistic assumptions. Apply **Business Tradeoffs** to an actual payment or investigation as a way to organize evidence. A concept describes one part of the system; it does not, by itself, establish that a customer committed fraud or that a model should take a particular action.

### Think like a data scientist

1. **Name the unit.** Are you reasoning about a person, account, device, transaction, merchant, or sequence of events? Keep the unit consistent when you count and compare.
2. **Place it on the timeline.** What happened, when was it recorded, and when could a decision-maker first know it? Keep later investigation outcomes separate from prediction-time evidence.
3. **Separate observation from interpretation.** A field is a measurement or proxy. State what it directly records before inferring behavior or intent.
4. **Choose a comparison.** Ask what normal or expected means for this unit, time period, and context. A raw value rarely explains risk by itself.
5. **Connect evidence to an action.** Say what decision this information could change, who bears the cost of an error, and what additional evidence would change your conclusion.

### Worked example

Blocking one fraudulent payment may prevent a loss, but blocking a legitimate customer can cause abandonment, support calls, and lost trust. Sending a case to review also consumes staff time and delays the customer. When applying **Business Tradeoffs**, state what is directly known, what is inferred, and what remains uncertain. Then identify the smallest additional observation that would make the interpretation more reliable.

### Common reasoning trap

Optimizing fraud recall alone while ignoring legitimate-customer impact and operating cost. Another useful check is to ask whether the same observation could arise from a legitimate customer, a measurement problem, or a change in how the system collects data. If so, the concept should guide investigation or comparison rather than act as a verdict.

### Check your understanding

Write a decision objective with at least three costs. State whose costs are included and which are not measurable yet.

Try explaining the answer aloud without using the page’s technical vocabulary. If you cannot say what is observed, when it is known, and what decision it informs, revisit the definition and example.

### Continue the learning path

Use the [chapter guide](README.md) to connect this idea to the other concepts in **losses and customer friction**. The chapter’s central question is: **What harm is the business trying to reduce, and what harm can the intervention create?**
