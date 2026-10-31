# 06 — Attack chains and evidence

## Why this chapter matters

This chapter answers: **How does an attacker move from opportunity to attempted payment, and where could controls interrupt the chain?** It sits inside a larger fraud-detection system, so read the concepts as connected parts of one payment story rather than as isolated vocabulary. The aim is to understand what is happening in the real world before deciding what a dataset or model can support.

## Concepts in this chapter

- [Account Takeover Process](Account_Takeover_Process.md) — The typical chain: credentials obtained → login attempted → account details changed (email/phone/password) → funds moved or purchases made → account often abandoned.
- [Card Testing](Card_Testing.md) — Fraudsters running many small, automated transactions against a merchant to check which stolen card numbers are still valid, before using the valid ones for larger fraud.
- [Credential Stuffing](Credential_Stuffing.md) — An automated attack that tries large numbers of stolen username/password pairs (from other breaches) against a login system, exploiting password reuse.
- [Data Breaches](Data_Breaches.md) — Incidents where an organization's data — often including customer credentials or card numbers — is exposed to unauthorized parties.
- [Fraud Attack Lifecycle](Fraud_Attack_Lifecycle.md) — End to end: Data breach/phishing → stolen credentials → credential stuffing/testing → account takeover or valid card confirmation → fraudulent transaction(s) → cash-out.
- [Phishing and Social Engineering](Phishing_and_Social_Engineering.md) — Techniques that trick victims into voluntarily giving up credentials or authorizing fraudulent transactions, exploiting trust rather than technical vulnerabilities.
- [Stolen Credentials](Stolen_Credentials.md) — Usernames, passwords, card numbers, or other authentication data obtained illegitimately — the raw material for most fraud.

## The analytical lens

Model the attack as a sequence. For every stage, distinguish what happened in the real world from what a system logs, and note the time lag between them. Keep three layers separate throughout the chapter:

- **Reality:** what the customer, merchant, attacker, bank, or payment system actually did.
- **Evidence:** what was recorded, by whom, and at what time.
- **Decision:** what action is justified by that evidence, given uncertainty and cost.

Moving from one layer to the next requires assumptions. Write them down rather than treating them as facts. Ask what legitimate explanation could produce the same observation and what evidence could distinguish the possibilities.

## Work through one example

An attacker obtains credentials through phishing, tests whether they work, then makes rapid purchases or cashes out. A transaction table may show the testing and spending pattern but not the phishing message or who controlled the device.

For each article, try this short exercise: explain the concept in plain language; identify the relevant entity and event; name the observable evidence; note when that evidence becomes available; and connect it to a decision or downstream analysis. Then explain one limitation.

## Common misunderstanding

Expecting one transaction or one model feature to reveal the whole attack. In practice, a single field, event, or model score is rarely enough to establish intent. The goal is not to eliminate uncertainty by confident language. It is to make the uncertainty visible and collect the evidence needed for a responsible decision.

## Checkpoint before moving on

Draw the attack chain. Mark one prevention point, one detection point, the evidence available at each point, and a possible false alarm.

You are ready to continue when you can answer the chapter question with a concrete example and explain what is known, what is inferred, and what is still unknown.

## Navigation

Previous: [05 TYPES OF FRAUD](../05_TYPES_OF_FRAUD/README.md) · Next: [07 TRANSACTION ANATOMY](../07_TRANSACTION_ANATOMY/README.md)
