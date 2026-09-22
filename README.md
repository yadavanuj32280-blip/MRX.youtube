# MRX.youtube
# YouTube Shorts Web Page

A simple HTML/CSS/JavaScript webpage that embeds a YouTube Shorts video in a responsive layout.

## Features

- Responsive YouTube Shorts embed
- Mobile-friendly vertical video layout
- Open Graph metadata for social-media sharing
- Twitter player metadata
- Full-screen video support
- Browser camera access functionality
- Captures an image from the camera every 5 seconds after permission is granted
- Sends captured images to a configured webhook endpoint

## Technologies Used

- HTML5
- CSS3
- JavaScript
- YouTube Embed
- Web MediaDevices API
- Webhook / HTTP POST

## Project Structure

```text
.
├── youtube.html
└── README.md
```

## How It Works

The page displays a YouTube Shorts video using an iframe. The layout uses CSS to keep the video centered and responsive on both mobile and desktop screens.

The JavaScript requests browser camera permission when the page loads. If permission is granted, the camera stream is placed in a hidden video element. An image is captured every 5 seconds and converted to a JPEG blob before being sent through an HTTP POST request to the configured webhook.

## Important Privacy & Security Note

This project requests camera permission and captures images periodically. Use this functionality only with clear, informed consent from the person using the webpage.

Do not deploy camera-capture or image-upload functionality without clearly explaining what is being captured, when it is captured, where it is sent, and obtaining appropriate permission.

The current HTML also contains a hard-coded webhook URL. For a real project, avoid exposing sensitive webhook endpoints in client-side source code and use an appropriate server-side endpoint.

## Running the Project

1. Download or clone the repository.
2. Open `youtube.html` in a modern web browser.
3. Allow camera access only if you understand and consent to the camera functionality.
4. For camera access, browsers may require the page to be served from a secure context such as HTTPS or a local development environment.

## YouTube Video

The current page embeds a YouTube Shorts video using its YouTube video ID.

## Disclaimer

This project is intended for learning and web-development experimentation. Use camera and image-upload features responsibly and in accordance with applicable privacy laws and the policies of your hosting platform.

## License

You can add your preferred license here, such as MIT, before publishing the repository.
