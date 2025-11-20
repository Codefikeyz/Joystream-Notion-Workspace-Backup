# Report ⚡Term 17

### Activity Summary

This week our Working Group served indeed purpose and deliver all the tasks which we plan.

What we’ve done:

- created the page with all existing categories;
- reviewed threads and posts on forum;
- moderated threads and posts on forum;.
- moved threads and replaced categories if needed;
- started creating the guide for deputy lead.

### **Forum statistics**

| How many threads were created | 90 |
| --- | --- |
| How many threads were deleted | 2 |
| How many posts were created  | 43 |
| How many posts were deleted | 17 |
| How many posts exists* | 1187 |

*Value obtained by running the following query:

```graphql
query AllExistingPosts($councilEndTimeStamp: DateTime!) {
  forumPosts(limit: 100000, where: {createdAt_lte: $councilEndTimeStamp}) {
    id
  }
}

{
  "councilEndTimeStamp": 1657673292000
}
```

### **Statistic for each Category**

How many threads exists in each Category?

How many threads was created during the last scoring period?

| Category | Total Threads | Creating During Term |
| --- | --- | --- |
| Bounties  | 96 | 6 |
| Content Creators | 16 | 1 |
| Validators | 2 | 0 |
| Discussions | 17 | 0 |
| Help & Support  | 10 | 0 |
| Creatives | 16 | 4 |
| Marketing | 37 | 17 |
| Bounty Suggestions | 4 | 0 |
| Finished Bounties  | 2 | 0 |
| Council Reports | 35 | 5 |
| Budget | 4 | 0 |
| Pre-Proposal Discussion | 26 | 1 |
| Problems & Failures | 1 | 0 |
| Governance | 0 | 0 |
| Development  | 9 | 2 |
| Atlas Feedback | 3 | 1 |
| Education | 16 | 0 |
| Grants/Funding | 25 | 23 |
| Lounge | 21 | 10 |
| Working Groups | 0 | 0 |
| Forum Working Group  | 35 | 2 |
| Content Working Group | 36 | 4 |
| Builders Working Group  | 28 | 1 |
| Storage Providers Working Group | 32 | 3 |
| Marketing Working Group | 35 | 3 |
| Distribution Working Group | 30 | 4 |
| HR Working Group | 36 | 3 |
| Forum Structure | 0 | 0 |

### **Charts showing the forum history over time**

Threads and posts made since genesis 

![Screenshot 2022-08-02 at 15.46.24.png](Report%20%E2%9A%A1Term%2017/Screenshot_2022-08-02_at_15.46.24.png)

### **A summary of all `forum` (except regular posting) transactions made by the group, who made it, and why, eg.**

Moderation of threads

| Thread ID | Made by | Reason | Block |
| --- | --- | --- | --- |
| 497 | Black_fish | duplicate thread | 1779984 |

Moderation of posts

| Post ID | Made by | Reason | Block |
| --- | --- | --- | --- |
|  |  |  |  |

Threads moved

| Thread ID | Block | Made by | Reason | Old Category | New Category |
| --- | --- | --- | --- | --- | --- |
| 508 | 1745519 | songoku | wrong category | 28 | 1 |
| 525 | 1763141 | songoku | wrong category | 1 | 29 |
| 508 | 1763215 | songoku | wrong category | 1 | 28 |
| 380 | 1763237 | songoku | wrong category | 1 | 29 |
| 499 | 1765424 | songoku | wrong category | 1 | 29 |
| 511 | 1765919 | songoku | wrong category | 1 | 29 |
| 487 | 1765964 | songoku | wrong category | 1 | 29 |
| 481 | 1766020 | songoku | wrong category | 1 | 29 |
| 502 | 1776966 | songoku | wrong category | 1 | 18 |
| 503 | 1776993 | songoku | wrong category | 1 | 18 |
| 495 | 1777001 | songoku | wrong category | 1 | 18 |
| 537 | 1777031 | songoku | wrong category | 1 | 29 |
| 504 | 1777041 | songoku | wrong category | 1 | 18 |
| 500 | 1777063 | songoku | wrong category | 1 | 25 |
| 501 | 1777070 | songoku | wrong category | 1 | 18 |
| 471 | 1779262 | songoku | wrong category | 1 | 18 |
| 486 | 1779290 | songoku | wrong category | 1 | 18 |
| 492 | 1779308 | songoku | wrong category | 1 | 18 |
| 459 | 1779323 | songoku | wrong category | 1 | 18 |
| 462 | 1779422 | songoku | wrong category | 1 | 18 |
| 470 | 1779449 | songoku | wrong category | 1 | 18 |
| 419 | 1779472 | songoku | wrong category | 1 | 29 |
| 380 | 1779486 | songoku | wrong category | 29 | 1 |
| 224 | 1779516 | songoku | wrong category | 1 | 29 |
| 260 | 1779577 | songoku | wrong category | 1 | 18 |
| 428 | 1789474 | songoku | wrong category | 1 | 29 |
| 483 | 1789495 | songoku | wrong category | 1 | 29 |
| 484 | 1789521 | songoku | wrong category | 1 | 29 |
| 414 | 1789531 | songoku | wrong category | 1 | 29 |
| 431 | 1789543 | songoku | wrong category | 1 | 29 |
| 397 | 1789566 | songoku | wrong category | 1 | 29 |
| 505 | 1789580 | songoku | wrong category | 30 | 29 |
| 319 | 1789594 | songoku | wrong category | 1 | 29 |
| 400 | 1789605 | songoku | wrong category | 1 | 29 |
| 369 | 1789626 | songoku | wrong category | 1 | 29 |
| 152 | 1789865 | songoku | wrong category | 1 | 30 |
| 519 | 1790175 | songoku | wrong category | 28 | 18 |
| 538 | 1790205 | songoku | wrong category | 28 | 29 |
| 318 | 1790221 | songoku | wrong category | 28 | 32 |
| 369 | 1790239 | songoku | wrong category | 1 | 2 |
| 260 | 1790253 | songoku | wrong category | 18 | 32 |
|  557 | 1794726 | songoku | wrong category | 1 | 29 |
| 563 | 1814030 | songoku | wrong category | 28 | 29 |
| 566 | 1815760 | songoku | wrong category | 28 | 29 |
| 561 | 1815796 | songoku | wrong category | 28 | 29 |
| 562 | 1815807 | songoku | wrong category | 28 | 29 |
| 556 | 1815814 | songoku | wrong category | 28 | 29 |
| 559 | 1815828 | songoku | wrong category | 28 | 30 |
| 567 | 1815839 | songoku | wrong category | 1 | 29 |
| 565 | 1815846 | songoku | wrong category | 1 | 29 |
| 348 | 1815861 | songoku | wrong category | 1 | 2 |
| 341 | 1815875 | songoku | wrong category | 1 | 2 |
| 284 | 1815893 | songoku | wrong category | 1 | 30 |
| 579 | 1834225 | songoku | wrong category | 1 | 29 |
| 575 | 1834231 | songoku | wrong category | 1 | 29 |
| 587 | 1862466 | songoku | wrong category | 1 | 29 |
| 578 | 1862492 | songoku | wrong category | 28 | 29 |
| 577 | 1862510 | songoku | wrong category | 28 | 29 |
| 576 | 1862519 | songoku | wrong category | 28 | 29 |

Categories changed 

| Category ID | Made by | Reason | Block |
| --- | --- | --- | --- |
|  |  |  |  |

Categories deleted

| Category ID | Made by | Reason | Block |
| --- | --- | --- | --- |
|  |  |  |  |

Categories Created

| Category ID | Made by | Reason | Block |
| --- | --- | --- | --- |
|  |  |  |  |
|  |  |  |  |

Category Archival Status Updated 

| Category ID | Made by | Reason | Block | New Archival Status |
| --- | --- | --- | --- | --- |
|  |  |  |  |  |

Category Moderator Updated

| Category ID | Made by | Reason | Block | Moderator |
| --- | --- | --- | --- | --- |
| 30 | secret_girl | access for Forum Moderator | 1775339 | songoku |
| 18 | secret_girl | access for Forum Moderator | 1775343 | songoku |
| 33 | secret_girl | access for Forum Moderator | 1839165 | Counsellor |

Sticky Thread Changes