# List all bounties (extensive)

Created: October 19, 2022 5:26 PM
Description: Lists all bounties and all bounty entries with usernames, contributors. titles and descriptions
Tags: Bounties

```jsx
query {bounties (limit: 2000){id,creator{handle},title,description,oracle{handle},contributions{contributor{handle},amount},cherry,entrantStake,fundingType{__typename},workPeriod,judgingPeriod,totalFunding,discussionThreadId,isTerminated,entries{id,worker{handle},workSubmitted,works{entryId,title,description}}}}
```