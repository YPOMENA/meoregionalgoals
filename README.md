# YPO MENA Member Engagement — FY26–27 Goals & Action Plan

A single-page static site tracking the MENA Regional Member Engagement
FY26–27 SMART goals, synced from the team's Monday.com board.

No build step, no dependencies — it's one static HTML file
(`index.html`) with inline CSS/JS. Task checkmarks, added tasks,
owner/date edits, and comments are stored in the visitor's own
browser (localStorage), so each person who opens it keeps their own
copy of progress — nothing is shared between devices or synced back
to Monday.com automatically.

## Push to GitHub

```bash
git init
git add .
git commit -m "Initial commit: MENA member engagement FY26-27 site"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

## Deploy on Vercel

**Option A — via the Vercel dashboard**
1. Go to https://vercel.com/new
2. Import the GitHub repo you just pushed.
3. Framework preset: choose "Other" (it's a static site, no build
   command needed).
4. Click Deploy.

**Option B — via the Vercel CLI**
```bash
npm i -g vercel
vercel
```
Follow the prompts (link to a new project, accept the defaults —
no build command, output directory is the project root).

## Updating the content later

- Task text, owners, and due dates baked into the page live inside
  the `GOALS` and `HOUSEKEEPING` JavaScript objects near the bottom
  of `index.html`.
- If your Monday.com board changes significantly, export it again
  (Excel/CSV) and ask Claude to regenerate `index.html` from the new
  export, then push the updated file.
