# Future Information

Any data generated after the prediction point — e.g. whether a chargeback eventually occurred, or the customer's transactions the following week — that must never be used as a feature.

## Key Points

- The most classic leakage error: accidentally computing an aggregate feature using data from after the transaction being predicted
- Especially easy to introduce with careless groupby/rolling operations
