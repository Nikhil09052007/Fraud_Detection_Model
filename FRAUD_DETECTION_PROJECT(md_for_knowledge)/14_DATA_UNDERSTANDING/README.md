# 14 — Evidence before modeling

## Why this chapter matters

This chapter answers: **What are the dataset’s rows, columns, coverage, quality issues, distributions, and collection limits?** It sits inside a larger fraud-detection system, so read the concepts as connected parts of one payment story rather than as isolated vocabulary. The aim is to understand what is happening in the real world before deciding what a dataset or model can support.

## Concepts in this chapter

- [Categorical Data](Categorical_Data.md) — Columns representing discrete categories — merchant category, payment method, country — that need special encoding for most ML models.
- [Data Dictionary](Data_Dictionary.md) — A reference document listing every column, its data type, meaning, and valid value range — the map you constantly refer back to.
- [Data Types](Data_Types.md) — The technical type of each column — numeric, categorical, boolean, datetime, text — which determines how it can be processed and modeled.
- [Dataset Overview](Dataset_Overview.md) — A high-level summary of the dataset — number of rows, columns, time range covered, and overall fraud rate.
- [Distributions](Distributions.md) — How values of a given feature are spread — critical for spotting outliers, skew, and differences between fraud and non-fraud populations.
- [Duplicates](Duplicates.md) — Records that appear more than once in the dataset, either from genuine data errors or legitimate repeated transactions that look identical.
- [Exploratory Data Analysis](Exploratory_Data_Analysis.md) — The systematic process of visualizing and summarizing data to uncover patterns, anomalies, and relationships before modeling — the practical application of everything else in this folder.
- [Missing Data](Missing_Data.md) — Fields with no recorded value — common in fraud data (e.g. a new customer with no transaction history yet).
- [Numerical Data](Numerical_Data.md) — Continuous or discrete numeric columns — amount, account age, transaction count — that often need scaling or transformation before modeling.

## The analytical lens

Check schema, key uniqueness, duplicates, missingness, distributions, time coverage, target prevalence, and train/test differences. Validate findings against how the data was collected. Keep three layers separate throughout the chapter:

- **Reality:** what the customer, merchant, attacker, bank, or payment system actually did.
- **Evidence:** what was recorded, by whom, and at what time.
- **Decision:** what action is justified by that evidence, given uncertainty and cost.

Moving from one layer to the next requires assumptions. Write them down rather than treating them as facts. Ask what legitimate explanation could produce the same observation and what evidence could distinguish the possibilities.

## Work through one example

A feature can appear useful because it is missing for a particular device population or because the train and test periods differ. Data profiling reveals such patterns before they become unexplained model behavior.

For each article, try this short exercise: explain the concept in plain language; identify the relevant entity and event; name the observable evidence; note when that evidence becomes available; and connect it to a decision or downstream analysis. Then explain one limitation.

## Common misunderstanding

Treating a successful notebook run as proof that the data is valid or representative. In practice, a single field, event, or model score is rarely enough to establish intent. The goal is not to eliminate uncertainty by confident language. It is to make the uncertainty visible and collect the evidence needed for a responsible decision.

## Checkpoint before moving on

Summarize one field’s distribution, missingness, time trend, and association with the label. Give at least one alternative explanation.

You are ready to continue when you can answer the chapter question with a concrete example and explain what is known, what is inferred, and what is still unknown.

## Navigation

Previous: [13 DATA SCIENCE FORMULATION](../13_DATA_SCIENCE_FORMULATION/README.md) · Next: [15 FEATURE ENGINEERING](../15_FEATURE_ENGINEERING/README.md)
