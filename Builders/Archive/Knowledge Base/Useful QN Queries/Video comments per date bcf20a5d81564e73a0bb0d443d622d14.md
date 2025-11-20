# Video comments per date

Created: April 6, 2023 5:29 PM
Tags: Comments, Videos

```jsx
query {
  videoReactionsConnection(
    where: {
      AND: [
        { createdAt_gt: "2023-03-01T00:00:00.000Z" }
        { createdAt_lt: "2023-04-01T00:00:00.000Z" }
      ]
    }
  ) {
    totalCount
  }

  commentsConnection(
    where: {
      AND: [
        { createdAt_gt: "2023-03-01T00:00:00.000Z" }
        { createdAt_lt: "2023-04-01T00:00:00.000Z" }
      ]
    }
  ) {
    totalCount
  }
}
```