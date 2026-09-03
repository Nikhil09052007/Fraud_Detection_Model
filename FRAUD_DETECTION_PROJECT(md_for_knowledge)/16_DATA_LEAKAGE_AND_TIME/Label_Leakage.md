# Label Leakage

A specific, severe form of leakage where the feature itself is derived from or highly correlated with the label-generating process — e.g. using 'was this transaction disputed' as a feature to predict fraud.

## Key Points

- Produces near-perfect but completely meaningless offline metrics
- Often subtle — audit any feature that's suspiciously perfectly correlated with the label
