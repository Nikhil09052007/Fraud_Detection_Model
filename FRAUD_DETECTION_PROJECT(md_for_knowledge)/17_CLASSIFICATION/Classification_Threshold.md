# Classification Threshold

The cutoff probability above which a transaction is classified as fraud (e.g. score > 0.7 = block). Adjusting this threshold directly trades off precision and recall.

## Key Points

- Not a fixed model property — a tunable business decision
- Different thresholds may be used for different actions (review vs. hard block)
