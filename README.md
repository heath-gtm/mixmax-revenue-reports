# Mixmax Revenue Reports

Archive of Mixmax GTM revenue reports — weekly, monthly, and quarterly — published to GitHub Pages and mirrored to a Notion archive database.

## Live site

[heath-gtm.github.io/mixmax-revenue-reports/](https://heath-gtm.github.io/mixmax-revenue-reports/)

## Structure

```
/
├── index.html                  # Landing — latest of each frequency
├── weekly/
│   ├── index.html              # Weekly archive index
│   └── YYYY-MM-DD-{type}-v{N}.html       # Versioned report
│   └── YYYY-MM-DD-{type}-latest.html     # Mirror of the current version
├── monthly/
│   ├── index.html              # Monthly archive index
│   └── YYYY-MM-{type}-v{N}.html
│   └── YYYY-MM-{type}-latest.html
├── quarterly/
│   ├── index.html              # Quarterly archive index
│   └── QN-YYYY-{type}-v{N}.html
│   └── QN-YYYY-{type}-latest.html
└── assets/
    ├── style.css               # Shared stylesheet for index pages
    └── *.png                   # Workflow diagrams + chart images
```

## Report types

| Code | Meaning | Frequencies |
| --- | --- | --- |
| `gtm` | GTM Leadership Report (org-wide) | Weekly, Monthly, Quarterly |
| `cro` | CRO Report (CRO-only) | Weekly, Monthly, Quarterly |
| `tldr` | Weekly TL;DR | Weekly |
| `ahead` | Month-Ahead / Quarter-Ahead Plan | Monthly, Quarterly |
| `wrapup` | Period Wrap-Up | Monthly, Quarterly |
| `board` | Board Snapshot | Quarterly |

## Versioning

Every report starts at `v1`. If a report is republished for the same period (corrected data, late edits), the version auto-increments and the older `-v{N-1}.html` remains in place for audit. `-latest.html` always points at the highest version. The Notion archive mirrors this with `Version`, `Is Latest`, and `Archive State` (Current / Superseded) fields.

## How reports are published

1. Primary: commit versioned HTML to this repo → served via GitHub Pages.
2. Backup: full rendered content mirrored into the [HTML Report Archive](https://www.notion.so/mixmax/HTML-Report-Archive-89fc45e4dc1443aab88d19bc5481b308) Notion database.
3. Index: a bullet is appended to the corresponding parent page (Weekly / Monthly / Quarterly Performance Reports) linking to both.

Publishing is automated via the `mixmax-weekly-gtm-report`, `mixmax-monthly-gtm-report`, and `mixmax-quarterly-gtm-report` Cowork plugins.
