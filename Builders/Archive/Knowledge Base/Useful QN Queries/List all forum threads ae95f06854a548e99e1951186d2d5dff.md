# List all forum threads

Created: January 7, 2023 5:27 AM
Description: list all forum threads, author handle, title, category, sorted by date (earliest first)
Tags: Forum, Forum Threads

```jsx
query MyQuery {
  forumThreads(limit: 3000, orderBy: createdAt_ASC) {
    id
    title
    category {
      title }
    author {
      handle
      id
    }
    initialPostId
    createdInEvent {
      inBlock
    }
    isVisible
    tags {
      id
    }
  }
}
```