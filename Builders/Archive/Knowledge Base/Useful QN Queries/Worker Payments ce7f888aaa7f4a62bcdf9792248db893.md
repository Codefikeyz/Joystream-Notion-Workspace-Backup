# Worker Payments

Created: May 10, 2022 9:00 AM
Description: Get all Worker payments
Tags: Payments, Working Groups (WGs)

1000 payments sorted by block height

```jsx
query { rewardPaidEvents (orderBy: [inBlock_DESC], limit: 1000) {
inBlock amount groupId worker { membership{handle} rewardPerBlock missingRewardAmount
} } }
```

1000 payments sorted by amount

```jsx
query { rewardPaidEvents (orderBy: [amount_DESC], limit: 1000) {
inBlock amount groupId worker { membership{handle} rewardPerBlock missingRewardAmount
} } }
```