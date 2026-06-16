# 🔒 PrivacyKit — Photo Privacy Tools

**7 photo tools in a single HTML file. No server. No upload. Fully offline.**

🌐 **Live:** https://darkenamber.github.io/privacykit  
🛠 **Part of:** [darkenamber.com/tools](https://darkenamber.com/tools)  
📄 **License:** MIT

---

## Why PrivacyKit?

Every photo you take contains hidden metadata: **your GPS location, device model, timestamps, editing software.**  
Most online tools ask you to upload the photo — which defeats the purpose.

PrivacyKit runs entirely in your browser.  
**Your photos never leave your device.**

---

## ✨ Features

| | |
|---|---|
| 🔒 **Privacy first** | All processing in-browser, zero network requests |
| 📁 **Single file** | Download once, works forever, no install |
| 📱 **Mobile ready** | Full touch support — drag, pinch, two-finger rotate |
| 🎨 **3 themes** | Dark · Light · Retro 8-bit |
| 🌐 **2 languages** | English / Русский |
| 🆓 **Free forever** | No paywall, no limits, no registration |

---

## 🧰 Tools

### 🔍 EXIF Viewer & Cleaner

Reveals everything hidden in your photo — then removes it with **verification**.

**What it reads:**
- 📍 GPS coordinates → clickable Google Maps link
- 📷 Device: make, model, lens, ISO, shutter, aperture, focal length, flash
- 🕐 Date taken, date modified, timezone offset
- 🛠 Editing software (Lightroom, Snapseed, etc.)
- ✍️ Author, copyright, description

**What it strips:**
| Block | Contains | Status |
|-------|----------|--------|
| EXIF IFD | Camera data, timestamps | ✅ Removed |
| XMP (APP1) | Adobe history, GPS copy | ✅ Removed |
| IPTC (APP13) | Author, caption, location | ✅ Removed |
| ICC (APP2) | Color profile | ✅ Removed |
| PNG chunks | All metadata | ✅ Canvas strip |
| WEBP metadata | All metadata | ✅ Canvas strip |

**Verification report** — after every clean, shows exactly what happened:
```
📍 GPS Location        ✅ REMOVED
📷 Device info         ✅ REMOVED
🕐 Timestamps          ✅ REMOVED
🛠 Software            — was empty
✍️ Author / Copyright  ✅ REMOVED
🎨 Color profile (ICC) ℹ not sensitive
```

File is **re-parsed after cleaning** to verify what actually remains — not just assumed.

---

### ✏️ Metadata Editor

Edit what's written into the file:
- Author, Copyright, Description, Software
- GPS coordinates (manual entry)
- Empty field = **delete** that field from the file
- Auto-rename by date taken: `IMG_3847.jpg` → `2024-03-15_14-22.jpg`

---

### ✂️ Crop
- Draw selection freely or choose preset ratio: 1:1 · 4:3 · 16:9 · 9:16 · 4:5
- Rule of thirds grid overlay while selecting
- Result preview before download

---

### 🔄 Rotate & Flip
- Rotate: 90° · 180° · 270°
- Flip: horizontal · vertical
- Operations stack — preserved when switching tabs
- Live size + transform indicator

---

### 📐 Resize
- Quick presets: 1920×1080 · 1280×720 · 800×600 · 1080×1080
- Percentage presets: 75% · 50% · 25%
- Custom px with lock aspect ratio
- Shows % of original size

---

### 🌊 Watermark

Full gesture control — especially on mobile:

| Gesture | Action |
|---------|--------|
| 1 finger drag | Move text position |
| Pinch in/out | Resize text |
| 2-finger rotate | Rotate to any angle |

- Color, opacity controls
- Tile mode — cover entire photo (rotation applies to pattern)
- Live indicator: `32px · 45°`
- Syncs with size slider

---

### 🗜️ Compress
- JPEG quality slider
- **Side-by-side preview**: original vs compressed
- Shows file size before/after + reduction %
- PNG re-encode supported

---

## 🚀 Quick Start

**Online:**
```
https://darkenamber.github.io/privacykit
```

**Local:**
```bash
git clone https://github.com/darkenamber/privacykit.git
open privacykit.html
```

**Or just:** download `privacykit.html` → double-click → done.

---

## 📱 Mobile

- Tab bar shows icons only on small screens (fits all 7 tabs)
- All inputs use 16px font — no iOS auto-zoom
- Crop: draw with finger, page scroll locked during selection
- Watermark: full multi-touch (drag + pinch + rotate)
- Large tap targets throughout

---

## 🛠️ Tech Stack

| | |
|---|---|
| Language | HTML5 + CSS3 + Vanilla JS |
| EXIF read | [exifr](https://github.com/MikeKovarik/exifr) v7.1.3 |
| EXIF write | [piexifjs](https://github.com/hMatoba/piexifjs) v1.0.6 |
| Frameworks | None |
| Build tools | None |
| File size | ~95 KB |

---

## 📋 Format Support

| Format | Read | Clean | Crop | Watermark | Compress | Rotate | Resize |
|--------|------|-------|------|-----------|----------|--------|--------|
| JPEG | ✅ Full | ✅ Binary+XMP | ✅ | ✅ | ✅ | ✅ | ✅ |
| PNG | ⚠️ | ✅ Canvas | ✅ | ✅ PNG | ✅ | ✅ | ✅ |
| WEBP | ⚠️ | ✅ Canvas | ✅ | ✅ | ✅ | ✅ | ✅ |
| HEIC | ⚠️ Browser | ✅ → JPEG | ✅ | ✅ | ✅ | ✅ | ✅ |

> HEIC: native in Safari (iOS/macOS). Chrome requires a recent version.

---

## 🌟 Support

If PrivacyKit was useful:

- ⭐ **Star on GitHub** — helps others find it
- ☕ **[Ko-fi](https://ko-fi.com/darkenamber)** — keeps it free
- 🐛 **Issues** — bug reports welcome
- 💡 **Discussions** — feature ideas

---

## 🗺️ Roadmap

- [ ] Format converter (HEIC→JPG, PNG→WebP…)
- [ ] Photos → PDF
- [ ] Quality analyzer (sharpness, exposure, print size)
- [ ] Face blur
- [ ] Batch mode + ZIP download
- [ ] More languages (AZ, TR, DE)

---

## 🌐 DarkenAmber Ecosystem

| Project | Description |
|---------|-------------|
| 🔒 **PrivacyKit** | Photo privacy tools — you are here |
| 🔧 [IT Tools](https://github.com/DarkenAmber/DarkenAmber-it-tools) | Networking & developer tools |
| 📱 Mobile Apps | Flutter apps on Google Play |
| 🏠 Smart Home | ESP32-based IoT devices |

---

## 📜 License

[MIT](LICENSE) © 2025 DarkenAmber

---

<div align="center">

*Your photos. Your device. Your privacy.*

**[darkenamber.com](https://darkenamber.com)**

</div>
