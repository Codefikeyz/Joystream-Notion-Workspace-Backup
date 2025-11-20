# Dicord Modification

# Problem

---

Our current Discord onboarding process allows new users to select from the following roles:

- **Aspiring Earner**
- **Aspiring Developer**
- **Aspiring Creator**
- **Aspiring Community Worker**
- **Aspiring Server Engineer**

Once a role is chosen, users gain unrestricted access to all channels within the server. Additionally, other roles are assigned either manually or through on-chain verification.

This open access creates several challenges:

1. **Potential for Spam:** Users can exploit full access to post irrelevant content across multiple channels.
2. **Security Risks:** Members are vulnerable to phishing attempts and other malicious activities if scammers infiltrate the server.
3. **Reduced User Experience:** Unchecked spam and clutter can discourage valuable participation and overwhelm legitimate users.

To address these risks, we need a more structured approach that limits initial access and ensures better moderation without compromising engagement.

# Objective

The primary goal of this modification is to **reduce spam** and **minimize inactive channels** within the Discord server. Streamlining channel access ensures members can focus on active, relevant conversations without being overwhelmed. By fostering a more organized environment, we enhance user experience, prevent important messages from getting lost in clutter, and encourage meaningful engagement. This "less is more" approach will help members stay connected and active where it matters most.

# Execution

### Channel Access Restriction:

The adjustments in the table below are to be implemented for the listed roles:

- aspiring earner
- aspiring developer
- aspiring creator
- aspiring community worker
- aspiring server engineer

| Server Category | Channels | Permissions | Adjustments |
| --- | --- | --- | --- |
| **Events** | All | Read and write |  |
| **Getting Started** | All | Read only (Default) |  |
| **Discussion** | All | Read and write |  |
| **Creator-Community** | All | Read only | #Creator-support & #suggestion-box: Read and write |
| **Creator-Rewards** | All | Read only |  |
| **DAO** | All | Read only |  |
| **Work** | All | Read only |  |
| **Targeted Announcements** | All | Read only (Default) |  |

The server categories above should have all the channels set with the permissions indicated in same column, specifically for the Discord roles listed above. 

## NOTE

The roles below should have READ and WRITE access to the channels in the table above:

- Jsgenesis
- Community Mod
- Council members
- DAO
- Founding member
- Marketing lead
- HR Lead
- HR workers
- Builder lead
- Content lead
- Distribution lead
- Forum lead
- Storage lead
- Apps lead
- Membership lead
- WG leads
- Builder workers
- Content workers
- Distribution workers
- Forum workers
- Storage workers
- Marketing workers
- App worker
- Membership worker
- YPP
- Treasury multisig
- EthAdmin multisig
- JoyOp Multisig
- On-chain identity verified
- Ambassador (n/s)
- Creator community Admin (n/s)
- Creators (n/s)
- Gleev creator (n/s)

**I am uncertain of the process for assigning the ones marked (n/s)**

### Channel Cleanup:

There are several inactive or rarely used channels in the server, we can archive them In any case a use for them arises in future.

**Channels to be archived:**

- #Bridges
- #intros
- #hangout
- #wiki
- #suggestion box
- #rewards
- #X-followers
- #discord-joiners
- #survey-rewards
- #treasury-budgeting
- #Council-notion log
- #Council work
- #Roadmap-and-okrs

The **Archived** category should be set to **"Read-Only"** for discord admins, ensuring that no other members can view or interact with the archived channels.