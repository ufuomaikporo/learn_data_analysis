# Portfolio Projects

[Roadmap overview](../README.md) · [Data contract](../data/README.md) · [Phase 6 schedule](../weekly-schedules/phase-06-portfolio-career.md)

The roadmap builds two complementary projects from the same small synthetic dataset:

- [Project A — SQL + Power BI financial performance dashboard](project-a-sql-power-bi.md)
- [Project B — Excel + Python variance investigation](project-b-excel-python.md)

Apply project work after the relevant topic and guided lab, and reserve week/phase gates for integration and review. Schedules use Project Work only for a distinct application, review or milestone; they do not repeat the lab task as another assignment. The project briefs define the complete portfolio deliverables and final acceptance criteria.

Both projects use the clean [finance_monthly.csv](../data/finance_monthly.csv) starter dataset so their results can be reconciled across tools. Project A also uses the separate [segment_lookup.csv](../data/segment_lookup.csv) lookup table; it is dimension data, not a copy of the finance facts. The separate [finance_monthly_unclean.csv](../data/finance_monthly_unclean.csv) is only for designated cleaning practice and isolated quality tests; do not use it to calculate project findings. Separate project fact datasets are not needed.

The starter data does not support bank transaction, credit, or customer-segmentation claims. Optional public data can strengthen breadth if its permission, definition, extraction date, and transformations are documented.

## Shared quality bar

Each project includes a README with business question, audience, scope, setup and run steps, tools/versions, source and license, data dictionary, KPI definitions, checks and results, findings, limitations, and next action. Include reproducible source files and images of visual outputs. Specify that work is independent, not a client engagement. Do not publish private data or credentials. Verify links, a fresh-copy run, and Q1 control totals before publishing.

## Optional extension after the foundation

Choose **one**: FP&A forecast with scenarios and three-statement links; risk/credit monitoring with a properly sourced labeled loan dataset and governance limitations; or investment performance with documented price/return conventions. Verify data licensing and whether the dataset supports each metric. Advanced risk and quant work needs additional statistics, validation, and potentially education; a toy model is not approved for lending or trading.
