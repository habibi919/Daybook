# Daybook

A private, offline daily journaling app. No account, no cloud, no analytics — everything lives on your device. Built as a plain HTML/CSS/JS Progressive Web App (no React, no build step, no server).

## Files
- `index.html` — the entire app (HTML + CSS + JS inline)
- `manifest.webmanifest` — makes it installable to your home screen
- `service-worker.js` — lets it launch offline once installed
- `icons/` — the home-screen app icons

## Try it right now (desktop)
Open `index.html` in a browser. The app fully works and your entries persist.
(Opening it as a local file means no install/offline icon — for that, host it. See below.)

## Put it on your phone as a real app
A PWA needs to be served over **HTTPS** to install. Two easy, free ways:

**Fastest — Netlify Drop**
1. Go to https://app.netlify.com/drop
2. Drag this whole `daybook` folder onto the page → you get an `https://…` link.
3. Open that link on your phone:
   - **iPhone (Safari):** Share → *Add to Home Screen*
   - **Android (Chrome):** menu (⋮) → *Install app* / *Add to Home screen*
4. Launch it from the new icon — full screen, no browser bars, works offline.

**Permanent — GitHub Pages**
1. Put these files in a repo, enable Pages (Settings → Pages → deploy from branch).
2. Visit the Pages URL on your phone and Add to Home Screen as above.

## Using it
- **First launch:** set a 4-digit passcode (hashed, stored only on your device).
- **Today:** tap a mood to color the day, then write. Text autosaves as you type.
- **Journal:** every page, newest first. Tap to read; ⋯ to edit, copy, or delete.
- **Moods:** the month as a color mosaic. Tap a colored day to open it.
- **Settings (gear, top-right of Today):** Export / Import backup, Change passcode.

## Back up your data
Entries live in this browser/installed app only. Use **Settings → Export backup**
now and then to save a `.json` file. **Import backup** restores it (on a new phone,
after clearing data, etc.).

## Notes
- Forgot the passcode? There's no recovery by design. Clearing the app's site data
  resets it — but that also erases entries, so keep a backup.
- To change anything, just edit `index.html`. The design tokens (colors, fonts,
  spacing) are CSS variables at the top of the `<style>` block.
