# Customer 360 — Vercel Deployment

## Files
```
customer360-deploy/
├── index.html      ← main app (self-contained)
├── vercel.json     ← Vercel routing & cache config
└── README.md
```

## Deploy Options

### Option A — Drag & Drop (fastest)
1. Go to https://vercel.com → New Project
2. Scroll to "Deploy without Git" → drag this entire folder
3. Click Deploy → get live URL instantly

### Option B — Vercel CLI
```bash
npm install -g vercel
cd customer360-deploy
vercel
# follow prompts → get live URL
```

To redeploy after changes:
```bash
vercel --prod
```

### Option C — GitHub
1. Push this folder to a GitHub repo
2. Vercel dashboard → Import repo → Deploy
3. Every git push auto-deploys

## Notes
- No build step required — pure static HTML
- External CDN deps (auto-loaded by browser):
  - Google Fonts (Inter, DM Mono)
  - Chart.js 4.4.1 from cdnjs
- Works on Vercel free (Hobby) plan
