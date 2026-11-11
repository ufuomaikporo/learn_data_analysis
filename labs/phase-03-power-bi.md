# Phase 3 Lab — Power BI Modeling and Reporting

[Schedule](../weekly-schedules/phase-03-power-bi.md) · [Data contract](../data/README.md) · [Project A](../projects/project-a-sql-power-bi.md) · [Worked solutions](../solutions/phase-03-power-bi.md)

Use local Power BI Desktop and a copy of the fixture. Keep provided CSVs read-only; save transformed queries and test data separately from the source files. The sample is synthetic and safe to share, but check terms and avoid uploading unrelated/private data. A local PBIX and screenshots suffice; a cloud account or paid sharing is not required.

## Week 11 — Import and quality

1. Get data from the CSV; name the imported table `Finance`. Set `month` to Date, amounts to decimal/fixed decimal, and other columns to appropriate types. Inspect Power Query errors and missing values.
2. Check row count, category counts, unique IDs and unique month/segment/category combinations. Record any transformation and refresh from the unchanged source.
3. Do not silently drop bad rows or replace missing amounts with zero; isolate test data when experimenting.

## Week 12 — Model the grain

1. Inspect the source and propose a fact-table grain, keys and dimensions appropriate for monthly finance reporting.
2. Implement the model and document relationship cardinality, filter direction, slicer fields and any ambiguous paths.
3. Sketch the model, identify keys and grain, and test that the fact count and category totals do not increase after filtering. Document source and refresh behavior for each dimension.

## Week 13 — Measures and checks

Adapt table/column names to your model.

1. Create actual revenue and expense measures.
2. Create budget revenue and expense measures, then actual and budget profit measures. Check signs against the KPI contract.
3. Add revenue and expense favorable variance measures and percentage variance. Format currency and percentage appropriately.
4. Verify full Q1 and January Retail controls under date and segment filters. If adding a category filter, test and document how it interacts with the measures.
5. Test percentage behavior with a zero budget-profit denominator in a separate test model or measure. Record the observed result and do not claim an undefined value is zero.

## Week 14 — Report design

1. Add cards for actual/budget profit and favorable variance, a monthly profit trend, and a segment variance visual. Use clear labels, CAD units, a readable palette, and a visible reporting period.
2. Add date and segment slicers from dimensions. Check January Retail against your independently calculated controls.
3. Add text explaining that values are simulated and that favorable expense variance has the opposite sign from raw expense variance. Test interactions and empty selections.

## Week 15 — Exceptions and storytelling

1. Import [finance_monthly_unclean.csv](../data/finance_monthly_unclean.csv) as a separately named test query. Use Power Query or explicit quality checks to identify data-quality issues; leave the clean [finance_monthly.csv](../data/finance_monthly.csv) unchanged and out of the test transformations.
2. Create a reconciliation table for Excel, SQL and Power BI: quarter controls, three monthly profits, and January Retail. Resolve mismatches rather than adjusting displayed totals.
3. Write a concise recommendation about what to investigate, not an invented explanation. State sample size, grain, incomplete financial scope and uncertainty. Record real review feedback, or label it self-review.

## Week 16 — Handoff

1. Save PBIX, model sketch, measure definitions, SQL scripts, screenshots and a README. Explain how to replace/repoint the CSV source when opening on a different computer and then refresh.
2. Open a copy from a clean project folder, refresh and recheck totals and a filtered slice. Document Desktop version and any limitations.
3. Give a two-minute walkthrough and complete the [Project A acceptance criteria](../projects/project-a-sql-power-bi.md). Publish only when the project is reproducible and ready.
