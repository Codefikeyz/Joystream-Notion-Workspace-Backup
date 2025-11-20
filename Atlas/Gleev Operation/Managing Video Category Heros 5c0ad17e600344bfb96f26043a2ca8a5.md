# Managing Video Category Heros

## Download a video

1. Go to the video page and open the dev tools. You can do this in Chrome by pressing `cmd shift j` or clicking right-click on the page and clicking inspect
2. Go to the `Elements` tab in the dev tools. Press command F and type `<video`
3. Find the highlighted video in the HTML markup
4. Copy the URL in the `src` attribute. Open the URL in a new tab, click the kebab menu on the video, and download it.
5. Use some software to shorten the video. On Mac you can use QuickTime

## Upload cut video to linode

1. Download Cyberduck [https://cyberduck.io/download/](https://cyberduck.io/download/) It will allow you to upload videos to the Linode server with a pleasant UI.
2. Once installed, open the app and click Open Connection. In the drop-down menu at the top choose more options, search linode, and select the Frankfurt one. Close the window and select Linode Frankfurt from the dropdown again
3. Provide access key and secret key and connect(ask me for it)
4. Open `atlas-featured-content`folder and move the file to the folder. Once is uploaded right click on the file and click share.
5. Click right-click again on the file and click Copy URL and choose `HTTPS URL`
6. Use URL in mutation