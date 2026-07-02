# QR Code Generator

A fully client-side web app for generating QR codes from URLs — no server, no accounts, no expiry. Both the QR encoding library and ZIP library are bundled directly in the HTML, so it works by simply opening the file in a browser.

## Features

- **Single QR Code** — enter a URL, validate it, and generate a QR code instantly
- **Batch QR Codes** — provide a list of label + URL pairs and generate all at once
- Customizable size, error correction level, and dark/light colors
- Download individual QR codes as **PNG** or **SVG**
- Download all batch QR codes at once as a **ZIP** file (PNG or SVG)
- Files are named after the label you provide

## Usage

No installation or build step required. Just open `index.html` in any modern browser.

### Option 1 — Open directly (recommended)

Double-click `index.html` in Finder, or run:

```bash
open index.html
```

### Option 2 — Python local server

```bash
python3 -m http.server 8080
```

Then visit `http://localhost:8080`.

### Option 3 — Node

```bash
npx serve .
```

### Option 4 — VS Code Live Server

Right-click `index.html` in the VS Code Explorer → **Open with Live Server**.

## How it works

QR codes are generated entirely in the browser using [qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator). No data is sent to any external service. The generated QR codes encode the URL directly into the pattern, so they are permanent and will never expire.

## Project structure

```text
qr-generator/
└── index.html   # entire app — HTML, CSS, JS, and bundled libraries
```
