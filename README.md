<p align="center">
  <img src="https://img.shields.io/badge/status-active-success" alt="Status" />
  <img src="https://img.shields.io/badge/license-MIT-blue" alt="License" />
</p>

<p align="center">
  <h1 align="center">WhatsApp Link Generator</h1>
  <p align="center">Generate shortened WhatsApp links with pre-filled messages & QR codes.</p>
</p>

---
## https://github.com/Ibrahim404-cyber/What-sapp-short-link/deployments/github-pages

## ✨ Features

- **Country Code Picker** — Dropdown with ~200 countries + flag emoji display
- **Auto-Detect Country** — Automatically selects your country via IP geolocation
- **Pre-filled Message** — Optional message text included in the generated link
- **Short Links** — Uses wa.link API to create shortened WhatsApp URLs
- **QR Code** — Generates a scannable QR code (via QRCode.js)
- **Material Design 3** — Dark theme with M3 color tokens
- **Copy & Open** — One-click copy or open the generated link

## 🚀 Getting Started

### Prerequisites

- A modern browser (Chrome, Firefox, Safari, Edge)
- An HTTP server (required for IP geolocation — CORS restriction)

### Installation

```bash
# Clone the repo
git clone https://github.com/yourusername/whatsapp-link-generator.git
cd whatsapp-link-generator

# Serve locally (any of these)
python3 -m http.server 8080
# or
npx serve .
# or
php -S localhost:8080
```

Then open `http://localhost:8080` in your browser.

### Usage

1. Open the app (your country is auto-selected via IP)
2. Select a country code if the auto-detection didn't match
3. Enter the phone number
4. Optionally type a pre-filled message
5. Tap **Generate Link**
6. Copy the short link or scan the QR code

## 🛠 Built With

| Tool | Purpose |
|------|---------|
| Vanilla HTML / CSS / JS | Core stack |
| [wa.link](https://wa.link) | URL shortening |
| [QRCode.js](https://github.com/davidshimjs/qrcodejs) | QR code generation |
| [ip-api.com](https://ip-api.com) | IP geolocation |
| Material Design 3 | Dark theme system |

## 📁 Files

```
├── index.html          # Single-page application (SPA)
├── README.md           # This file
└── report.txt          # Build report
```

## 🌐 API Reference

### IP Geolocation (ip-api.com)

```
GET https://ip-api.com/json/
```

Returns your public IP's country code (ISO alpha-2). Used on page load to pre-select your country. Free tier — no API key required.

### URL Shortening (wa.link)

The app calls the wa.link API with a full `wa.me` URL and displays the shortened result.

## ⚠️ Notes

- IP auto-detection **requires an HTTP server** (CORS policy blocks `file://`). Any local dev server works.
- Fallback country is **Bangladesh (+880)** if geolocation fails.
- Zero dependencies to install — everything loads from CDN.

## 📄 License

MIT
