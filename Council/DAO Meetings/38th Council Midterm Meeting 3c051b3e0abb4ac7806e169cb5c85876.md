# 38th Council Midterm Meeting

Agenda: Agenda:
- Tech development roadmap and update
Tags: Gleev, Roadmap, Tools, YPP, builders, development
Date: October 16, 2024
Venue: Community Voice 1 channel
Status: Done
Facilitator: Leet_joy
Duration: < 1 hour
Moderator: leet_joy
Attendance: Lezek
Freakstatic
Leetjoy
Codefikeyz
Vikan
Spat_sochi
Genius
Ilich
Thegrimsavage
Transcript: N/A

### **Meeting Notes: Development Priorities and Updates**

### **1. SDK Development**

- Objective:
    - Build a basic SDK to abstract common functions used across Joystream applications (e.g., Atlas, Pioneer, CLI). This will benefit internal teams and external builders by reducing complexity.
    - The SDK would help keep codebases clean by centralizing shared functionalities.
- Challenges:
    - Determining the core functionalities to include in the v1 will require research.
    - Suggestions were made to extract the most frequently used features from existing apps.
    - There’s value in gathering feedback from builders on what they would find most useful in an SDK, but access to these external builders is limited at the moment.
- Priority and Timeline:
    - This task has been postponed to next quarter (Q1 ‘24) due to the complexity and high effort required.
    - Lezek confirmed that the longer timeframe was based on the assumption that he would be the sole contributor. Adding more developers would speed up the process.

### **2. Gated Content (CRT/NFT-based)**

- Overview:
    - Goal: Implement functionality to allow creators to gate videos behind creator tokens (CRT) or NFTs, ensuring only eligible users can access the content.
    - Users could either buy an NFT or hold specific creator tokens to unlock premium content.
- Challenges:
    - Design Complexity: The UI implementation, especially for Atlas, is challenging due to the need for seamless integration with authentication processes. No current designs are ready for this feature.
    - Performance Considerations: Authentication must be efficient to prevent delays when users try to access gated content.
    - Dependencies: The success of this feature depends heavily on how the authentication mechanism is implemented in the platform.
- Discussion:
    - Lezek noted that simpler alternatives like subscriptions or pay-per-view models might be easier to implement initially.
    - CRT and NFT-based access models are less familiar to users and could cause confusion.
    - Suggestion: Focus first on building a manual subscription or pay-per-view system and explore CRT/NFT-based gating later.

### **3. Creator Token Issuance Caps**

- Problem:
    - Creators currently have no way to limit the total supply of their tokens. New tokens can always be minted via AMM operations, even after an initial supply is set.
    - This lack of control creates uncertainty for creators who wish to manage their token issuance, similar to the capped issuance models used by Bitcoin.
- Proposed Solution:
    - Introduce an issuance cap feature that allows creators to define a maximum supply for their tokens.
    - Even after a public sale, there needs to be a mechanism to prevent new tokens from being minted through AMMs.
- Discussion:
    - Challenge: Implementing issuance caps will require a runtime upgrade, as it is not currently possible to restrict token creation after an AMM is opened.
    - This feature aligns with upcoming public sales on Gleev and could provide creators with better tools for token management.

### **4. YouTube Sync Feature**

- Status:
    - This feature aimed to allow creators to sync their YouTube content with Joystream automatically.
    - However, API access restrictions have made this feature impractical.
- Discussion:
    - Zeesshan reported that public API limitations might make it impossible to implement the feature without using the user authentication API.
    - The issue is not currently a high priority, as creators have not raised concerns about syncing YouTube content or expressed fear of account bans.

### **5. Storage & Content Distribution Improvements**

- Objective:
    - Implement an efficient storage and distribution system for Joystream, ensuring users with valid roles can access the right content without delays.
    - This involves significant updates to various apps and nodes, including Argus, Colossus, Atlas, Orion, and Query Nodes.
- Challenges:
    - Role Complexity: Users can have hundreds of dynamic roles across channels, making authentication and authorization difficult.
    - Solution: A new lit-auth node will manage role-based access, issuing tokens that verify user permissions. Atlas will use these tokens to request content from Argus.

---

### **6. Fiat On-Ramp Integration**

- Overview:
    - Joystream is considering integrating with Guardarian to allow users to buy creator tokens, NFTs, and JOY with credit cards.
    - Guardarian offered a discounted price of $5K for this integration.
- Discussion:
    - While the technical work is minimal, it’s essential to evaluate whether there will be enough demand to justify the cost.
    - There are concerns about country-specific restrictions, which could limit adoption.

### **7. Transcoding Support**

- Objective:
    - Improve the video upload process by introducing transcoding to optimize storage and ensure compatibility across devices.
    - This feature will prevent large, unoptimized video files from slowing down streaming.
- Challenges:
    - Some creators upload videos that are too large or in formats incompatible with mobile viewing, negatively impacting the viewing experience.
    - Implementation: Videos will need to be uploaded through Orion instead of directly to Colossus, requiring changes in Atlas and other apps.
- Discussion:
    - Lezek mentioned that Klaudiusz has made some progress with a proof of concept, which could serve as a starting point for implementation.

### **Action Items and Next Steps**

1. **SDK Development:** Postponed to Q1; Lezek to update the roadmap.
2. **Gated Content:** Explore pay-per-view and subscription models first.
3. **Token Issuance Caps:** Add to backlog for future runtime upgrades.
4. **YouTube Sync:** On hold due to API limitations.
5. **Storage Improvements:** Schedule a follow-up call to finalize the approach.
6. **Fiat On-Ramp:** Evaluate Guardarian’s country support and demand.
7. **Transcoding:** Follow up with Klaudiusz and plan the next steps.

---

### **End of Session.**