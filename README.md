# AE bracket measurement Check — PWA

This folder is an installable Progressive Web App (PWA). It preserves the existing calculator's reference values, ±0.050 inclusive measurement tolerance, adjusted-error formula, rounding-down-to-0.1 behavior, and ALL OK decision logic.

## Install on Android
1. Upload the contents of this folder to a static web host that serves the site over **HTTPS** (required for service workers and PWA installation; localhost is also suitable for testing).
2. Open the hosted `index.html` in Chrome on Android.
3. Open Chrome's menu and choose **Install app** or **Add to Home screen** (wording varies by Chrome version).
4. Launch **AE bracket measurement Check** from the home screen. The app shell is cached for offline use after the first successful load.

Do not open `index.html` directly as a `file://` URL; PWA installation requires an HTTPS origin.

## Files
- `index.html` — calculator UI and unchanged calculation logic
- `manifest.webmanifest` — app name, display mode, and icons
- `service-worker.js` — offline app-shell caching
- `icons/` — PWA icons

## Local preview
From this directory, run `python3 -m http.server 8080` and open `http://localhost:8080/` in a browser. For actual Android installation, use HTTPS hosting.
