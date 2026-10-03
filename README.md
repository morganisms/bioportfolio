# BioPortfolio

A single-file web app for scoring and prioritizing a biotech / diagnostics project portfolio.

**Run it:** download `bioportfolio.html` and open it in any modern browser. There's no install and no server.

## Features

- **Portfolio**: ranked table with an overall rank, value score and priority (High / Medium / Low). You can sort columns and filter by project type. Mandatory (compliance-required) projects are listed separately and not ranked.
- **Prioritization matrix**: X-axis is the value score and Y-axis is execution confidence (configurable). Hover a point for details or click it to edit.
- **Add / edit project**: 1–5 scoring with written definitions for each score, an optional scoring rationale, and a live score preview.
- **Admin**: rename the five criteria and edit their descriptions, 1/3/5 score definitions and weights. You can also set the Y-axis criterion, priority thresholds and project types.
- **Excel**: download a template (with a criteria guide), import projects, and export the ranked portfolio.
- **Backup**: export your portfolio and configuration to JSON and restore it later.

## Default scoring model

| # | Criterion | Weight | Role |
|---|-----------|--------|------|
| 1 | Strategic fit | 25% | Value score |
| 2 | Clinical / patient impact | 30% | Value score |
| 3 | Commercial value | 30% | Value score |
| 4 | Urgency / time-criticality | 15% | Value score |
| 5 | Execution confidence | — | Matrix Y-axis only |

Value score = weighted average of the value criteria, scaled from 20 (all 1s) to 100 (all 5s). Default thresholds: High ≥ 75, Medium ≥ 50.

The Commercial value revenue bands are placeholders. Calibrate them to your business before use.

## Data

Data is stored in the browser's local storage, so it stays on your machine. Export a JSON backup regularly. Excel import and export load SheetJS from cdnjs, which needs an internet connection; CSV import works offline.
