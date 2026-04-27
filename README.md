# Lumen Bank — v4 (Massive feature update)

A demo banking + investing PWA. Single HTML file, drag-and-drop deploy to GitHub Pages.

---

## What's new in v4

This version is a major upgrade from v3. New features:

- **Invest view** — Buy and sell 12 simulated stocks (AAPL, MSFT, GOOGL, NVDA, TSLA, etc.) with live-updating prices, mini sparklines, P&L tracking, and cost basis
- **Analytics view** — Income vs spending, daily 14-day bar chart, category donut, top merchants
- **Budgets** — Set monthly limits per category, track progress with color-coded bars
- **Subscriptions** — Auto-detected recurring charges (Spotify, Netflix, Bell Canada, etc.)
- **Rewards** — Standard / Gold / Platinum tiers with 1% / 2% / 3% cashback. Earn points by spending.
- **Auto-arriving transactions** — Lumen simulates real banking life: Starbucks ☕, Amazon 📦, Uber 🚗, biweekly paycheck 💼, etc., arrive in the background with toast notifications
- **Onboarding flow** — First-time users get a guided setup
- **Card tier visuals** — Card design changes (Standard / Gold / Platinum) based on rewards tier
- **Confetti** — When your paycheck arrives 🎉

---

## How to deploy to GitHub Pages

1. Go to [github.com/new](https://github.com/new)
2. Name the repo `lumen-bank` (or anything you like). Make it **Public**.
3. **Don't check** "Add a README" — leave the new repo empty.
4. Click **Create repository**.
5. On the next page, click **uploading an existing file** (the small link in the middle).
6. Drag all 6 files from this folder into the upload box:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icon-192.png`
   - `icon-512.png`
   - `apple-touch-icon.png`
7. Scroll down, click **Commit changes**.
8. In the repo, click **Settings** (top tab) → **Pages** (left sidebar).
9. Under "Source", pick **Deploy from a branch**, choose `main` branch and `/ (root)`. Click **Save**.
10. Wait 30–60 seconds. Your app will be live at:
    ```
    https://YOUR-USERNAME.github.io/lumen-bank/
    ```

---

## How to install on iPhone home screen

1. On iPhone, open the URL above in **Safari** (must be Safari).
2. Tap the **Share** button (square with up-arrow).
3. Scroll down, tap **Add to Home Screen**.
4. Tap **Add**.
5. The Lumen icon appears on your home screen. Tap it — opens fullscreen, no browser bars.

---

## How to install on Mac

1. Open the URL in **Chrome** or **Edge**.
2. Click the install icon in the address bar (looks like a small monitor with a down-arrow), or:
   - Chrome menu → "Install Lumen…"
3. Lumen launches as a standalone app in its own window.

---

## Login

- **Username:** `DemaHot`
- **Password:** `Carmi101@`

(Both are case-sensitive.)

---

## How to update the app after pushing changes

If you upload a new version of `index.html` to the repo, browsers may cache the old one. To force the update:

### On Mac
- Hard refresh: **Cmd + Shift + R**

### On iPhone
This is the most reliable way to get a fresh install:
1. **Long-press the Lumen icon** on your home screen → **Remove App** → **Delete from Home Screen**
2. Open **Settings → Safari → Clear History and Website Data**
3. Open the URL again in Safari, **Add to Home Screen** again

---

## Files in this folder

| File | Purpose |
|---|---|
| `index.html` | The whole app (HTML + CSS + JS in one file, ~176KB) |
| `manifest.json` | Tells iOS/Android how to install as an app |
| `sw.js` | Service worker — makes the app work offline |
| `icon-192.png`, `icon-512.png` | App icons |
| `apple-touch-icon.png` | iOS-specific icon |

---

## Demo controls

In **Settings**:
- **Live notifications** toggle — turn off auto-arriving transactions if you want a static demo
- **Hide balance** — for screenshots
- **Seed sample data** — instantly populates 9 transactions + payroll for screenshots
- **Reset demo data** — wipes everything back to starting balance
- **Sign out** — back to login screen

---

## Known limitations

- **Stocks are simulated** — real stock APIs require keys + CORS proxies. The simulation does a believable random walk around real-world base prices.
- **Crypto prices are real** — fetched live from CoinGecko, with Binance and Coinbase as fallbacks.
- **All your money is fake** — this is a demo; nothing is real or transmitted anywhere.
- **No backend** — everything lives in your browser's localStorage.

---

Built single-file for easy GitHub Pages deployment. Have fun with it.
