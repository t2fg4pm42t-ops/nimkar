# נמכר · Nimkar — Israel real-estate deals explorer

Single-file web app over the Israel Tax Authority deals register (via OVER's public database), 1998 → today.

- `index.html` — the whole app (Leaflet embedded, no build step)
- `nimkar-sw.js` — service worker: offline app shell when served over https

## Hosting on GitHub Pages
Settings → Pages → Source: *Deploy from a branch* → `main` / `(root)`.
The app then lives at `https://<user>.github.io/<repo>/`.

Data is fetched live by each viewer's browser from `over.org.il` (≈20 queries/min per viewer) and cached in the browser (IndexedDB). CPI from the CBS API. Nothing is sent anywhere else.
