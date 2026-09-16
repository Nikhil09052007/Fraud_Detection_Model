## # Intelligent Fraud Detection & Risk Scoring Platform

This is my end-to-end Data Science project for understanding and
building a fraud detection system for a fintech transaction environment.

The project is intentionally designed to begin from the roots of the
problem rather than starting directly with a dataset or machine learning
algorithm.

The objective is to understand:

- how money moves through a financial system,
- how digital payments work,
- how fraudulent activity occurs,
- how fraudulent behavior appears in transaction data,
- how financial institutions detect suspicious activity,
- where Machine Learning can contribute,
- what exactly the model is predicting,
- how model predictions become risk scores,
- how risk scores become business decisions,
- and how the resulting system is monitored and improved.


# The project structure for the conceptual understanding along with Implementation:
                    PROJECT
                       │
          ┌────────────┴────────────┐
          │                         │
          ▼                         ▼
   KNOWLEDGE LAYER          IMPLEMENTATION LAYER
          │                         │
     01 → 26                  data/
          │                   notebooks/
          │                   src/
          │                   app/
          │                   tests/
          │
          └──────────────┐
                         ▼
                 UNDERSTAND FIRST
                         ↓
                 IMPLEMENT SECOND



# Why This Project Exists

Fraud detection is not fundamentally a machine learning problem.

It is a financial and behavioral problem that can be formulated as a
machine learning problem.

A financial institution first has a real-world problem:

> How can we identify potentially fraudulent transactions while
> minimizing unnecessary disruption to legitimate customers?

Only after understanding that problem can we ask:

> What information is available?
>
> What patterns indicate risk?
>
> What should the model predict?
>
> How should the prediction be evaluated?
>
> How should the business act on the prediction?

Therefore, this project follows:

REAL-WORLD PROBLEM
        ↓
DOMAIN UNDERSTANDING
        ↓
BEHAVIORAL UNDERSTANDING
        ↓
DATA
        ↓
DATA SCIENCE
        ↓
MACHINE LEARNING
        ↓
DECISION SYSTEM
        ↓
BUSINESS IMPACT



# How to Use This Repository

The folders are intended to be studied sequentially.

Do not begin with Machine Learning.

Follow the progression:

01 → Understand the financial world
02 → Understand the payment ecosystem
03 → Understand the payment lifecycle
04 → Understand fraud
05 → Understand different fraud types
06 → Understand how fraudulent behavior occurs
07 → Understand transaction structure
08 → Understand how real-world behavior becomes data
09 → Understand normal vs abnormal behavior
10 → Understand existing fraud detection approaches
11 → Understand real-time detection
12 → Define the business problem
13 → Formulate the Data Science problem
14 → Understand the dataset
15 → Engineer meaningful features
16 → Prevent temporal/data leakage
17 → Understand classification
18 → Handle class imbalance
19 → Evaluate the model
20 → Convert predictions into risk
21 → Make business decisions
22 → Explain model decisions
23 → Build the real-time system
24 → Monitor the system
25 → Evaluate business impact
26 → Connect everything into one mental model



* Below, is the whole worklflow structure or the project which is used implement the project form its entire stage.

                    REAL WORLD
                        │
                        ▼
              How does money move?
                        │
                        ▼
              How does a payment work?
                        │
                        ▼
                 What is fraud?
                        │
                        ▼
             How does fraud happen?
                        │
                        ▼
        What does fraudulent behavior look like?
                        │
                        ▼
             What does the system observe?
                        │
                        ▼
             How is fraud detected today?
                        │
                        ▼
          Where can Machine Learning help?
                        │
                        ▼
            What does our data represent?
                        │
                        ▼
             What exactly are we predicting?
                        │
                        ▼
                How do we evaluate it?
                        │
                        ▼
              How do we make decisions?
                        │
                        ▼
               BUSINESS OUTCOME


* Fraud Detection & Risk Scoring Platform — Project Workflow


                    REAL-WORLD FINANCIAL SYSTEM
                              │
                              ▼
                    ┌───────────────────┐
                    │   A transaction   │
                    │      occurs       │
                    └─────────┬─────────┘
                              │
                              ▼
                 ┌────────────────────────┐
                 │ What information exists │
                 │ about this transaction? │
                 └────────────┬───────────┘
                              │
                              ▼
                    TRANSACTION DATA
          ┌──────────────┬──────────────┬──────────────┐
          │              │              │              │
       Customer       Transaction     Merchant       Device
          │              │              │              │
       Account          Time          Location         IP
          │              │              │              │
          └──────────────┴──────────────┴──────────────┘
                              │
                              ▼
                   UNDERSTAND THE DATA
                              │
                              ▼
                   ┌──────────────────┐
                   │ What does normal │
                   │ behavior look    │
                   │ like?            │
                   └────────┬─────────┘
                            │
                            ▼
                   ┌──────────────────┐
                   │ What does fraud  │
                   │ look like?       │
                   └────────┬─────────┘
                            │
                            ▼
                     DATA EXPLORATION
                            │
                            ▼
               ┌──────────────────────────┐
               │ Identify behavioral      │
               │ patterns & anomalies     │
               └────────────┬─────────────┘
                            │
                            ▼
                    FEATURE ENGINEERING
                            │
                            ▼
              ┌────────────────────────────┐
              │ Convert raw events into    │
              │ meaningful risk signals    │
              └──────────────┬─────────────┘
                             │
                             ▼
                    MACHINE LEARNING
                             │
                             ▼
              ┌────────────────────────────┐
              │ Predict probability/risk   │
              │ of fraudulent transaction  │
              └──────────────┬─────────────┘
                             │
                             ▼
                       MODEL OUTPUT
                             │
                       Risk Score
                             │
                             ▼
                    DECISION ENGINE
              ┌──────────────┼──────────────┐
              ▼              ▼              ▼
           APPROVE          REVIEW         BLOCK
              │              │              │
              └──────────────┼──────────────┘
                             ▼
                     BUSINESS OUTCOME
                             │
              ┌──────────────┼──────────────┐
              ▼              ▼              ▼
          Fraud Loss     Customer UX    Review Cost
                             │
                             ▼
                    MONITOR THE SYSTEM
                             │
                             ▼
                  FEEDBACK / NEW DATA
                             │
                             └──────────────►
                              CONTINUOUS
                              IMPROVEMENT

* The project therefore follows the journey:
Real-world problem
       ↓
Financial transaction
       ↓
Fraud behavior
       ↓
Observable data
       ↓
Data understanding
       ↓
Feature engineering
       ↓
Fraud prediction
       ↓
Risk score
       ↓
Business decision
       ↓
Business outcome
       ↓
Monitoring & improvement


# A financial company processes a huge number of transactions.

Most transactions are legitimate.

A small proportion may be fraudulent.

The company therefore needs to answer:

"Should we allow this transaction, investigate it, or stop it?"


* Understand the Payment Ecosystem

                  CUSTOMER
                    │
                    │ Payment
                    ▼
                 MERCHANT
                    │
                    ▼
             PAYMENT GATEWAY
                    │
                    ▼
              PROCESSOR
                    │
             ┌──────┴──────┐
             ▼             ▼
       CARD NETWORK    OTHER SYSTEMS
             │
             ▼
        ISSUING BANK



* The Knowledge Architecture

FRAUD_DETECTION_PROJECT/
│
├── README.md
│
├── 01_FINANCIAL_WORLD/
│   ├── ...
│
├── 02_PAYMENT_ECOSYSTEM/
│   ├── ...
│
├── 03_PAYMENT_LIFECYCLE/
│   ├── ...
│
├── 04_FINANCIAL_FRAUD/
│   ├── ...
│
├── 05_TYPES_OF_FRAUD/
│   ├── ...
│
├── 06_HOW_FRAUD_HAPPENS/
│   ├── ...
│
├── 07_TRANSACTION_ANATOMY/
│   ├── ...
│
├── 08_FRAUD_AS_DATA/
│   ├── ...
│
├── 09_NORMAL_VS_ABNORMAL_BEHAVIOR/
│   ├── ...
│
├── 10_FRAUD_DETECTION/
│   ├── ...
│
├── 11_REAL_TIME_FRAUD_DETECTION/
│   ├── ...
│
├── 12_BUSINESS_PROBLEM/
│   ├── ...
│
├── 13_DATA_SCIENCE_FORMULATION/
│   ├── ...
│
├── 14_DATA_UNDERSTANDING/
│   ├── ...
│
├── 15_FEATURE_ENGINEERING/
│   ├── ...
│
├── 16_DATA_LEAKAGE_AND_TIME/
│   ├── ...
│
├── 17_CLASSIFICATION/
│   ├── ...
│
├── 18_CLASS_IMBALANCE/
│   ├── ...
│
├── 19_MODEL_EVALUATION/
│   ├── ...
│
├── 20_RISK_SCORING/
│   ├── ...
│
├── 21_DECISION_ENGINE/
│   ├── ...
│
├── 22_EXPLAINABILITY/
│   ├── ...
│
├── 23_REAL_TIME_SYSTEM/
│   ├── ...
│
├── 24_MONITORING/
│   ├── ...
│
├── 25_BUSINESS_EVALUATION/
│   ├── ...
│
└── 26_COMPLETE_MENTAL_MODEL/
    └── ...





---


# Data Validation in Fraud Detection — Theoretical & Intuitive View

| Validation Step | What We Are Really Asking | Why It Matters in a Real Fraud System | Intuitive / Business Meaning | What Can Go Wrong If We Skip It |
|-----------------|---------------------------|---------------------------------------|------------------------------|---------------------------------|
| **1. Target Distribution (Fraud Rate)** | How rare is fraud in this population? | Fraud is almost always a minority class. The rarity directly determines which metrics are meaningful, how we should set thresholds, and whether class imbalance techniques are required. | A model that always says “not fraud” can look extremely accurate while being completely useless. We need to know the base rate so we can judge real detection power versus customer friction. | We optimise for accuracy, celebrate high numbers, and deploy a model that blocks almost no fraud (or blocks far too many legitimate customers). |
| **2. Missingness Landscape** | Is missingness random, or does it carry behavioural / channel meaning? | In payment systems, many fields are systematically missing for certain product types, regions, devices, or attack patterns. Missingness itself is often a signal. | A transaction with no device fingerprint may be harder for an attacker to hide — or easier. Knowing the pattern tells us whether “missing” should later become a feature. | We blindly impute or drop columns, destroy a useful signal, or create features that only exist for a biased subset of traffic. |
| **3. Constant / Near-Constant Columns** | Does this column ever change? | A feature that never varies cannot help separate fraud from legitimate behaviour. It also often indicates a deprecated field, logging error, or extremely narrow segment. | Keeping constant columns wastes memory, confuses feature importance, and can make pipelines slower for zero gain. | We carry noise into modelling, inflate dimensionality, and later wonder why certain features have zero importance. |
| **4. Cardinality of Categorical Variables** | How many distinct values does this field take? | High-cardinality fields (card IDs, email domains, DeviceInfo, etc.) can be extremely powerful identity signals, but they also create severe risks of overfitting, memory explosion, and entity leakage. | The same card or device appearing repeatedly is often a strong behavioural clue. But treating every unique value as a separate category can make the model memorise training entities instead of learning general patterns. | We one-hot encode recklessly, create millions of sparse columns, leak future identity information, or discard a strong signal because it looked “too messy.” |
| **5. Relationship Between Transaction & Identity Tables** | What fraction of transactions actually have richer identity / device context? | In real payment flows, identity data is frequently missing. A production system must score both fully observed and sparsely observed transactions. | Only ~24% of transactions in this dataset have identity information. That is not a defect — it is a structural property of the ecosystem. The model must remain useful for the other 76%. | We build features that only work when identity data is present, creating a model that is effectively blind for the majority of live traffic. |
| **6. Suspicious / Impossible Values** | Are there values that violate basic domain constraints? | Some anomalies are pure data-quality bugs. Others are genuine rare fraud patterns that look “impossible” under normal assumptions. | Negative amounts, future timestamps, or extreme outliers can either be pipeline errors or early warning signs of sophisticated attacks. | We either train on corrupted data or accidentally remove rare but highly informative fraud cases. |

---

**Core Principle**

Data validation in fraud detection is not a cleaning ritual.  
It is the first rigorous attempt to understand how the observable transaction world relates to the hidden fraud world — how rare the event is, how incomplete our visibility is, which signals are stable, and which ones are fragile.

Only after this understanding is in place do we earn the right to engineer features or train models.



---
