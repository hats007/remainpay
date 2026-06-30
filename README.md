# RemindPay — PWA Setup Guide

A payment and policy reminder app that works on iPhone and Android.

## Files in this folder

```
remindpay/
├── index.html       ← Main app
├── manifest.json    ← PWA metadata (name, icon, theme)
├── sw.js            ← Service worker (offline support)
├── netlify.toml     ← Netlify deployment config
└── icons/
    ├── icon-192.png ← Home screen icon (Android)
    └── icon-512.png ← Splash screen icon
```

---

## Deploy in 60 seconds (Netlify Drop — no account needed)

1. Go to **https://app.netlify.com/drop**
2. Drag the entire `remindpay/` folder onto the page
3. Netlify gives you a URL like `https://amazing-name-123.netlify.app`
4. Open that URL on your phone

---

## Install on iPhone

1. Open the URL in **Safari** (must be Safari, not Chrome)
2. Tap the **Share** button (box with arrow at bottom)
3. Scroll down → tap **"Add to Home Screen"**
4. Tap **"Add"** — the app icon appears on your home screen

---

## Install on Android

1. Open the URL in **Chrome**
2. Chrome shows a banner: **"Add RemindPay to home screen"** — tap it
   OR tap the 3-dot menu → **"Add to Home Screen"**
3. Tap **"Install"**

---

## Deploy with GitHub Pages (free, permanent)

```bash
cd remindpay
git init
git add .
git commit -m "RemindPay PWA"
gh repo create remindpay --public --push --source=.
# Then go to repo Settings → Pages → Deploy from main branch
```

Your URL: `https://yourusername.github.io/remindpay/`

---

## Features

- Add reminders with name, amount, category, due date, repeat
- Categories: Insurance, Loan/EMI, Subscription, Tax, Utility
- "This Month" view with total due amount
- Alerts tab with notification history
- Toast notifications for urgent items (due in ≤3 days)
- Push notifications (when enabled) for due date reminders
- Works offline after first load
- Dark mode support (follows phone system setting)
- Data saved locally on device (localStorage)
