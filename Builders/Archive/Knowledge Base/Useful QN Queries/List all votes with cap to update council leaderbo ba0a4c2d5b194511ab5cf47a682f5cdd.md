# List all votes with cap to update council leaderboard spreadsheet

Created: January 3, 2023 6:58 AM

```jsx
query MyQuery {
  castVotes(limit: 1000) {
    id
    castBy
    deletedAt
    electionRoundId
    stakeLocked
    voteFor {
      memberId
    }
    voteForId
    stake
    votecasteventcastVote {
      inBlock
    }
  }
}
```

To sort: `castVotes (limit:500, orderBy:createdAt_ASC)`

For further sorting, filtering paste the result in [here](https://www.convertcsv.com/json-to-csv.htm), import the CSV to a spreadsheet and sort there.