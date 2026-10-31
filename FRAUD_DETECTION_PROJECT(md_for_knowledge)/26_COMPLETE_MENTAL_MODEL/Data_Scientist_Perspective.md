# Data Scientist Perspective

How a data scientist should think about this whole system day to day: business problem first, careful problem formulation, leakage-free features, rigorous imbalance-aware evaluation, and honest communication of tradeoffs to the business.

## Key Points

- Technical skill (Sections 13-19) is necessary but not sufficient without business framing (Section 12) and systems awareness (Section 23-24)
- The best fraud data scientists move fluidly between statistical rigor and business tradeoff conversations

## Understand Data Scientist Perspective

### Put the idea in context

Trace ideas backward to their assumptions and forward to their consequences. Every model choice should connect to a business need, data evidence, and an operational action. Apply **Data Scientist Perspective** to an actual payment or investigation as a way to organize evidence. A concept describes one part of the system; it does not, by itself, establish that a customer committed fraud or that a model should take a particular action.

### Think like a data scientist

1. **Name the unit.** Are you reasoning about a person, account, device, transaction, merchant, or sequence of events? Keep the unit consistent when you count and compare.
2. **Place it on the timeline.** What happened, when was it recorded, and when could a decision-maker first know it? Keep later investigation outcomes separate from prediction-time evidence.
3. **Separate observation from interpretation.** A field is a measurement or proxy. State what it directly records before inferring behavior or intent.
4. **Choose a comparison.** Ask what normal or expected means for this unit, time period, and context. A raw value rarely explains risk by itself.
5. **Connect evidence to an action.** Say what decision this information could change, who bears the cost of an error, and what additional evidence would change your conclusion.

### Worked example

Start with payment behavior, define the prediction point, gather only available evidence, build a model, evaluate errors, choose a policy, then observe customer and loss outcomes. New labels and attack patterns feed the next version. When applying **Data Scientist Perspective**, state what is directly known, what is inferred, and what remains uncertain. Then identify the smallest additional observation that would make the interpretation more reliable.

### Common reasoning trap

Treating data science as a one-time training run rather than an iterative system with feedback and constraints. Another useful check is to ask whether the same observation could arise from a legitimate customer, a measurement problem, or a change in how the system collects data. If so, the concept should guide investigation or comparison rather than act as a verdict.

### Check your understanding

Explain the complete project using one example transaction, including where uncertainty, latency, labels, and customer costs enter.

Try explaining the answer aloud without using the page’s technical vocabulary. If you cannot say what is observed, when it is known, and what decision it informs, revisit the definition and example.

### Continue the learning path

Use the [chapter guide](README.md) to connect this idea to the other concepts in **connect the full loop**. The chapter’s central question is: **How does a real financial event become data, a prediction, a decision, an outcome, and new evidence?**
