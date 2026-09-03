# Score Calibration

Ensuring that a model's output probability actually matches real-world frequency — e.g. among all transactions scored at 0.7, roughly 70% should truly be fraud.

## Key Points

- Many models (e.g. gradient boosted trees) are not calibrated by default and need techniques like Platt scaling or isotonic regression
- Critical when the score itself (not just its ranking) is used in business logic or reporting
