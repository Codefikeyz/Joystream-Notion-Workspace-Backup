# Getting Started Guide

## 1. Table for the design of the work

<aside>
📎 [**https://docs.google.com/spreadsheets/d/1wEW-edUKKdxoTckmMGTnNYId9du-_ypd2HdeKbzZhYU/edit#gid=1277179909**](https://docs.google.com/spreadsheets/d/1JBVPN0ES4lZHOgBWC3DiYqBZrwSVBzLmEo35pbS200Q/edit#gid=1683304710)

</aside>

Study the tabs in the table before you begin.

**sheet 2 - “Information”**
Here is the first piece of information you need for your work.

**Sheet 2 - “Schedule”**
This is where the dates and curators are assigned to check the videos for certain days of the week.

**Subsequent sheets** - are weeks, where all video statistics are entered by day.

## 2. Data output

Once you have decided on the date for which you want to check the video material, copy the template for the data output (info sheet):

<aside>
🛠

{
  videos(limit: 10000, where: {createdAt_gt: "**2023-05-04**", createdAt_lt: "**2023-05-05**"}) {
    id
    title
    channel {
      language {
        iso
      }
      title
      ownerMember {
        handle
        controllerAccount
      }
    }
    duration
    mediaMetadata {
      size
    }
    category {
      id
      name
    }
    ytVideoId
    license {
      code
      customText
      attribution
      createdAt
      updatedAt
    }
    nft {
      id
      creatorRoyalty
    }
    commentsCount
    reactionsCount
    
  }
}

</aside>

**And paste this command here:**

<aside>
👉🏿 [http://query.joystream.org/graphql](https://query.joystream.org/graphql)

</aside>

<aside>
💡 Alternative Link: [https://query.joystream.org/graphql](https://query.joystream.org/graphql)

</aside>

**There you go:**

![Снимок экрана 2022-05-08 в 21.02.52.png](Getting%20Started%20Guide/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-05-08_%D0%B2_21.02.52.png)

**Pay attention to the date:**
If you want videos for 2022-05-05 - you specify a whole day. Until 2022-05-06.
below are the commands you don't need to change, they are needed for the full details of each video.
You only change the date.
**And click on PLAY.**

![Снимок экрана 2022-05-08 в 21.03.28.png](Getting%20Started%20Guide/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-05-08_%D0%B2_21.03.28.png)

After that in the right column you will see the output of all videos for the day.

**Select and copy this data:**
(Attention! Strictly: not manually, but with your keyboard - ctrl (windows) or cmd (ios) + A (All), so that all lines are copied exactly!)

![Снимок экрана 2022-05-08 в 21.07.38.png](Getting%20Started%20Guide/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-05-08_%D0%B2_21.07.38.png)

**And paste this data into the online converter:**

<aside>
👉🏿 [https://www.convertcsv.com/json-to-csv.htm](https://www.convertcsv.com/json-to-csv.htm)

</aside>

![Снимок экрана 2022-05-08 в 21.14.37.png](Getting%20Started%20Guide/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-05-08_%D0%B2_21.14.37.png)

**Below you will see this result.
This is the data you need to insert into the worksheet (сopy them):**

![Снимок экрана 2022-05-08 в 21.15.57.png](Getting%20Started%20Guide/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-05-08_%D0%B2_21.15.57.png)

**In the worketable on the desired sheet, select the row on the left (put your cursor on the line number) and paste this data.**

![Снимок экрана 2022-05-08 в 21.18.54.png](Getting%20Started%20Guide/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-05-08_%D0%B2_21.18.54.png)

**There you go:**

![Снимок экрана 2022-05-08 в 21.21.45.png](Getting%20Started%20Guide/%D0%A1%D0%BD%D0%B8%D0%BC%D0%BE%D0%BA_%D1%8D%D0%BA%D1%80%D0%B0%D0%BD%D0%B0_2022-05-08_%D0%B2_21.21.45.png)

**Now you can check the all videos:**

## 3. In order to thoroughly check all videos and identify errors and violations, if any, you need to study all existing licenses:

<aside>
🇺🇸 Types of licenses:

[Licenses.pdf](Getting%20Started%20Guide/Licenses.pdf)

</aside>

<aside>
🇷🇺 Типы лицензий:

[Лицензии.pdf](Getting%20Started%20Guide/%D0%9B%D0%B8%D1%86%D0%B5%D0%BD%D0%B7%D0%B8%D0%B8.pdf)

</aside>

## **4. Video Tutorial for extracting the scheduled videos:**

[~~https://play.joystream.org/video/27663~~](https://play.joystream.org/video/27663) - oops