# How to fill out the Memberships WG in the Council Network Summary

### This point looks like this:

![Untitled](How%20to%20fill%20out%20the%20Memberships%20WG%20in%20the%20Council%20/Untitled.png)

**First, you need to find the hash of the block where the period ended - [guide](How%20to%20find%20the%20start%20and%20end%20block%20of%20the%20council%20cb6e33effa5a4b75b0ba8624cbd5e179.md)**

### How to calculate how many invitations are left

1. Open this page - [https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Frpc.joystream.org%3A9944#/chainstate](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Frpc.joystream.org%3A9944#/chainstate)
    
    ![Untitled](How%20to%20fill%20out%20the%20Memberships%20WG%20in%20the%20Council%20/Untitled%201.png)
    
2. Select:
selected state query: members
> membershipById(MemberId): Membership
MemberId: 3439 (Group Leader)
blockhash to query at: [Block where the period ended]
**Then click on the plus sign on the right**
    
    ![Untitled](How%20to%20fill%20out%20the%20Memberships%20WG%20in%20the%20Council%20/Untitled%202.png)
    
    **Enter the resulting figure after the invites into the Council Network Summary**
    

### How to calculate how much is left in the group budget

1. Open this page - [https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Frpc.joystream.org%3A9944#/chainstate](https://polkadot.js.org/apps/?rpc=wss%3A%2F%2Frpc.joystream.org%3A9944#/chainstate)
    
    ![Untitled](How%20to%20fill%20out%20the%20Memberships%20WG%20in%20the%20Council%20/Untitled%201.png)
    
2. Select:
selected state query: membershipWorkingGroup
> budget(): BalanceOf
blockhash to query at: [Block where the period ended]
**Then click on the plus sign on the right**
    
    ![Untitled](How%20to%20fill%20out%20the%20Memberships%20WG%20in%20the%20Council%20/Untitled%203.png)
    
    **Enter the result into the Council Network Summary**