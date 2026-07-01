# Spark Homes Repair Estimator

A mobile-first, offline-capable Progressive Web App for creating repair estimates during property walkthroughs.

## How to run locally

No build tools or server-side code are required. You can open `index.html` directly for a quick preview, but PWA installation and the service worker require serving the folder over HTTP/HTTPS.

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000/
```

## GitHub Pages deployment

1. Upload every file in this folder to the root of a GitHub repository.
2. In GitHub, go to **Settings -> Pages**.
3. Set the source to the main branch/root folder.
4. Open the Pages URL on Chrome for Android or Safari for iOS.
5. Add it to the home screen to install as a PWA.

## Included files

- `index.html` - the complete app with vanilla HTML/CSS/JavaScript and inlined XLSX/JSZip libraries.
- `manifest.json` - PWA manifest for installability.
- `sw.js` - service worker for offline app-shell caching.
- `icon-180.png`, `icon-192.png`, `icon-512.png` - PWA/home-screen icons.
- `SUBMISSION_WRITEUP.pdf` - one-page contest writeup.

## Feature checklist

- Multiple saved projects in localStorage.
- Project switching without losing data.
- 75+ default repair items organized by the required sections and groups.
- No Action Needed option for every group.
- Per-project unit-cost overrides and global CSV price updates.
- Add custom line items and delete any line item per project.
- Adjustable room support for bathrooms, bedrooms, living/common areas, kitchen, systems, interior/general, and exterior.
- Progress tracking by reviewed group.
- Mobile camera/photo attachment with individual photo removal.
- Export downloads `.xlsx` when no photos are attached and `.zip` with Excel + photos when photos exist.
- Creative additions: Deal Analyzer, Voice Walkthrough, Aging Penalty Engine, and Missed-Cost Sentinel.

## Notes

All user data stays on the device in localStorage. The app is designed for Chrome for Android and Safari for iOS. For best offline behavior, load the deployed app once while online before going offline.
