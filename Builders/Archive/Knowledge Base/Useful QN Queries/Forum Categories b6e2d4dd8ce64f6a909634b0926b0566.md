# Forum Categories

Created: May 9, 2022 8:27 PM
Description: List all forum categories (including deleted categories)
Tags: Categories, Forum

```graphql
query {forumCategories{id,createdAt,deletedAt,parentId,status{__typename}}}
```