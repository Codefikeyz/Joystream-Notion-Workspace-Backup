# Figma structure

## **Quick links**

1. [Final designs](https://www.figma.com/files/project/33106318/%E2%9C%85-Final?fuid=1017378024164173256),
2. [Work in progress designs](https://www.figma.com/files/project/33106300/%F0%9F%9A%A7-Work-in-progress?fuid=1017378024164173256),
3. [**"Joystream Atlas" legacy file**](https://www.figma.com/file/Vk2Z4QOiVa5bB6q3cBIG5J/Joystream-Atlas),
4. [Web Components](https://www.figma.com/file/Pf31tuYpozYmpq163U2ho8/Web-Components),
5. [Foundation](https://www.figma.com/file/Cc3VDoK6qglJ617ChA2EMr/Foundation),

## **Context**

![Untitled](Figma%20structure/Untitled.png)

Because Figma is a cloud-based tool, all our design files are stored in the cloud and are organized within a structure imposed by the tool. Figma allows for up to 4 layers of organization:

`Organization Workspace (Org tier only) → Teams → Projects → Files → Pages`

As an Atlas Design Team, we use Figma in the [Professional tier](https://www.figma.com/pricing/), which allows us to operate within **one Team**, have an **unlimited number of Projects** with an **unlimited number of Files** inside.

## **Structure overview**

<aside>
💡 **Tip:** You can pin Projects to your sidebar in Figma, by clicking on the star next to the Project card. Pinned Projects can be rearranged.

</aside>

![Untitled](Figma%20structure/Untitled%201.png)

![Untitled](Figma%20structure/Untitled%202.png)

| Projects | Files |
| --- | --- |
| [**🎨 Resources](https://www.figma.com/files/project/33106243/%F0%9F%8E%A8-Design-System?fuid=730334878476004289)**
*Contains libraries Figma files and other design resources* | - [**📄 Foundation](https://www.figma.com/file/Cc3VDoK6qglJ617ChA2EMr/Foundation)**
*Library of Atlas design tokens
-*  [**📄 Web Components](https://www.figma.com/file/Pf31tuYpozYmpq163U2ho8/Web-Components)**
*Library of Atlas design web components
-* [**📄 Icons](https://www.figma.com/file/2tlBY1JQtRMoyjmjJQ9jam/Icons)**
*Library of Atlas icons
-* [**📄 Figma Utilities](https://www.figma.com/file/yjuGz1asfGbifsCIOVUoPn/Utilities)**
*Library of utility Figma components used to document our designs* |
| [**✅ Final](https://www.figma.com/files/project/33106318/%E2%9C%85-Final?fuid=730334878476004289)**
*Designs and prototypes ready for development* | ***Page name 1, Page 2...***

For each page there should be a separate Figma file with the following structure:

• Thumbnail
• 🖼 **Design**, with the designs of static pages themselves
• 📊 **RWD**, with responsive versions of those pages
• 💠 **Local components**
• 🔀 **User stories**, with a separate prototype for each user story. Each prototype should have it’s own “description” frame (see details below)

**🚨 These files should be kept up-to-date.** |
| [**🚧 Work in progress](https://www.figma.com/files/project/33106300/%F0%9F%9A%A7-Work-in-progress?fuid=730334878476004289)**
*Designs and prototypes that designers are working on* | ***Page name 1, Page 2...***

The only rule here: For each page there should be a separate Figma file.

You can structure your files however you want. It’s your workspace. Adjust it however you feel most efficient. |
| [**🏗 Temp workspace](https://www.figma.com/files/project/33106822/%F0%9F%8F%97-Temp-Workspace?fuid=730334878476004289)**
*Irrelevant Figma files, explorations, experimentations, etc.* | [**📄 Joystream Atlas](https://www.figma.com/file/Vk2Z4QOiVa5bB6q3cBIG5J/Joystream-Atlas)**
*A soon-to-be-deprecated Figma file containing designs from the "pre Figma Team era", when everything used to be kept within a single file.* |
| [**🛠 Pioneer (Tweaks)](https://www.figma.com/files/project/33712705/%F0%9F%9B%A0-Pioneer-(Tweaks)?fuid=730334878476004289)**
*Loosely organized space for Figma files with designs for simple Pioneer tweaks* |  |

# **Ok, but how do I work with that?**

1. Create a file in **Work in progress** project and do your explorations and iterations there
2. When the designs are accepted, simply duplicate the file
3. Do the clean-up:
    - Delete unnecessary stuff (frames, elements, etc)
    - Move final static pages to Design page
    - Prepare RWD screens and keep them in RWD page
    - If local components exist, move them to Local components (if exist) page
4. Create user stories page and prepare prototypes
5. Change the thumbnail from work in progress to “can be implemented”
6. Move the file to Final project