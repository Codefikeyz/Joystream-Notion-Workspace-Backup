# Channel deleted by moderator events

Created: February 15, 2023 7:11 AM
Tags: Channels, Curators, Moderation

```jsx
query MyQuery {
  channelDeletedByModeratorEvents {
    id
    actor {
      ... on ContentActorMember {
        dummy
        member {
          handle
        }
      }
      ... on ContentActorLead {
        dummy
      }
      ... on ContentActorCurator {
        curator {
          id
        }
      }
    }
    channelId
    inBlock
    rationale
  }
}
```