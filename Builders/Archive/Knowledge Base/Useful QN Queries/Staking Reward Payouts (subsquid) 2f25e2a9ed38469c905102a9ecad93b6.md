# Staking Reward Payouts (subsquid)

Created: July 13, 2023 8:55 PM
Tags: Subsquid

```jsx
query vesting_updates {
  events(where: {name_contains: "Staking.Rewarded"}, limit: 20000,) {
    name args block { height }
  }
}
```