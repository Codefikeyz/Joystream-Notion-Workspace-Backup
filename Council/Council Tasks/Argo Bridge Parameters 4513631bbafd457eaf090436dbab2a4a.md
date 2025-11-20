# Argo Bridge Parameters

Public Notion URL: https://joystream.notion.site/4513631bbafd457eaf090436dbab2a4a
Priority: N/A or finished
Tags: Funding/funds, argo bridge, bridge, council, financial, markets, multisig (stablecoins), security, treasury
Created time: June 6, 2024 4:33 PM
Owner: tomato
Work Status: Done
Governance Status: Proposal Approved
Archive Status: No
Days passed since task created: 531
Proposals: Argo Bridge Parameters - V1 (https://www.notion.so/Argo-Bridge-Parameters-V1-05c815b7c79c4733a51e20bce0992666?pvs=21), Argo Bridge Parameters - v1 (https://www.notion.so/Argo-Bridge-Parameters-v1-04ac270cf4a24bceb280c0583707cf1f?pvs=21)
Proposals #: 2
Threads: Argo bridge parameters (https://www.notion.so/Argo-bridge-parameters-575f4bffb56449afbcb85df560cb320a?pvs=21), Argo v2 bridge structure (https://www.notion.so/Argo-v2-bridge-structure-7ceb12a358ec493d8a4c501f67306d0b?pvs=21), Argo - Ethereum Community Bridge (https://www.notion.so/Argo-Ethereum-Community-Bridge-329d95bfd673484f8fa7ed3e3d906358?pvs=21)
Threads #: 3
Parent-task: Argo Bridge Gameplan (Argo%20Bridge%20Gameplan%20966c7d4373e44ef1bda2b35f0059fafd.md), Argo Bridge Parameters (Argo%20Bridge%20Parameters%204513631bbafd457eaf090436dbab2a4a.md)
Sub-tasks: Argo Bridge Parameters (Argo%20Bridge%20Parameters%204513631bbafd457eaf090436dbab2a4a.md), Council to make 5/9 Argo multisig BASE election (Council%20to%20make%205%209%20Argo%20multisig%20BASE%20election%205341735d4768466fae270dbef387d615.md)
Last edited time: July 1, 2024 3:52 PM

| Multsig Name | Network | Use / Frequency | Risk | Suggested multisig setup | Final decision | **Rationale/Arguments** |
| --- | --- | --- | --- | --- | --- | --- |
| EthAdmin | BASE | admin of our Ethereum (Base) contracts / Low frequency / can unpause (TBC) | Highest | 4/7 or 5/9 | 5/9 - council to elect 9 multisig operators for this (should be unique people to other multisigs) | - leetjoy/klaudiusz both in favor of 5/9 / ethadmin takes actions rarely / better to have new addresses and not reuse previous addresses / wiser to get more / can we actually get 9 signers? |
| EthOp | BASE | can finalize transfers, minting new tokens, subject to minting limits / Frequency dependent upon bridge use (maybe more frequent)  | High | 2/3, 3/4 or 3/5 | 3/5 - aspire for this number (should be unique people to other multisigs) | - really active people for this role / risk is they can mint / can arbitrarily mint tokens (even to their own account) / should be different operators - signers need to approve each TX (about 1-2 mins per TX) |
| JoyOp | Joystream | can finalize transfers, minting new tokens, subject to minting limits / Frequency dependent upon bridge use (maybe more frequent) | High | 2/3, 3/4 or 3/5 | 3/5 - aspire for this number (should be unique people to other multisigs) | - really active people for this role / risk is they can mint / can arbitrarily mint tokens (even to their own account) / should be different operators - signers need to approve each TX (about 1-2 mins per TX) |
| Pauser role addresses | BASE | Addresses which can immediately pause the bridge - no new transfers can be req’d or finalized / no new minting or burning / can only be unpaused by ethAdmin | Low | multisig possible, but it has been suggested to have single addresses | 3-5 people, don’t need to be unique | N/A |
| Pauser role addresses (set by council) | Joystream Council / Proposal | Addresses which can immediately pause the bridge - no new transfers can be req’d or finalized / no new minting or burning / can only be unpaused by ethAdmin | Low | multisig possible, but it has been suggested to have single addresses | 3-5 people, don’t need to be unique | N/A |
| Multisig / Governance | Parameter | Description | Delay | Suggested Parameter | Final Decision | **Rationale/Arguments** |
| EthAdmin | Minting Limits | limits how many wrapped $JOY can be minted within a given time period | Subject to timelock delay | N/A | 1.5m per 24h | - klaudiusz: wrapped TXs will be a fraction (like 10%) of native transfers / may make sense to set it higher initially - leetjoy suggests 1m/24h for first 7-14 days - klaudiusz suggests higher to account for LP etc |
| EthAdmin | Minting Limit Period Length | time duration in blocks (Base blocks - 2s) | Subject to timelock delay | N/A | Per 24h | - klaudiusz: wrapped TXs will be a fraction (like 10%) of native transfers / may make sense to set it higher initially - leetjoy suggests 1m/24h for first 7-14 days - klaudiusz suggests higher to account for LP etc |
| EthAdmin | Timelock Delay | Delay to allow participants to exit if there is any security compromise | Subject to timelock delay | 5 days | 2 days for initial phase, then move to 5 days after 2-3 week period | Gives people the chance to exit, should take into account public days. Flipside may be that a change may be necessary quicker. |
| EthAdmin | Bridging Fee (ETH) | Fee for EVM>JOY transfer | Subject to timelock delay | $5-10 range | $5 | - klaudiusz: each tx has to be manually clicked by operators / leetjoy+tomato rationale, should be lower to incentivize use |
| Joystream Council / Proposal | Bridging Fee ($JOY) | Fee for JOY>EVM transfer | Subject to proposal grace period delay (1 day) | $5-10 range | $5 | - klaudiusz: finalizing TX on BASE will cost gas fees (current fees are very low—roughly 2c per tx) |
| JoyOp multisig | Unpause Delay | Blocks to unpause Argo pallet after freezing (JOY blocks - 6s) — unpaused by JOY multisig | N/A - uses extrinsics, so action in immediate | 6 hours | 12 hours | N/A |

## Notes

- All of the parameters are mutable, so it is aimed to review them periodically after the bridge launches and is fully operational.
- It is suggested that whichever council is elected at the time that is 2 weeks after wrapped $JOY becomes available on DEXs does a review of these parameters and considers adjusting them.
- The final sizes of multisigs are dependent on how many people the DAO has available and are willing and suitable candidates, therefore the multisig sizes may be slightly smaller.
- The minting limits have been set on the slightly higher size to begin with, this is for the purpose of allowing liquidity providers and others to be able to convert enough wrapped $JOY for the token to be worthwhile on DEXs. It is aimed that at a future date after launch that we will review the numbers, actual use and risks and lower the amount (ideally 2-3 weeks after the bridge has launched as is operational)

## Concerns

- Max multisig signers = 19 people, unclear if DAO has enough people for this

| Multsig Name | Network | Use / Frequency | Risk | Suggested multisig setup | Final decision |
| --- | --- | --- | --- | --- | --- |
| EthAdmin | BASE | admin of our Ethereum (Base) contracts / Low frequency / can unpause (TBC) | Highest | 4/7 or 5/9 | 5/9 - council to elect 9 multisig operators for this (should be unique people to other multisigs) |
| EthOp | BASE | can finalize transfers, minting new tokens, subject to minting limits / Frequency dependent upon bridge use (maybe more frequent) | High | 2/3, 3/4 or 3/5 | 3/5 - aspire for this number (should be unique people to other multisigs) |
| JoyOp | Joystream | can finalize transfers, minting new tokens, subject to minting limits / Frequency dependent upon bridge use (maybe more frequent) | High | 2/3, 3/4 or 3/5 | 3/5 - aspire for this number (should be unique people to other multisigs) |
| Pauser role addresses | BASE | Addresses which can immediately pause the bridge - no new transfers can be req’d or finalized / no new minting or burning / can only be unpaused by ethAdmin | Low | multisig possible, but it has been suggested to have single addresses | 3-5 people, don’t need to be unique |
| Pauser role addresses (set by council) | Joystream Council / Proposal | Addresses which can immediately pause the bridge - no new transfers can be req’d or finalized / no new minting or burning / can only be unpaused by ethAdmin | Low | multisig possible, but it has been suggested to have single addresses | 3-5 people, don’t need to be unique |
| Multisig / Governance | Parameter | Description | Delay | Suggested Parameter | Final Decision |
| EthAdmin | Minting Limits | limits how many wrapped $JOY can be minted within a given time period | Subject to timelock delay | N/A | 1.5m per 24h |
| EthAdmin | Minting Limit Period Length | time duration in blocks (Base blocks - 2s) | Subject to timelock delay | N/A | Per 24h |
| EthAdmin | Timelock Delay | Delay to allow participants to exit if there is any security compromise | Subject to timelock delay | 5 days | 2 days for initial phase, then move to 5 days after 2-3 week period |
| EthAdmin | Bridging Fee (ETH) | Fee for EVM>JOY transfer | Subject to timelock delay | $5-10 range | $5 |
| Joystream Council / Proposal | Bridging Fee ($JOY) | Fee for JOY>EVM transfer | Subject to proposal grace period delay (1 day) | $5-10 range | $5 |
| JoyOp multisig | Unpause Delay | Blocks to unpause Argo pallet after freezing (JOY blocks - 6s) — unpaused by JOY multisig | N/A - uses extrinsics, so action in immediate | 6 hours | 12 hours |