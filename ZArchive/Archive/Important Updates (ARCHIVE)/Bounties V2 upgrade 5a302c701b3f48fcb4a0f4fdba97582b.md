# Bounties V2 upgrade

Areas Impacted: Bounties, Pioneer, Runtime
Current Status: Ongoing
Severity: PSA
Type: Upgrade
Created at: April 12, 2022 3:37 PM
Last Updated: April 12, 2022 3:46 PM

- @bedeho provided list of `Bounties v2` features April 12, 2022 on Discord ([link](https://discord.com/channels/811216481340751934/813361923172335648/963276522381275146)):
    - Allow creator to provide funding to oracle
    - Working period and judgement period are always without a time limit, as it in most real scenarios is not possible to forecast how long it will take.
    - The oracle, or the council, can switch out the oracle to another one if it goes stale.
    - No more automated slashing of entrants based on when they withdraw.
    - Allow cancellation of bounty be creator for full funding period.
    - Allow cancellation of bounty at any time by council, returning funds to funders.
    - Fixing a long list of security bugs
    - *“Things are a bit more complicated now, which you always want to avoid, but the module is also much more flexible and secure. One thing we did not take very seriously before was strategic behaviour between participants, for example where someone would fund a bounty only to be able to extort the oracle for their payoff, since the oracle payoff happened only when the last funder had cashed out in a failure case. Now we believe most of these bad cases are not present.”*
    
    ![Untitled](Bounties%20V2%20upgrade/Untitled.png)