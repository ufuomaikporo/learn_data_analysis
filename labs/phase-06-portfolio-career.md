# Phase 6 Lab — Portfolio and Career

[Schedule](../weekly-schedules/phase-06-portfolio-career.md) · [Project briefs](../projects/README.md) · [Career progression](../04-career-progression.md)

Use the work already created. Preserve the original CSVs and store repaired/test data as separate copies; do not overwrite source files during audits. Save a dated checklist and distinguish a genuine external review from a self-review. Never publish personal, employer or confidential data.

## Week 27 — Project A audit

1. Check that the SQLite import and scripts run in order on a fresh database, and that data quality checks surface exceptions in [finance_monthly_unclean.csv](../data/finance_monthly_unclean.csv). Keep Project A results based on the clean [finance_monthly.csv](../data/finance_monthly.csv).
2. Compare Q1 and monthly figures, plus January Retail, across SQL and Power BI. Review relationship cardinality and filter propagation.
3. List missing evidence, repair the highest-impact defect, and rerun the affected checks.

## Week 28 — Project A packaging

1. Write a README with audience, question, data source, grain, definitions, tools, run steps, findings and limitations.
2. Save SQL scripts, PBIX, model diagram, screenshots and reconciliation. Explain how to repoint and refresh the input on another machine.
3. Run instructions from a clean project folder. Publish only synthetic/authorized data and label this as independent work.

## Week 29 — Project B audit

1. Compare workbook and pandas outputs against SQL, including Q1, monthly profit and January Retail.
2. Review sign conventions, denominator handling and quality checks. Document any discrepancy and its fix.
3. Independently hand-calculate one segment/month and trace it to source rows.

## Week 30 — Project B analysis

1. Rank the month-segment favorable variances and reconcile them to the total profit variance. Document both favorable and unfavorable cases.
2. Run duplicate/missing-row tests using [finance_monthly_unclean.csv](../data/finance_monthly_unclean.csv), and test zero-denominator behavior with a separate test input. Make errors visible and preserve the clean project baseline.
3. Write the decision memo with a descriptive finding, limitations, plausible but unverified explanations and next data request.
4. Refine the notebook, workbook and chart using the validated results. Keep the chart traceable to the calculation and preserve the clean project baseline.

## Week 31 — Project B packaging

1. Save workbook, notebook, CSV summary, chart and memo. Document versions, environment setup, working directory and output locations.
2. In a fresh environment where feasible, restart and run the notebook top-to-bottom. Reopen and refresh the workbook from a clean data copy; record actual results.
3. Check project links and privacy, then compare against the [shared rubric](../projects/README.md).

## Week 32 — Portfolio review and applications

1. Present each project in two minutes: question, approach, check, finding, limitation and next step.
2. Ask a reviewer for clarity and reproducibility feedback if possible; otherwise conduct and label a self-review. Record and address meaningful issues.
3. Publish Project B when ready. Tailor applications to roles whose requirements match your demonstrated skills; apply earlier if already ready.

## Week 33 — SQL and Excel interview

1. Set a timer and independently write a joined, grouped query and a running-profit window query. Validate counts and results after the timer.
2. Recreate a budget/actual Excel summary and explain a favorable expense variance and undefined percentage.
3. Log elapsed time, errors, corrections, and one specific practice goal. Do not invent interview scores or employer feedback.

## Week 34 — BI and Python interview

1. Explain the star schema and a DAX measure under a month/segment filter. Show the January Retail result and the reason category filter behavior needs attention.
2. Recreate a pandas groupby/merge with uniqueness and missing-value checks; explain how a bad lookup can inflate totals.
3. Practise explaining a refresh failure, missing value, and duplicate key; document resolution steps.

## Week 35 — Finance case and stakeholder conversation

1. Prepare a five-minute variance case using the synthetic data. State the decision, observed figures, favorable/unfavorable signs and missing context.
2. Practise responding to questions about profit versus cash flow, uncertainty and next steps.
3. Run a mock interview with a person if available; otherwise self-record. Capture actual feedback or clearly mark self-assessment.

## Week 36 — Final gate and next steps

1. Independently follow each project's setup from a clean copy and verify all rubric checks. Repair broken links, stale instructions or unexplained discrepancies.
2. Review a current set of relevant postings and tailor resume bullets with truthful scope. Clearly label synthetic portfolio projects and distinguish them from paid experience.
3. Record applications, target roles, a 90-day learning plan and the chosen optional specialization only if it fits your interests.
4. Complete the [final tracker gate](../05-study-tracker.md). A completed roadmap is evidence of practice, not a guarantee of hiring.
