# GitHub Issue Tracker — Cloud

Automated GitHub issue tracking for CSA Solutioning — monitors 14 repos every 30 min.

## What It Does

| Workflow | Schedule | Purpose |
|----------|----------|---------|
| **Issue Tracker** | Every 30 min | Detect new issues → ADO Bug + Email + Teams |
| **Dashboard** | Every 30 min + after tracker | Live dashboard on GitHub Pages |

## Live Dashboard

🔗 **https://ritesh-microsoft.github.io/Github_Tracking/**

## Architecture

- **GitHub REST API** → fetch issues (built-in `GITHUB_TOKEN`)
- **ADO REST API** → create Bug work items (PAT)
- **Logic Apps** → send email + Teams messages (no admin consent needed)
- **GitHub Pages** → host live dashboard
- **State** → JSON committed to repo
