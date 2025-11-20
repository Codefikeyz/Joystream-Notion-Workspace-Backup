# Members with gifted/bought/invited status

Created: February 5, 2023 9:38 PM
Tags: Gifted, Invitation, Membership

```jsx
query MyQuery {
  memberships(offset: 4500, limit: 1000, orderBy: createdAt_ASC) {
    id
    handle
    entry {
      ... on MembershipEntryPaid {
        __typename
        membershipBoughtEvent {
          inBlock
        }
      }
      ... on MembershipEntryInvited {
        __typename
        memberInvitedEvent {
          inBlock
        }
      }
      ... on MembershipEntryGifted {
        __typename
        membershipGiftedEvent {
          inBlock
        }
      }
      ... on MembershipEntryMemberCreated {
        __typename
        memberCreatedEvent {
          inBlock
        }
      }
    }
  }
}
```