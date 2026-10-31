# 02 — Actors and responsibility

## Why this chapter matters

This chapter answers: **Which parties send instructions, move funds, authorize the payment, and keep the records?** It sits inside a larger fraud-detection system, so read the concepts as connected parts of one payment story rather than as isolated vocabulary. The aim is to understand what is happening in the real world before deciding what a dataset or model can support.

## Concepts in this chapter

- [Acquiring Bank](Acquiring_Bank.md) — The merchant's bank, which receives payment on the merchant's behalf and requests authorization from the card network/issuing bank.
- [Card Network](Card_Network.md) — The rail that connects issuing and acquiring banks — e.g. Visa, Mastercard — routing authorization requests and enforcing network rules.
- [Customer](Customer.md) — The person initiating a payment, using a card, wallet, or bank transfer to pay a merchant. The customer's account, device, and behavioral history are the richest source of fraud signal.
- [How Payment Entities Interact](How_Payment_Entities_Interact.md) — A full payment flow: Customer → Merchant → Gateway → Processor → Card Network → Issuing Bank (approves/declines) → back down the chain to the merchant, in usually under a second.
- [Issuing Bank](Issuing_Bank.md) — The customer's bank, which issued the card or account and makes the final call on whether to approve or decline a transaction.
- [Merchant](Merchant.md) — The business receiving payment for goods or services. Merchants connect to the payment ecosystem through a gateway and acquiring bank relationship.
- [Payment Gateway](Payment_Gateway.md) — Software that captures payment details at checkout and securely transmits them to the payment processor. It's the technical front door of a transaction.
- [Payment Processor](Payment_Processor.md) — The company that handles the technical routing of a transaction between the gateway, card network, and banks, executing the mechanics of authorization and settlement.

## The analytical lens

Distinguish the message path from the money path. For each actor, ask what it can observe, when it observes it, and which action it can take. Keep three layers separate throughout the chapter:

- **Reality:** what the customer, merchant, attacker, bank, or payment system actually did.
- **Evidence:** what was recorded, by whom, and at what time.
- **Decision:** what action is justified by that evidence, given uncertainty and cost.

Moving from one layer to the next requires assumptions. Write them down rather than treating them as facts. Ask what legitimate explanation could produce the same observation and what evidence could distinguish the possibilities.

## Work through one example

A shopper submits a checkout request. The gateway packages the request, a processor routes it, the card network carries it to the issuer, and the issuer approves or declines against its records. The merchant, acquirer, and issuer may see different fields and have different responsibilities.

For each article, try this short exercise: explain the concept in plain language; identify the relevant entity and event; name the observable evidence; note when that evidence becomes available; and connect it to a decision or downstream analysis. Then explain one limitation.

## Common misunderstanding

Assuming every party sees the same data or can reverse every outcome. In practice, a single field, event, or model score is rarely enough to establish intent. The goal is not to eliminate uncertainty by confident language. It is to make the uncertainty visible and collect the evidence needed for a responsible decision.

## Checkpoint before moving on

Sketch the authorization message path and the later settlement path. Mark where a fraud score could be added and who could act on it.

You are ready to continue when you can answer the chapter question with a concrete example and explain what is known, what is inferred, and what is still unknown.

## Navigation

Previous: [01 FINANCIAL WORLD](../01_FINANCIAL_WORLD/README.md) · Next: [03 PAYMENT LIFECYCLE](../03_PAYMENT_LIFECYCLE/README.md)
