# Category Score

Group: Forum
JSG Grading Status: Completed
Score: 0.5
Grade Name: CATEGORY_SCORE
Spot Check Completed: No

Option 2 chosen.

“Which, if any, categories or subcategories should be deleted or moved”

- Not addressed, but not clear if their should be either.

“Which, if any, threads should be moved”

- Not addressed, but not clear if their should be either.

“Implement the new category system, without deleting any threads or posts.”

- Done

One problem found was that category “Community” was never created. This technically violates:

- “are not implemented exactly as approved (without technical reasons) before the end of the term”

~~However, it seems to strict for “just” forgetting one.~~

Reason:

`There are no way to update Category on Forum. Tried to replace “Discussion Category” for “Community Category”. Unfortunately this action now is unavailable.`

Both title and description can be replaced (it may not to wise to do so though).

Still, this was why:

```markdown
- Which, if any, categories or subcategories should be deleted or moved
- Which, if any, threads should be moved
```

was asked

`CATEGORY_SCORE=0.5`

---

### Notes

With the runtime upgrade at block `#697,500`, 
we know have gone from 20 to 40 max categories. This means we can 
implement the previously designed system, or a new better one.

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