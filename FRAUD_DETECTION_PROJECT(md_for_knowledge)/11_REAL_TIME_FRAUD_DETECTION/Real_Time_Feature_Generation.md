# Real-Time Feature Generation

Computing the features a model needs (velocity, deviation from average, device recognition) on the fly, at the moment of the transaction, using low-latency data stores.

## Key Points

- Often relies on pre-aggregated, continuously updated feature stores rather than computing from raw history each time
- Latency here directly eats into the overall decision budget
