# Temporal Data Splitting

Splitting training and test data by time (e.g. train on Jan-Oct, test on Nov-Dec) rather than randomly, to accurately simulate how the model will actually be used in production.

## Key Points

- The correct default splitting strategy for essentially all fraud detection problems
- Prevents both train/test leakage and gives a realistic estimate of future performance
