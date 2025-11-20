# Forum Category created events

Created: February 15, 2023 4:39 AM
Tags: Categories, Forum, Forum Categories, Leaderboard, Metaprotocol

```jsx
query MyQuery {
  categoryCreatedEvents(limit: 1000) {
    id
    category {
      id
      title
    }
    inBlock
    createdAt
  }
}
```