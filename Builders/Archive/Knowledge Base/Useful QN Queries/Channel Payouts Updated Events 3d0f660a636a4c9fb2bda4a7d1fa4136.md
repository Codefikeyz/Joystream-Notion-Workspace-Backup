# Channel Payouts Updated Events

Created: June 14, 2023 2:35 PM

```graphql
query {
  channelPayoutsUpdatedEvents(where: {payloadHash_eq: $payloadHash}) {
    id
    payloadSize
    payloadHash
    payloadDataObject {
      id
      isAccepted
     
    }
  }
}
```