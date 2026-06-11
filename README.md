# Break Time Invoice — PWA (Installable Web App)

This folder contains your invoice app set up as a Progressive Web App (PWA),
so it can be installed on iOS, Android, and desktop directly from the browser
— no app store needed.

## Files
- `index.html` — your invoice app (with PWA tags added)
- `manifest.json` — app name, icons, theme color
- `sw.js` — service worker (enables offline use)
- `icon-192.png`, `icon-512.png` — app icons (generated from your logo)

## IMPORTANT: Requires HTTPS hosting
PWAs only install correctly when served over HTTPS (or on `localhost` for
testing). Opening `index.html` directly via `file://` will NOT let you
install it as an app or use the offline service worker.

## Free hosting options (pick one)
1. **GitHub Pages** — create a repo, upload these files, enable Pages in
   Settings. Free, gives you a `https://yourname.github.io/...` URL.
2. **Netlify Drop** — go to https://app.netlify.com/drop and drag this folder
   in. Instantly get a live HTTPS URL, no account required for a quick test.
3. **Vercel / Cloudflare Pages** — similar drag-and-drop or Git-based free
   hosting with HTTPS.

## How to install on iOS
1. Open the hosted URL in **Safari** (must be Safari, not Chrome).
2. Tap the **Share** button (square with arrow).
3. Tap **"Add to Home Screen"**.
4. The app icon appears on your home screen and opens full-screen, like a
   native app.

## How to install on Android
1. Open the hosted URL in **Chrome**.
2. Tap the menu (⋮) → **"Add to Home screen"** or **"Install app"**.
3. Confirm — the app installs with its icon and launches full-screen.

## Notes
- Once installed, the app works offline (forms, calculations, printing).
- `window.print()` works on desktop browsers; on mobile it opens the
  device's native print/PDF dialog.
- To update the app later, just replace these files on your host —
  the service worker will fetch the new version on next load (you may need
  to close and reopen the app once for the update to fully apply).
