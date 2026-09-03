# Authentication vs Authorization

Authentication proves identity ('who are you'); authorization decides permission ('can this transaction go through'). Both can independently fail even when the other succeeds.

## Key Points

- Authentication answers identity; authorization answers eligibility/risk
- A well-authenticated user can still be declined for authorization reasons (insufficient funds, risk score)
- Fraud models mostly operate at the authorization stage
