# Membership Gifted Events

Created: February 5, 2023 8:46 PM
Tags: Gifted, Membership

```jsx
query MyQuery {
  membershipGiftedEvents(limit: 1000) {
    id
    handle
    inBlock
    newMemberId
  }
}
```