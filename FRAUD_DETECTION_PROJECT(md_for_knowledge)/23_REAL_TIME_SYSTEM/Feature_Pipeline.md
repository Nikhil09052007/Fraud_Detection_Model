# Feature Pipeline

The system that computes and serves the features a model needs, both offline (for training) and online (for real-time scoring), ideally from the same underlying logic to avoid train/serve skew.

## Key Points

- Train/serve skew — where offline and online feature computation subtly differ — is a major source of production bugs
- Often implemented via a dedicated 'feature store' serving both training and real-time paths
