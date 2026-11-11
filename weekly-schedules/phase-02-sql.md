# Phase 2 — SQL, Weeks 5–10

[Schedule index](README.md) · [Phase 2 lab](../labs/phase-02-sql.md) · [Data contract](../data/README.md)

**Time:** 6 × 9 = 54 hours. **Outcome:** Reproducible SQLite import, annotated analysis queries and quality checks. Primary: [W3Schools SQL](https://www.w3schools.com/sql/). Supplements: [Udemy Complete SQL Bootcamp](https://www.udemy.com/course/the-complete-sql-bootcamp/) and [SQLite docs](https://www.sqlite.org/docs.html). The Udemy course uses PostgreSQL and W3Schools examples may use another dialect; adapt and test all lab SQL in SQLite.

### Weekly study map

Use the tutorial navigation for each topic; use only the relevant optional Udemy sections within the existing weekly hours.

| Week | Primary W3Schools SQL topic | Supplement when needed |
|---|---|---|
| 5 | SELECT, WHERE and ORDER BY. | Udemy: SQL basics; [SQLite CLI](https://www.sqlite.org/cli.html) for setup/import. |
| 6 | GROUP BY, HAVING, CASE and NULL. | Udemy: aggregates and conditional expressions; SQLite docs for `NULLIF`. |
| 7 | JOINs and keys. | Udemy: joins; SQLite docs for its supported join syntax. |
| 8 | Subqueries, filters and missing values. | Udemy: subqueries; SQLite docs for date functions and quality checks. |
| 9 | Review GROUP BY and subqueries as the foundation. | [SQLite WITH](https://www.sqlite.org/lang_with.html) and [window functions](https://www.sqlite.org/windowfunctions.html) are required for CTEs and windows not sufficiently covered by the primary tutorial; use related Udemy material if available. |
| 10 | Review W3Schools joins, aggregates and CASE. | SQLite documentation for date handling and safe division; revisit Udemy for weak areas. |

## Weekly cadence and schedule

| Day | Duration | Focus |
|---|---:|---|
| Day 1 | 1 hour | Primary study |
| Day 2 | 1.5 hours | Lab practice |
| Day 3 | 1.5 hours | Study or lab practice |
| Day 4 | 3 hours | Lab and project work |
| Day 5 | 2 hours | Evidence and review |
| **Total** | **9 hours** | All project work is included |

Each scheduled Lab Exercise identifies the numbered step or steps to complete in that week's lab; follow them in ascending order. For three-step labs, Day 5 is a review of the final step. The final self-check question in each week's log names that week's concepts and asks how to apply them as a data analyst in the real world, with an example and explanation. The weekly Goal and Deliverables links open the full lab. Study-map supplements are optional unless noted as needed for a gap.

## Week 5 - SELECT and setup
**Goal:** Import the fixture into SQLite and retrieve filtered rows. Follow the [Week 5 lab procedure](../labs/phase-02-sql.md#week-5--create-and-import).

**Learning Outcomes:** Import a CSV, inspect fields and types, and retrieve rows with SELECT, WHERE and ORDER BY.

**Use Case:** When you receive an unfamiliar database, inspect its columns and select only the records needed to answer a question.

- [ ] **Day 1 (1h): SELECT, WHERE, ORDER BY**
  - **Study:** SELECT, WHERE, ORDER BY.
  - **Study Resource:**
    - [SQL SELECT](https://www.w3schools.com/sql/sql_select.asp)
    - [SQL WHERE](https://www.w3schools.com/sql/sql_where.asp)
    - [SQL ORDER BY](https://www.w3schools.com/sql/sql_orderby.asp)

- [ ] **Day 2 (1.5h): Install SQLite and Import a Clean Fixture**
  - **Study:** SQLite setup; CSV import.
  - **Study Resource:** [SQLite command-line import](https://www.sqlite.org/cli.html)
  - **Lab Exercise:** Complete Step 1 in the [Week 5 lab](../labs/phase-02-sql.md#week-5--create-and-import).

- [ ] **Day 3 (1.5h): Filter Months/Categories and Check Types**
  - **Study:** SQL WHERE and date filtering.
  - **Study Resource:**
    - [SQL WHERE](https://www.w3schools.com/sql/sql_where.asp)
    - [SQLite date functions](https://www.sqlite.org/lang_datefunc.html)
  - **Lab Exercise:** Complete Step 2 in the [Week 5 lab](../labs/phase-02-sql.md#week-5--create-and-import).

- [ ] **Day 4 (3h): Save Setup/Import and Basic Queries**
  - **Study Resource:**
    - [SQLite command-line import](https://www.sqlite.org/cli.html)
    - [SQL SELECT](https://www.w3schools.com/sql/sql_select.asp)
  - **Lab Exercise:** Complete Step 3 in the [Week 5 lab](../labs/phase-02-sql.md#week-5--create-and-import).

- [ ] **Day 5 (2h): Run Row-Count and January Retail Checks from a Fresh Database**
  - **Study Resource:**
    - [SQLite command-line import](https://www.sqlite.org/cli.html)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Complete Step 4 in the [Week 5 lab](../labs/phase-02-sql.md#week-5--create-and-import) and record results in the [Week 5 log](../logs/week-05.md).

**Deliverables:** Completed [Week 5 lab artifacts](../labs/phase-02-sql.md#week-5--create-and-import), project work where assigned, and recorded checks/evidence.

**Self-Check:** Answer the questions in the [Week 5 log](../logs/week-05.md).

## Week 6 - Group and reconcile

**Goal:** Complete the **Group and reconcile** lab and verify its outputs. Follow the [Week 6 lab procedure](../labs/phase-02-sql.md#week-6--group-and-reconcile).

**Learning Outcomes:** Group records, apply conditions, handle NULLs and calculate revenue, expense, profit and variance.

**Use Case:** When results are needed by month or segment, summarize revenue and expenses, calculate profit, and compare totals with a trusted check.

- [ ] **Day 1 (1h): GROUP BY, HAVING, CASE and NULL**
  - **Study:** GROUP BY, HAVING, CASE and NULL.
  - **Study Resource:**
    - [SQL GROUP BY](https://www.w3schools.com/sql/sql_groupby.asp)
    - [SQL HAVING](https://www.w3schools.com/sql/sql_having.asp)
    - [SQL CASE](https://www.w3schools.com/sql/sql_case.asp)
    - [SQL NULL Values](https://www.w3schools.com/sql/sql_null_values.asp)

- [ ] **Day 2 (1.5h): Aggregate Revenue and Expense**
  - **Study:** SQL grouping; conditional aggregation; revenue and expense.
  - **Study Resource:**
    - [SQL GROUP BY](https://www.w3schools.com/sql/sql_groupby.asp)
    - [SQL CASE](https://www.w3schools.com/sql/sql_case.asp)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Complete Step 1 in the [Week 6 lab](../labs/phase-02-sql.md#week-6--group-and-reconcile).

- [ ] **Day 3 (1.5h): Calculate Profit and Favorable Variance**
  - **Study Resource:**
    - [finance KPI definitions and control totals](../data/README.md)
    - [SQL CASE](https://www.w3schools.com/sql/sql_case.asp)
  - **Lab Exercise:** Complete Step 2 in the [Week 6 lab](../labs/phase-02-sql.md#week-6--group-and-reconcile).

- [ ] **Day 4 (3h): Save Monthly and Segment KPI Queries**
  - **Study Resource:**
    - [SQL GROUP BY](https://www.w3schools.com/sql/sql_groupby.asp)
    - [SQL CASE](https://www.w3schools.com/sql/sql_case.asp)
  - **Lab Exercise:** Complete Step 3 in the [Week 6 lab](../labs/phase-02-sql.md#week-6--group-and-reconcile).

- [ ] **Day 5 (2h): Reconcile Q1 and Monthly Totals with Excel**
  - **Study Resource:**
    - [SQL GROUP BY](https://www.w3schools.com/sql/sql_groupby.asp)
    - [Excel SUMIFS Function](https://www.w3schools.com/excel/excel_sumifs.php)
    - [SQLite NULLIF function](https://www.sqlite.org/lang_corefunc.html#nullif)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Complete Step 4 in the [Week 6 lab](../labs/phase-02-sql.md#week-6--group-and-reconcile) and record results in the [Week 6 log](../logs/week-06.md).

**Deliverables:** Completed [Week 6 lab artifacts](../labs/phase-02-sql.md#week-6--group-and-reconcile), project work where assigned, and recorded checks/evidence.

**Self-Check:** Answer the questions in the [Week 6 log](../logs/week-06.md).

## Week 7 - Keys and joins

**Goal:** Complete the **Keys and joins** lab and verify its outputs. Follow the [Week 7 lab procedure](../labs/phase-02-sql.md#week-7--keys-and-joins).

**Learning Outcomes:** Choose keys and join types, match facts to lookup data, and detect unmatched rows or duplicated totals.

**Use Case:** When transaction rows use codes stored in a separate table, match them carefully and check that unmatched or repeated codes do not change totals.

- [ ] **Day 1 (1h): Primary/Foreign Keys and JOIN Types**
  - **Study:** Primary/foreign keys and JOIN types.
  - **Study Resource:**
    - [SQL Primary Key](https://www.w3schools.com/sql/sql_primarykey.asp)
    - [SQL Foreign Key](https://www.w3schools.com/sql/sql_foreignkey.asp)
    - [SQL JOIN](https://www.w3schools.com/sql/sql_join.asp)
    - [SQL LEFT JOIN](https://www.w3schools.com/sql/sql_join_left.asp)
    - [SQLite foreign keys](https://www.sqlite.org/foreignkeys.html)

- [ ] **Day 2 (1.5h): Create and Populate Segment Lookup**
  - **Study:** SQL joins; lookup tables.
  - **Study Resource:**
    - [SQL JOIN](https://www.w3schools.com/sql/sql_join.asp)
    - [SQLite command-line import](https://www.sqlite.org/cli.html)
  - **Lab Exercise:** Complete Step 1 in the [Week 7 lab](../labs/phase-02-sql.md#week-7--keys-and-joins).

- [ ] **Day 3 (1.5h): Compare Inner and Left Joins, Including an Unmatched Test**
  - **Study:** Compare inner and left joins, including an unmatched test.
  - **Study Resource:**
    - [SQL JOIN](https://www.w3schools.com/sql/sql_join.asp)
    - [SQL LEFT JOIN](https://www.w3schools.com/sql/sql_join_left.asp)
  - **Lab Exercise:** Complete Step 2 in the [Week 7 lab](../labs/phase-02-sql.md#week-7--keys-and-joins).

- [ ] **Day 4 (3h): Join Lookup to Facts**
  - **Study:** Join lookup to facts.
  - **Study Resource:** [SQL LEFT JOIN](https://www.w3schools.com/sql/sql_join_left.asp)
  - **Lab Exercise:** Complete Step 3 in the [Week 7 lab](../labs/phase-02-sql.md#week-7--keys-and-joins).

- [ ] **Day 5 (2h): Explain Fan-Out and Why Unmatched Rows Matter**
  - **Study Resource:**
    - [SQL JOIN](https://www.w3schools.com/sql/sql_join.asp)
    - [SQL LEFT JOIN](https://www.w3schools.com/sql/sql_join_left.asp)
  - **Lab Exercise:** Complete Step 4 in the [Week 7 lab](../labs/phase-02-sql.md#week-7--keys-and-joins) and record results in the [Week 7 log](../logs/week-07.md).

**Deliverables:** Completed [Week 7 lab artifacts](../labs/phase-02-sql.md#week-7--keys-and-joins), project work where assigned, and recorded checks/evidence.

**Self-Check:** Answer the questions in the [Week 7 log](../logs/week-07.md).

## Week 8 - Data-quality checks and subqueries

**Goal:** Complete the **Data-quality checks and subqueries** lab and verify its outputs. Follow the [Week 8 lab procedure](../labs/phase-02-sql.md#week-8--data-quality-checks-and-subqueries).

**Learning Outcomes:** Find missing, duplicate or invalid records and use subqueries to isolate exceptions.

**Use Case:** Before reporting results, find missing, repeated, or invalid records and isolate problem groups without hiding them.

- [ ] **Day 1 (1h): Subqueries and Duplicate/Missing Checks**
  - **Study:** Subqueries and duplicate/missing checks.
  - **Study Resource:**
    - [SQL WHERE](https://www.w3schools.com/sql/sql_where.asp)
    - [SQL GROUP BY](https://www.w3schools.com/sql/sql_groupby.asp)
    - [SQL HAVING](https://www.w3schools.com/sql/sql_having.asp)
    - [SQL NULL Values](https://www.w3schools.com/sql/sql_null_values.asp)
    - [SQLite expressions and subqueries](https://www.sqlite.org/lang_expr.html#subquery_expressions)

- [ ] **Day 2 (1.5h): Detect Broken Rows in a Separate Test Table**
  - **Study:** SQL data-quality checks; NULLs and duplicate keys.
  - **Study Resource:**
    - [SQL NULL Values](https://www.w3schools.com/sql/sql_null_values.asp)
    - [SQL GROUP BY](https://www.w3schools.com/sql/sql_groupby.asp)
  - **Lab Exercise:** Complete Step 1 in the [Week 8 lab](../labs/phase-02-sql.md#week-8--data-quality-checks-and-subqueries).

- [ ] **Day 3 (1.5h): Compare Filtered and Grouped Results**
  - **Study:** Compare filtered and grouped results.
  - **Study Resource:**
    - [SQL WHERE](https://www.w3schools.com/sql/sql_where.asp)
    - [SQL GROUP BY](https://www.w3schools.com/sql/sql_groupby.asp)
  - **Lab Exercise:** Complete Step 2 in the [Week 8 lab](../labs/phase-02-sql.md#week-8--data-quality-checks-and-subqueries).

- [ ] **Day 4 (3h): Write Reusable Checks and Exceptions Report**
  - **Study Resource:**
    - [SQL GROUP BY](https://www.w3schools.com/sql/sql_groupby.asp)
    - [SQL NULL Values](https://www.w3schools.com/sql/sql_null_values.asp)
  - **Lab Exercise:** Complete Step 3 in the [Week 8 lab](../labs/phase-02-sql.md#week-8--data-quality-checks-and-subqueries).

- [ ] **Day 5 (2h): 20 Job Postings and Record Skill Gaps**
  - **Study Resource:** [career and interview guide](../04-career-progression.md)
  - **Lab Exercise:** Complete Step 4 in the [Week 8 lab](../labs/phase-02-sql.md#week-8--data-quality-checks-and-subqueries) and record results in the [Week 8 log](../logs/week-08.md).

**Deliverables:** Completed [Week 8 lab artifacts](../labs/phase-02-sql.md#week-8--data-quality-checks-and-subqueries), project work where assigned, and recorded checks/evidence.

**Self-Check:** Answer the questions in the [Week 8 log](../logs/week-08.md).

## Week 9 - CTE and window calculations

**Goal:** Complete the **CTE and window calculations** lab and verify its outputs. Follow the [Week 9 lab procedure](../labs/phase-02-sql.md#week-9--cte-and-window-calculations).

**Learning Outcomes:** Organize multi-step queries with CTEs and calculate running or prior-period values with window functions.

**Use Case:** When comparing results across time, a running total or prior-month value can reveal trends while preserving the original monthly detail.

- [ ] **Day 1 (1h): Ctes and SQLite Window Functions**
  - **Study:** CTEs and SQLite window functions.
  - **Study Resource:**
    - [SQLite WITH and CTEs](https://www.sqlite.org/lang_with.html)
    - [SQLite window functions](https://www.sqlite.org/windowfunctions.html)

- [ ] **Day 2 (1.5h): Build Monthly Profit CTE**
  - **Study:** Common table expressions; monthly profit aggregation.
  - **Study Resource:**
    - [SQLite WITH and CTEs](https://www.sqlite.org/lang_with.html)
    - [SQL CASE](https://www.w3schools.com/sql/sql_case.asp)
  - **Lab Exercise:** Complete Step 1 in the [Week 9 lab](../labs/phase-02-sql.md#week-9--cte-and-window-calculations).

- [ ] **Day 3 (1.5h): Calculate Running Profit and Prior-Month Profit**
  - **Study Resource:** [SQLite window functions](https://www.sqlite.org/windowfunctions.html)
  - **Lab Exercise:** Complete Step 2 in the [Week 9 lab](../labs/phase-02-sql.md#week-9--cte-and-window-calculations).

- [ ] **Day 4 (3h): Save and Annotate Queries**
  - **Study Resource:**
    - [SQLite WITH and CTEs](https://www.sqlite.org/lang_with.html)
    - [SQLite window functions](https://www.sqlite.org/windowfunctions.html)
  - **Lab Exercise:** Complete Step 3 in the [Week 9 lab](../labs/phase-02-sql.md#week-9--cte-and-window-calculations).

- [ ] **Day 5 (2h): Reconcile Running Totals and Explain Window vs Aggregation**
  - **Study Resource:**
    - [SQLite window functions](https://www.sqlite.org/windowfunctions.html)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Review Step 3 in the [Week 9 lab](../labs/phase-02-sql.md#week-9--cte-and-window-calculations) and record results in the [Week 9 log](../logs/week-09.md).

**Deliverables:** Completed [Week 9 lab artifacts](../labs/phase-02-sql.md#week-9--cte-and-window-calculations), project work where assigned, and recorded checks/evidence.

**Self-Check:** Answer the questions in the [Week 9 log](../logs/week-09.md).

## Week 10 - Repeatable handoff

**Goal:** Complete the **Repeatable handoff** lab and verify its outputs. Follow the [Week 10 lab procedure](../labs/phase-02-sql.md#week-10--repeatable-handoff).

**Learning Outcomes:** Handle dates and undefined percentages, answer a business question, and rerun documented SQL from a clean database.

**Use Case:** When handing SQL work to a teammate, document how to rebuild and rerun it so they can reproduce the same results.

- [ ] **Day 1 (1h): Date Handling and Safe Division**
  - **Study:** Date handling and safe division.
  - **Study Resource:**
    - [SQLite date functions](https://www.sqlite.org/lang_datefunc.html)
    - [SQLite scalar functions: NULLIF](https://www.sqlite.org/lang_corefunc.html)

- [ ] **Day 2 (1.5h): Add Filter and Zero-Denominator Cases**
  - **Study:** SQL filters; date functions; undefined percentages.
  - **Study Resource:**
    - [SQL WHERE](https://www.w3schools.com/sql/sql_where.asp)
    - [SQLite scalar functions: NULLIF](https://www.sqlite.org/lang_corefunc.html)
  - **Lab Exercise:** Complete Step 1 in the [Week 10 lab](../labs/phase-02-sql.md#week-10--repeatable-handoff).

- [ ] **Day 3 (1.5h): Answer the Project Business Question in SQL**
  - **Study Resource:**
    - [finance KPI definitions and control totals](../data/README.md)
    - [SQL GROUP BY](https://www.w3schools.com/sql/sql_groupby.asp)
  - **Lab Exercise:** Complete Step 2 in the [Week 10 lab](../labs/phase-02-sql.md#week-10--repeatable-handoff).

- [ ] **Day 4 (3h): Rebuild Database and Run All Scripts in Order**
  - **Study:** Rebuild database and run all scripts in order.
  - **Study Resource:** [SQLite command-line import](https://www.sqlite.org/cli.html)
  - **Lab Exercise:** Complete Step 3 in the [Week 10 lab](../labs/phase-02-sql.md#week-10--repeatable-handoff).

- [ ] **Day 5 (2h): Document Outputs, SQLite Version and Phase Gate**
  - **Study Resource:**
    - [SQLite command-line import](https://www.sqlite.org/cli.html)
    - [SQL SELECT](https://www.w3schools.com/sql/sql_select.asp)
    - [Excel SUMIFS Function](https://www.w3schools.com/excel/excel_sumifs.php)
  - **Lab Exercise:** Complete Step 4 in the [Week 10 lab](../labs/phase-02-sql.md#week-10--repeatable-handoff) and record results in the [Week 10 log](../logs/week-10.md).

**Deliverables:** Fresh-database run, analysis scripts, version notes and reconciliation.  

**Self-Check:** Answer the questions in the [Week 10 log](../logs/week-10.md).


**Exit:** New database reproduces 12 rows, the Q1 controls and the monthly controls. Queries demonstrate joins, grouping, CASE, CTE, windows and visible failure checks.
