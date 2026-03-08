# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is "The Infrastructure & Operations Academy" — a curated, self-paced curriculum mapping infrastructure/ops career skill tracks to industry certifications with pricing, free resources, study guides, and progress tracking. The site lives at [infraopsacademy.com](https://infraopsacademy.com/). Content lives in both `README.md` (single-page GitHub view) and `docs/` (MkDocs Material site).

## Repository Structure

- `README.md` — The entire academy content (single-page view for GitHub)
- `docs/` — MkDocs site pages (same content, split into separate pages)
- `docs/index.md` — Site homepage with stats and track summary table
- `docs/tracks/` — Individual skill track pages (13 tracks)
- `docs/certifications.md` — Certification quick reference table
- `docs/CNAME` — Custom domain (infraopsacademy.com)
- `mkdocs.yml` — MkDocs Material theme configuration
- `CONTRIBUTING.md` — Contributor guidelines
- `.github/ISSUE_TEMPLATE/` — Templates for suggesting certs, resources, and reporting issues
- `.github/workflows/deploy-docs.yml` — Auto-deploys MkDocs site to GitHub Pages on push to main

## Key Conventions

### README Structure (in order)
1. Centered header with shields.io provider badges and stats line
2. Table of Contents (two rows: sections + skill tracks)
3. "How to Use This Repo" section
4. Numbered skill tracks (currently 13), each as a `###` heading
5. Certification Quick Reference table (all certs in one table)
6. Total Cost Per Track summary table
7. Saving Money tips
8. Free or Low Cost Resources (courses, YouTube, labs subsections)
9. Recommended Reading (books with links)
10. Community (Reddit, Discord/Slack, Podcasts)
11. Contributing, Support, License

### Formatting Rules
- Use **unicode emojis** in README section headings (not GitHub shortcodes like `:emoji:`)
- Skill tracks use `### N. Track Name` headings in README
- Certifications use `- [ ]` checkboxes with `[Cert Name](official-link) — $cost` format
- Provider badges use shields.io `?style=flat` format
- Books link to Amazon for paid, original source for free online books

### When Adding Content
- Update the stats line in the README header (cert count, track count, total cost, resource count)
- Update both the Quick Reference table AND the Cost Per Track table
- Update both `README.md` AND the corresponding `docs/` page
- Update `docs/index.md` track summary table and `docs/certifications.md`
- Add relevant provider badges to the header if introducing a new provider
- Add free resources to the "Free or Low Cost Resources" section when applicable
- Keep Atlassian certs ordered by ACP number
- Exclude certs with unpublished/unavailable pricing

### Study Guides
- Each track has a "Study Guides" section with book recommendations
- Publishers: Sybex (CompTIA/AWS), O'Reilly (cloud-native/DevOps), Pearson (Red Hat)
- All books link to Amazon
- Format: `[*Book Title*](amazon-link) — Author (Publisher, Edition, Year)`

### MkDocs Site
- Site URL: `https://infraopsacademy.com/` (custom domain via Route 53 + GitHub Pages)
- Theme: Material for MkDocs with light/dark mode toggle, tabbed navigation, search, footer
- Auto-deploys via GitHub Actions on push to `main`
- Navigation is defined in `mkdocs.yml` under the `nav` key
- Uses admonitions (`!!! note`, `!!! tip`) instead of blockquotes for callouts

### GitHub Details
- Remote: `https://github.com/SamuelTillman/infra-ops-academy`
- Branch protection is enabled on `main` (PRs required for contributors, admin bypass enabled)
- Labels include: `good first issue`, `enhancement`, `certification`, `help wanted`
