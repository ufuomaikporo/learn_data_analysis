# Project A — SQL + Power BI Financial Performance Dashboard

[Projects index](README.md) · [Data contract](../data/README.md) · [Phase 2 schedule](../weekly-schedules/phase-02-sql.md) · [Phase 3 schedule](../weekly-schedules/phase-03-power-bi.md)

**Question:** How did Q1 actual revenue, expense and profit compare with budget by month and segment?  
**Audience:** A finance manager deciding where to investigate.

## Build

Treat the provided CSVs as read-only; save database transformations, test variants and report outputs separately. Import the clean [finance_monthly.csv](../data/finance_monthly.csv) fixture and the [segment_lookup.csv](../data/segment_lookup.csv) lookup extract into the same SQLite database. The lookup file represents master/reference data; in production, it would typically be maintained as a source-system or warehouse table and may be delivered separately from the facts. Validate fact grain and types, preserve lookup-key uniqueness, and save annotated SQL for quality checks, monthly KPIs, segment variance, and a running profit calculation. Import clean facts and dimensions into Power BI; model a calendar and segment dimension, create measures using the [KPI contract](../data/README.md), and provide month and segment filters. Show revenue, expense, profit, favorable variance, and trends. Use [finance_monthly_unclean.csv](../data/finance_monthly_unclean.csv) only for isolated quality tests, not for dashboard results. Avoid many-to-many ambiguity and demonstrate that filters affect measures consistently.

## Evidence

- SQL import steps and scripts.
- Data/model diagram.
- PBIX, screenshots, and a short accessible findings summary.
- Measure definitions and cross-tool Q1/monthly reconciliation.
- One favorable and one unfavorable example.
- One-page recommendation with limitations.

Confirm totals remain correct for a filtered segment and month. This is a financial-performance dashboard, not a banking transaction or customer segmentation analysis.

## Acceptance

- 12 clean baseline rows; use the unclean fixture only for isolated quality tests.
- Q1 revenue 599,000 CAD, expense 342,000 CAD, profit 257,000 CAD, and favorable profit variance 10,000 CAD.
- Explain why expense favorable variance reverses the sign.
- Repeat checks without filters and on at least one month/segment slice.
