# YouTube Shorts Security-Awareness Demo
<img width="1536" height="1024" alt="ChatGPT Image Sep 22, 2026, 06_00_51 PM" src="https://github.com/user-attachments/assets/c26978ff-109e-4baa-bf4e-079ca7e69244" />


```text

 __   __ _____ _____ ___  _   _ _____ ____  
 \ \ / /| ____|_   _/ _ \| \ | | ____|  _ \ 
  \ V / |  _|   | || | | |  \| |  _| | |_) |
   | |  | |___  | || |_| | |\  | |___|  _ < 
   |_|  |_____| |_| \___/|_| \_|_____|_| \_\
```

## Overview

This project is a local HTML demonstration styled as a YouTube Shorts page. It is intended for:

- Security-awareness training
- Demonstrating how social-engineering pages can appear trustworthy
- Teaching users to inspect permissions, embeds, and external requests
- Testing defensive browser and content-security controls

> **Important:** This demo must not be used to impersonate YouTube, deceive users, collect personal information, or access a camera without clear, informed consent.

## Security Warning

The original version of `youtube.html` contains functionality that:

1. Requests access to the visitor’s camera.
2. Captures images periodically.
3. Uploads captured images to an external webhook.

This behavior is invasive and should not be used in a deceptive page or deployed publicly.

For a safe demonstration:

- Remove the camera-access code.
- Remove hidden `<video>` and `<canvas>` elements.
- Remove the webhook URL and upload logic.
- Display a visible training notice instead of collecting data.
- Ask for explicit consent before testing any browser permission.
- Use a local mock endpoint if network behavior must be demonstrated.
- Never store or transmit real images or personal information.

## Recommended Safe Changes

The page should clearly identify itself as a training demo:

```html
<div class="training-banner" role="note">
    Security-awareness demo — no camera access or data collection is performed.
</div>
```

Suggested CSS:

```css
.training-banner {
    position: fixed;
    top: 0;
    left: 0;
    z-index: 10;
    width: 100%;
    padding: 12px;
    color: #fff;
    background: #b00020;
    font: 600 14px/1.4 system-ui, sans-serif;
    text-align: center;
}
```

## Privacy and Consent Requirements

Before conducting any authorized test:

- Obtain written permission from participants.
- Explain exactly what the page does.
- Explain which browser permissions are requested.
- Avoid collecting images, audio, credentials, or identifying information.
- Provide an obvious way to stop the demonstration.
- Delete all test data after the exercise.
- Use a private, access-controlled test environment.

## Responsible Use

This project is suitable for defensive education and authorized testing only. Do not use it to:

- Trick people into granting browser permissions
- Impersonate a real service
- Harvest credentials or personal data
- Capture photographs without informed consent
- Send data to third-party services without authorization
- Bypass browser security controls

## License

Use, modify, and distribute this training material only in accordance with applicable law, organizational policy, and explicit participant consent.
