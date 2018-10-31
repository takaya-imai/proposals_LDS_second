# proposals_LDS_second

these are proposals for the Second Lightning Developer Summit, 8th and 9th Nov. 2018.

* Standard format for LApps to get an invoice from LN wallet

```
"lightning:" format is recommended in BOLT #11 when requesting lightning payment from LApps to LN wallet. I think that opposite way is also needed, that is, a case that LApps want to send lightning payment to LN wallet seamlessly.
```

* Parallel Payment Channel

```
if a channel between Alice and Bob has many small payments which are one directional primarily, the channel is exhausted later. In this case, rebalancing is also a solution but it will be effective if this happens slowly. "Parallel Payment Channel" is secondary channel to keep on making many small payments between Alice and Bob. if primary channel seems to be exhausted, it starts to make secondary channel.
```

* Continuous Payment Chunk (like coupon tickets)

```
LApps like pay-per-click needs to issue many invoices for api provider to receive lightning pay. It is possible to implement on application side but overhead for payment process is very large. "Streaming Payments" is a solution for it. Payment amount is changeable for one invoice (one preimage hash) by delaying to send preimage but receiving lightning pay by "Streaming Payments" is not continuous but just last and it needs user permission to pay for each amount changes. "Continuous Payments Chunk" is a way to receive many lightning payments by just one invoice. This way is to make one invoice include several preimage hashes such as 100 hashes and limit payment amount for one preimage hash in advance in order to make seamless lightning payments with just the first user permission securely.
```
