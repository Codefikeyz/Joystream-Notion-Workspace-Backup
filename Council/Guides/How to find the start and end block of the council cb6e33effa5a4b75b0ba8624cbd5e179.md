# How to find the start and end block of the council term

# How to find the start and end block of the council term

1. Go to a GraphQL Client (Ex: [https://graphql-console.subsquid.io/?graphql_api=https://query.joystream.org/graphql](https://graphql-console.subsquid.io/?graphql_api=https://query.joystream.org/graphql))
2. Paste the following query
    
    ```jsx
    query {
      electedCouncils{
        id,
        electedAtBlock,
        endedAtBlock
      }
    }
    ```
    
3. Check the result of the right panel and search for the council term you want

Video: [https://gleev.xyz/video/12595](https://gleev.xyz/video/12595)

## How to find the block hash with a block number

1. Go to a chain explorer (Ex: [https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Frpc.joystream.org%3A9944#/explorer](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Frpc.joystream.org%3A9944#/explorer))
2. Paste the block number on the “search” field

![Untitled](How%20to%20find%20the%20start%20and%20end%20block%20of%20the%20council/Untitled.png)

1. Copy the hash

![Untitled](How%20to%20find%20the%20start%20and%20end%20block%20of%20the%20council/Untitled%201.png)

Video: [https://gleev.xyz/video/21828](https://gleev.xyz/video/21828)

## Accounting

### How to Calculate Validators Rewards

1. Find start and end block of the council. 
Example:
- Start: 1051200
- End: 1152000
2. Find the start and end block hash’s
Example:
- Start: 0xa0cba7c304e93007103fc698c695a3fde593d81c1da8ef2f1a7b50232f7094f6 
- End: 0xbdd8dee4663db9c98eb1b3242561fb9952daf2aa77b2a9fe9a315e3f047167be
3. Find the era at the start and at the end of the term
    1. Open the chain state (Ex: [https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Frpc.joystream.org%3A9944#/chainstate](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Frpc.joystream.org%3A9944#/chainstate))
    2. Select `staking` ,`activeEra` and paste the hash of the start block on the `blockhash to query at`. Repeat the process for the end block.
        
        ![Untitled](How%20to%20find%20the%20start%20and%20end%20block%20of%20the%20council/Untitled%202.png)
        
        Example result:
        - Start: 1764
        - End: 1932
        
4. Find the reward of the `start era` and of the `end era`
    1. Open the chain state (Ex: [https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Frpc.joystream.org%3A9944#/chainstate](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Frpc.joystream.org%3A9944#/chainstate))
    2. Select “staking”, “erasValidatorReward” and fill the “era index”
    Example result: 
    - 69.86 k tJOY
    - 43.72 k tJOY
        
        ![Untitled](How%20to%20find%20the%20start%20and%20end%20block%20of%20the%20council/Untitled%203.png)
        
    3. Calculate an average between the start era reward and end era reward
    Example result:
    - (69.86 + 43.72) /  2 = 56.79 k tJOY
    4. Multiply the average era reward by the amount of eras in 15 days (60)
    Example result: 
    - 56.79 * 60 = 3 407,4 k tJOY = 3.4 M tJOY