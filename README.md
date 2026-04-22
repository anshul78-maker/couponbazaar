# 🏷️ CouponBazaar

> **India's community coupon marketplace** — Browse verified deals and earn commission by listing your own coupons.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/YOUR_USERNAME/couponbazaar)

---

## ✨ Features

| Feature | Description |
|---|---|
| 🔍 Browse & Search | Filter coupons by category, brand, or code |
| 🏷️ Coupon Detail | Full info, copy code, expiry countdown |
| ⭐ Reviews & Ratings | Community ratings per coupon |
| 💼 Sell Coupons | List your own deals in 60 seconds |
| 📊 Seller Dashboard | Earnings, redemptions, wallet balance |
| 💸 UPI Payouts | Instant Razorpay payouts to any UPI ID |
| 🔔 Notifications | Real-time alerts for sales and expiry |
| 📱 Mobile App | React Native app for Android & iOS |

---

## 🛠️ Tech Stack

```
Frontend (Web)     React 18 + Vite
Mobile App         React Native + Expo
Backend API        Node.js + Express
Database           Supabase (PostgreSQL)
Auth               Supabase Auth
Payments           Razorpay (UPI Payouts)
Hosting (Web)      Vercel
Hosting (API)      Railway
```

---

## 📁 Project Structure

```
couponbazaar/
│
├── src/
│   ├── App.jsx                  # Main web app (all pages)
│   └── main.jsx                 # React entry point
│
├── mobile/
│   └── CouponBazaarApp.jsx      # React Native mobile app
│
├── backend/
│   └── razorpay_backend.js      # Node.js API server
│
├── database/
│   └── supabase_schema.sql      # Full DB schema + triggers + RLS
│
├── index.html                   # HTML entry point
├── vite.config.js               # Vite config
├── vercel.json                  # Vercel deployment config
├── package.json                 # Dependencies
├── .env.example                 # Environment variable template
└── README.md                    # This file
```

---

## 🚀 Quick Start (Web App)

### 1. Clone the repo
```bash
git clone https://github.com/YOUR_USERNAME/couponbazaar.git
cd couponbazaar
```

### 2. Install dependencies
```bash
npm install
```

### 3. Set up environment variables
```bash
cp .env.example .env.local
# Fill in your Supabase and Razorpay keys
```

### 4. Set up the database
1. Go to [supabase.com](https://supabase.com) → New Project
2. Open **SQL Editor** → New Query
3. Paste the entire contents of `database/supabase_schema.sql`
4. Click **Run** ✅

### 5. Start the dev server
```bash
npm run dev
# App runs at http://localhost:3000
```

---

## 📱 Mobile App Setup

```bash
# Install Expo CLI
npm install -g expo-cli

# Go to mobile folder
cd mobile

# Install dependencies
npx expo install @react-navigation/native @react-navigation/bottom-tabs
npx expo install @react-navigation/stack react-native-screens
npx expo install react-native-safe-area-context react-native-gesture-handler
npx expo install @supabase/supabase-js
npx expo install expo-clipboard expo-haptics

# Start the app
npx expo start
```

Scan the QR code with **Expo Go** app on your phone to preview instantly.

---

## ⚙️ Backend API Setup

```bash
cd backend
npm install express razorpay @supabase/supabase-js dotenv

# Create .env file
cp .env.example .env
# Add your Razorpay and Supabase keys

# Start server
node razorpay_backend.js
# API runs at http://localhost:4000
```

### Deploy backend to Railway (free)
1. Go to [railway.app](https://railway.app) → New Project
2. Connect your GitHub repo
3. Add environment variables in Railway dashboard
4. Railway auto-deploys on every push ✅

---

## ☁️ Deploy Web App to Vercel

### Option A — One-click deploy
Click the **Deploy with Vercel** button at the top of this README.

### Option B — Manual deploy
```bash
# Install Vercel CLI
npm install -g vercel

# Deploy
vercel

# Follow the prompts → your site is live!
```

### Add Environment Variables on Vercel
1. Go to Vercel Dashboard → Your Project → Settings → Environment Variables
2. Add all variables from `.env.example`
3. Redeploy

---

## 💳 Razorpay Setup

1. Sign up at [razorpay.com](https://razorpay.com)
2. Go to **Settings → API Keys** → Generate Test Key
3. Add `VITE_RAZORPAY_KEY_ID` to your `.env.local`
4. For payouts: enable **Razorpay X** (business account)
5. Add webhook URL in Razorpay Dashboard:
   ```
   https://your-backend.railway.app/api/webhook/razorpay
   ```

---

## 🗺️ Full Launch Roadmap

| Week | Task | Status |
|---|---|---|
| Week 1 | Web app UI complete | ✅ Done |
| Week 1 | Supabase DB schema | ✅ Done |
| Week 2 | Razorpay commission flow | ✅ Done |
| Week 2 | React Native mobile app | ✅ Done |
| Week 3 | Deploy web app to Vercel | ⬜ Your turn |
| Week 3 | Deploy backend to Railway | ⬜ Your turn |
| Week 4 | Connect real Supabase DB | ⬜ Your turn |
| Week 4 | Go live with Razorpay test | ⬜ Your turn |
| Week 5 | Publish Android app (Play Store) | ⬜ Your turn |
| Week 6 | Publish iOS app (App Store) | ⬜ Your turn |

---

## 🌐 Custom Domain

Buy a `.in` domain (~₹500/year) from:
- [GoDaddy](https://godaddy.com)
- [Namecheap](https://namecheap.com)
- [BigRock](https://bigrock.in)

Connect to Vercel in 2 clicks: **Project → Settings → Domains → Add**

---

## 🔒 Security

- All routes protected by Supabase Row Level Security (RLS)
- Razorpay webhooks verified by HMAC signature
- Sellers cannot redeem their own coupons
- Environment variables never exposed to frontend

---

## 📞 Support & Contact

Built with ❤️ for India's smart shoppers.

For help or feature requests, open a GitHub Issue.

---

## 📄 License

MIT License — free to use, modify, and deploy commercially.
