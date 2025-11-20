# Vested payment from WG budget

Visit - https://polkadot.js.org/apps/?rpc=wss://rpc.joyutils.org#/extrinsics

![Untitled](Vested%20payment%20from%20WG%20budget/Untitled.png)

Step 1 - Select Lead account

Step 2 - Choose name of working group

Step 3 - Choose vestedspendfrombudget extrinsic

Step 4 - Put the wallet address to receive vested payment

Step 5 - Put in amount to be vested, in HAPI  (use [joyutils.org](http://joyutils.org) for conversion)

Step 6 - Amount to be released perblock. (in HAPI)

14,400 (daily blocks) x 365 (days) = 5,256,000 (Use formula to get for the desired number of days, months, years)

Amount per block = Amount in JOY/Total block (eg. 240,000 JOY / 5,256,000 = 0.0456621) convert result to HAPI using joyutils.org

Step 7 - Choose a starting block in future, use [https://joystream.subscan.io/](https://joystream.subscan.io/) to see latest blocks

Step 8 - Turn ON include rationale option and input rationale for transaction

Step 9 - Sign and submit transaction