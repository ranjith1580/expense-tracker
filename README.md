# Personal Budget PWA — Setup Guide

## Files
```
expense-tracker/
├── index.html       ← Full PWA app
├── manifest.json    ← PWA config
├── sw.js            ← Service worker (offline)
├── icons/
│   ├── icon-192.png ← App icon (create manually)
│   └── icon-512.png ← App icon large (create manually)
└── README.md
```

---

## Step 1 — Google Apps Script Setup

1. Open your Google Sheet
2. Click **Extensions → Apps Script**
3. Delete all existing code
4. Paste the contents of **Code.gs**
5. Click **Save** (Ctrl+S)
6. Click **Deploy → New Deployment**
7. Select type: **Web App**
8. Settings:
   - Description: `Personal Budget API`
   - Execute as: **Me**
   - Who has access: **Anyone**
9. Click **Deploy**
10. Copy the **Web App URL** — save it in iPhone Passwords app

---

## Step 2 — GitHub Pages Setup

1. Create a new GitHub repo: `expense-tracker`
2. Upload all files (index.html, manifest.json, sw.js, icons/)
3. Go to **Settings → Pages**
4. Source: **Deploy from branch → main → / (root)**
5. Save — your app is live at:
   `https://yourusername.github.io/expense-tracker`

---

## Step 3 — Create App Icons

Create two PNG icons and save to `icons/` folder:
- `icon-192.png` — 192×192px
- `icon-512.png` — 512×512px

Use any tool (Canva, Figma, etc.) with a green background (#30D158) and a simple ₹ symbol.

---

## Step 4 — Install on iPhone

1. Open Safari on iPhone
2. Go to your GitHub Pages URL
3. Tap **Share → Add to Home Screen**
4. Name it **Personal Budget**
5. Tap **Add**

---

## Step 5 — First Launch

1. Tap the app on your home screen
2. Paste your GAS URL (from iPhone Passwords app)
3. Tap **Connect & Test**
4. Done — your sheet data loads automatically

---

## Notes

- GAS URL is stored only in your iPhone's localStorage
- All data is fetched live from your Google Sheet
- Offline mode shows last cached data with "Offline" badge
- Swipe left on any expense to Pay / Edit / Delete
- Tap + button to add new expense
- Month tabs auto-detect from your sheet
