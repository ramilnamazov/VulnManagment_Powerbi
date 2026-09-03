# US Infrastructure Vulnerability Dashboard

**[Live demo →](https://ramilnamazov.github.io/VulnManagment_Powerbi/)**

A Power BI-style vulnerability management dashboard, rebuilt as a single self-contained HTML file so anyone can open it in a browser — no Power BI license, no data gateway, nothing to install. Built to show what a security/IT team would actually look at day to day: what's critical, what's overdue, and what's on the CISA KEV list.

All data is **synthetic** — generated to look and behave like a real vuln-management export, with no real assets, hosts, or CVEs tied to any organization.

## What's in it

- **Vulnerability Overview** — KPI tiles (open findings, critical/high counts, CISA KEV exposure), severity breakdowns, and asset-tag distribution (US Managed / Non-US Managed / Tangerine)
- **Regulatory & Compliance** — compliance posture and SLA tracking against remediation targets
- **Patch History (7 days)** — rolling view of recent patch activity

## Why it's interactive, not a screenshot

- **Click-to-filter KPI tiles** — click a tile (e.g. "CISA KEV") and the rest of the dashboard filters to it, the way Power BI cross-filtering works
- **Filter chips** — active filters show as removable chips along the top
- **Tabbed pages** — Overview / Compliance / Patch History, like separate Power BI report pages
- Runs entirely client-side: plain HTML/CSS/JS, no build step, no external libraries, no backend

## Run it locally

Just open `index.html` in any browser — or clone the repo and double-click the file:

```bash
git clone https://github.com/ramilnamazov/VulnManagment_Powerbi.git
cd VulnManagment_Powerbi
start index.html   # macOS: open index.html
```

## Stack

HTML5, CSS3, vanilla JavaScript. Styled to match the Power BI / Fluent UI look and feel (Segoe UI, Fluent color tokens, report-page chrome).
