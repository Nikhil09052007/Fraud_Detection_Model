# API

The interface through which upstream systems (payment gateway, processor) send transaction data and receive a fraud decision, typically a low-latency synchronous request-response API.

## Key Points

- Defines the contract for what data comes in and what decision/score comes out
- Latency and reliability of this API directly gate the entire payment authorization flow
