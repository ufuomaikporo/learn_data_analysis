# Phase 5 Lab — Python and pandas

[Schedule](../weekly-schedules/phase-05-python.md) · [Data contract](../data/README.md) · [Project B](../projects/project-b-excel-python.md) · [Worked solutions](../solutions/phase-05-python.md)

From your project root on Windows PowerShell, create an isolated environment and use the same interpreter for Jupyter:

```powershell
py -m venv .venv
.\.venv\Scripts\python.exe -m pip install pandas matplotlib jupyter
.\.venv\Scripts\python.exe -m jupyter lab
```

If `py` is unavailable, use your installed Python executable. These are learning-environment dependencies, not part of this roadmap's own installation. Record Python and package versions and the working directory. Keep the provided CSVs unchanged in a `data` subfolder; write cleaned copies, summaries and figures to separate output files or folders. Notebook relative paths depend on the notebook's working directory. Document the command and directory needed to run it.

## Week 21 — Fundamentals and financial functions

1. Work through W3Schools variables, types, lists, dictionaries, conditions and functions. Practise a small dictionary representing a segment/month.
2. Implement functions for profit and favorable variance using the definitions in the data contract. Define percentage to return `None` when the denominator is zero.
3. Test your functions against a hand-calculated month/segment and verify that revenue improvement and expense increase have opposite sign effects.
4. Save notebook and setup notes; do not use hidden notebook state as the only way to reproduce the result.

## Week 22 — Files, validation and errors

1. Read a copy of the CSV using Python's standard `csv` module. Check headers and parse dates/amounts; explain the difference between strings and numbers.
2. Raise or display clear errors containing row context for missing fields, invalid dates or invalid amounts. Never turn malformed amounts into zero.
3. Use [finance_monthly_unclean.csv](../data/finance_monthly_unclean.csv) as a separate faulty input; demonstrate validation failures and preserve both it and the clean [finance_monthly.csv](../data/finance_monthly.csv).
4. Record how to recover and rerun using the clean input.

## Week 23 — pandas ingestion and quality

1. Use `pandas.read_csv`, explicitly parse `month`, and inspect dtypes, shape and head. Check expected columns, NULLs, nonnegative amounts, valid categories, month starts, duplicate IDs and duplicate business keys.
2. Stop the baseline analysis with a clear error if checks fail. On [finance_monthly_unclean.csv](../data/finance_monthly_unclean.csv), show duplicate and missing-value detection; explain a possible remediation but do not silently discard rows.
3. Run the baseline row and category-count checks. Record pandas version and check output.

## Week 24 — Merge, group and reconcile

1. Load [segment_lookup.csv](../data/segment_lookup.csv) as a DataFrame. Merge on `segment` with `validate="many_to_one"` and an indicator; fail explicitly if any row is unmatched. Confirm row count stays 12.
2. Group/pivot by month, segment and category; compute revenue and expense sums separately for budget and actual. Derive profit and favorable variances; retain names and units.
3. Export a segment-month summary to a separate outputs folder. Reconcile Q1, all monthly profits, and January Retail with Excel and SQL. Save the checks alongside the notebook.
4. Demonstrate that a duplicated lookup key fails validation in a test-only copy; leave [segment_lookup.csv](../data/segment_lookup.csv) unchanged.

## Week 25 — Visualize and investigate

1. Plot monthly actual versus budget profit with axes, CAD units, dates and a title. Save the figure to the outputs folder.
2. Sort month-segment favorable profit variance and show each contribution. Reconcile the results to the independent data controls.
3. Test a zero budget denominator separately and label its percentage undefined. Write a short memo with one observation, a limitation and a question for a data owner; do not infer a cause.

## Week 26 — Run from scratch

1. Restart the notebook kernel, run every cell in order and verify that outputs are created without reliance on a prior interactive session.
2. Record Python/package versions, input location, install and launch commands, output paths and checks. Test the instructions in a clean virtual environment or on a clean copy if feasible; record what was actually tested.
3. Preserve the workbook, notebook, exported summary, chart, quality-test evidence and management memo. Verify the [Project B rubric](../projects/project-b-excel-python.md) and [phase gate](../05-study-tracker.md).
