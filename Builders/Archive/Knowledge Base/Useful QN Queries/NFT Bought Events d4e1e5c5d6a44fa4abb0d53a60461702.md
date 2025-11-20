# NFT Bought Events

Created: July 13, 2023 11:34 PM

```jsx
query MyQuery {
  nftBoughtEvents(limit: 1000) {
    id
    price
    videoId
    video {
      title
    }
  }
}
```