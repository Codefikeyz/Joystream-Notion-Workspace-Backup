# Report ⚡Term 18

### Activity Summary

This week our Working Group served indeed purpose and deliver all the tasks which we plan.

What we’ve done:

- created the page with all existing categories;
- reviewed threads and posts on forum;
- moderated threads and posts on forum;.
- moved threads and replaced categories if needed;
- created guide: how to make summary for deputy lead

### **Forum statistics**

| How many threads were created | 66 |
| --- | --- |
| How many threads were deleted | 0 |
| How many posts were created  | 59 |
| How many posts were deleted | 23 |
| How many posts exists* | 1313 |

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
| Bounties  | 95 | 0 |
| Content Creators | 18 | 2 |
| Validators | 2 | 1 |
| Discussions | 18 | 0 |
| Help & Support  | 10 | 0 |
| Creatives | 11 | 2 |
| Marketing | 51 | 10 |
| Bounty Suggestions | 5 | 1 |
| Finished Bounties  | 2 | 0 |
| Council Reports | 40 | 5 |
| Budget | 4 | 0 |
| Pre-Proposal Discussion | 27 | 1 |
| Problems & Failures | 1 | 0 |
| Governance | 0 | 0 |
| Development  | 9 | 0 |
| Atlas Feedback | 3 | 0 |
| Education | 16 | 0 |
| Grants/Funding | 24 | 0 |
| Lounge | 34 | 20 |
| Working Groups | 0 | 0 |
| Forum Working Group  | 39 | 4 |
| Content Working Group | 39 | 4 |
| Builders Working Group  | 29 | 2 |
| Storage Providers Working Group | 34 | 3 |
| Marketing Working Group | 38 | 3 |
| Distribution Working Group | 31 | 4 |
| HR Working Group | 39 | 3 |
| Forum Structure | 0 | 0 |

### **Charts showing the forum history over time**

Threads and posts made since genesis 

![Screenshot 2022-08-10 at 15.43.27.png](Report%20%E2%9A%A1Term%2018/Screenshot_2022-08-10_at_15.43.27.png)

### **A summary of all `forum` (except regular posting) transactions made by the group, who made it, and why, eg.**

Moderation of threads

| Thread ID | Made by | Reason | Block |
| --- | --- | --- | --- |
| 522 | songoku | test thread | 1931264 |

Moderation of posts

| Post ID | Made by | Reason | Block |
| --- | --- | --- | --- |
|  |  |  |  |

Threads moved

| Thread ID | Block | Made by | Reason | Old Category | New Category |
| --- | --- | --- | --- | --- | --- |
| 607 | 1883143 | Counsellor | wrong category | 25 | 19 |
| 586 | 1883346 | Counsellor | wrong category | 33 | 1 |
| 574 | 1884282 | Counsellor | wrong category | 33 | 1 |
| 581 | 1884399 | Counsellor | wrong category | 33 | 1 |
| 627 | 1892735 | songoku | wrong category | 28 | 18 |
| 624 | 1892792 | songoku | wrong category | 28 | 29 |
| 619 | 1892811 | songoku | wrong category | 28 | 18 |
| 603 | 1892899 | songoku | wrong category | 28 | 2 |
| 602 | 1892927 | songoku | wrong category | 28 | 29 |
| 583 | 1898837 | Counsellor | wrong category | 33 | 23 |
| 649 | 1931292 | songoku | wrong category | 28 | 29 |
| 628 | 1931297 | songoku | wrong category | 28 | 29 |
| 636 | 1931303 | songoku | wrong category | 28 | 29 |
| 635 | 1931309 | songoku | wrong category | 28 | 29 |
| 601 | 1931316 | songoku | wrong category | 28 | 29 |
| 637 | 1931327 | songoku | wrong category | 28 | 29 |
| 600 | 1931337 | songoku | wrong category | 28 | 29 |
| 596 | 1931343 | songoku | wrong category | 28 | 29 |
| 657 | 1973414 | songoku | wrong category | 28 | 29 |
| 653 | 1973433 | songoku | wrong category | 28 | 29 |
| 651 | 1973442 | songoku | wrong category | 28 | 29 |
| 656 | 1973453 | songoku | wrong category | 1 | 29 |

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
| 33 | secret_girl | access for Forum Moderator | 1877640 | Counsellor |
| 30 | secret_girl | access for Forum Moderator | 1877652 | advo |
| 1 | secret_girl | access for Forum Moderator | 1877657 | Counsellor |
| 25 | secret_girl | access for Forum Moderator | 1877666 | advo |
| 33 | secret_girl | access for Forum Moderator | 1878104 | Counsellor |
| 1 | secret_girl | access for Forum Moderator | 1878154 | Counsellor |
| 25 | secret_girl | access for Forum Moderator | 1878388 | Counsellor |
| 19 | secret_girl | access for Forum Moderator | 1878395 | Counsellor |
| 33 | secret_girl | access for Forum Moderator | 1896110 | Counsellor |
| 23 | secret_girl | access for Forum Moderator | 1897085 | Counsellor |

Sticky Thread Changes

| Category ID | Made by | Reason | Block | New Archival Status |
| --- | --- | --- | --- | --- |
|  |  |  |  |  |