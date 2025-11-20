# Channel Payment Made Events

Created: July 10, 2023 1:45 PM
Description: Channel payments made - not claims
Tags: Channels, Payments, Rewards

```jsx
query MyQuery {
  channelPaymentMadeEvents {
    id
    amount
    inBlock
    payeeChannelId
    payeeChannel {
      title
    }
    rationale
  }
}
```