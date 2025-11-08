1. Directory Layout of this project is as follows

    /project-root
    │
    ├── index.html
    ├── targets.mind
    ├── config.json
    ├── /media
    │    ├── image1.jpg
    │    ├── video1.mp4
    │    ├── image2.jpg
    │    ├── video2.mp4
    │    └── ...

2. Workflow for Adding New AR Content from now on:

    I. Drop your image and video in /media/.
    II. Regenerate and replace your targets.mind file from https://hiukim.github.io/mind-ar-js-doc/tools/compile to include all images in the order you will add video.
    III. Update config.json by adding a new entry like:
        { "targetIndex": 3, "videoSrc": "media/video4.mp4" }

3. Notes:
    Keep video short <10MB