# Channels created in term

Created: May 9, 2022 8:32 PM
Description: Get all channels created in Council Term
Tags: Channels, Content Directory

```graphql
query NewChannels($councilStartBlock: Int!, $councilEndBlock: Int!) {
  channels(where: {createdInBlock_gt: $councilStartBlock, createdInBlock_lte: $councilEndBlock}, limit: 1000) {
    createdInBlock
    title
    id
    isPublic
    isCensored
  }
}
```