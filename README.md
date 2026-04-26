# Lumen Bank — Demo PWA (v2)

Apple-style demo banking app with live crypto prices. Forced light mode, triple-fallback price feed, plus 18 new features.

## Login
- Username: `DemaHot`
- Password: `Carmi101@`

## Files (just 5 — drag them all into your repo)

```
lumen-bank/
├── index.html          # Whole app (HTML + CSS + JS in one file)
├── manifest.json       # PWA manifest
├── sw.js               # Service worker
├── icon-192.png
├── icon-512.png
├── apple-touch-icon.png
└── README.md
```

## How to update v1 → v2 on your existing GitHub repo

1. Open your repo on GitHub
2. Click **Add file → Upload files**
3. Drag everything from this folder, **including overwriting `index.html`**
4. Commit changes
5. Wait ~30 seconds for GitHub Pages to redeploy

## How to get the new version on your iPhone

The old version is cached. To force-refresh:

**Easiest method:**
1. On your iPhone, **delete the Lumen icon** from home screen (long-press → Remove App → Delete from Home Screen)
2. Open Safari, go to your `https://YOUR_USERNAME.github.io/lumen-bank/` URL
3. iPhone Settings app → Safari → Clear History and Website Data → Clear (this clears the old service worker)
4. Go back to your URL in Safari → Share → Add to Home Screen → Add
5. Tap the new icon → log in with `DemaHot` / `Carmi101@`

## Why the rebuild

v1's "Sign In does nothing" symptom on your phone was caused by the page calling a JavaScript file that failed to load. v2 puts everything back into a single `index.html` so this can't happen — there's only one file to upload.

## Features

**Visible right away:**
- Forced light mode (works on iPhone dark mode)
- Live portfolio sparkline chart
- Animated balance (flashes green/red on changes)
- Crypto rows pulse on price ticks
- Live status indicator (green/orange/red dot top-right)

**Tap to use:**
- 💳 **Card** — tap eye icon to flip and see CVV
- 💰 **Send/Receive/Exchange/Top up** — full transaction flow
- 🧾 **Pay bills** — Electric, Internet, Phone, Rent, Water, Streaming presets
- 🎯 **Savings goals** — set target, contribute, watch progress fill
- 🔔 **Notifications** — bell icon, every action creates one
- 🔍 **Activity tab** — search transactions, filter by category
- 🍩 **Donut chart** — monthly spending breakdown by category
- ❄️ **Freeze card** — Cards tab → blocks sending while frozen
- 👁️ **Hide balance** — Settings → privacy mode
- ⚡ **% buttons** — 25/50/75/Max in Send modal
- 📷 **QR code** — Receive screen
- 💸 **Buy with USD** — direct from any crypto detail screen

## Crypto prices

Three sources with auto-failover:
1. **CoinGecko** (primary)
2. **Binance** (fallback if CoinGecko blocked)
3. **Coinbase** (last resort)

Refreshes every 30 seconds. The dot top-right shows status:
- 🟢 Green = live data
- 🟠 Orange = cached (using last known prices)
- 🔴 Red = no connection

## Reset / change settings

- **Reset balances:** Settings → Reset demo data
- **Change password:** edit `index.html`, find these lines near the top of the `<script>` block:
  ```js
  const VALID_USER = "DemaHot";
  const VALID_PASS = "Carmi101@";
  ```
- **All data is local** — nothing goes to a server. Per-device storage.

## Demo only

This is a fake bank. No real money, no real banking, no real authentication (the login check is client-side). Don't use this for anything real.
