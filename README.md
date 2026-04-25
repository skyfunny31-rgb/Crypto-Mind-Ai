# CryptoMind AI — Coinbase Wallet Mini App

## 🚀 Deploy করার ধাপ

### Step 1: GitHub এ upload করুন
1. github.com এ নতুন repository বানান
2. এই সব ফাইল upload করুন

### Step 2: Vercel এ deploy করুন
1. vercel.com এ login করুন
2. "Add New Project" → GitHub repo select করুন
3. **Root Directory:** `public` সেট করুন
4. Deploy করুন → আপনার URL পাবেন (e.g. `your-app.vercel.app`)

### Step 3: Coinbase Developer Portal
1. developers.coinbase.com এ যান
2. "Create Mini App" click করুন
3. App URL দিন: `https://your-app.vercel.app`
4. App ID কপি করুন

### Step 4: App ID যোগ করুন
`public/index.html` এ এই লাইন update করুন:
```js
await window.MiniKit.init({ appId: 'YOUR_COINBASE_APP_ID' });
```

### Step 5: Manifest update করুন
`public/.well-known/farcaster.json` এ আপনার domain দিন।

## 📁 File Structure
```
coinbase-miniapp/
├── public/
│   ├── index.html          ← Main app
│   └── .well-known/
│       └── farcaster.json  ← Mini App manifest
└── vercel.json             ← Vercel config
```

## ✅ Features
- Claude AI powered crypto chatbot
- Any language support
- Live price charts (CoinCap API)
- Mobile-optimized UI
- Coinbase Wallet compatible
