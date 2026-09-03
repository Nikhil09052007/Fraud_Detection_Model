# Data Drift

When the statistical properties of input features change over time relative to what the model was trained on — e.g. a new payment method becoming popular shifts the payment-method feature distribution.

## Key Points

- Doesn't necessarily mean fraud patterns changed — could just be legitimate business/user growth
- Detected by comparing live feature distributions against training-time distributions
