# Vesting Extrinsics (subsquid)

Created: July 13, 2023 6:36 PM
Tags: Subsquid

```jsx
query vesting_updates {
  events(where: {name_contains: "Vesting.VestingUpdated"}, limit: 10000,) {
    name args block { height }
  }
}
```