# Membership Bought Events

Created: February 5, 2023 8:38 PM
Tags: Bought, Membership

```jsx
query MyQuery {
  membershipBoughtEvents(limit: 1000) {
    id
    inBlock
    handle
    newMember {
      id
    }
  }
}
```