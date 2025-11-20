# Validator Count Increase post-mortem

Tags: Post-mortem

Proposal: [https://pioneerapp.xyz/#/proposals/preview/170](https://pioneerapp.xyz/#/proposals/preview/170)

Description: This was the 1st validator count increase on mainnet. It increased the validator count from 30 > 35.

Date/time: Blockheight ~1537900 - ~1539000

Events:

1. Proposal execution went fine and there were no issues noticed.
2. The waiting validator set had few nominators, this meant the minimum validator stake went from ~2.8169m $JOY at blockheight 1537953 to 199,134 $JOY after the era completed and more validators were added. It may be that there is some confusion on how to read the UI.
    1. 3 newly elected validators had nominators, 2 had no nominators
    2. The long term impact of this aren’t considered here and it is presumed the nominators will balance out over time to the newer validators.
        1. After approx 12 hours the minimum stake (at blockheight 1543749) had risen to ~2.6108m $JOY.
        2. One of the newly elected Validators went offline about a day or so after the validator count increase (at least this is how it appears): [https://polkadot.js.org/apps/#/explorer/query/0xc29cf63a5f74760de3b8bea1bb9c164a0e74855b32799689b4c2a8183318a939](https://polkadot.js.org/apps/#/explorer/query/0xc29cf63a5f74760de3b8bea1bb9c164a0e74855b32799689b4c2a8183318a939)
3. After monitoring the average block time post-proposal execution, no latency issues were immediately noticed. The average block time of the past 50 blocks seldom deviated significantly from `6.000s` (monitored using this page: [https://polkadot.js.org/apps/#/explorer/latency](https://polkadot.js.org/apps/#/explorer/latency)) for a while after the extra validators were elected.

Notes:

1. The low validator stake issue for waiting validators wasn’t really noticed by anyone until shortly before the increase happened. I would suggest in the future that for this specific proposal type (Validator Count Increase) that we are more vigilant about checking the waiting validator list when execution of the proposal nears.
2. The current tooling for nominating validators is less than ideal as identifying validators is very difficult. New tooling is coming out sometime soon which will greatly improve the UX for this and hopefully make this issue not be a problem in the future.
3. Besides notifying `@everyone` on Discord and using the forum, there currently doesn’t seem to be a communication channel to communicate specifically with Validators and Nominators to address issues. There has been some discussion and work on implementing email notifications within Pioneer which may help with this problem.
4. The current tooling for monitoring validator performance isn’t ideal, besides this page ([https://polkadot.js.org/apps/#/explorer/latency](https://polkadot.js.org/apps/#/explorer/latency)) there currently aren’t detailed stats available, and the linked page only covers the previous 50 blocks. The problem with this is that ideally we should be able to easily bring up stats for a validator count change for something like 1000 blocks pre + post upgrade so it is trivial to see if there were any problems.
    1. Previously on testnets we had some scripts that could analyze certain aspects of validator performance.