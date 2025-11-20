# Proposal Discussion posts

Created: February 15, 2023 6:56 AM
Tags: Proposals

```jsx
query MyQuery {
  proposalDiscussionPostCreatedEvents(limit: 1000) {
    id
    inBlock
    text
    postId
    post {
      author {
        handle
      }
      discussionThread {
        proposal {
          title
        }
        proposalId
      }
      discussionThreadId
    }
  }
}
```