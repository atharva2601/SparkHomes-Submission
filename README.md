# Spark Homes Repair Estimator

A mobile-first, offline-capable Progressive Web App for creating repair estimates during property walkthroughs

## Live app

The app is deployed on GitHub Pages and can be opened directly from the live link

Opening the deployed link loads `index.html` directly and launches the repair estimator app

```text
https://atharva2601.github.io/SparkHomes-Submission/
```

## How to run locally

No build tools or server side code is required

For the best preview, serve the folder over HTTP so the PWA manifest and service worker work correctly

```bash
python3 -m http.server 8000
```

## Included files

- `index.html` - the complete app with vanilla HTML/CSS/JavaScript and inlined XLSX/JSZip libraries
- `manifest.json` - PWA manifest for installability
- `sw.js` - service worker for offline app shell caching
- `icon-180.png`, `icon-192.png`, `icon-512.png` - PWA/home screen icons

## Feature checklist

- Multiple saved projects in localStorage
- Project switching without losing data
- 75+ default repair items organized by the required sections and groups
- Add custom items and delete any item per project
- Adjustable room support for bathrooms, bedrooms, living/common areas, kitchen, systems, interior/general, and exterior
- Progress tracking by reviewed group.
- Mobile camera/photo attachment with individual photo removal.
- Export downloads `.xlsx` when no photos are attached and `.zip` with Excel + photos when photos exist.
- Creative additions: Deal Analyzer, Voice Walkthrough, Aging Penalty Engine, and Missed Cost Sentinel.

## Notes

All user data stays on the device in localStorage. The app is designed for Chrome for Android and Safari for iOS. For best offline behavior, load the deployed app once while online before going offline
