# stateSubscription

Created: May 9, 2022 8:27 PM
Description: Put this in QN and it’ll tell you if its updating. Doesn’t work on non-JSG QNs right now.
Tags: QN status, Subscription

```graphql
subscription
	{stateSubscription
    	{lastCompleteBlock,lastProcessedEvent,indexerHead,chainHead}
  }
```