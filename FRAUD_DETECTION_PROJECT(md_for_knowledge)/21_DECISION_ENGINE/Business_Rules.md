# Business Rules

Explicit, hand-written logic layered on top of (or ahead of) the model — e.g. 'always block transactions from sanctioned countries' — for cases requiring certainty or compliance, not probability.

## Key Points

- Handle hard-fail cases the model shouldn't need to 'learn' (e.g. legal/compliance requirements)
- Can override the model's decision in either direction when needed
