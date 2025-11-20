# Videos created in term

Created: May 9, 2022 8:31 PM
Description: Get all videos created in Council Term
Tags: Content Directory, Videos

```graphql
query NewVideos($councilStartBlock: Int!, $councilEndBlock: Int!) {
  videos(where: {createdInBlock_gt: $councilStartBlock, createdInBlock_lte: $councilEndBlock}, limit: 1000) {
		id 
    title
    createdInBlock
    channelId
    categoryId
    isCensored
    isExplicit
    isFeatured
    isPublic
  }
}
```