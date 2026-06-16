# Project context for Claude Code

## What this is
A static one-page marketing website for **We Care Senior Home Care**, a non-medical
in-home senior care provider serving Lawrenceville, Duluth, Suwanee, Buford, and
Gwinnett County, GA. Phone: (404) 317-4137. Email: seniorcarewecare@gmail.com.

The whole site is a single self-contained `index.html`. No build step, no framework,
no dependencies. Fonts load from Google Fonts; all CSS and JS are inline. Keep it
this way unless explicitly told otherwise (see "Tech decisions" below).

## Files
- `index.html` — the entire website
- `vercel.json` — clean URLs + basic security headers
- `README.md` — human deploy notes
- `CLAUDE.md` — this file

## Tech decisions (do not change without asking)
- **Stay vanilla HTML/CSS/JS.** This is a brochure site. Do NOT migrate to Next.js,
  React, or any framework. No bundler, no node_modules. The value here is zero
  dependencies and long-term durability.
- Hosting is **Vercel**. `index.html` is served at the root automatically.
- If a contact form backend is needed, use a single Vercel serverless function in
  `/api` (plain JS) or a Formspree endpoint. Do not add a framework for this.

## Deployment tasks (the human will approve auth prompts)
1. `git init`, commit, create the GitHub repo, and push to `main`.
2. Deploy to Vercel (CLI `vercel` / `vercel --prod`, or the dashboard import).
3. Pause for the human at: GitHub login/OAuth, Vercel login/OAuth, and any DNS change.
   Run the commands; let the human click the approvals.
4. For the custom domain `wecareseniorhome.com`: deploy and confirm the Vercel URL
   works FIRST, then do the DNS cutover, so the live site never goes dark.

## Known follow-ups / open items
- The contact form currently uses a `mailto:` handler. Replace with a real handler
  (Vercel serverless function or Formspree) for reliable lead capture. Recommended
  first post-launch task.
- Multi-page SEO build (next big lever): split into separate pages — one per service
  (personal care, companion care, respite care, etc.) and one per city (Lawrenceville,
  Duluth, Suwanee, Buford), each with its own title/H1 in the "[service] in [city] GA"
  pattern. Keep each as a plain `.html` page.

## Owner placeholders still in index.html (do NOT invent these)
Search the file for `Owner:` comments. These need real input before going fully live:
1. Hero photo (replace the placeholder block with a real caregiver/client photo).
2. Three real Google reviews + reviewer first names (never fabricate reviews).
3. The real Google review link on the "Read all reviews" button.
4. "Licensed, bonded, and insured" and "Background-checked caregivers" lines —
   add ONLY if verified true. These are deliberately omitted as a liability matter.

## Guardrails
- Do not publish unverified trust/credential claims (licensing, insurance, background checks).
- Do not invent reviews, addresses, or business facts.
- Keep NAP (name, address/service-area, phone) identical across the site and any
  listings you touch.
