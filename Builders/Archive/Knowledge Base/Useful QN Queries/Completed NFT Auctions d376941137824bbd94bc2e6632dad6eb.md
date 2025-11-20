# Completed NFT Auctions

Created: July 13, 2023 11:25 PM

```jsx
query MyQuery {
  auctions(limit: 1200, where: {isCompleted_eq: true}) {
    id
    isCompleted
    topBid {
      amount
      nft {
        video {
          title
        }
        lastSalePrice
        lastSaleDate
      }
    }
    auctionType {
      ... on AuctionTypeEnglish {
        __typename
        duration
        extensionPeriod
        minimalBidStep
        plannedEndAtBlock
      }
      ... on AuctionTypeOpen {
        __typename
        bidLockDuration
      }
    }
    winningMemberId
    winningMember {
      handle
    }
    startsAtBlock
    startingPrice
    endedAtBlock
    buyNowPrice
    nft {
      creatorRoyalty
    }
  }
}
```