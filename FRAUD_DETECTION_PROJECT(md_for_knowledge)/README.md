# Fraud Detection: A First-Principles Learning Path

This knowledge base explains fraud detection from the real-world payment system through data science, model decisions, and business outcomes. It is written for a reader who may be new to finance or machine learning. The goal is not to memorize definitions: it is to learn how to ask good questions, recognize uncertainty, and turn evidence into a defensible decision.

## Start here

Read the chapter guides in order. Each guide links to every concept page in its section, gives the chapter's main question, walks through an example, and ends with a checkpoint. Concept pages add a practical example, a data-science lens, common traps, and a short exercise.

## The 26 chapters

1. [The Financial World](01_FINANCIAL_WORLD/README.md) — What are money, accounts, banks, cards, merchants, and transactions?
2. [The Payment Ecosystem](02_PAYMENT_ECOSYSTEM/README.md) — Which organizations and people participate in a payment?
3. [The Payment Lifecycle](03_PAYMENT_LIFECYCLE/README.md) — How does a payment move from initiation to a final outcome?
4. [Financial Fraud](04_FINANCIAL_FRAUD/README.md) — What makes an event fraud, and how is it different from a dispute or loss?
5. [Types of Fraud](05_TYPES_OF_FRAUD/README.md) — What is targeted, how is it attacked, and where does it happen?
6. [How Fraud Happens](06_HOW_FRAUD_HAPPENS/README.md) — How do attackers move from opportunity to attempted payment?
7. [Transaction Anatomy](07_TRANSACTION_ANATOMY/README.md) — What does a transaction record contain and what does each field mean?
8. [Fraud as Data](08_FRAUD_AS_DATA/README.md) — How do real events become records, features, and labels?
9. [Normal vs Abnormal Behavior](09_NORMAL_VS_ABNORMAL_BEHAVIOR/README.md) — Compared with what context is an event unusual?
10. [Fraud Detection](10_FRAUD_DETECTION/README.md) — How do rules, models, and human review work together?
11. [Real-Time Fraud Detection](11_REAL_TIME_FRAUD_DETECTION/README.md) — What can be known and acted on before a payment response is due?
12. [The Business Problem](12_BUSINESS_PROBLEM/README.md) — Which losses and customer harms should a system balance?
13. [Data Science Formulation](13_DATA_SCIENCE_FORMULATION/README.md) — What exact event, target, time, and action should be modeled?
14. [Data Understanding](14_DATA_UNDERSTANDING/README.md) — What does the dataset contain, and where might it mislead us?
15. [Feature Engineering](15_FEATURE_ENGINEERING/README.md) — How can raw observations become useful, point-in-time signals?
16. [Data Leakage and Time](16_DATA_LEAKAGE_AND_TIME/README.md) — Was every feature available at the prediction moment?
17. [Classification](17_CLASSIFICATION/README.md) — What does a classifier predict, and how is a score produced?
18. [Class Imbalance](18_CLASS_IMBALANCE/README.md) — How do rare fraud cases change training and evaluation?
19. [Model Evaluation](19_MODEL_EVALUATION/README.md) — Does the model perform well at realistic costs and constraints?
20. [Risk Scoring](20_RISK_SCORING/README.md) — How should scores be calibrated and interpreted?
21. [The Decision Engine](21_DECISION_ENGINE/README.md) — How does a score become approve, review, or decline?
22. [Explainability](22_EXPLAINABILITY/README.md) — What can an explanation tell us, and what can it not prove?
23. [The Real-Time System](23_REAL_TIME_SYSTEM/README.md) — What services and contracts make decisions reliable?
24. [Monitoring](24_MONITORING/README.md) — How do we notice changing data, behavior, and outcomes?
25. [Business Evaluation](25_BUSINESS_EVALUATION/README.md) — Did the system improve realized outcomes enough to justify its costs?
26. [The Complete Mental Model](26_COMPLETE_MENTAL_MODEL/README.md) — How does the full system connect and improve over time?

## A way to reason through every concept

When you meet a new term or model result, ask these questions:

1. **What is the real-world unit?** A person, account, device, merchant, transaction, or sequence of events?
2. **What happened, and when?** Separate the event time from the time the system learned about it.
3. **What is directly observed?** A data field is a measurement or proxy, not automatically the underlying truth.
4. **What is inferred?** State the assumptions that connect the observation to behavior or risk.
5. **What else could explain it?** Consider legitimate activity, missing data, broken collection, and changes in customer behavior.
6. **What decision could change?** Identify who acts, what the action is, and the cost of being wrong in either direction.
7. **How will we know it worked?** Choose an evaluation that reflects rarity, time, review capacity, customer impact, and matured labels.

A compact mental model is:

```text
Real payment behavior
        ↓
Events recorded by different systems
        ↓
Features available at a defined prediction time
        ↓
A model estimates or ranks risk
        ↓
A policy chooses an action
        ↓
Customers and the business experience outcomes
        ↓
Mature labels and monitoring inform the next version
```

At each arrow, information can be delayed, missing, ambiguous, or biased. Strong data science makes those limits explicit instead of hiding them behind a model score.

## Use a running example

Imagine a card payment that looks unusual. Trace it through the chapters:

- Who initiated it, which account funded it, and which organizations handled it?
- At what lifecycle stage is the decision being made?
- What behavior might be suspicious, and what legitimate explanation is possible?
- Which fields exist at that moment, and how trustworthy are they?
- What target and follow-up horizon define a fraud outcome?
- How would the model be evaluated at the real fraud rate?
- Should the payment be approved, reviewed, challenged, or declined?
- What explanation can an analyst use, and what evidence is still missing?
- How will delayed outcomes and customer impact be monitored?

If you can answer these questions clearly, you are doing the central work of applied data science: framing a decision, examining evidence, measuring uncertainty, and connecting analysis to consequences.

## How this connects to the implementation notebooks

The conceptual path is paired with the repository's [notebook learning path](../notebooks/README.md). The knowledge chapters establish the questions and assumptions; the notebooks show how those ideas appear in a benchmark dataset and model workflow. The IEEE-CIS dataset is a teaching benchmark, so its patterns and results should not be treated as a production bank's operating evidence.
