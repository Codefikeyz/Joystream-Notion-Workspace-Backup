# Category Score

Group: Forum
Score Status: Not Completed
Score: 0
Reports Gathered: No
Grade Name: CATEGORY_SCORE
Handover Weight: 1
Builder Weight: 4
Spot Check Completed: No
Content Weight: 2
Distributor Weight: 3
Forum Weight: 1
HR Weight: 4
Lead Opportunities Weight: 1
Marketer Weight: 0
Marketing Weight: 0
Plan Weight: 1
Property 1: 2
Property 2: 4
Scoring Weights: Council 7 (../../Council%207%207f116be5a8f54180abd97510bc5cfbc7.md)
Storage Weight: 3
Summary Weight link: 1

No categories created, and no indication of proposals.

### Notes

With the runtime upgrade scheduled for block `#697,500`, we are going from 20 to 40 max categories. This means we can implement the previously designed system, or a new better one.

There are multiple tasks associated with this metric:

1. OPTIONAL: If the old, previously approved, system is found lacking, design a new system of categories and sub-categories.
2. Get an proposal for a/the new category system approved by the
Council. If a "brand" new system is designed, the proposal must include a design brief to explain the reasoning behind it. Regardless, it must
include a an overview of:
    - Which, if any, categories or subcategories should be deleted or moved
    - Which, if any, threads should be moved
3. Implement the new category system, without deleting any threads or posts.

### Scoring Calculations

If the changes made

- are not approved by the council
- are not implemented exactly as approved (without technical reasons) before the end of the term
- ends up permanently deleting any post or thread

the score is automatically zero.

To get a full score, the changes must be completed before:

`max[council_approval_block+14400 , runtime_upgrade_block + 28800]`

If completed after the block above, but before the council
 terms ends, the score will be linear from 1 to 0 (assuming no other 
violations).