# Elion Phones – Vercel deploy

Static site, no build step.

## Deploy (easiest: GitHub)
1. Create a GitHub repo and upload everything in this folder (so `index.html` is at the root).
2. Go to vercel.com → Add New → Project → import the repo.
3. Framework Preset: **Other**. Leave Build Command and Output Directory empty. Click Deploy.

## Deploy (Vercel CLI)
```
npm i -g vercel
cd elion-phones
vercel --prod
```

## Structure
- `index.html` – the store (HTML, CSS, JS)
- `data/seed.json` – products and store settings
- `images/` – product photos, hero image, logo layers
- `vercel.json` – clean URLs, `/admin` route, caching

## Admin
Open `yoursite.vercel.app/#admin` (or `/admin`). Default password: `elion2026` – change it after logging in.

## Important
There is no server database on Vercel. Admin changes are saved only in the browser of whoever makes them, so customers keep seeing `data/seed.json`.
To change what everyone sees: edit `data/seed.json` (and add photos to `images/`), then redeploy.
