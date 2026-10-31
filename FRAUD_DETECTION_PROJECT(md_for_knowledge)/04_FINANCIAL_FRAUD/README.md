# 04 — Intent, event, and outcome

## Why this chapter matters

This chapter answers: **What behavior is unauthorized or deceptive, and what evidence can establish that classification?** It sits inside a larger fraud-detection system, so read the concepts as connected parts of one payment story rather than as isolated vocabulary. The aim is to understand what is happening in the real world before deciding what a dataset or model can support.

## Concepts in this chapter

- [Fraud vs Chargeback](Fraud_vs_Chargeback.md) — A chargeback is a formal reversal of a transaction, initiated by a cardholder or issuer. It's a *signal* often used as a proxy for fraud, but not every chargeback is fraud (some are legitimate disputes or 'friendly…
- [Fraud vs Default](Fraud_vs_Default.md) — Default is a legitimate borrower failing to repay a debt they genuinely intended (at least initially) to repay; fraud involves deception from the start.
- [Fraud vs Theft](Fraud_vs_Theft.md) — Theft is the physical or direct taking of an asset (e.g. stealing a wallet); fraud is deception used to obtain something, often without direct physical taking.
- [Fraudulent vs Legitimate Transaction](Fraudulent_vs_Legitimate_Transaction.md) — A legitimate transaction is authorized by the true account owner; a fraudulent one is not — regardless of how 'normal' it might look on the surface.
- [What is Financial Fraud](What_is_Financial_Fraud.md) — Financial fraud is the intentional use of deception to gain an unauthorized financial benefit — using someone else's funds, identity, or credentials without legitimate authorization.
- [Who is a Fraudster](Who_is_a_Fraudster.md) — The individual or organized group intentionally executing deceptive financial actions — ranging from an opportunistic individual to sophisticated fraud rings using automation.
- [Why Fraud is Hard to Detect](Why_Fraud_is_Hard_to_Detect.md) — Fraud is rare, adversarial, constantly evolving, and often only confirmed long after the transaction — making it one of the hardest real-world ML problems.

## The analytical lens

Separate underlying intent from the evidence available in a dataset. Ask who adjudicates the label, when it matures, and which legitimate outcomes can look similar. Keep three layers separate throughout the chapter:

- **Reality:** what the customer, merchant, attacker, bank, or payment system actually did.
- **Evidence:** what was recorded, by whom, and at what time.
- **Decision:** what action is justified by that evidence, given uncertainty and cost.

Moving from one layer to the next requires assumptions. Write them down rather than treating them as facts. Ask what legitimate explanation could produce the same observation and what evidence could distinguish the possibilities.

## Work through one example

A cardholder disputes a purchase weeks after it was approved. The dispute is an observable outcome; it might indicate stolen-card fraud, a merchant mistake, a family member’s purchase, or friendly fraud. The label needs a clear adjudication rule.

For each article, try this short exercise: explain the concept in plain language; identify the relevant entity and event; name the observable evidence; note when that evidence becomes available; and connect it to a decision or downstream analysis. Then explain one limitation.

## Common misunderstanding

Equating theft, default, dispute, loss, and fraud. These overlap in some cases but answer different questions. In practice, a single field, event, or model score is rarely enough to establish intent. The goal is not to eliminate uncertainty by confident language. It is to make the uncertainty visible and collect the evidence needed for a responsible decision.

## Checkpoint before moving on

Take a disputed transaction and list at least two explanations. What extra evidence would distinguish them, and when would it become available?

You are ready to continue when you can answer the chapter question with a concrete example and explain what is known, what is inferred, and what is still unknown.

## Navigation

Previous: [03 PAYMENT LIFECYCLE](../03_PAYMENT_LIFECYCLE/README.md) · Next: [05 TYPES OF FRAUD](../05_TYPES_OF_FRAUD/README.md)
