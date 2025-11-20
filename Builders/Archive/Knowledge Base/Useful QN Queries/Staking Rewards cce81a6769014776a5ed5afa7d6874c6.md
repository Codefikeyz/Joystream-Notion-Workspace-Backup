# Staking Rewards

Created: February 27, 2023 8:43 AM
Tags: Nominators, Rewards, Staking, Subsquid, Validators

```jsx
query MyQuery {
  events(limit: 3000, where: { name_eq: "Staking.Rewarded"},
    orderBy: block_height_DESC) 
  { name args block{height} }
}
```