# Hello, I'm Adriano Velazquez

> A living record of offensive security practice: Hack The Box write-ups, industry certifications, and home-lab / project builds.

**Live site:** `https://Nano068.github.io/Security-Portfolio/` — replace `Nano068` after you push this repo (see [Getting it live](#getting-it-live) below).

---

## What's in here

| Folder | Contents |
|---|---|
| [`writeups/`](writeups/) | Hack The Box machine & challenge write-ups (methodology, not spoilers-before-retire where applicable) |
| [`certifications/`](certifications/) | Real-world certifications, with dates, verification links, and notes |
| [`projects/`](projects/) | Home lab / personal security projects — tools, detections, automations |
| [`scripts/`](scripts/) | Standalone scripts and utilities used across engagements and labs |
| [`labs/`](labs/) | Home lab architecture, network diagrams, and build logs |
| [`docs/`](docs/) | Source for the GitHub Pages site (the live portfolio front-end) |

Each folder has its own `README.md` explaining the format and a `TEMPLATE.md` (or template entry) to copy when adding new content.

## How to use this repo

1. Copy the relevant template (e.g. `writeups/htb-machines/TEMPLATE.md`) into a new file named after the box/cert/project.
2. Fill it in.
3. Add a row/entry to that folder's `README.md` index so it shows up in the table.
4. Commit and push — the GitHub Pages site pulls its "latest activity" list from these index files, so keep them current.

## Current status

<!-- STATS:START -->
| Category | Count |
|---|---|
| HTB Machines | 0 |
| HTB Challenges | 0 |
| Certifications | 0 |
| Projects | 1 |
<!-- STATS:END -->

*(Update this table as you add entries — or wire up the optional GitHub Action in `.github/workflows/` to do it for you.)*

## Getting it live

This repo ships with a static site in `docs/` for GitHub Pages, published at
`https://Nano068.github.io/Security-Portfolio/`. If Pages isn't already enabled on the
repo, turn it on once under **Settings → Pages → Build and deployment → Source:
Deploy from a branch → Branch: `main`, folder `/docs` → Save.**

## License

Write-ups describe methodology and lessons learned — no flags, no box credentials, and no content that violates the [Hack The Box terms of service](https://help.hackthebox.com/en/articles/5188925-hack-the-box-terms-of-service). See [`LICENSE`](LICENSE) for code/content licensing.
