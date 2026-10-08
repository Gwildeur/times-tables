# Times Tables Trainer (Einmaleins-Trainer)

A simple app for practising times tables. The app itself is in German. Open `index.html` in Safari (double-click it) and play.

- Pick which tables (1–12) to practise
- 10 questions per round, about half chosen from facts not yet learned
- Missed questions come back a few questions later in the same round
- Progress is remembered in the browser; a fact counts as learned after 3 correct answers in a row
- "My progress" shows a 12×12 colour grid (green = learned, amber = getting there, red = needs work, grey = not tried); tap a square for details
- Progress can be reset from the progress screen

Note: progress is stored per browser and per file location, so moving `index.html` or clearing Safari's website data starts fresh.

## On an iPhone

The app has an on-screen keypad and works as a Home Screen app. Host it (for example with GitHub Pages), open the web address in Safari, then tap Share → Add to Home Screen. After the first visit it also works offline.

## Files

- `index.html` — the whole app
- `manifest.webmanifest`, `sw.js`, `icons/` — Home Screen icon, app name and offline support. When releasing, bump the `CACHE` version in `sw.js` so phones pick up the new version.
