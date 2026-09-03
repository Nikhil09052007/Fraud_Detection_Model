# Train/Test Leakage

When information from the test set influences the training process — e.g. computing a global average using the full dataset before splitting, or randomly (not temporally) splitting time-ordered fraud data.

## Key Points

- Random splits are almost always wrong for fraud data — use temporal splits instead
- Fitting any transformation (scalers, encoders) must happen on train data only, then applied to test data
