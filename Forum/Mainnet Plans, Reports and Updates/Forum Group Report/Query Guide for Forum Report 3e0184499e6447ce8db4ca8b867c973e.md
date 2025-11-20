# Query Guide for Forum Report

Json to CSV Converter: [https://konklone.io/json/](https://konklone.io/json/)

Json Editor: [https://jsoneditoronline.org/#right=local.mabepi&left=local.bepupe](https://jsoneditoronline.org/#right=local.mabepi&left=local.bepupe)

Query Explorer: [https://graphql-console.subsquid.io/?graphql_api=https://query.joystream.org/graphql](https://graphql-console.subsquid.io/?graphql_api=https://query.joystream.org/graphql)

Alternative Query Explorer: [https://query.joystream.org/graphql](https://query.joystream.org/graphql)

Joystream Explorer: [https://joystream.explorer.subsquid.io/graphql](https://joystream.explorer.subsquid.io/graphql)

Joy Scanner: [https://jscan.io/](https://jscan.io/)

### Blocks and Dates of each Council Terms

```graphql
query{
  electedCouncils {
    electedAtTime
    endedAtTime
    electedAtBlock
    endedAtBlock
  }
}
```

### No. of created threads (last term)

```graphql
query ForumDataReport($councilStartBlock: Int!, $councilEndBlock: Int!) {
    threadCreatedEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}, limit: 10000) {
    inBlock
    thread {
      id
      title
      author {
        handle
      }
      category {
        id
        title
      }
    }
  }
}

{
  "councilStartBlock": XXXXXX,
  "councilEndBlock": XXXXXX
  
}
```

### No. of deleted threads (last term)

```graphql
query ForumDataReport($councilStartBlock: Int!, $councilEndBlock: Int!) {
  threadDeletedEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}, limit: 10000) {
    inBlock
    thread {
      title
      id
      author {
        handle
      }
      category {
        title
        id
      }
    }
  }
}
```

### No. of created/deleted posts (last term)

Created post check in: [https://jscan.io/](https://jscan.io/)

You can also sum below query and add to new threads created

```graphql
query CreatedPosts($councilStartBlock: Int!, $councilEndBlock: Int!) {
  postAddedEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}, limit: 10000) {
    inBlock
    postId
  }
  postDeletedEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}, limit: 10000) {
    id
    inBlock
  }
}
```

### No. of threads on forum (overall)

```graphql
query ForumDataReport($councilStartBlock: Int!, $councilEndBlock: Int!) {
    threadCreatedEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}, limit: 10000) {
    inBlock
    thread {
      id
      title
      author {
        handle
      }
      category {
        id
        title
      }
    }
  }
    threadDeletedEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}, limit: 10000) {
    inBlock
    thread {
      title
      id
      author {
        handle
      }
      category {
        title
        id
      }
    }
  }
}
```

### No. of posts on forum (overall)

```graphql
{
  forumPosts(where: {deletedAt_eq: null, createdAt_gt: "1970-01-01T00:00:00.000Z", createdAt_lt: "2023-01-30T04:53:24.000Z"}, limit: 9999) {
    thread {
      categoryId
    }
  }
}
```

### Moderation of threads

```graphql
query ForumDataReport($councilStartBlock: Int!, $councilEndBlock: Int!) {
  threadDeletedEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}, limit: 10000) {
    inBlock
    thread {
      title
      id
      author {
        handle
      }
      category {
        title
        id
      }
    }
  }
}

query ForumDataReport($councilStartBlock: Int!, $councilEndBlock: Int!) { 
  threadModeratedEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}, limit: 100) {
    inBlock
    rationale
    thread {
      id
      author {
        handle
      }
    }
  }
}
```

### Moderation of posts

```graphql
query ForumDataReport($councilStartBlock: Int!, $councilEndBlock: Int!) { 
  postModeratedEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}, limit: 100) {
    inBlock
    rationale
  }
}
```

### Categories Deleted

```graphql
query ForumDataReport($councilStartBlock: Int!, $councilEndBlock: Int!) {
  categoryDeletedEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}, limit: 10000) {
    inBlock
    category {
      id
      title
      description
    }
  }
}
```

### Categories Created

```graphql
query ForumDataReport($councilStartBlock: Int!, $councilEndBlock: Int!) {
  categoryCreatedEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}, limit: 10000) {
    category {
      id
      parentId
      parent {
        title
      }
      title
      description
    }
    inBlock
  }
}
```

### Threads Moved

```graphql
query ForumDataReport($councilStartBlock: Int!, $councilEndBlock: Int!) {
  threadMovedEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}, limit: 10000) {
    inBlock
    actorId
    thread {
      id
      title
      author {
        handle
      }
    }
    oldCategory {
      id
      title
    }
    newCategory {
      id
      title
    }
  }
}
```

### Sticky Thread Changes in Last Term

```graphql
query ForumDataReport($councilStartBlock: Int!, $councilEndBlock: Int!) {
  categoryStickyThreadUpdateEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}, limit: 10000) {
    inBlock
    category {
      title
      id
    }
    newStickyThreads {
      title
      id
    }
  }
}
```

### Category Archival Status Updated

```graphql
query ForumDataReport($councilStartBlock: Int!, $councilEndBlock: Int!) {
  categoryArchivalStatusUpdatedEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}, limit: 10000) {
    inBlock
    category {
      id
      title
      description
      moderators {
        id
      }
    }
    newArchivalStatus
  }
}
```

### Category Moderator Updated

```graphql
query ForumDataReport($councilStartBlock: Int!, $councilEndBlock: Int!) {
  categoryMembershipOfModeratorUpdatedEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}, limit: 10000) {
    inBlock
    category {
      id
      title
    }
    moderator {
      id
    }
    moderatorId
    newCanModerateValue
  }
}
```

### Worker Rewards

```graphql
query ($councilStartBlock: Int!, $councilEndBlock: Int!) {
  rewardPaidEvents(where: {AND: {group: {name_eq: "XXX"}, inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}}, limit: 10000) {
    amount
    worker {
      membership {
        handle
      }
    }
    inBlock
  }
}

WG= "forumWorkingGroup"
```

### Thread Authors (FM or Not?)

```graphql
query MyQuery($councilStartBlock: Int!, $councilEndBlock: Int!) {
  threadCreatedEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}) {
    threadId
    thread {
      author {
        handle
        isFoundingMember
      }
      title
    }
  }
}
```