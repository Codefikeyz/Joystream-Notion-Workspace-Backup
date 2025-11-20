# Budget Increment Pre-proposal

Important notes:

- Validator rewards do not come from the council treasury.
- The budget increment proposal type is expressed in a daily replenishment rate which started at 366k $JOY per day and was adjusted down to 50k $JOY in June 2023, just prior to the token being listed on its first exchange: [https://pioneerapp.xyz/#/proposals/preview/345](https://pioneerapp.xyz/#/proposals/preview/345)
    - Therefore, it is important to talk about the budget increment proposal in terms of daily budgets and not in terms of per-council term budgets. The council term will be changing in the upcoming `nara` runtime upgrade from 15 days > 30 days.
- At the current rate of spending and replenishment of the council treasury and adjustments to the EMA-30 rate it is very likely we will encounter a situation in the next 30-60 days where we will have a possibly dangerously low amount of tokens in the council treasury
    - It should be noted, that the `budget increment` proposal has a constitutionality of `2`, this means that after `nara` it will take anywhere from 30-60 days to change this amount in the future.
    - The council should always have some amount of emergency funds available because we can have many unexpected operational costs relating to running a CDN for video hosting and other liquidity or marketing related costs.
- The council budget increment does not directly impact inflation of the $JOY token. Although it can increase or decrease the amount available in $JOY for the DAO to utilize, none of the tokens exist until they are paid to a recipient via worker rewards or a funding request that is approved. As such the amount in the treasury should be seen as the amount available for future elected councils to utilize, which they will hopefully do responsibly.
- If there is an excess of tokens in the council treasury this can present a security risk to the DAO. There is currently no mechanism for the council to decrease the amount via governance (although they could decrease the replenishment rate and wait for the excess to be used) however the DAO can entrust a staked participant of the DAO to burn tokens. This has been done twice before:
    - August 2023 burning: [https://pioneerapp.xyz/#/forum/thread/527](https://pioneerapp.xyz/#/forum/thread/527) (25 million $JOY or ~2.5% of the total supply was burned)
    - December 2023 burning: [https://pioneerapp.xyz/#/forum/thread/736](https://pioneerapp.xyz/#/forum/thread/736) (10 million $JOY or ~1% of the total supply was burned)
    

Strategy:

- Based up numerous discussions of this parameter, the DAO is going to soon enter a state where the council treasury will go lower than 10m and will likely deplete some time soon. It is difficult to precisely predict this due to a variety of factors and ongoing budget discussions outside of this proposal.
- Rather than try to set a parameter that is the result of some “perfect” prediction of future budget discussions, it has been suggested that in the interest of time and making a decision that we just target an inflationary amount: [https://pioneerapp.xyz/#/forum/thread/782](https://pioneerapp.xyz/#/forum/thread/782) (note: despite the use of the word `inflationary` this increment does not directly impact token inflation as mentioned in the opening `Important notes` section)
- If we choose the below process/strategy we will be setting the increment higher than it probably needs to be and:
    - trusting that future councils will not needlessly increase budgets even if there are tokens available (we already have historical precedent that we have had >50m in the council treasury and no council went on a crazy spending spree)
    - trusting that future councils will also be sensible and will burn tokens periodically if the council treasury is too high (we also have historical precedent that this has occurred more than once)

Parameters:

1. `cushion price` - The USD exchange price that we anticipate to be a possible low price. It is nearly impossible to fully predict something like this, but it should be set lower than the current market price to give the replenishment rate some cushion.
    1. I recommend we target `0.02` for this. The current price is about `0.027`
2. `USD weekly budget target` - The USD weekly budget target price the DAO aims to realistically spend. This should include council, worker and WG lead payments as well as any other expenses that the DAO pays (such as market liquidity, marketing expenses, incentive programs, exchange listing fees, partnership fees, grants etc). This should not include validator rewards.
    1. This is open to discussion but I think should be an average of the past few terms spending—there is obviously some interest in lowering various budgets and costs but we are not targeting a “perfect increment amount” with this strategy
3. `buffer` - Some % value above `cushion price` * `USD weekly budget target`.
    1. I recommend between 10-20%
4. `min % target` & `max % target` - These two parameters are the % of the total supply we should aim to have the treasury be at at any given time. In the event either of these are breached the council should either look at executing a burning event or conducting a review to adjust the replenishment rate.
    1. I suggest we choose a target here of 1.5-2.5%

![Untitled](Budget%20Increment%20Pre-proposal/Untitled.png)