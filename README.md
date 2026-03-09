# Konarskis Clean Slopes - Landing Page

This is a minimalistic, high-performance landing page for **Konarskis Clean Slopes**, a zero-waste remote mulching service in Cyprus. Built with mobile-first principles and modern aesthetics, it is designed for speed, trust, and conversion.

## 🚀 Setup & Deployment

### 1. Add Your Video
To ensure the video loads instantly as requested, we serve two versions: one for high-quality desktop viewing and a lightweight version for mobile.

**1. High-Quality Desktop Video (`video-desktop.mp4`)**
Best for large screens, uses 1080p resolution. Targeted at ~3Mbps to keep the file size under 25MB for a 1-minute loop.
```bash
ffmpeg -i video-original.mov -vcodec libx264 -b:v 3000k -maxrate 4000k -bufsize 6M -preset slow -pix_fmt yuv420p -an -vf "scale=1920:-2" -movflags +faststart video-desktop.mp4
```

**2. Lightweight Mobile Video (`video-mobile.mp4`)**
Optimized for 3G/4G connections and smaller screens. Resized to 720p with a 1MB bitrate limit and 24fps.
```bash
ffmpeg -i video-original.mov -vcodec libx264 -b:v 1000k -maxrate 1500k -bufsize 2M -preset veryslow -pix_fmt yuv420p -an -r 24 -vf "scale=1280:-2" -movflags +faststart video-mobile.mp4
```

### Why these flags?
*   **`-movflags +faststart`**: Moves the MOOV atom (metadata) to the front so the video starts playing while it's still downloading.
*   **`-an`**: Removes the audio track to save significant file size (not needed for muted background loops).
*   **`-pix_fmt yuv420p`**: Ensures compatibility with all mobile browsers (especially older iOS/Safari versions).

## 🛠 Tech Stack
*   **HTML5 / CSS3**
*   **Tailwind CSS (via CDN):** For rapid styling without build steps.
*   **Google Fonts (Inter):** For clean, professional typography.
*   **JavaScript:** For simple WhatsApp message generation.

## 📝 Content Management
Since there are no build steps, you can modify any text, pricing, or images directly in the `index.html` file. The structure is semantic and commented for ease of use.

---
*Document version 2.0 — March 2026*
