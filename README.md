# FeeKiller

Upload a screenshot of a food-delivery cart or receipt and FeeKiller finds the markup: it reads the order, compares it with the restaurant's direct prices, surfaces promo codes, and writes a refund request you can paste into support chat.

**Live:** https://trillionaire-sim.vercel.app

## Stack

- Next.js 14 (App Router), React 18, Tailwind CSS
- Supabase for auth and data
- A vision model API for reading screenshots

## Run locally

```bash
npm install
npm run dev
```

Create `.env.local` with:

```
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=
VISION_API_URL=
VISION_API_KEY=
VISION_MODEL=
```

## Structure

```
app/                     pages (landing, login, /app) and API routes
app/api/afai/            screenshot analysis and deal routing
app/api/extractVendorLink/  finds the restaurant's direct ordering link
src/components/          FeeKiller UI, auth, city picker, deal router
src/services/            location and vendor lookups
```
