# from.the.hide

A personal photography practice tool for a street and colour photographer. Installable as a Progressive Web App and works fully offline after first load.

## Structure

- `index.html` — the entire app: markup, CSS, and JS, all inlined. No external requests, no CDN fonts.
- `manifest.json` — PWA manifest (name, icons, colours, display mode).
- `sw.js` — service worker that caches all assets on install for offline use.
- `icons/icon-192.png`, `icons/icon-512.png` — app icons.

## Deploy on Netlify (drag and drop)

1. Go to [netlify.com](https://netlify.com) and sign in (GitHub login works fine).
2. From the dashboard, drag this whole folder onto the "Sites" area — or use "Add new site" → "Deploy manually" and drop the folder.
3. Netlify gives you a URL like `from-the-hide.netlify.app`.

## Deploy on Netlify (via GitHub, auto-deploy on push)

1. Push this repository to GitHub.
2. On [netlify.com](https://netlify.com), click "Add new site" → "Import an existing project" → choose the repo.
3. No build command is needed — leave the build command empty and set the publish directory to the repository root (`.`).
4. Netlify deploys automatically on every push to the main branch.

## Deploy on GitHub Pages

1. Push this repository to GitHub.
2. In the repo settings, open "Pages", and set the source to the `main` branch, root directory.
3. GitHub gives you a URL like `username.github.io/repo-name`.

## Install on iPhone (Safari)

1. Open the deployed URL in Safari on the iPhone.
2. Tap the Share icon.
3. Tap "Add to Home Screen".
4. Launch from the home screen icon — it opens full screen, no browser chrome, and works offline after the first load.

## Notes

- Everything (prompts, colour swatches, pairings, lens descriptions) is hardcoded in `index.html`. Nothing is fetched at runtime.
- The service worker caches all app assets on install, so the app works with no network connection after the first visit.
- No external dependencies, fonts, or API calls.
