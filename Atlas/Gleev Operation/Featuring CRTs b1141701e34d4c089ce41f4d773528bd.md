# Featuring CRTs

## Overview

Creator tokens marketplace supports featuring of selected tokens

The bottom carousel supports featuring up to 10 tokens at the time
The top carousel only shows featured CRTs **only** ⚠️ with video trailers uploaded to Edit token page by channels. 

The GUI explains to creators that they need to become “Token Expert” before the token can be featured. 

”Token Expert” status is granted to all tokens / channels which have done all of the following:

- Edited token description (or benefits or uploaded trailer)
- Opened AMM market
- Started at least one revenue share

## How to obtain list of channels with “token expert” status

Use this GraphQL query

```jsx
{
  creatorTokens(where:{
  
    OR: [
      {
            description_not_eq: "",
        revenueShares_some:{
              startingAt_gt: 0,
            },
            ammCurves_some: {
              ammSlopeParameter_gt: 0
            },
      },
      {
        benefits_some: {
          title_not_eq: ""
        },
        revenueShares_some:{
              startingAt_gt: 0,
            },
            ammCurves_some: {
              ammSlopeParameter_gt: 0
            },
      },
       {
        trailerVideo_some: {
          id_isNull: false
        },
        revenueShares_some:{
              startingAt_gt: 0,
            },
            ammCurves_some: {
              ammSlopeParameter_gt: 0
            },
      }
    ]
  }) {
    id
    # revenueShares {
    #   id
    # }
    # ammCurves {
    #   id
    # }
    # description
    # benefits {
    #   title
    # }
    channel {
      channel{
        title
      }
    }
  }
}
```

## How to feature CRTs

⚠️ NB: Minimum 4 tokens need to be featured to enable the carousel

The mechanics is exactly the same as featuring NFTs. Below is example of mutation for creator tokens. Same endpoint and authorisation rules as featuring NFTs apply. 

```
mutation MyMutation {
  setFeaturedCrts(featuredCrtsIds: ["18", "14","36"]) {
    newNumberOfCrtsFeatured
  }
}
```