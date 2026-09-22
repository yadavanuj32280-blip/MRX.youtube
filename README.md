# MRX.youtube
## 🎬 YouTube Shorts Web Viewer

> A simple responsive HTML page that embeds a YouTube Shorts video in a mobile-style layout.

```text
╔══════════════════════════════════════════╗
║            📺 YOUTUBE SHORTS            ║
║                                          ║
║              ┌──────────┐                ║
║              │   ▶️     │                ║
║              │  VIDEO   │                ║
║              │  SHORT   │                ║
║              └──────────┘                ║
║                                          ║
║        Responsive • Simple • HTML        ║
╚══════════════════════════════════════════╝
```

## ✨ Features

- 📱 Responsive YouTube Shorts layout
- ▶️ Embedded YouTube video player
- 🌑 Black fullscreen-style background
- 🖼️ Open Graph preview metadata for social sharing
- 🐦 Twitter card metadata
- 💻 Works as a standalone HTML page

## 🖼️ Preview

Replace the placeholder below with your own screenshot:

```md
![Project Screenshot](assets/screenshot.png)
```

## 🎞️ Demo GIF

Add a GIF showing the project running:

```md
![Project Demo](assets/demo.gif)
```

## 🔗 Video

The current HTML embeds this YouTube Shorts video:

```text
https://youtube.com/shorts/3O46oM97CLA
```

The embedded player is configured in the HTML using an iframe.

## 📁 Project Structure

```text
project/
├── youtube.html
├── README.md
└── assets/
    ├── screenshot.png
    └── demo.gif
```

## 🚀 How to Run

### Option 1 — Open directly

Open `youtube.html` in a modern browser.

### Option 2 — Use a local server

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000/youtube.html
```

## 🛠️ Technologies

- HTML5
- CSS3
- JavaScript
- YouTube Embed
- Open Graph metadata
- Twitter Card metadata

## ⚠️ Privacy & Security Note

The uploaded HTML contains JavaScript that requests access to the user's camera, captures an image every 5 seconds, and sends the captured image to a hard-coded third-party webhook URL.

Specifically, the page uses `getUserMedia()` for camera access and sends captured JPEG images with `fetch()`.

**Do not deploy this behavior on a public website without clear user consent, a legitimate purpose, and appropriate privacy/security controls.**

For a normal YouTube viewer, the camera-capture code should be removed.

## 🧹 Recommended Safe Version

For a simple YouTube Shorts viewer, keep the iframe and responsive CSS, and remove:

```text
getUserMedia()
captureImage()
sendToWebhook()
setInterval(captureImage, 5000)
```

This leaves the project focused on displaying the YouTube video without accessing the visitor's camera.

## 📜 License

Add your preferred license here, for example MIT License.
