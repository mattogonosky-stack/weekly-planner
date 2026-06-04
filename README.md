# Weekly Focus Planner

A work week planner hosted on GitHub Pages, backed by Supabase (homebasefinances project).

## Features
- **3-column task board** — Primary / Secondary / Monitor & Learn
- **Copilot import** — paste any Copilot plan, auto-parses bullets and assigns focus areas
- **Copy Week Forward** — rolls non-done tasks to next week in one click
- **Finance sidebar** — live bill summary, upcoming bills (next 14 days), and vacation fund progress from homebasefinances DB
- **Supabase auth** — sign in with your homebasefinances account

## Hosted URL
Once deployed: `https://<your-github-username>.github.io/weekly-planner/`

## Setup

### 1. Create GitHub repo
```bash
git init
git add .
git commit -m "Initial weekly planner"
git remote add origin https://github.com/<your-username>/weekly-planner.git
git push -u origin main
```

### 2. Enable GitHub Pages
- Go to repo Settings → Pages
- Source: **Deploy from a branch**
- Branch: `main` / `/ (root)`
- Save — site will be live in ~60 seconds

### 3. Add redirect URI in Supabase
- Go to Supabase → Authentication → URL Configuration
- Add `https://<your-username>.github.io` to **Redirect URLs**

### 4. Sign in
- Use your existing homebasefinances Supabase account email/password
- Or create a new account from the sign-in screen

## Tech
- Pure HTML/CSS/JS — no build step, no framework
- Supabase JS v2 (CDN)
- Tables: `planner_tasks`, `planner_weeks`, `planner_wins`, `planner_blockers`
- Reads from existing: `bills`, `workspaces`, `vacation_log`
