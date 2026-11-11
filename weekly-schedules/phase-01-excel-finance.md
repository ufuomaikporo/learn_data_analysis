# Phase 1 — Excel and Finance, Weeks 1–4

[Schedule index](README.md) · [Phase 1 lab](../labs/phase-01-excel-finance.md) · [Data contract](../data/README.md)

**Time:** 4 × 9 = 36 hours. **Outcome:** An auditable budget-versus-actual workbook and management summary. Use matching [W3Schools Excel tutorials](https://www.w3schools.com/excel/) as the primary study resource. Microsoft documentation is secondary for covered topics and fills gaps such as CSV import and Power Query. [Udemy Excel Essentials](https://www.udemy.com/course/excel-essentials-the-complete-series-levels-1-2-3/) is optional supplementary practice. Use the lab's manual alternative if Power Query is unavailable in free Excel for the web.

### Weekly study map

Use the direct W3Schools topic links as primary study material wherever available. Use the linked Microsoft documentation as secondary guidance or as the primary source for gaps such as CSV import and Power Query. Udemy is optional and targeted; it does not add hours to the schedule.

| Week | Primary study | Supplement as needed |
|---|---|---|
| 1 | W3Schools: [tables](https://www.w3schools.com/excel/excel_tables.php), [number formats](https://www.w3schools.com/excel/excel_format_numbers.php), [sort](https://www.w3schools.com/excel/excel_sort.php), [filter](https://www.w3schools.com/excel/excel_filter.php); [finance definitions](../data/README.md). | Microsoft: [tables](https://support.microsoft.com/en-us/excel/get-started/create-and-format-tables), [number formats](https://support.microsoft.com/en-us/excel/get-started/available-number-formats-in-excel), [sort](https://support.microsoft.com/en-us/excel/sort-data-in-a-range-or-table-in-excel), [filter](https://support.microsoft.com/en-us/excel/get-started/filter-data-in-a-range-or-table-in-excel), [CSV import](https://support.microsoft.com/en-us/excel/get-started/import-or-export-text-txt-or-csv-files). Udemy: Excel basics and tables. |
| 2 | W3Schools: [SUMIFS](https://www.w3schools.com/excel/excel_sumifs.php), [relative references](https://www.w3schools.com/excel/excel_rel_ref.php), [absolute references](https://www.w3schools.com/excel/excel_abs_ref.php), [XLOOKUP](https://www.w3schools.com/excel/excel_xlookup.php). | Microsoft: [SUMIFS](https://support.microsoft.com/en-us/excel/functions/sumifs-function), [relative and absolute references](https://support.microsoft.com/en-us/excel/switch-between-relative-and-absolute-references), [XLOOKUP](https://support.microsoft.com/en-us/excel/functions/xlookup-function). Udemy: formulas and lookups. |
| 3 | W3Schools: [PivotTables](https://www.w3schools.com/excel/excel_table_pivot_intro.php), [charts](https://www.w3schools.com/excel/excel_charts.php), [tables](https://www.w3schools.com/excel/excel_tables.php). | Microsoft: [PivotTables](https://support.microsoft.com/en-us/office/create-a-pivottable-to-analyze-worksheet-data-a9a84538-bfe9-40a9-a8e9-f99134456576), [charts](https://support.microsoft.com/en-us/excel/get-started/create-a-chart-from-start-to-finish), [Power Query](https://support.microsoft.com/en-us/excel/use-power-query-in-excel-for-the-web). Udemy: pivots/charts. |
| 4 | Revisit W3Schools [SUMIFS](https://www.w3schools.com/excel/excel_sumifs.php), [PivotTables](https://www.w3schools.com/excel/excel_table_pivot_intro.php) and [charts](https://www.w3schools.com/excel/excel_charts.php); use the [KPI contract](../data/README.md) and stakeholder request in the lab. | Microsoft: [SUMIFS](https://support.microsoft.com/en-us/excel/functions/sumifs-function), [PivotTables](https://support.microsoft.com/en-us/office/create-a-pivottable-to-analyze-worksheet-data-a9a84538-bfe9-40a9-a8e9-f99134456576). Udemy: interpreting and presenting workbook results. |

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

## Week 1 - Finance and data grain
**Goal:** Identify the dataset grain and establish a finance baseline. Follow the [Week 1 lab procedure](../labs/phase-01-excel-finance.md#week-1--setup-and-finance-foundations).

**Learning Outcomes:** Identify the dataset's fields and row grain, distinguish revenue from expense, and calculate a basic profit and variance.

**Use Case:** When a new finance file arrives, identify what each row represents and agree on the terms before calculating or reporting results.

- [ ] **Day 1 (1h): Revenue, Expense, Profit and Variance**
  - **Study:** Revenue, expense, profit and variance.
  - **Study Resource:**
    - [OpenStax: income statement, revenue and expenses](https://openstax.org/books/principles-finance-2e/pages/5-1-the-income-statement)
    - [Boise State: comparing budget to actual](https://boisestate.pressbooks.pub/bsumbaaccounting/chapter/7-2-comparing-budget-to-actual/)
    - [finance KPI definitions and control totals](../data/README.md)

- [ ] **Day 2 (1.5h): Inspect CSV and Define Fields/Grain**
  - **Study Resource:**
    - [Excel Tables](https://www.w3schools.com/excel/excel_tables.php)
    - [Excel Filter](https://www.w3schools.com/excel/excel_filter.php)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Complete Step 1 in the [Week 1 lab](../labs/phase-01-excel-finance.md#week-1--setup-and-finance-foundations).

- [ ] **Day 3 (1.5h): Excel Tables, Types and Formats**
  - **Study:** Excel tables, types and formats.
  - **Study Resource:**
    - [Excel Tables](https://www.w3schools.com/excel/excel_tables.php)
    - [Excel Format Numbers](https://www.w3schools.com/excel/excel_format_numbers.php)
  - **Lab Exercise:** Complete Steps 1 and 2 in the [Week 1 lab](../labs/phase-01-excel-finance.md#week-1--setup-and-finance-foundations).

- [ ] **Day 4 (3h): Import Fixture**
  - **Study Resource:**
    - [Excel Tables](https://www.w3schools.com/excel/excel_tables.php)
    - [Excel Sort](https://www.w3schools.com/excel/excel_sort.php)
    - [Excel Filter](https://www.w3schools.com/excel/excel_filter.php)
    - [Microsoft: import text or CSV files](https://support.microsoft.com/en-us/excel/get-started/import-or-export-text-txt-or-csv-files)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Complete Step 3 in the [Week 1 lab](../labs/phase-01-excel-finance.md#week-1--setup-and-finance-foundations).

- [ ] **Day 5 (2h): Check 12 Rows and Hand-Calculate January Retail**
  - **Study Resource:**
    - [OpenStax: income statement, revenue and expenses](https://openstax.org/books/principles-finance-2e/pages/5-1-the-income-statement)
    - [Boise State: comparing budget to actual](https://boisestate.pressbooks.pub/bsumbaaccounting/chapter/7-2-comparing-budget-to-actual/)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Complete Steps 4 and 5 in the [Week 1 lab](../labs/phase-01-excel-finance.md#week-1--setup-and-finance-foundations) and record results in the [Week 1 log](../logs/week-01.md).

**Deliverables:** Completed [Week 1 lab artifacts](../labs/phase-01-excel-finance.md#week-1--setup-and-finance-foundations), project work where assigned, and recorded checks/evidence.

**Self-Check:** Answer the questions in the [Week 1 log](../logs/week-01.md).

## Week 2 - Formula-driven analysis

**Goal:** Complete the **Formula-driven analysis** lab and verify its outputs. Follow the [Week 2 lab procedure](../labs/phase-01-excel-finance.md#week-2--formula-driven-analysis).

**Learning Outcomes:** Use SUMIFS, cell references and XLOOKUP to calculate budget, actual and favorable variance, including zero-denominator cases.

**Use Case:** When a manager asks for actual-versus-budget totals by month or segment, formulas can calculate them consistently and show what each code means.

- [ ] **Day 1 (1h): SUMIFS and Relative/Absolute References**
  - **Study:** SUMIFS and relative/absolute references.
  - **Study Resource:**
    - [Excel SUMIFS Function](https://www.w3schools.com/excel/excel_sumifs.php)
    - [Excel Relative References](https://www.w3schools.com/excel/excel_rel_ref.php)
    - [Excel Absolute References](https://www.w3schools.com/excel/excel_abs_ref.php)

- [ ] **Day 2 (1.5h): Calculate Budget and Actual by Category**
  - **Study:** SUMIFS; budget and actual by category.
  - **Study Resource:**
    - [Excel SUMIFS Function](https://www.w3schools.com/excel/excel_sumifs.php)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Complete Step 1 in the [Week 2 lab](../labs/phase-01-excel-finance.md#week-2--formula-driven-analysis).

- [ ] **Day 3 (1.5h): XLOOKUP**
  - **Study:** XLOOKUP.
  - **Study Resource:**
    - [Excel XLOOKUP Function](https://www.w3schools.com/excel/excel_xlookup.php)
  - **Lab Exercise:** Complete Step 2 in the [Week 2 lab](../labs/phase-01-excel-finance.md#week-2--formula-driven-analysis).

- [ ] **Day 4 (3h): Add Profit, Favorable and Percentage Variance Formulas**
  - **Study Resource:**
    - [Excel SUMIFS Function](https://www.w3schools.com/excel/excel_sumifs.php)
    - [Excel IF Function](https://www.w3schools.com/excel/excel_if.php)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Complete Steps 3 and 4 in the [Week 2 lab](../labs/phase-01-excel-finance.md#week-2--formula-driven-analysis).

- [ ] **Day 5 (2h): Test Signs and Zero Denominator**
  - **Study Resource:**
    - [Excel IF Function](https://www.w3schools.com/excel/excel_if.php)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Complete Step 5 in the [Week 2 lab](../labs/phase-01-excel-finance.md#week-2--formula-driven-analysis) and record results in the [Week 2 log](../logs/week-02.md).

**Deliverables:** Completed [Week 2 lab artifacts](../labs/phase-01-excel-finance.md#week-2--formula-driven-analysis), project work where assigned, and recorded checks/evidence.

**Self-Check:** Answer the questions in the [Week 2 log](../logs/week-02.md).

## Week 3 - Power Query, pivots, and exceptions

**Goal:** Complete the **Power Query, pivots, and exceptions** lab and verify its outputs. Follow the [Week 3 lab procedure](../labs/phase-01-excel-finance.md#week-3--power-query-pivots-and-exceptions).

**Learning Outcomes:** Import and check data, summarize it with PivotTables, choose clear charts and identify exceptions.

**Use Case:** When a new file has messy values, clean a separate copy, summarize the data, and flag problems before sharing a chart.

- [ ] **Day 1 (1h): Pivottables, Chart Choice and Power Query**
  - **Study:** PivotTables, chart choice and Power Query.
  - **Study Resource:**
    - [Excel PivotTable introduction](https://www.w3schools.com/excel/excel_table_pivot_intro.php)
    - [Excel Charts](https://www.w3schools.com/excel/excel_charts.php)
    - [Microsoft: Power Query in Excel for the web](https://support.microsoft.com/en-us/excel/use-power-query-in-excel-for-the-web)

- [ ] **Day 2 (1.5h): Import/Clean a Copy with Power Query or Use the Manual Web Alternative**
  - **Study:** Power Query; CSV import and data cleaning.
  - **Study Resource:**
    - [Excel Tables](https://www.w3schools.com/excel/excel_tables.php)
    - [Microsoft: import text or CSV files](https://support.microsoft.com/en-us/excel/get-started/import-or-export-text-txt-or-csv-files)
    - [Microsoft: Power Query in Excel for the web](https://support.microsoft.com/en-us/excel/use-power-query-in-excel-for-the-web)
  - **Lab Exercise:** Complete Step 1 in the [Week 3 lab](../labs/phase-01-excel-finance.md#week-3--power-query-pivots-and-exceptions).

- [ ] **Day 3 (1.5h): Build Month and Segment Pivots**
  - **Study Resource:**
    - [Excel PivotTable introduction](https://www.w3schools.com/excel/excel_table_pivot_intro.php)
  - **Lab Exercise:** Complete Step 2 in the [Week 3 lab](../labs/phase-01-excel-finance.md#week-3--power-query-pivots-and-exceptions).

- [ ] **Day 4 (3h): Add Clear Trend and Variance Visuals**
  - **Study Resource:**
    - [Excel Charts](https://www.w3schools.com/excel/excel_charts.php)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Complete Step 3 in the [Week 3 lab](../labs/phase-01-excel-finance.md#week-3--power-query-pivots-and-exceptions).

- [ ] **Day 5 (2h): Test Missing/Duplicate Copy, Explain Findings Without Claiming Causation**
  - **Study Resource:**
    - [Excel COUNTIFS Function](https://www.w3schools.com/excel/excel_countifs.php)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Complete Steps 4 and 5 in the [Week 3 lab](../labs/phase-01-excel-finance.md#week-3--power-query-pivots-and-exceptions) and record results in the [Week 3 log](../logs/week-03.md).

**Deliverables:** Completed [Week 3 lab artifacts](../labs/phase-01-excel-finance.md#week-3--power-query-pivots-and-exceptions), project work where assigned, and recorded checks/evidence.

**Self-Check:** Answer the questions in the [Week 3 log](../logs/week-03.md).

## Week 4 - Management handoff

**Goal:** Complete the **Management handoff** lab and verify its outputs. Follow the [Week 4 lab procedure](../labs/phase-01-excel-finance.md#week-4--management-handoff).

**Learning Outcomes:** Reconcile Q1 results, answer follow-up questions and communicate findings with assumptions and limitations.

**Use Case:** When a manager asks why profit differs from budget, measure the revenue and expense differences and explain what the data cannot tell you.

- [ ] **Day 1 (1h): The Fictional Stakeholder Request**
  - **Study Resource:** [finance KPI definitions and control totals](../data/README.md)

- [ ] **Day 2 (1.5h): Check the Data and Calculate the Requested Q1 Figures**
  - **Study:** SUMIFS, KPI definitions and variance calculations.
  - **Study Resource:**
    - [Excel SUMIFS Function](https://www.w3schools.com/excel/excel_sumifs.php)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Complete Steps 1 and 2 in the [Week 4 lab](../labs/phase-01-excel-finance.md#week-4--management-handoff).

- [ ] **Day 3 (1.5h): Investigate Month and Segment Follow-Up Questions**
  - **Study Resource:**
    - [Excel PivotTable introduction](https://www.w3schools.com/excel/excel_table_pivot_intro.php)
    - [Excel Filter](https://www.w3schools.com/excel/excel_filter.php)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Complete Steps 3 and 4 in the [Week 4 lab](../labs/phase-01-excel-finance.md#week-4--management-handoff).

- [ ] **Day 4 (3h): Draft the Management Memo**
  - **Study Resource:**
    - [Boise State: comparing budget to actual](https://boisestate.pressbooks.pub/bsumbaaccounting/chapter/7-2-comparing-budget-to-actual/)
    - [OpenStax: income statement, revenue and expenses](https://openstax.org/books/principles-finance-2e/pages/5-1-the-income-statement)
    - [Purdue OWL: memo format and sample](https://owl.purdue.edu/owl/subject_specific_writing/professional_technical_writing/memos/format.html)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Complete Step 5 in the [Week 4 lab](../labs/phase-01-excel-finance.md#week-4--management-handoff).

- [ ] **Day 5 (2h): Present Findings and Limitations**
  - **Study Resource:**
    - [Boise State: comparing budget to actual](https://boisestate.pressbooks.pub/bsumbaaccounting/chapter/7-2-comparing-budget-to-actual/)
    - [Career and interview guide](../04-career-progression.md)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Complete Step 6 in the [Week 4 lab](../labs/phase-01-excel-finance.md#week-4--management-handoff) and record results in the [Week 4 log](../logs/week-04.md).

**Deliverables:** Reconciled workbook, one-page memo, clean-input check and presentation.  

**Self-Check:** Answer the questions in the [Week 4 log](../logs/week-04.md).

**Exit:** 12 rows, three monthly profit controls and Q1 totals agree with the data contract. Show both expense and revenue favorable-variance logic, explicit undefined percentage behavior, and a one-page explanation.
