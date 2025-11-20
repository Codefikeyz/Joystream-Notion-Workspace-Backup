# Show all slashes from proposals

Created: February 27, 2023 7:06 AM
Description: Show all slashes from proposals
Tags: Proposals, Slashing, Subsquid

```jsx
query MyQuery {
  events(limit: 3000, where: { name_eq: "Balances.Slashed"},
    orderBy: block_height_DESC) 
  { name args block{height} }
}
```