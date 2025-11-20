# Featured content in Atlas

![Hero-9e23d1bf1a90b1721ad0fca5008bc620.png](Featured%20content%20in%20Atlas/Hero-9e23d1bf1a90b1721ad0fca5008bc620.png)

## **Intro**

Atlas mostly relies on blockchain state to display content. However, there are some parts of Atlas that are intended to be controlled by Gateways in the future. To start moving in this direction, some of Atlas content is controlled by Orion (future Gateway Node). This currently includes:

- Video hero (full-width video banner displayed on the home page)
- Featured videos for each video category (accessible via `Discover` view)

## **Community process**

### **Actors**

- *Content curators* - members of the community responsible for preparing suggestions of new featured content
- *Content admin* - member of the community with required credentials, responsible for making requests to update featured content. They act based on input from *content curators*
- *Reviewer* - optional actor from JSG responsible for approving some types of featured content

### **General process**

In general the process for updating the featured content will look as follows:

1. *Content curators* prepare ideas for new featured content. This includes preparing metadata according to the [structure below](https://github.com/Joystream/atlas/blob/master/docs/community/featured-content.md#metadata-structure) and preparing any necessary assets (video cuts, posters, etc.)
2. Optionally, if video hero is affected, video hero propositions should be sent to the *reviewer* for approval
3. Once all content is ready and optionally approved, *content curators* should send all required metadata and assets to the *content admin*
4. *Content admin*, using their credentials, makes assets publicly accessible and updates the featured content in Orion
5. Changes are live in Atlas

**Get your keys to work!**

<aside>
💡 S3 vault access key:
S3 vault secret key:
Orion Secret:

</aside>

## Let's start in order:

<aside>
🪟 **WINDOWS**

First, you need to install Python

Then we type a command in the terminal:
cd C:\python
Then:
python s3cmd --configure
If it doesn't work, then first:
pip install python-dateutil
Then s3cmd --configure

Result:

![Снимок экрана 2022-09-22 в 18.38.45.png](Featured%20content%20in%20Atlas/%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_2022-09-22_%25D0%25B2_18.38.45.png)

Next, we enter the keys:

here are the keys: S3 storage access key: 

S3 storage secret key: 

Orion secret: 

Then fill in as in the screenshot:

![Снимок экрана 2022-09-22 в 18.41.43.png](Featured%20content%20in%20Atlas/%25D0%25A1%25D0%25BD%25D0%25B8%25D0%25BC%25D0%25BE%25D0%25BA_%25D1%258D%25D0%25BA%25D1%2580%25D0%25B0%25D0%25BD%25D0%25B0_2022-09-22_%25D0%25B2_18.41.43.png)

</aside>

<aside>
🍏 **MAC OS**

**Perform the following steps:**

Installing s3cmd in the terminal:

npm i -g joystream-cli
/bin/bash -c "$(curl -fsSL [https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh](https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh))"

brew install s3cmd

s3cmd --configure

s3cmd la

(Enter the keys as requested.)

(HTTP Proxy server: n)

S3 Endpoint: [eu-central-1.linodeobjects.com](http://eu-central-1.linodeobjects.com/)

**Like this:**

![Screenshot 2022-06-02 at 17.00.22-01.png](Featured%20content%20in%20Atlas/Screenshot_2022-06-02_at_17.00.22-01.png)

(DNS: 1. %(bucket).eu-central-1.linodeobjects.com)

</aside>

### You can now change the video hero and video splash screen categories.

1. Explore all video categories - 15 types.
**All categories:**

<aside>
💡 **Gaming
Howto & Style
News & Politics
Entertainment
Music
Film & Animation
People & Blogs
Comedy
Pets & Animals
Science & Technology
Education
Autos & Vehicles
Nonprofits & Activism
Travel & Events
Sports**

</aside>

1. You need to select one video from each category and download it to your computer.
(No additional video covers are needed.)

To do this, simply right-click and click "save as...".

<aside>
💡 Tip: Immediately sign the name of the file including: Video ID, category name, and category number. The name should be short for convenience and not contain spaces.
You'll need this to help you navigate better later when you start changing each category.

</aside>

![Снимок экрана 2022-06-02 в 12.55.17.png](Featured%20content%20in%20Atlas/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-06-02_%D0%B2_12.55.17.png)

![Снимок экрана 2022-06-02 в 12.51.06.png](Featured%20content%20in%20Atlas/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-06-02_%D0%B2_12.51.06.png)

![Снимок экрана 2022-06-02 в 12.50.32.png](Featured%20content%20in%20Atlas/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-06-02_%D0%B2_12.50.32.png)

![Снимок экрана 2022-06-02 в 12.53.35.png](Featured%20content%20in%20Atlas/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-06-02_%D0%B2_12.53.35.png)

![Снимок экрана 2022-06-02 в 13.01.11.png](Featured%20content%20in%20Atlas/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-06-02_%D0%B2_13.01.11.png)

![Снимок экрана 2022-06-02 в 12.58.14.png](Featured%20content%20in%20Atlas/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-06-02_%D0%B2_12.58.14.png)

1. After you have downloaded all the videos, you need to shorten them by selecting the most interesting and beautiful fragment. The finished video should be exactly 10 seconds long. (If you need advice on a program, I recommend Movavi Video Converter 21 Premium. It's very handy.) Save all finished videos in a separate folder.

2. **Go to the CLI.**
Use the following commands:

**To upload a video:**

> s3cmd put "**/Users/kiraovchinnikova/Desktop/категории/готовые/5630_15.mp4**" s3://atlas-featured-content/category-featured-videos/**15/5630_15.mp4**
> 

**Where:** 

/Users/kiraovchinnikova/Desktop/categories/ready/5630_15.mp4 - is the path to the file;

15 - is the number of the video category;

5630_15.mp4 - the name of your file

You need to specify the path to the video file on your computer. And the name (where in bold). To do this, right-click on the file and press "option" (For MAC).
Below is a video hint.

[Screen Recording 2022-06-02 at 15.46.54.mov](Featured%20content%20in%20Atlas/Screen_Recording_2022-06-02_at_15.46.54.mov)

**To make a downloaded file public, use the following command:**

> s3cmd setacl s3://atlas-featured-content/category-featured-videos/15/5630_15.mp4 --acl-public
> 

**Check in the CLI if the files were uploaded:**

> s3://atlas-featured-content/category-featured-videos/
> 

If you've done everything correctly, the video will open in your browser. Check:

[https://eu-central-1.linodeobjects.com/atlas-featured-content/category-featured-videos/**1/23656_1.mp4**](https://eu-central-1.linodeobjects.com/atlas-featured-content/category-featured-videos/1/23656_1.mp4)

1. **Now go to Playground:**

[http://query.joystream.org/graphql](http://query.joystream.org/graphql)

![Снимок экрана 2022-06-10 в 12.16.28.png](Featured%20content%20in%20Atlas/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-06-10_%D0%B2_12.16.28.png)

[https://orion.joystream.org/graphql](https://orion.joystream.org/graphql)

**Insert into the left side:**

> mutation {
setCategoryFeaturedVideos(
categoryId: "**1**"
videos: [
{
videoId: **23656**
videoCutUrl: "[https://atlas-featured-content.eu-central-1.linodeobjects.com/category-featured-videos/**1/1-23656.mp4](https://atlas-featured-content.eu-central-1.linodeobjects.com/category-featured-videos/1/1-13272.mp4)"**
},
{ videoId: **23657** },
{ videoId: **23659** }
{ videoId: **26622** }
]
) {
videoId
videoCutUrl
}
}
> 

**Fill in (all in bold) the number of the video category you are changing, insert a link to your video.
And below the video IDs to be recommended additionally here:**

![Screenshot 2022-06-02 at 16.21.55.png](Featured%20content%20in%20Atlas/Screenshot_2022-06-02_at_16.21.55.png)

![Screenshot 2022-06-02 at 16.22.18.png](Featured%20content%20in%20Atlas/Screenshot_2022-06-02_at_16.22.18.png)

**Enter your Orion secret key :**

> {
  "Authorization": "YOUR_SECRET_KEY_HERE"
}
> 

**Like this:**

![Screenshot 2022-06-02 at 16.10.10.png](Featured%20content%20in%20Atlas/Screenshot_2022-06-02_at_16.10.10.png)

## DONE! Do this with every video file and poster for all video categories!

---

# VIDEO - HERO:

![Безымянный-2 [Восстановлен]-08.png](Featured%20content%20in%20Atlas/%D0%91%D0%B5%D0%B7%D1%8B%D0%BC%D1%8F%D0%BD%D0%BD%D1%8B%D0%B8-2_%D0%92%D0%BE%D1%81%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BB%D0%B5%D0%BD-08.png)

In the same principle, we change the hero of the video, but with slightly different commands in the CLI.
Upload the video you want to set on the home page. And cut it down to 30 seconds.
And in this case you need a cover. (You can just take a screenshot of a nice frame).

![Снимок экрана 2022-06-02 в 15.14.52.png](Featured%20content%20in%20Atlas/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-06-02_%D0%B2_15.14.52.png)

**UPLOAD:**

> s3cmd put "/Users/kiraovchinnikova/Desktop/hero/26678_Hero_Kira.mp4" [s3://atlas-featured-content/video-hero/26678_Hero_Kira.mp4](s3://atlas-featured-content/video-hero/26678_Hero_Kira.mp4)
> 

**Make Public:**

> s3cmd setacl s3://atlas-featured-content/video-hero/26678_Hero_Kira.mp4  --acl-public
> 

Click

![Снимок_экрана_2022-06-02_в_14.31.25-removebg-preview.png](Featured%20content%20in%20Atlas/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-06-02_%D0%B2_14.31.25-removebg-preview.png)

![Снимок экрана 2022-06-02 в 13.52.05.png](Featured%20content%20in%20Atlas/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-06-02_%D0%B2_13.52.05.png)

**Check for all downloads:**

> s3cmd ls s3://atlas-featured-content/video-hero/]
> 

![Снимок экрана 2022-06-02 в 13.55.40.png](Featured%20content%20in%20Atlas/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-06-02_%D0%B2_13.55.40.png)

**If you did everything right and made the files public - check the links in your browser. They should open.**

[https://atlas-featured-content.eu-central-1.linodeobjects.com/video-hero/26678_Hero_Kira.mp4](https://atlas-featured-content.eu-central-1.linodeobjects.com/video-hero/26678_Hero_Kira.mp4)

and

[https://atlas-featured-content.eu-central-1.linodeobjects.com/video-hero/Hero_poster.jpg](https://atlas-featured-content.eu-central-1.linodeobjects.com/video-hero/Hero_poster.jpg)

**Now go here:**

[**http://query.joystream.org/graphql**](http://query.joystream.org/graphql)

> mutation {
setVideoHero(
newVideoHero: {
videoId: "**26678**"
heroTitle: "**Open Content And Creativity w/ Eclipsing Binary**"
heroVideoCutUrl: "[https://atlas-featured-content.eu-central-1.linodeobjects.com/video-hero/**26678_1.mp4**](https://atlas-featured-content.eu-central-1.linodeobjects.com/video-hero/26678_1.mp4)"
heroPosterUrl: "[https://atlas-featured-content.eu-central-1.linodeobjects.com/video-hero/**Hero_poster.jpg**](https://atlas-featured-content.eu-central-1.linodeobjects.com/video-hero/Hero_poster.jpg)"
}
) {
videoId
heroTitle
heroVideoCutUrl
heroPosterUrl
}
}
> 

Enter the ID and title of the video you are uploading.
Change the links whose endings are in bold to the video titles and artwork you uploaded as well.

**At the bottom is your key. Orion secret in quotes:**

> {
"Authorization": "——————"
}
> 

![Снимок экрана 2022-06-02 в 14.21.40.png](Featured%20content%20in%20Atlas/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-06-02_%D0%B2_14.21.40.png)

Click

![Снимок_экрана_2022-06-02_в_14.31.25-removebg-preview.png](Featured%20content%20in%20Atlas/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-06-02_%D0%B2_14.31.25-removebg-preview.png)

[Запись экрана 2022-06-02 в 14.48.51.mov](Featured%20content%20in%20Atlas/%D0%97%D0%B0%D0%BF%D0%B8%D1%81%D1%8C_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-06-02_%D0%B2_14.48.51.mov)

## DONE!