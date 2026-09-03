# US Infrastructure Vulnerability Dashboard

**[Open the live dashboard →](https://ramilnamazov.github.io/VulnManagment_Powerbi/)**

A Power BI-style vulnerability management dashboard, rebuilt as a single self-contained HTML file so anyone can open it in a browser — no Power BI license, no data gateway, nothing to install. Built to show what a security/IT team would actually look at day to day: what's critical, what's overdue, and what's on the CISA KEV list.

![Clicking a bar cross-filters the whole dashboard, and switching pages keeps the filter applied](assets/dashboard-demo.gif)

All data is **synthetic** — generated to look and behave like a real vuln-management export, with no real assets, hosts, or CVEs tied to any organization.

## What's in it

| Vulnerability Overview | Regulatory & Compliance | Patch History (7 days) |
|---|---|---|
| ![Vulnerability Overview page](assets/overview.jpg) | ![Regulatory & Compliance page](assets/compliance.jpg) | ![Patch History page](assets/patch-history.jpg) |

- **Vulnerability Overview** — KPI tiles (open findings, critical/high counts, CISA KEV exposure), severity breakdowns, and asset-tag distribution (US Managed / Non-US Managed / Tangerine)
- **Regulatory & Compliance** — SLA breach aging by severity, a 12-month remediation trend, CISA KEV exposure, open risk exceptions (POA&M), and a scorecard mapped to FedRAMP, NIST SP 800-53, CMMC 2.0, OSFI B-13, and FFIEC
- **Patch History (7 days)** — daily patched-vs-pending activity, SLA outcome by severity, and a filterable patch activity log by business line

## Why it's interactive, not a screenshot

- **Cross-filtering** — click a bar, KPI tile, or table row and every chart on the page recalculates against that slice, exactly like Power BI's cross-filter behavior (see the GIF above)
- **Filters persist across pages** — filter on the Overview page, switch to Compliance or Patch History, and the same filter is still applied
- **Filter chips** — active filters show as removable chips along the top, with one-click "Clear all filters"
- **Real drill-down tables** — Top Hosts, Top Vulns, CISA KEV Exposure, Risk Exceptions (POA&M), and a 1,000+ row Patch Activity Log, all filterable
- **CSV export** — "Export filtered rows" dumps the currently filtered slice
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
