# NFT bids

Created: February 15, 2023 7:13 AM
Tags: NFTs, auctions, bids

```jsx
query MyQuery {
  bids(limit: 1000) {
    id
    amount
    bidder {
      handle
    }
    bidderId
    nft {
      id
      video {
        title
      }
    }
    createdAt
  }
}
```