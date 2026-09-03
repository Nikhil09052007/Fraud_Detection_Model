# How Payment Entities Interact

A full payment flow: Customer → Merchant → Gateway → Processor → Card Network → Issuing Bank (approves/declines) → back down the chain to the merchant, in usually under a second.

## Key Points

- Each hop can add its own fraud check
- Latency at each hop matters — real-time fraud detection must fit within this window
- Data available to your model depends on which entity you are in this chain

## Example

A customer taps their card → gateway captures details → processor routes to Visa → Visa routes to the issuing bank → issuing bank scores the transaction and returns approve/decline → response flows back to the terminal, all within ~1-2 seconds.
