# 05 — Fraud typologies

## Why this chapter matters

This chapter answers: **Which asset, identity, account, channel, and stage is being attacked?** It sits inside a larger fraud-detection system, so read the concepts as connected parts of one payment story rather than as isolated vocabulary. The aim is to understand what is happening in the real world before deciding what a dataset or model can support.

## Concepts in this chapter

- [Account Takeover](Account_Takeover.md) — When a fraudster gains unauthorized access to a legitimate customer's account — usually via stolen credentials — and uses it to transact or extract value.
- [Application Fraud](Application_Fraud.md) — Fraud committed at the point of applying for a product — a credit card, loan, or bank account — typically using stolen or synthetic identity.
- [Card Fraud](Card_Fraud.md) — Any fraud involving unauthorized use of a payment card — the broad umbrella covering both card-present and card-not-present fraud.
- [Card Not Present Fraud](Card_Not_Present_Fraud.md) — Fraud where only card details (number, expiry, CVV) are used — typical of online/e-commerce transactions, without the physical card present.
- [Card Present Fraud](Card_Present_Fraud.md) — Fraud where the physical card is used at a point-of-sale terminal — typically via a stolen or cloned (skimmed) card.
- [Friendly Fraud](Friendly_Fraud.md) — When a legitimate cardholder makes a real purchase, then falsely disputes it as unauthorized to get a refund while keeping the goods.
- [Identity Fraud](Identity_Fraud.md) — Using someone else's real personal information (name, SSN, DOB) without consent to open accounts, apply for credit, or transact.
- [Loan Fraud](Loan_Fraud.md) — Obtaining a loan through misrepresentation — false income, false identity, or no intent to repay from the outset.
- [Payment Fraud](Payment_Fraud.md) — The broad category of fraud occurring during the payment process itself — includes card fraud, wire fraud, and unauthorized transfers.
- [Synthetic Identity Fraud](Synthetic_Identity_Fraud.md) — Creating a new, fake identity by combining real (often stolen) and fabricated information — e.g. a real SSN with a fake name and date of birth — to build credit history and eventually 'bust out'.
- [Transaction Fraud](Transaction_Fraud.md) — Fraud occurring on an individual transaction, on an already-existing, legitimately-opened account — the core focus of real-time fraud scoring.

## The analytical lens

Describe an attack with several labels instead of forcing it into one exclusive category. Identify the attack objective and the observable evidence each label would imply. Keep three layers separate throughout the chapter:

- **Reality:** what the customer, merchant, attacker, bank, or payment system actually did.
- **Evidence:** what was recorded, by whom, and at what time.
- **Decision:** what action is justified by that evidence, given uncertainty and cost.

Moving from one layer to the next requires assumptions. Write them down rather than treating them as facts. Ask what legitimate explanation could produce the same observation and what evidence could distinguish the possibilities.

## Work through one example

A stolen card used online is card-not-present payment fraud and may also be part of an account-takeover campaign. Typologies can overlap because they describe different dimensions: the target, method, channel, or lifecycle stage.

For each article, try this short exercise: explain the concept in plain language; identify the relevant entity and event; name the observable evidence; note when that evidence becomes available; and connect it to a decision or downstream analysis. Then explain one limitation.

## Common misunderstanding

Treating fraud types as mutually exclusive classes or assuming one feature identifies an entire attack. In practice, a single field, event, or model score is rarely enough to establish intent. The goal is not to eliminate uncertainty by confident language. It is to make the uncertainty visible and collect the evidence needed for a responsible decision.

## Checkpoint before moving on

Describe one scenario by target, method, channel, and stage. Which parts can transaction data reveal, and which require investigation?

You are ready to continue when you can answer the chapter question with a concrete example and explain what is known, what is inferred, and what is still unknown.

## Navigation

Previous: [04 FINANCIAL FRAUD](../04_FINANCIAL_FRAUD/README.md) · Next: [06 HOW FRAUD HAPPENS](../06_HOW_FRAUD_HAPPENS/README.md)
