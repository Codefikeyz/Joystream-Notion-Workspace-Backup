# Video likes/reactions by channel

Created: April 6, 2023 5:28 PM
Tags: Channels, Likes / Reactions, Orion v2, Videos

```jsx
query {
  videoReactionsConnection(
    where: {
      reaction_eq: LIKE
      video: { channel: { id_eq: "7692" } }
      createdAt_gt: "2023-03-01T00:00:00.000Z"
      createdAt_lt: "2023-04-01T00:00:00.000Z"
    }
    orderBy: [createdAt_DESC]
  ) {
    totalCount
  }
}
```

[https://orion.joystream.org/v2/graphql](https://orion.joystream.org/v2/graphql)