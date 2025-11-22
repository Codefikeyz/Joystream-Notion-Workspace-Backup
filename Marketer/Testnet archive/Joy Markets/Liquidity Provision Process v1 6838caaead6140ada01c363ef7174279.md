# Liquidity Provision Process v1

## **Overview**

This proposal aims to introduce a Liquidity Provision Process within the Joystream DAO governance. The goal is to explore and fund initiatives that directly contribute to enhancing JOY token liquidity while also allowing the DAO to slowly accumulate USDT for [SAFE](https://pioneerapp.xyz/#/proposals/preview/497). By strategically providing additional liquidity, the proposal anticipates an increase in organic trading volume. High trading volume is a crucial factor for larger exchanges, and this approach aims to meet one of the major requirements for gaining visibility on such platforms. This strategy may lead to potential gains over time, particularly in navigating high market volatility and sudden spikes, as the buy and sell orders will be strategically placed below and above market prices.

## **Proposal**

Starting from Term 26, initiate a hiring process for a responsible worker for liquidity provision operations and allocate 500K JOY and 25,000 USDT to enhance liquidity on MEXC and [Gate.io](http://gate.io/) exchanges. 

Initial liquidity allocation per exchange:

| MEXC | Gate.io |
| --- | --- |
| 250,000 JOY | 250,000 JOY |
| 12,500 USDT | 12,500 USDT |

It is recommended to use **Hummingbot (**[https://hummingbot.org/](https://hummingbot.org/)) for such operations.

Hummingbot is proven and efficient, passing rigorous tests by MWG and Council. Its open-source nature, and community-driven development enhance reliability. Hummingbot is a reliable choice with successful testing and active community support. For many crypto market making firms, Hummingbot is the trusted starting point for creating secure, scalable algo trading solutions.

A few potential alternatives could include:

- External Market Makers: Collaborating with external market makers using tools other than Hummingbot. However, this introduces dependency and may incur additional costs. The average market-making retainer fees are around $5,000 per month, excluding actual trading assets.
- Token Incentives: Implementing token incentives to encourage community members to provide liquidity organically. However, this may not guarantee consistent liquidity.

***Recommended initial configuration:***

The recommended strategy serves as a reference for the community to understand the process. The exact strategy will be subject to discussion between the council and the operator.

Strategy: ****`pure_market_making` ****([link](https://hummingbot.org/strategies/pure-market-making/#strategy-tier))
This strategy allows Hummingbot operator to run a market making strategy on a single trading pair on a spot exchanges.

`bid_spread` = 2% 
How far away from the mid price do you want to place the first bid order?

`ask_spread` = 1%
How far away from the mid price do you want to place the first ask order?

`order_refresh_time` = 30 seconds
How often do you want to cancel and replace bids and asks (in seconds)?

`order_amount` = 10,000 JOY
What is the amount of JOY per order?

`price_ceiling` = 0.1$
Price point above which only sell orders will be placed

`price_floor` = 0.035$
Enter the price below which only buy orders will be placed

`order_levels` = 10
How many orders do you want to place on both sides

`order_level_spread` = 1%
Price increments (as percentage) for subsequent orders

`filled_order_delay` = 90 seconds
How long do you want to wait before placing the next order if your order gets filled (in seconds)?

Table for placed orders at any given time:

**Sell orders:**

| JOY amount | Price |
| --- | --- |
| 10000 | Current price +1% |
| 10000 | Current price +2% |
| 10000 | Current price +3% |
| 10000 | Current price +4% |
| 10000 | Current price +5% |
| 10000 | Current price +6% |
| 10000 | Current price +7% |
| 10000 | Current price +8% |
| 10000 | Current price +9% |
| 10000 | Current price +10% |

**Buy orders:**

| JOY amount | Price |
| --- | --- |
| 10000 | Current price -2% |
| 10000 | Current price -3% |
| 10000 | Current price -4% |
| 10000 | Current price -5% |
| 10000 | Current price -6% |
| 10000 | Current price -7% |
| 10000 | Current price -8% |
| 10000 | Current price -9% |
| 10000 | Current price -10% |
| 10000 | Current price -11% |

**Max buy price:** 0.10$ (no buy orders to be placed above 0.10$ per JOY)

**Min sell price:** 0.035$ (no sell orders to be placed below 0.035$ per JOY)

**Order execution timeout:** 90 seconds (no orders to be placed during 90 seconds after any order was executed)

## Execution Process

The proposed execution process spans several stages, including a hiring announcement, candidate interviews, signal proposal submission, staking requirements fulfillment, and reporting. A detailed timeline for each stage is outlined in the proposal to provide clarity on the expected duration.

The proposed implementation involves the following key steps:

1. **Hire a worker/s responsible for liquidity provision operations**
    
    **Announcing Stage (5 days)**: Create a forum on Pioneer for applications for this role, collect submissions.
    
    **Candidate requirements**: To qualify for the liquidity provision role, candidates must demonstrate availability to stake a minimum of 1,000,000 JOY, high availability, and experience with trading and trading automation software.
    
    **Interview (3 days)**: Interview applicants and select worker to perform operations.
    
    **Hiring Signal Proposal (2 days):** Submit a detailed signal proposal for the elected candidate, describing their responsibilities and the agreed-upon compensation model. Proposal should also include their JOY and USDT Ethereum address.
    
    **Fulfil Staking Requirement (1 day):** The hired worker/s must stake the agreed-upon JOY amount in their role to be fully accountable to the council.
    
2. **Provide worker with liquidity (2 days):** 
Send 500,000 JOY to the worker's root address as specified in the hiring proposal.
Send 25,000 USDT to the hired worker's USDT address.
3. **Start operations (3 days)
Exchanges:** Create necessary sub-accounts on MEXC and Gate.io.
**Reporting:** The assigned worker is required to provide regular and transparent reporting to the council. This includes submitting API keys for used sub-accounts and reporting on the status of operations in a dedicated Pioneer thread. The reports must include the starting balance and ending balance for the term and submitted every Term.
**Funding:** Deposit funds to sub-accounts.
**Start operations:** Host, configure and run market-making software.

## Accumulation of USDT for the DAO SAFE

In the event of needing to accumulate USDT for the DAO [SAFE](https://pioneerapp.xyz/#/proposals/preview/497), collaborative adjustments to the strategy will be made by the council and the liquidity provision operator. While enhancing JOY token liquidity, the operator can gradually accumulate additional USDT for the DAO [SAFE](https://pioneerapp.xyz/#/proposals/preview/497) fund. This dual-purpose approach aligns with Joystream DAO's goals of liquidity enhancement and financial stability. However, it is essential to exercise caution in decisions regarding the accumulation of large amounts of USDT, as it can impact JOY markets. 

In initial recommended configuration liquidity on sell side slightly higher: (1% closer to the current price)
bid_spread = 2%
ask_spread = 1%

all this parameters to be adjusted by operator overtime to meet minimum requirements for accumulation USDT per week, however under some circumstances when the markets are flat it might not be as efficient (placed sell orders wont be executed as market is flat)

**The maximum USDT accumulation per week must not exceed 5,000 USDT.**

To prevent bureaucracy and reduce costs (Ethereum transaction fees), withdrawals of accumulated USDT to the DAO [SAFE](https://pioneerapp.xyz/#/proposals/preview/497) will be processed by the operator upon request (signal proposal).

## **Security Measures**

To safeguard the Liquidity Provision Process, security measures include secure configuration, transparent reporting through Pioneer threads and API keys, continuous monitoring, and a staking requirement of 1 million JOY for the assigned worker. These measures collectively uphold the integrity and security of the operation.

## **Operator Protection**

To protect the worker's stake, a careful procedure is in place to ensure fairness and transparency. Before any decision on slashing the worker's stake, the following measures will be followed:

**1. Proper Investigation**

- Before initiating any action to slash the worker's stake, the council is obligated to conduct a thorough investigation into the circumstances leading to the potential slashing.
- The investigation will aim to determine whether the worker's actions were in violation of established guidelines or were influenced by external factors beyond their control.

**2. Community Input**

- The council will actively seek input from the Joystream community before making any decisions related to slashing the worker's stake.
- A dedicated forum on Pioneer will be provided for community members to express their opinions, concerns, and insights regarding the situation.

**3. Decision-Making:**

- Decisions will be communicated openly, providing a clear rationale for the actions taken.

**Slashing operator stake can be used to compensate for damage that has occurred directly due to the actions of the operator (or their inaction).**

## Custody Adjustments

In the event that the DAO needs to adjust any parameters of this proposal, a new detailed proposal must be submitted and approved by the council.

**Relevant links**

[Crypto Trading Platform | Buy Bitcoin, Ethereum, Altcoin, DeFi, Kickstarter | MEXC](https://www.mexc.com/)

[Buy/Sell Bitcoin, Ethereum | Cryptocurrency Exchange | Gate.io](https://www.gate.io/)

[Hummingbot - the open source OS for crypto algo traders](https://hummingbot.org/)

[Pure Market Making - Hummingbot](https://hummingbot.org/strategies/pure-market-making/#example-order-flow)

## **Conclusion**

The proposal for implementing a Liquidity Provision Process within Joystream DAO governance using Hummingbot offers compelling reasons that outweigh the associated costs. While alternatives might seem simpler at first glance, the proposed approach aligns with the community's values and provides a strong foundation for a more liquid, efficient, and accessible JOY market without relying on third party market makers.