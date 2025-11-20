# Problems with releasing stake from voting

Areas Impacted: Elections, Pioneer, Query Node, Voting
Current Status: Ongoing
Severity: Low, PSA
Type: Bug, Information
Created at: May 9, 2022 6:46 PM
Last Updated: May 16, 2022 8:03 AM

Some users have reported difficulty in releasing stake after voting in an election.

1. `All Accounts` method
    - On this page ([https://dao.joystream.org/#/profile](https://dao.joystream.org/#/profile)) under `All Accounts` a `Release Stake` button is shown next to votes.
    - This button is **currently broken** and has already been reported here: https://github.com/Joystream/pioneer/issues/2988. Hopefully it will be fixed soon!
2. `Election` > `Past Votes` method
    - Most users can release their stake by visiting this page: [https://dao.joystream.org/#/election/past-votes](https://dao.joystream.org/#/election/past-votes)
3. `Extrinsic` method
    - Some users do not see the button described in method 2. This can be because the Query Node hasn’t registered their vote. This issue has been reported https://github.com/Joystream/joystream/issues/3727 and will hopefully be fixed soon, in the meantime...
    - A user can go to [https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Frpc.joystream.org:9944#/extrinsics](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Frpc.joystream.org:9944#/extrinsics)
        
        1. Go to `Developer` > `Extrinsics`
        
        2. Select your wallet address that voted
        3. Under your address, select `referendum` > `releaseVoteStake()`
        
        4. Click `Submit Transaction`
        
        Example screenshot:
        
        ![Untitled](Problems%20with%20releasing%20stake%20from%20voting/Untitled.png)