# Project B — Excel + Python Variance Investigation

[Projects index](README.md) · [Data contract](../data/README.md) · [Phase 1 schedule](../weekly-schedules/phase-01-excel-finance.md) · [Phase 5 schedule](../weekly-schedules/phase-05-python.md)

**Question:** Which segment and month contributed most to the Q1 profit variance, and what should management investigate next?  
**Audience:** A finance business partner.

## Build

Keep all provided CSVs read-only; save the workbook, notebook, cleaned/test copies and generated outputs as separate project files. Create an Excel table with `SUMIFS`/PivotTables, budget/actual/favorable variance, and a clear chart. Build a Python notebook that reads the clean [finance_monthly.csv](../data/finance_monthly.csv), validates grain and missing data, groups the facts, and produces a report and plot. Reconcile both outputs with [Project A](project-a-sql-power-bi.md) and the [control totals](../data/README.md). Provide a management memo with calculated contributions, assumptions, competing explanations, and questions for a real data owner.

## Evidence

- Workbook with source, checks, and summary sheets.
- Clean-run notebook with environment and output instructions.
- CSV summary and chart.
- Decision memo.
- Reconciliation table and known limitations.

Test the separate [finance_monthly_unclean.csv](../data/finance_monthly_unclean.csv) fixture and document the detected issues without changing either source file. Do not use the unclean fixture for project calculations.

## Acceptance

- Q1 checks match.
- A segment/month result is independently hand-checked.
- Zero-denominator behavior is demonstrated on a separate test input; missing/duplicate-row behavior is tested with the unclean fixture. Neither test input changes the clean project data.
- Findings describe variance, not an asserted cause or real business effect.
