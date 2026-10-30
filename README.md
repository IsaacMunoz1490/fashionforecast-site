# Fashion Forecast — Website

Marketing and legal site for the Fashion Forecast iPhone app.
Hosted on GitHub Pages. No build step, no dependencies — pure HTML.

## File structure

```
fashion-forecast-site/
├── index.html      ← Home / landing page
├── assets/         ← Logo and app screenshots used by index.html
│   ├── fashion-forecast-logo.png
│   ├── wardrobe.png
│   ├── shuffle.png
│   ├── week.png
│   └── pack.png
├── privacy.html    ← Privacy Policy  (submit URL to Apple)
├── terms.html      ← Terms of Use
├── support.html    ← Support page    (submit URL to Apple)
└── README.md
```

## Before you publish

1. Open **privacy.html** and **support.html** — replace `hello.fashionforecast@gmail.com`
   with whatever support email you create.
2. Open **index.html** footer — confirm the copyright name is correct.
3. Update the `Effective:` date in privacy.html and terms.html if needed.

## Deploy to GitHub Pages

1. Create a new **public** GitHub repo (e.g. `fashion-forecast-site`)
2. Push all files to the `master` branch root
3. Go to repo → **Settings → Pages**
4. Source: `Deploy from a branch` → Branch: `master` / `/ (root)` → Save
5. The site is live at `https://getfashionforecast.com/` (custom domain).

The `CNAME` file in the repo root holds the custom domain. Don't delete it,
and pull before pushing so it isn't overwritten. DNS is on Cloudflare
(4 GitHub Pages A records + `www` CNAME, all DNS only).

## Apple URLs to submit

| Field               | URL                                                                 |
|---------------------|---------------------------------------------------------------------|
| Privacy Policy URL  | `https://getfashionforecast.com/privacy.html`  |
| Support URL         | `https://getfashionforecast.com/support.html`  |
| Marketing URL       | `https://getfashionforecast.com/`              |

## When you add sync / Supabase

Update `privacy.html` before shipping sync — add sections for:
- Account data (photos, items stored server-side)
- Sign in with Apple
- Data deletion (required by Apple once accounts exist)
- Data retention policy

---
Built with ♻️ plain HTML — no framework, no build tools.
