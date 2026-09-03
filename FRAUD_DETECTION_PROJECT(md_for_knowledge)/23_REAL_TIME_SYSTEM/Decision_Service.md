# Decision Service

The component implementing Section 21's Decision Engine logic in the live system — combining model scores and business rules into a final action, exposed via the API.

## Key Points

- Typically the final internal step before a response is returned upstream
- Should log every decision and its inputs for later monitoring and auditing
