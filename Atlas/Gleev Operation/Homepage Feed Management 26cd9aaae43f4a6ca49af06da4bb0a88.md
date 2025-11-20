# Homepage Feed Management

Homepage feed on Gleev is managed by the concept of video relevancy score ®. The relevancy score is contained in Orion. Gleev query for homepage displays all videos in descending order based on the relevancy score R, which is periodically recalculated in Orion. 

Recalculation of relevancy score is triggered by the increase to a certain fixed increment that is defined in config of:
- comments
- video views
- reactions

## Video Relevancy Forumula

```
R = ((N * -A) + (B * views_num) + (C * comments_num) + (D * reactions_num))*CW
```

Where 

`N` =  newness

`N = (E * days_since_published_on_gleev + F * days_since_published_on_yt) / (E + F)`

A..F are float numbers (have decimals, e.g. 1.56)

```
 newnessWeight: A,
    viewsWeight: B,
    commentsWeight: C,
    reactionsWeight: D,
    joysteamTimestampSubWeight: E,
    ytTimestampSubWeight: F
```

`CW` = channel Weight, Float (number with decimals)

when CW <1, this would decrease channel score

when CW>1, this would increase channel score

## Current Parameters

<aside>
💡 
The parameters of the above formula can be changed via mutation in Orion

Current parameters are set to:
A=1.5
B=0
C=0
D=0
E=0.3
F=0.7

</aside>

## How to set individual channel weights

<aside>
💡 Examples below are based on the Postman App to send HTTP requests to Orion (backend) Make sure to download it using the link below

</aside>

[Download Postman | Get Started for Free](https://www.postman.com/downloads/)

- To use this mutation User should either be a Root gateway user or an operator with `SET_CHANNEL_WEIGHTS` permission.
- The gateway user first needs to be authorized using Orion Auth API's `/anonymous-auth` endpoint

### How to authorize

Request type: POST
Endpoint URL: [https://orion.gleev.xyz/api/v1/anonymous-auth](https://orion.gleev.xyz/api/v1/anonymous-auth)
Body:

```
{
    "userId": "hereGoesAuthenticatedUserID"
}
```

So the part “heregoes..” needs to be replaced with the real userID 

<aside>
💡 👆 **userID can be obtained from `@zeeshanakram` on discord.**

</aside>

**Hit Send**

Once sent, you will get the `session_id` value in the cookies tab of the response, you need to copy it (see bottom of the screenshot)

![Untitled](Homepage%20Feed%20Management/Untitled.png)

This session ID will need to be included to the request header for changing the weights of individual channels

### How to set individual channel weights

Request type: POST
Endpoint URL: [https://orion.joystream.org/graphql](https://orion.joystream.org/graphql)
Headers: Add `Cookie` as new header Key, and add `session_id=*`instead of `*` post the session ID you copied in the previous step above.

![Screenshot 2023-11-15 at 16.29.19.png](Homepage%20Feed%20Management/Screenshot_2023-11-15_at_16.29.19.png)

Body: use the snippet below, but replace the IDs with IDs of channels you want to update the weights for

```
mutation MyMutation {
  setChannelsWeights(inputs: [{channelId: "10225", weight: 1.5}, {channelId: "10226", weight: 2.5}]) {
    channelId
    isApplied
  }
}
```

In postman app, that would look like so:

![Screenshot 2023-11-15 at 16.32.30.png](Homepage%20Feed%20Management/Screenshot_2023-11-15_at_16.32.30.png)

The successful response should be looking like so

![Screenshot 2023-11-15 at 16.35.28.png](Homepage%20Feed%20Management/Screenshot_2023-11-15_at_16.35.28.png)

### Suggested Weights  for channels with different tiers

Silver = 2-3 (higher for better diamond channels) 

Gold = 3-4 (higher for better diamond channels) 

Diamond = 4-5 (higher for better diamond channels) 

<aside>
💡 The video relevance scores are updated every 1 hour, so it might take max of 1 hr for weights to take effect

</aside>

## How to change overall formula for relevancy of the videos

Via  mutation in Orion, using the same authorisation via sessnio_id  as explained above. 

Below is the example of query:

```
mutation SetVideoWeights {
  setVideoWeights(
      commentsWeight: 0.0, joysteamTimestampSubWeight: 0.3, newnessWeight: 1.5, 
      reactionsWeight: 0.0, 
      viewsWeight: 0, 
      ytTimestampSubWeight: 0.7) {
    isApplied
  }
}
```

And this is how it looks like in Postman, for successfull response

![Screenshot 2023-11-01 at 16.12.05.png](Homepage%20Feed%20Management/Screenshot_2023-11-01_at_16.12.05.png)

## How to affix selected videos to the top of the page

issue: [https://github.com/Joystream/orion/issues/303](https://github.com/Joystream/orion/issues/303)). 

The operators can use `setOrUnsetPublicFeedVideo` to include the videos in the public feed, e.g.

```
mutation MyMutation {
  setOrUnsetPublicFeedVideos(
      (operation: SET, videoIds: ["1", "2"])) {
    numberOfEntitiesAffected
  }
}
```

## How to check which videos are included in Homepage Feed

```
{
  videos(where: {includeInHomeFeed_eq:true}) {
    id
    title
		relevancyScore
  }
}
```

## How to check which language does the video have in Orion

```
# Get video by ID
{
  videoById(id: "paste_here_ID"){
    id
    title
    orionLanguage
  }
}

# Get videos by channel ID
{
  videos(where:{channel: {id_eq: "channel_id"}}) {
    id
    title
    orionLanguage
  }
}
```