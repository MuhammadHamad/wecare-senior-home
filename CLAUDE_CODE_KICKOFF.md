# Kickoff prompt for Claude Code

Open a terminal in this project folder, run `claude`, then paste the prompt below.
Claude Code reads CLAUDE.md automatically, so it already has the full context.

---

## Deploy prompt (paste this)

This is a static one-page site (vanilla HTML, no framework — keep it that way). I want
to put it on GitHub and deploy to Vercel. Please:

1. Initialize git, make a first commit, create a GitHub repo named `wecare-senior-home`,
   and push to main. Pause and let me approve the GitHub login when prompted.
2. Deploy to Vercel with the CLI. Pause and let me approve the Vercel login. Give me the
   live preview URL when it's done so I can confirm it works before anything else.
3. Do NOT touch DNS or the custom domain yet — I'll tell you when.

Walk me through each auth step as we hit it.

---

## Follow-up prompts (use after the site is live)

**Real contact form:**
> Replace the mailto contact form with a Vercel serverless function in /api that emails
> submissions to seniorcarewecare@gmail.com. Keep the front end as plain HTML/JS.

**Custom domain (only when ready to switch):**
> I'm ready to point wecareseniorhome.com at this. Add the domain in Vercel and give me
> the exact DNS records to set at my registrar. Confirm the Vercel URL works before we cut over.

**Multi-page SEO build (the big growth lever):**
> Split this into separate pages, keeping everything vanilla HTML: one page per service
> (personal care, companion care, respite care, meal prep, medication reminders,
> mobility/transportation) and one page per city (Lawrenceville, Duluth, Suwanee, Buford).
> Each page needs its own title tag and H1 in the "[service] in [city] GA" pattern, plus
> internal links back to the homepage and contact section. Reuse the existing styles.
