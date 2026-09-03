# Customer Behavior Features

Features summarizing a customer's historical patterns — average transaction amount, typical merchants, usual times — used to detect deviation.

## Key Points

- Usually the most predictive feature category in fraud models
- Require careful, leakage-free rolling aggregation (only using data before the current transaction)
