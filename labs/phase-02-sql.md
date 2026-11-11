# Phase 2 Lab — SQLite and Finance Queries

[Schedule](../weekly-schedules/phase-02-sql.md) · [SQL tutorial](https://www.w3schools.com/sql/) · [Data contract](../data/README.md) · [Worked solutions](../solutions/phase-02-sql.md)

Work in a project folder containing a copy of the `data` directory. Treat the provided CSVs as read-only; save test variants and transformed outputs separately. Install the [SQLite command-line tools](https://www.sqlite.org/download.html), note the version, and start `sqlite3 finance.db` from that folder. Paths in the dot-command below are relative to that working directory; use the actual location if different. Save the SQL and import command in your own setup instructions. `.import` is an SQLite shell command, not SQL; other database clients may have different import workflows.

## Week 5 — Create and import

Create a `finance` table with an appropriate primary key, required fields, type/value constraints and a unique business key, then import the clean [finance_monthly.csv](../data/finance_monthly.csv) into it. Week 7 adds `segment_lookup` to this same `finance.db`. Dates are ISO text here; validate their shape/month-start separately. The shell's `.import` handling and options are documented in the [SQLite CLI guide](https://www.sqlite.org/cli.html). Do not rerun setup in a populated database; use a fresh database for a clean run.

1. Import the clean CSV into `finance`. If import fails, stop and fix the path, SQLite version or input; do not proceed with an empty database.
2. Filter by month and category, inspect imported values and types, and validate that ISO date text represents month starts.
3. Save the setup, import command and basic queries in clean-run instructions.
4. Start from a fresh database and reproduce the row-count and January Retail slice checks against the data contract.

## Week 6 — Group and reconcile

1. Write a grouped query by month and segment that separately aggregates revenue and expense for actual and budget.
2. Subtract expense from revenue for actual/budget profit; calculate favorable profit variance as actual minus budget profit. Use the same filter conditions for each measure.
3. Aggregate the full quarter and reconcile revenue, expense, profit and favorable profit variance to the independent controls. Check each monthly control.
4. Handle zero denominators in percentage calculations without reporting them as zero. Explain why an undefined ratio is not the same as zero.

## Week 7 — Keys and joins

1. In the existing `finance.db` alongside the finance facts, import [segment_lookup.csv](../data/segment_lookup.csv) into a `segment_lookup` table with `segment` as the primary key and `segment_description` as its descriptive label.
2. Left join facts to the lookup on segment; compare the joined row count with the base and find facts with no lookup. Group by segment to compare pre- and post-join sums.
3. In an isolated test copy, compare inner and left joins with an unmatched segment. Test the effect of a duplicate lookup key and explain how to prevent fan-out; leave the shared [segment_lookup.csv](../data/segment_lookup.csv) unchanged.
4. Save the join query, unmatched-key check, and observed results.

## Week 8 — Data-quality checks and subqueries

1. Write checks for count, duplicate IDs, duplicate `(month, segment, category)` combinations, NULL/negative amounts, invalid categories, missing lookup keys and invalid/non-month-start dates. Inspect exceptions, not just totals.
2. Import [finance_monthly_unclean.csv](../data/finance_monthly_unclean.csv) into an unconstrained staging/test table. Run the checks and save the exception rows. Keep this table out of baseline analysis and leave [finance_monthly.csv](../data/finance_monthly.csv) unchanged.
3. Write a subquery that returns segment-months with profit below their budget profit. Verify one result manually.
4. Record 20 relevant postings and recurring skills; do not retain private recruiter or personal data in a public repo.

## Week 9 — CTE and window calculations

1. Build a CTE with one row per month containing budget and actual profit. In an outer query calculate running actual profit and previous-month actual profit with window functions ordered by month.
2. Verify the monthly and running results, including the first month's previous-period value.
3. Explain why the CTE aggregates first and why window ordering and frame matter. Save queries and outputs.

## Week 10 — Repeatable handoff

1. Make a fresh database and run your setup, import, checks and analysis in documented order. Save SQLite version, commands and output.
2. Test the January Retail slice against the hand control; separately demonstrate zero denominator and quality exceptions on test-only inputs.
3. Compare SQL totals with Excel and save a reconciliation table. Include data grain, known limitations and the definition of favorable expense variance.
4. Complete the [phase gate](../05-study-tracker.md) and retain scripts for Project A.
