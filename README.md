# Squarecone Limited — Website

A static marketing site for Squarecone Limited ("Africa's Digital Solution"), built as plain HTML/CSS/JS — no build step required.

## Structure

```
index.html      Page markup and copy
styles.css      All styling (design tokens live at the top of the file)
script.js       Mobile nav toggle, footer year, contact form handling
assets/         Squarecone logo (logo.png / logo.jpeg)
vercel.json     Deployment config for Vercel
```

## Deploying to Vercel

**Option A — Vercel dashboard (no CLI)**
1. Go to https://vercel.com/new
2. Choose "Deploy" → drag and drop this whole folder, or connect it as a Git repository (push these files to a new GitHub repo first, then import it in Vercel).
3. Framework preset: choose **Other** (it's a static site — no build command needed).
4. Deploy.

**Option B — Vercel CLI**
```bash
npm i -g vercel
cd squarecone
vercel        # first deploy, follow the prompts
vercel --prod # promote to production
```

## Connecting www.squarecone.co

1. In the Vercel project → **Settings → Domains**, add `squarecone.co` and `www.squarecone.co`.
2. Vercel will show DNS records (usually an `A` record for the apex domain and a `CNAME` for `www`) — add these at your domain registrar.
3. Set `www.squarecone.co` as the primary domain if that's the one you want in the address bar; Vercel will redirect the other automatically.

## Things to update before launch

- **Contact form** — currently shows a message pointing people to email; it isn't wired to a real inbox. Easiest option: swap in a form service like Formspree or Vercel's own form handling, or add a small serverless function under `/api`.
- **Email address** — using `info@squarecone.co`; confirm this inbox is live before launch.
- **Phone number** — not included yet since none was provided; add it to the Contact section in `index.html` when available.
- **Drama Shots / Superwinnings links** — currently placeholder `#` links; swap in the live URLs once available.
- **Legal pages** — no privacy policy / terms links yet; add if required for NCA compliance or app store listings.
