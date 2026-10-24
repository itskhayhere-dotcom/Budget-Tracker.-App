# Moss / Line – Financial Freedom Planner

A calm, single-page financial planner: budgets, savings goals, debt payoff, habits, insights and PDF reports.
Installable as an app (PWA) and works offline after the first visit.

- **No backend, no account.** Everything is stored in your own browser (localStorage). Nothing is sent to a server.
- **Back up regularly:** Settings (gear icon) → Download backup (.json). Restore from the same screen.
- PDF reports are generated in the browser. The first export loads the jsPDF library from the jsDelivr CDN.

## Files
| File | Purpose |
|---|---|
| `index.html` | The app |
| `manifest.webmanifest` | App name, colours and icons (makes it installable) |
| `sw.js` | Service worker: offline support and updates |
| `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`, `apple-touch-icon.png` | App icons |

## Updating
Upload a new `index.html` and commit. To force every installed copy to refresh, also change `moss-line-v1` to `moss-line-v2` in `sw.js`.

## Run locally
`python3 -m http.server 8000`, then open http://localhost:8000
