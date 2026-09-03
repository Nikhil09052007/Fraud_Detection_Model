# Data Ingestion

The layer that receives incoming transaction events (and related data like login/device events) and makes them available to the rest of the system.

## Key Points

- Often built on streaming platforms (e.g. Kafka) for scalability and low latency
- Must handle both the real-time path (scoring) and the batch/historical path (retraining, monitoring)
