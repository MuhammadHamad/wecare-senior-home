# We Care Senior Home Care

Static one-page website for We Care Senior Home Care, a non-medical in-home senior care provider serving Lawrenceville, Duluth, Suwanee, Buford, and Gwinnett County, GA.

Built as a single self-contained `index.html` (no build step, no dependencies). Fonts load from Google Fonts; everything else is inline.

## Deploy

### Option A — GitHub + Vercel (recommended for ongoing edits)

```bash
git init
git add .
git commit -m "We Care Senior Home Care website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/wecare-senior-home.git
git push -u origin main
```

Then in Vercel: Add New Project, import the repo, deploy.
- Framework preset: Other
- Build command: none
- Output directory: root (leave default)

Every `git push` to `main` redeploys automatically.

### Option B — Drag and drop (fastest)

Drag this folder onto the Vercel new-project screen. It deploys instantly.

## Custom domain

To use `wecareseniorhome.com`, add it in Vercel under Project, Settings, Domains, then set the DNS records Vercel shows you at the domain registrar. Keep the existing site live until this one is confirmed working.

## Before going live (owner to complete)

These are marked with `Owner:` comments inside `index.html`:

1. Replace the hero photo placeholder with a real caregiver/client photo.
2. Paste three real Google reviews and the reviewer first names.
3. Add the real Google review link to the "Read all reviews" button.
4. Add "Licensed, bonded, and insured" and "Background-checked caregivers" ONLY once verified true.

## Known follow-up

The contact form currently opens the visitor's email app via `mailto:`. For reliable lead capture, replace it with a Formspree endpoint or a Vercel serverless function after launch.

## Files

- `index.html` — the website
- `vercel.json` — clean URLs and basic security headers
