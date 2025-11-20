# Joystream Tipping Bot

**Developer**: Create

**Maintainer**: Dzidex

**Version**: 1.0

**Background**: https://github.com/Joystream/discord-bot/issues/6

**Feature**: Discord users can send JOY among themselves using discord username without onchain transactions after depositing a small amount to the pool account. Users sign a signature to prove the origin of their funds and use a command to confirm their deposit. The server admin can set daily limits to number of transactions, deposit amount and withdrawal amount.

**Bot Pool Address**: 
(testing period)
`5EX1JGrkV84M7RLbaaYX4DSrNLC9ZSpfNU7TtobEaF2UMtxC`    (Substrate: prefix 42)
`j4TmusK6iMqZNx2nLrYzCuN9qtiGj4LPq6QjuGMdZ1KB71b9D`   (Joystream: prefix 126)

## How to use

### **The first step is to do on-chain JOY transfer from your account to the bot pool address. Then follow the below link and use the same account to sign the string “seed”. You will receive a signature.**
[https://polkadot.js.org/apps/?rpc=wss://rpc.joystream.org:9944#/signing](https://polkadot.js.org/apps/?rpc=wss://rpc.joystream.org:9944#/signing)

![Untitled](Joystream%20Tipping%20Bot/Untitled.png)

After that, you must confirm your deposit from discord by running the command `/verifyDeposit`

If deposit is confirmed successfully, you can use the commands `/send` and `/withdraw`

- `/verifydeposit`
    
    Verify your JOY deposit to the bot pool address.
    
    **wallet**: The wallet address from which you transferred JOY to the bot pool address.
    
    **signature**: the resulting signature after signing the string “seed” with the deposit account.
    
    example: 
    
    `/verifydeposit wallet j4Umbxo2oPWGH6o311bMVTZ69WuoyfSdGPjQxT32fwvaeAfGb signature 0xdcc74cd63263ed8eedf3f01c18a29dd41e4d75394465da01c35d733b2ec8a9204952c66296e8e257862df5d7f91d23556cd6d57925702d8010edb3437c6b4d84`
    
    After running this command you will see either of the following messages:
    
    - `Your input is incorrect.`
    In this case, either the “wallet” or “signature” parameters are incorrect.
    - `Your deposit is XXX JOY, but it cannot be processed because it will overflow the remaining deposit limit XXX JOY.`
    This means that the daily deposit limit has been reached and you must wait until the next day to verify the deposit.
    - `You have deposited XXX JOY to the tip pool. Your current balance is XXX JOY`
    This means that all went well and your balance is updated.

- `/getBalance`
    
    Get the amount of JOY that any user possess in the bot pool.
    
    **user_name**: the username of the discord user you would like to know the balance of. Username must be input with `@` at the beginning.
    
    example: `/getBalance user_name @Chaos77`
    
- `/send`
    
    Transfer JOY from the bot pool from your possession to another discord user
    
    **receiver**: the discord Username of the receiver, Username must be input with `@` at the beginning.
    
    **amount**: Amount of JOY to send
    
    example: `/send receiver @Chaos77 amount 10`
    
- `/withdraw`
Withdraw JOY from the discord pool to any Joystream account
**amount**: amount of JOY to withdraw
**wallet**: the account address to withdraw to
example: `/withdraw amount 10`

- `/help`
Link the user to this help page.
- `/set_limit`
The admin can set daily limits to transactions, amount of withdrawal, amount of deposit.

- `/status`
Displays the following information
    - Bot Version
    - Pool Wallet Address
    - Total Token Amount in the Pool
    - Daily transaction limit
    - Daily withdrawal limit
    - Daily deposit limit

## **Setup**

In order to start the discord bot server and connect it to the Joystream discord server, the admin must follow the next steps.

- Setup a mongodb server
- Create a Joystream wallet account. This will serve as the pool for all discord users who use the tipping bot.
- Configure the env file.
MONGO_URI = 'mongo uri'
SERVER_TOKEN = 'discord server token'
SERVER_WALLET_ADDRESS = "wallet address"
SERVER_WALLET_KEY="12 words"
ADMIN=”user ID of the Joystream discord server admin”
- Start the server