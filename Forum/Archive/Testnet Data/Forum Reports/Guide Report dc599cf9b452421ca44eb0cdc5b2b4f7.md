# Guide: Report

[Report ⚡Term 18 ](Guide%20Report/Report%20%E2%9A%A1Term%2018%205cd085d9b38247fe84f5f2b762adc425.md)

### Activity Summary

All tasks completed by Working Group for term should be provided.

### **Forum statistics**

- threads were created in particular term
- threads were deleted in particular term
- posts were created in particular term
- posts were deleted in particular term
- posts exists (in general) till the end of particular term

| How many threads were created | 0 |
| --- | --- |
| How many threads were deleted | 0 |
| How many posts were created  | 0 |
| How many posts were deleted | 0 |
| How many posts exists* | 0 |

*Use this query to get data about how many posts exists

```graphql
query AllExistingPosts($councilEndTimeStamp: DateTime!) {
forumPosts(limit: 100000, where: {createdAt_lte: $councilEndTimeStamp}) {
id
}

}

{
"councilEndTimeStamp": 1657673292000
}
```

I use this query to get these data:

- threads were created in particular term
- threads were deleted in particular term
- how many threads was created during the last scoring period
- a summary of all `forum` (except regular posting) transactions made by the group, who made it, and why, eg.
- charts showing the forum history over time*

*visualisation of a chart should be done in excel or similar tool

```graphql
query ForumDataReport($councilStartBlock: Int!, $councilEndBlock: Int!) {
  categoryCreatedEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}, limit: 100) {
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
  categoryArchivalStatusUpdatedEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}, limit: 100) {
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
  categoryDeletedEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}, limit: 100) {
    inBlock
    category {
      id
      title
      description
    }
  }
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
  threadMetadataUpdatedEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}, limit: 100) {
    inBlock
    thread {
      id
      title
      author {
        handle
      }
    }
  }
  threadDeletedEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}, limit: 100) {
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
  threadMovedEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}, limit: 100) {
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
  categoryMembershipOfModeratorUpdatedEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}, limit: 100) {
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
  categoryStickyThreadUpdateEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}, limit: 100) {
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
  threadCreatedEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}, limit: 100) {
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

```

I use this query to get these data:

- posts were created in particular term
- posts were deleted in particular term

```graphql
query CreatedPosts($councilStartBlock: Int!, $councilEndBlock: Int!) {
  postAddedEvents(where: {inBlock_gte: $councilStartBlock, inBlock_lt: $councilEndBlock}, limit: 1000) {
    inBlock
    postId
  }
  postDeletedEvents {
    id
    inBlock
  }
}
```