# Konarskis Clean Slopes - Landing Page

This is a minimalistic, high-performance landing page for **Konarskis Clean Slopes**, a zero-waste remote mulching service in Cyprus. Built with mobile-first principles and modern aesthetics, it is designed for speed, trust, and conversion.

## 🚀 Setup & Deployment

### 1. Add Your Video
To ensure the video loads instantly as requested, place your video file in this directory and name it `video.mp4`.
*   **Compression is Key:** Use a tool like [Handbrake](https://handbrake.fr/) or [FFmpeg](https://ffmpeg.org/) to compress the video.
*   **Target Size:** Aim for under **5-10MB**.
*   **Format:** H.264 or HEVC (H.265) for maximum compatibility.

### 2. Configure WhatsApp
Open `index.html` and scroll to the bottom. Replace the placeholder number with your actual business number:
```javascript
const whatsappNumber = "35799000000"; // Replace with your number (no + or 00)
```

### 3. Deploy to Firebase
This site is a pure static site with no build steps. To host on Firebase:
1.  Install Firebase CLI: `npm install -g firebase-tools`
2.  Login: `firebase login`
3.  Initialize: `firebase init hosting`
    *   *Public Directory:* `.` (current directory)
    *   *Configure as SPA:* No
    *   *GitHub Deploys:* No
4.  Deploy: `firebase deploy`

## 🛠 Tech Stack
*   **HTML5 / CSS3**
*   **Tailwind CSS (via CDN):** For rapid styling without build steps.
*   **Google Fonts (Inter):** For clean, professional typography.
*   **JavaScript:** For simple WhatsApp message generation.

## 📝 Content Management
Since there are no build steps, you can modify any text, pricing, or images directly in the `index.html` file. The structure is semantic and commented for ease of use.

---
*Document version 2.0 — March 2026*
