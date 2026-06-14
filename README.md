# LuxTorch PWA — Deployment Guide

## Files
- `index.html` — Main app
- `manifest.json` — PWA manifest
- `sw.js` — Service worker (offline support)

## Setup Steps

### 1. Add Your Gemini Key
In the app, tap ⚙️ (gear icon) → enter your Google Gemini API key.
Get one free at: https://aistudio.google.com/app/apikey

### 2. Host the Files
Upload all 3 files to any static host:
- **Vercel** (free): vercel.com → drag & drop folder
- **Netlify** (free): netlify.com → drag & drop folder
- **GitHub Pages**: push to repo → enable Pages

Your site must be on **HTTPS** for PWA install + camera/torch to work.

### 3. Install as PWA on Phone
1. Open the hosted URL in Chrome (Android) or Safari (iOS)
2. Android: tap ⋮ menu → "Add to Home Screen"
3. iOS: tap Share → "Add to Home Screen"

## How It Works
- **Turn ON** → Free, activates phone flashlight
- **Turn OFF** → Shows payment modal (Rs. 1,000 via Easypaisa to 03451959533)
- User uploads Easypaisa screenshot
- Gemini AI scans the image and verifies amount + recipient number
- If verified → torch turns off, unlock persists forever

## Payment Details Hardcoded
- Recipient: 03451959533
- Amount: Rs. 1,000
- Method: Easypaisa

To change these, edit `index.html` and search for `03451959533` / `1,000`.
