# GitHub Pages Setup Guide

## Quick Setup (5 minutes)

### 1. Create GitHub Repository

```bash
# Authenticate with GitHub (one-time)
gh auth login

# Create the repository
gh repo create health-reports --public --source=/Users/admin/.openclaw/workspace/health-reports --remote=origin --push
```

Or manually:
1. Go to https://github.com/new
2. Repository name: `health-reports`
3. Make it **Public**
4. Click "Create repository"

### 2. Connect Local Repo to GitHub

```bash
cd /Users/admin/.openclaw/workspace/health-reports
git remote add origin https://github.com/YOUR_USERNAME/health-reports.git
git push -u origin main
```

### 3. Enable GitHub Pages

1. Go to your repo on GitHub
2. Click **Settings** → **Pages**
3. Source: Deploy from a branch
4. Branch: `main` → `/ (root)`
5. Click **Save**

Your report will be live at:
```
https://YOUR_USERNAME.github.io/health-reports/health-report-2026-02-09.html
```

## Automated Reports

Once set up, reports will automatically:
1. Generate HTML at 9:00 PM daily
2. Commit to git
3. Push to GitHub
4. Be available instantly via URL

## Report URLs

Reports are named by date: `health-report-YYYY-MM-DD.html`

Example:
- Today: `health-report-2026-02-09.html`
- Tomorrow: `health-report-2026-02-10.html`

Access pattern:
```
https://YOUR_USERNAME.github.io/health-reports/health-report-YYYY-MM-DD.html
```

## Features

✅ Beautiful mobile-friendly design
✅ Interactive charts embedded
✅ No images needed (self-contained)
✅ Instant loading
✅ Shareable links
✅ Permanent archive
