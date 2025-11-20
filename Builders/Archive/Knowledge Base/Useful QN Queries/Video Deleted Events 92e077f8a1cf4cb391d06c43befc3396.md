# Video Deleted Events

Created: February 15, 2023 6:48 AM
Tags: Curators, Videos

```jsx
query MyQuery {
  videoDeletedEvents(limit: 1000) {
    id
    inBlock
    createdAt
    actor {
      ... on ContentActorCurator {
        dummy
        curator {
          id
          curatorGroups {
            curatorGroupId
            curator {
              id
            }
          }
        }
      }
      ... on ContentActorMember {
        member {
          handle
        }
      }
      ... on ContentActorLead {
        dummy
      }
    }
  }
}
```