# 01 — Foundation: money and records

## Why this chapter matters

This chapter answers: **What is actually happening when value moves, and which person, account, institution, or merchant is involved?** It sits inside a larger fraud-detection system, so read the concepts as connected parts of one payment story rather than as isolated vocabulary. The aim is to understand what is happening in the real world before deciding what a dataset or model can support.

## Concepts in this chapter

- [What is a Bank](What_is_a_Bank.md) — A bank is a licensed financial institution that holds customer money, facilitates payments, and extends credit. Banks play different roles in a transaction depending on whether they represent the customer (issuing)…
- [What is a Card](What_is_a_Card.md) — A card (debit or credit) is a physical or virtual instrument tied to an account that authorizes payments. It carries identifiers (card number, expiry, CVV) used to route and authenticate transactions.
- [What is a Financial Transaction](What_is_a_Financial_Transaction.md) — A financial transaction is an event where value moves from one party to another — a purchase, transfer, withdrawal, or payment. Every transaction has a payer, a payee, an amount, and a timestamp at minimum.
- [What is a Merchant](What_is_a_Merchant.md) — A merchant is any business that accepts payments from customers in exchange for goods or services. Merchants connect to the payment ecosystem via a payment gateway and acquiring bank.
- [What is an Account](What_is_an_Account.md) — An account is a record that holds a customer's balance and transaction history with a financial institution. It's the anchor point for identity, ownership, and history in fraud detection.
- [What is Fintech](What_is_Fintech.md) — Fintech (financial technology) refers to companies that use technology to deliver financial services — payments, lending, banking — often faster or more accessibly than traditional banks, frequently by partnering…
- [What is Money](What_is_Money.md) — Money is a socially and legally accepted medium of exchange — a way to trade value without bartering goods directly. In fraud systems, money almost never moves as physical cash; it moves as numbers changing in…

## The analytical lens

Translate the story into entities and relationships before choosing columns. Ask who owns each record, what balance or obligation changes, and who can correct an error. Keep three layers separate throughout the chapter:

- **Reality:** what the customer, merchant, attacker, bank, or payment system actually did.
- **Evidence:** what was recorded, by whom, and at what time.
- **Decision:** what action is justified by that evidence, given uncertainty and cost.

Moving from one layer to the next requires assumptions. Write them down rather than treating them as facts. Ask what legitimate explanation could produce the same observation and what evidence could distinguish the possibilities.

## Work through one example

A customer pays a merchant with a card. Separate the customer, the account that funds the purchase, the card that identifies the payment route, and the merchant receiving it. One person can have several accounts and instruments; a mismatch is a question to investigate, not proof of fraud.

For each article, try this short exercise: explain the concept in plain language; identify the relevant entity and event; name the observable evidence; note when that evidence becomes available; and connect it to a decision or downstream analysis. Then explain one limitation.

## Common misunderstanding

Treating a card number, account, customer, and transaction as if they were the same thing. In practice, a single field, event, or model score is rarely enough to establish intent. The goal is not to eliminate uncertainty by confident language. It is to make the uncertainty visible and collect the evidence needed for a responsible decision.

## Checkpoint before moving on

Draw one payment and label the payer, funding account, instrument, merchant, and institutions. State which records each party would hold.

You are ready to continue when you can answer the chapter question with a concrete example and explain what is known, what is inferred, and what is still unknown.

## Navigation

Next: [02 PAYMENT ECOSYSTEM](../02_PAYMENT_ECOSYSTEM/README.md)
