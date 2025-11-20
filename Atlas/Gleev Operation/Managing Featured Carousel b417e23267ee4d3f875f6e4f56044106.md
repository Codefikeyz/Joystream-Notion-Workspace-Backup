# Managing Featured Carousel

## Initial setup

1. Open Postman and provide the correct URL
- dev: [https://atlas-dev.joystream.org/orion-v2/graphql](https://atlas-dev.joystream.org/orion-v2/graphql)
- production: [https://orion.joystream.org/graphql](https://orion.joystream.org/graphql)
1. Change the HTTP method to POST
2. Go to the header tab and provide `x-operator-secret` header (ask me for the key if you don’t have it). This will allow you to read all the hidden queries and do all mutations that are not possible for regular users.
3. Then go to the body, switch radio buttons above the text field to GraphQL, and start writing queries and mutations.

## Get featured NFTs requests

```graphql
query {
    nftFeaturingRequests(orderBy: timestamp_DESC) {
        id
        nftId
        timestamp
        rationale
    }
}

```

## Get currently featured NFTs

```graphql
query {
    ownedNfts(where: {
        isFeatured_eq: true
    }) {
        id
        video {
            title
            duration
            createdAt
            viewsNum
            # ...other fields, if you want more information about the video
            channel {
                title
            }
        }
    }
}

```

## Set featured NFTs

```graphql
mutation  {
    setFeaturedNfts(featuredNftsIds: ["nftOrVideoId1", "nftOrVideoId2"]) {
        newNumberOfNftsFeatured
    }
}

```

**One important note -** you can only set an array of ids, and once you set them all the previously featured NFTs will be overwritten. For example, if you run:

```graphql
mutation {
    setFeaturedNfts(featuredNftsIds: ["1", "2"]) {
        newNumberOfNftsFeatured
    }
}

```

and then

```graphql
mutation {
    setFeaturedNfts(featuredNftsIds: ["3", "4"]) {
        newNumberOfNftsFeatured
    }
}

```

The featured NFTs will be only “3” and “4”.

If you want to add featured NFTs to existing ones you need to provide all the ids, so in the case above, you would have to write this mutation:

```graphql
mutation {
    setFeaturedNfts(featuredNftsIds: ["1", "2", "3", "4"]) {
        newNumberOfNftsFeatured
    }
}

```

I created an issue [https://github.com/Joystream/atlas/issues/4161](https://github.com/Joystream/atlas/issues/4161) to make this more flexible, but for now, this is how it works.

If you want to **reset** featured NFTs, provide an empty array:

```graphql
mutation  {
    setFeaturedNfts(featuredNftsIds: []) {
        newNumberOfNftsFeatured
    }
}

```