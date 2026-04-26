# Lumen Bank — v3 (Dark Revolut-style)

Demo banking + crypto PWA, installable on Mac browser and iPhone home screen. Full dark theme, desktop sidebar layout, dense data display.

## Login

- Username: `DemaHot`
- Password: `Carmi101@`

## What's new in v3

- **Full dark theme** (forced — no more bright white spaces)
- **Desktop layout**: 3-column dashboard (sidebar nav · main content · activity rail)
- **Mobile layout**: clean single-column with bottom nav
- News-style price ticker at the top
- Top movers cards
- Live mini-sparkline beside every crypto in the list
- Watchlist (star a crypto from its detail view)
- Markets view with Top / Gainers / Losers filters
- Wallet view showing all your accounts
- Spending-this-month limit progress in the right rail
- Chart period tabs: 24H / 7D / 1M / All
- Global search bar (desktop)

## Starting balances

- $10,000 USD cash
- 0.32 BTC
- 3 ETH

Live prices update every 30 seconds (CoinGecko → Binance → Coinbase fallback chain).

## Deploy to GitHub Pages (free)

1. Sign in at **github.com**, then go to **github.com/new**
2. Repository name: `lumen-bank` · Public · do not initialize with anything
3. Click **Create repository**
4. On the empty repo page, click **uploading an existing file**
5. Drag the **6 files** from this folder (index.html, manifest.json, sw.js, icon-192.png, icon-512.png, apple-touch-icon.png) into the upload area
6. Click **Commit changes**
7. Settings → Pages → Source: **Deploy from a branch** · Branch: **main** · Folder: **/ (root)** → Save
8. Wait ~1 min, refresh, copy the URL: `https://YOUR-USERNAME.github.io/lumen-bank/`

## Install on iPhone

1. Open the URL in **Safari** (not Chrome — iOS PWAs only work via Safari)
2. Tap the **Share** button (square with arrow)
3. Scroll → **Add to Home Screen** → **Add**

## If you already had v1 or v2 installed

The new version is a different cache. To force-update on iPhone:

1. Long-press the Lumen icon → **Remove App** → Delete
2. Settings app → **Safari** → **Clear History and Website Data** → Confirm
3. Re-open the URL in Safari → Add to Home Screen

On Mac, just hard-refresh the page: **Cmd + Shift + R** (Chrome) or hold Shift and click the reload button (Safari).

## Reset demo data

Settings → "Reset demo data" — restores starting balances and clears all transactions.
