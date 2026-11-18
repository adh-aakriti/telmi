# Telmi: landing page

## What this is
A one-page bilingual (EN/ES) landing page for a student project: a study
buddy that doesn't understand yet; students teach it out loud. The page
collects emails for a pilot with secondary schools (ESO/Bachillerato).

## Stack
- Single static file: index.html (plain HTML/CSS/JS, no build step)
- Live: https://telmi-pilot.vercel.app (Vercel project telmi-pilot, auto-deploys from main of github.com/adh-aakriti/telmi)
- Supabase (EU region) table `waitlist`, schema in supabase_setup.sql
- Form POSTs to Supabase REST with the public anon key (CONFIG block in the script)

## Rules
- Never put the service_role key or database password in any file.
- RLS: anon may INSERT only. Never add a SELECT policy for anon.
- Store only: email, role, lang, consent, created_at. No student data.
- Keep WCAG 2.1 AA: labels, focus styles, contrast, reduced motion.
- Keep EN and ES copy in sync (I18N object in index.html).
- Do not call the product an "AI tutor"; the student teaches, the AI learns.
- Product name: Telmi. The buddy is called Pip. App repo: https://github.com/jinin-alj/telmi (keep page claims in line with its README).
- Pip is drawn only from the app's brand files (assets/brand/pip in the app repo, copied to assets/pip here); never redraw it. The logo is Pip plus "telmi" in lowercase. favicon.png and apple-touch-icon.png are copies of the app's icons.
