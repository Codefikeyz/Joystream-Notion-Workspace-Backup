# How to pay with Vested Token Transfer

How to withdraw vested lead salary from the WG budget:

1. First you need to withdraw the desired funds from your WG budget to your account without vesting, using `group.spendFromBudget`. You should provide rationale and make the payment to your lead reward account. In polkadot-js the amount for this extrinsic is in HAPI so use joyutils to convert.
2. Once you have the funds in your account, you should use `vesting.vestedTransfer` to apply the vesting schedule. To keep things clear I have sent the payment from my reward account to my reward account (self). As `locked` you need to put the full payment amount, but **in JOY, not HAPI**. For me it's 227k JOY as specified in the plan. Then `perBlock` determines how long the vesting will take, this is also **in JOY, not HAPI**. I'm applying 1yr vesting so I took the full amount and divided it by the number of blocks in a year. 1yr=5256000 block, 2yr=10512000 block, you can use joyutils to convert. So for me `perBlock` is `227272.73/5256000 = 0.04324062595`. Lastly, as `startingBlock` ideally put a few blocks into the future from when you are sending the extrinsic. As you can see from the Pioneer screenshot, the vesting was properly applied.

![Screenshot 2024-03-11 at 16.08.46.png](How%20to%20pay%20with%20Vested%20Token%20Transfer/Screenshot_2024-03-11_at_16.08.46.png)

![Screenshot 2024-03-11 at 16.08.53.png](How%20to%20pay%20with%20Vested%20Token%20Transfer/Screenshot_2024-03-11_at_16.08.53.png)

![Screenshot 2024-03-11 at 16.08.59.png](How%20to%20pay%20with%20Vested%20Token%20Transfer/Screenshot_2024-03-11_at_16.08.59.png)