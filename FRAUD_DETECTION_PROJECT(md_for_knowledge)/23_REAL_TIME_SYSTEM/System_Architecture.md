# System Architecture

The overall design of how components — ingestion, features, model, decision service — connect and communicate to deliver a fraud decision within the authorization window.

## Key Points

- Typically a pipeline: event stream/API → feature store → model server → decision service → response
- Architecture choices (streaming vs request-response, feature store design) directly affect achievable latency
