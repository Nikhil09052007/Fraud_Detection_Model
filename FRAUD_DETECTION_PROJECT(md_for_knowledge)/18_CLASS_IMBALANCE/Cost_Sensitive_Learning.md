# Cost-Sensitive Learning

Training approaches that directly incorporate the differing real-world costs of false positives (false declines) vs false negatives (missed fraud) into the model's optimization objective.

## Key Points

- More directly aligned with the actual business tradeoffs from Section 12 than accuracy-based training
- Can be implemented via custom loss functions or class weights calibrated to real cost ratios
