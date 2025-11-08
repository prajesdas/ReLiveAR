# 🧠 WebAR Poster → Video Overlay (MindAR + Three.js)

A simple **marker-based WebAR project** where scanning a poster or image using your device’s camera plays a corresponding video overlay — built with **MindAR.js** and **Three.js**.

---

## 📁 Directory Layout

```

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

````

---

## ⚙️ Setup & Hosting

1. Clone or download the project folder.  
2. Open `index.html` directly in a browser that supports WebAR (Chrome, Edge, Safari).  
3. For best results, host it on a **local or static web server** (e.g., GitHub Pages, Vercel, or `python -m http.server`).

Example local run:
```bash
python -m http.server 8000
````

Then open:
👉 [http://localhost:8000](http://localhost:8000)

---

## 🧩 Workflow for Adding New AR Content

### Step I — Add Media

Drop your **image** (marker) and **video** into the `/media/` folder.
Example:

```
/media/
├── image3.jpg
└── video3.mp4
```

### Step II — Regenerate Target File

Go to the official MindAR target compiler:
🔗 [https://hiukim.github.io/mind-ar-js-doc/tools/compile](https://hiukim.github.io/mind-ar-js-doc/tools/compile)

Upload **all your images** (old + new) and generate a new `targets.mind` file.
Then, **replace the old** `targets.mind` file in your project.

### Step III — Update Config

Edit `config.json` to include a new entry matching your new media pair:

```json
[
  { "targetIndex": 0, "videoSrc": "media/video1.mp4" },
  { "targetIndex": 1, "videoSrc": "media/video2.mp4" },
  { "targetIndex": 2, "videoSrc": "media/video3.mp4" }
]
```

Make sure `targetIndex` corresponds to the order of your image in the compiled `.mind` file.

---

## 📹 Notes & Tips

* Keep each video **under 10MB** for smooth playback and faster loading.
* Use `.mp4` format for maximum browser compatibility.
* Use clear, high-contrast images for better AR marker detection.
* Always recompile `targets.mind` when adding or changing markers.

---

## 🧠 Tech Stack

* **MindAR.js** — marker-based WebAR framework
* **Three.js** — 3D rendering and video overlay
* **Vanilla JavaScript + HTML5 Video**

---

## 🚀 Quick Demo Flow

1. Open the site on your mobile or desktop browser.
2. Allow camera access.
3. Point the camera at one of your uploaded poster images.
4. Watch your **linked video** play over the marker in real-time!

---

## 🧑‍💻 Author

**Prajes Das**  **Sukalyan**
Student | Developer | AR Enthusiast
[GitHub: praJesDas](https://github.com/prajesdas)

---

## 🪪 License

This project is released under the **MIT License** — free for personal and educational use.

---

