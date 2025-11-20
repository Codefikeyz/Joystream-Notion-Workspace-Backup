# NFTs + sale information

Created: February 1, 2023 6:20 AM
Tags: NFTs, Videos

```jsx
query MyQuery {
  nftIssuedEvents(limit: 1000) {
    id
    royalty
    inBlock
    metadata
    videoId
    video {
      nft {
        lastSalePrice
        lastSaleDate
        video {
          title
        }
      }
      nftId
    }
  }
}
```