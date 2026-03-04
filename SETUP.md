# Landing Page Setup

## Images to Add

Copy these into `website/images/`:

1. **`app-icon.png`** — Already copied from app-store-assets
2. **`app-store-badge.svg`** — Placeholder included. Replace with the official badge from [Apple's Marketing Resources](https://developer.apple.com/app-store/marketing/guidelines/) for production
3. **`screenshot-1.png` through `screenshot-5.png`** — Pick your 5 best App Store screenshots (use the 6.3" versions for best fit)
4. **`og-image.png`** (optional) — 1200x630 social share image for link previews

## Update Before Launch

1. **App Store URL** — Replace `https://apps.apple.com/app/little-things/id0000000000` (appears twice in index.html) with your real App Store link once the app is live
2. **Privacy Policy / Support links** — Already pointing to your GitHub gists

## Deploy to GitHub Pages

Option A — Separate repo:
```bash
cd website
git init
git add .
git commit -m "Landing page"
git remote add origin git@github.com:knollmcb81/littlethings-site.git
git push -u origin main
# Enable GitHub Pages in repo Settings → Pages → Branch: main
```

Option B — Same repo, `/docs` folder (replaces mkdocs site):
```bash
cp -r website/* docs/
# Push to main, GitHub Pages serves from /docs
```

Option C — Custom domain:
- Add a `CNAME` file with your domain (e.g., `littlethingsapp.com`)
- Configure DNS to point to GitHub Pages

## Preview Locally

```bash
cd website
python3 -m http.server 8000
# Open http://localhost:8000
```
