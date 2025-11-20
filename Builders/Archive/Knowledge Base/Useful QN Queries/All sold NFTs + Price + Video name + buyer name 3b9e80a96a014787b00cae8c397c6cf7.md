# All sold NFTs + Price + Video name + buyer name

Created: January 16, 2023 5:56 AM
Tags: NFTs, Videos

```jsx
query MyQuery {
  nftBoughtEvents(orderBy: inBlock_ASC) {
    id
    inBlock
    member {
      handle
    }
    memberId
    price
    type
    videoId
    video {
      title
      nftId
      nft {
        id
      }
    }
  }
}
```