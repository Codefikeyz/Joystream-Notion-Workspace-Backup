# List all forum posts and show whether they are still editable

Created: January 6, 2023 3:36 AM
Tags: Deposits, Forum, Forum Posts

```jsx
**query MyQuery {
  forumPosts {
    authorId
    isVisible
    id
    postaddedeventpost {
      isEditable
      inBlock
    }
    threadId
  }
}**
```