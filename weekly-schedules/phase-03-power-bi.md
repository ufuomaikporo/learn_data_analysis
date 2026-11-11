# Phase 3 — Power BI, Weeks 11–16

[Schedule index](README.md) · [Phase 3 lab](../labs/phase-03-power-bi.md) · [Project A](../projects/project-a-sql-power-bi.md)

**Time:** 6 × 9 = 54 hours. **Outcome:** A local financial performance report with a comprehensible model, measures and reconciled filters. **Primary exception:** [Microsoft Learn Power BI training](https://learn.microsoft.com/en-us/training/powerplatform/power-bi/) because an official W3Schools Power BI tutorial could not be verified. Supplements: [Udemy Power BI course](https://www.udemy.com/course/microsoft-power-bi-up-running-with-power-bi-desktop/), [Power BI docs](https://learn.microsoft.com/en-us/power-bi/) and [DAX reference](https://learn.microsoft.com/en-us/dax/).

### Weekly study map

In the Microsoft Learn training hub select modules by topic; use selected Udemy sections only when helpful, within the weekly budget.

| Week | Primary Microsoft Learn topic | Supplement when needed |
|---|---|---|
| 11 | Get started; get, clean and transform data with Power Query. | Udemy: data import and transformations; Power BI docs for data types. |
| 12 | Model data, fact/dimension tables and relationships. | Udemy: modeling; Power BI docs for star schemas and relationships. |
| 13 | Create DAX measures and understand filter context. | Udemy: DAX; [DAX reference](https://learn.microsoft.com/en-us/dax/) for `CALCULATE` and `DIVIDE`. |
| 14 | Create reports, visuals, slicers and accessible presentation. | Udemy: visuals and interactions; Power BI docs for formatting. |
| 15 | Validate models, refresh and report design. | Udemy: refresh and reporting; Power BI docs for query errors and filters. |
| 16 | Review the data-to-report workflow and presentation. | Revisit relevant Udemy/official material while preparing the project handoff. |

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

## Week 11 - Import and Power Query
**Goal:** Import and inspect the finance data in Power BI. Follow the [Week 11 lab procedure](../labs/phase-03-power-bi.md#week-11--import-and-quality).

**Learning Outcomes:** Load the source, preserve the raw input, set column types and refresh a clean query.

**Use Case:** When a recurring data file arrives, Power Query can apply the same type checks and cleaning steps again without changing the source.

- [ ] **Day 1 (1h): Desktop and Data Types**
  - **Study:** Desktop and data types.
  - **Study Resource:** [Microsoft Learn: prepare data in Power BI](https://learn.microsoft.com/en-us/training/paths/prepare-data-power-bi/)

- [ ] **Day 2 (1.5h): Load CSV and Preserve Raw Input**
  - **Study:** Power BI data import; Power Query; source preservation.
  - **Study Resource:** [Microsoft Learn: prepare data in Power BI](https://learn.microsoft.com/en-us/training/paths/prepare-data-power-bi/)
  - **Lab Exercise:** Complete Step 1 in the [Week 11 lab](../labs/phase-03-power-bi.md#week-11--import-and-quality).

- [ ] **Day 3 (1.5h): Inspect Nulls and Column Types**
  - **Study Resource:** [Microsoft Learn: prepare data in Power BI](https://learn.microsoft.com/en-us/training/paths/prepare-data-power-bi/)
  - **Lab Exercise:** Complete Step 2 in the [Week 11 lab](../labs/phase-03-power-bi.md#week-11--import-and-quality).

- [ ] **Day 4 (3h): Transform and Load Clean Fact Table**
  - **Study:** Transform and load clean fact table.
  - **Study Resource:** [Microsoft Learn: prepare data in Power BI](https://learn.microsoft.com/en-us/training/paths/prepare-data-power-bi/)
  - **Lab Exercise:** Complete Step 3 in the [Week 11 lab](../labs/phase-03-power-bi.md#week-11--import-and-quality).

- [ ] **Day 5 (2h): Check 12 Records and Refresh**
  - **Study Resource:**
    - [Microsoft Learn: prepare data in Power BI](https://learn.microsoft.com/en-us/training/paths/prepare-data-power-bi/)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Review Step 3 in the [Week 11 lab](../labs/phase-03-power-bi.md#week-11--import-and-quality) and record results in the [Week 11 log](../logs/week-11.md).

**Deliverables:** Completed [Week 11 lab artifacts](../labs/phase-03-power-bi.md#week-11--import-and-quality), project work where assigned, and recorded checks/evidence.

**Self-Check:** Answer the questions in the [Week 11 log](../logs/week-11.md).

## Week 12 - Model the grain

**Goal:** Complete the **Model the grain** lab and verify its outputs. Follow the [Week 12 lab procedure](../labs/phase-03-power-bi.md#week-12--model-the-grain).

**Learning Outcomes:** Define fact and dimension tables, set relationships and test that filters do not duplicate amounts.

**Use Case:** When building a report from facts and lookup tables, define what one fact row means and connect the tables so filters do not count amounts twice.

- [ ] **Day 1 (1h): Fact/Dimension Grain and Relationships**
  - **Study:** Fact/dimension grain and relationships.
  - **Study Resource:**
    - [Glossary: fact tables and dimensions](../06-glossary.md#analysis-and-data-models)
    - [Microsoft: star schemas and grain](https://learn.microsoft.com/en-us/power-bi/guidance/star-schema)
    - [Microsoft Learn: model data and DAX](https://learn.microsoft.com/en-us/training/paths/model-data-power-bi/)

- [ ] **Day 2 (1.5h): Create Date and Segment Dimensions**
  - **Study:** Star schema; date and segment dimensions; relationships.
  - **Study Resource:**
    - [Microsoft: star schemas and grain](https://learn.microsoft.com/en-us/power-bi/guidance/star-schema)
    - [Microsoft Learn: model data and DAX](https://learn.microsoft.com/en-us/training/paths/model-data-power-bi/)
  - **Lab Exercise:** Complete Step 1 in the [Week 12 lab](../labs/phase-03-power-bi.md#week-12--model-the-grain).

- [ ] **Day 3 (1.5h): Check One-to-Many Relationship Directions**
  - **Study Resource:** [Microsoft: star schemas and grain](https://learn.microsoft.com/en-us/power-bi/guidance/star-schema)
  - **Lab Exercise:** Complete Step 2 in the [Week 12 lab](../labs/phase-03-power-bi.md#week-12--model-the-grain).

- [ ] **Day 4 (3h): Build Model and Sketch It**
  - **Study Resource:** [Microsoft: star schemas and grain](https://learn.microsoft.com/en-us/power-bi/guidance/star-schema)
  - **Lab Exercise:** Complete Step 3 in the [Week 12 lab](../labs/phase-03-power-bi.md#week-12--model-the-grain).

- [ ] **Day 5 (2h): Prove Segment/Date Filters Do Not Duplicate Data**
  - **Study Resource:**
    - [Microsoft: star schemas and grain](https://learn.microsoft.com/en-us/power-bi/guidance/star-schema)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Review Step 3 in the [Week 12 lab](../labs/phase-03-power-bi.md#week-12--model-the-grain) and record results in the [Week 12 log](../logs/week-12.md).

**Deliverables:** Completed [Week 12 lab artifacts](../labs/phase-03-power-bi.md#week-12--model-the-grain), project work where assigned, and recorded checks/evidence.

**Self-Check:** Answer the questions in the [Week 12 log](../logs/week-12.md).

## Week 13 - Measures and checks

**Goal:** Complete the **Measures and checks** lab and verify its outputs. Follow the [Week 13 lab procedure](../labs/phase-03-power-bi.md#week-13--measures-and-checks).

**Learning Outcomes:** Create DAX measures for actuals, budget, profit and variance, and verify their filter behavior.

**Use Case:** When report readers change date or segment filters, DAX measures should recalculate actuals, budgets, profit, and variances correctly.

- [ ] **Day 1 (1h): Measures, Filter Context and CALCULATE**
  - **Study:** Measures, filter context and CALCULATE.
  - **Study Resource:**
    - [Microsoft Learn: model data and DAX](https://learn.microsoft.com/en-us/training/paths/model-data-power-bi/)
    - [Microsoft DAX reference](https://learn.microsoft.com/en-us/dax/)

- [ ] **Day 2 (1.5h): Create Actual Revenue and Expense Measures**
  - **Study:** DAX measures; actual revenue and expense.
  - **Study Resource:**
    - [Microsoft Learn: model data and DAX](https://learn.microsoft.com/en-us/training/paths/model-data-power-bi/)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Complete Step 1 in the [Week 13 lab](../labs/phase-03-power-bi.md#week-13--measures-and-checks).

- [ ] **Day 3 (1.5h): Add Budget and Profit Measures**
  - **Study Resource:**
    - [Microsoft DAX reference](https://learn.microsoft.com/en-us/dax/)
    - [DAX DIVIDE function](https://learn.microsoft.com/en-us/dax/divide-function-dax)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Complete Step 2 in the [Week 13 lab](../labs/phase-03-power-bi.md#week-13--measures-and-checks).

- [ ] **Day 4 (3h): Add Favorable and Percentage Variance Measures**
  - **Study Resource:**
    - [Microsoft DAX reference](https://learn.microsoft.com/en-us/dax/)
    - [DAX DIVIDE function](https://learn.microsoft.com/en-us/dax/divide-function-dax)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Complete Steps 3 and 4 in the [Week 13 lab](../labs/phase-03-power-bi.md#week-13--measures-and-checks).

- [ ] **Day 5 (2h): Reconcile Q1 and January Retail**
  - **Study Resource:**
    - [Microsoft DAX reference](https://learn.microsoft.com/en-us/dax/)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Complete Step 5 in the [Week 13 lab](../labs/phase-03-power-bi.md#week-13--measures-and-checks) and record results in the [Week 13 log](../logs/week-13.md).

**Deliverables:** Completed [Week 13 lab artifacts](../labs/phase-03-power-bi.md#week-13--measures-and-checks), project work where assigned, and recorded checks/evidence.

**Self-Check:** Answer the questions in the [Week 13 log](../logs/week-13.md).

## Week 14 - Report design

**Goal:** Complete the **Report design** lab and verify its outputs. Follow the [Week 14 lab procedure](../labs/phase-03-power-bi.md#week-14--report-design).

**Learning Outcomes:** Select suitable visuals, add clear labels and slicers, and test accessibility and blank values.

**Use Case:** When stakeholders use a report, clear charts, labels, filters, and accessible design help them understand the results.

- [ ] **Day 1 (1h): Chart Selection and Accessibility**
  - **Study:** Chart selection and accessibility.
  - **Study Resource:**
    - [Microsoft Learn: prepare and visualize Power BI data](https://learn.microsoft.com/en-us/training/paths/prepare-visualize-data-power-bi/)
    - [Microsoft: accessible Power BI reports](https://learn.microsoft.com/en-us/power-bi/create-reports/desktop-accessibility-creating-reports)

- [ ] **Day 2 (1.5h): Add KPI Cards and Trend**
  - **Study:** Power BI KPI cards; monthly trends; variance visuals.
  - **Study Resource:** [Microsoft Learn: prepare and visualize Power BI data](https://learn.microsoft.com/en-us/training/paths/prepare-visualize-data-power-bi/)
  - **Lab Exercise:** Complete Step 1 in the [Week 14 lab](../labs/phase-03-power-bi.md#week-14--report-design).

- [ ] **Day 3 (1.5h): Add Variance by Segment and Month**
  - **Study Resource:**
    - [Microsoft Learn: prepare and visualize Power BI data](https://learn.microsoft.com/en-us/training/paths/prepare-visualize-data-power-bi/)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Complete Step 2 in the [Week 14 lab](../labs/phase-03-power-bi.md#week-14--report-design).

- [ ] **Day 4 (3h): Add Slicers, Labels and Narrative Context**
  - **Study Resource:**
    - [Microsoft Learn: prepare and visualize Power BI data](https://learn.microsoft.com/en-us/training/paths/prepare-visualize-data-power-bi/)
    - [Microsoft: accessible Power BI reports](https://learn.microsoft.com/en-us/power-bi/create-reports/desktop-accessibility-creating-reports)
  - **Lab Exercise:** Complete Step 3 in the [Week 14 lab](../labs/phase-03-power-bi.md#week-14--report-design).

- [ ] **Day 5 (2h): Test Filters, Units and Blanks**
  - **Study Resource:**
    - [Microsoft: accessible Power BI reports](https://learn.microsoft.com/en-us/power-bi/create-reports/desktop-accessibility-creating-reports)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Review Step 3 in the [Week 14 lab](../labs/phase-03-power-bi.md#week-14--report-design) and record results in the [Week 14 log](../logs/week-14.md).

**Deliverables:** Completed [Week 14 lab artifacts](../labs/phase-03-power-bi.md#week-14--report-design), project work where assigned, and recorded checks/evidence.

**Self-Check:** Answer the questions in the [Week 14 log](../logs/week-14.md).

## Week 15 - Exceptions and storytelling

**Goal:** Complete the **Exceptions and storytelling** lab and verify its outputs. Follow the [Week 15 lab procedure](../labs/phase-03-power-bi.md#week-15--exceptions-and-storytelling).

**Learning Outcomes:** Test refreshes and data exceptions, compare results across tools, and present evidence without overstating conclusions.

**Use Case:** Before sharing a report, compare its results with other tools and show data problems instead of presenting unsupported explanations.

- [ ] **Day 1 (1h): Refresh, Interactions and Reporting Limitations**
  - **Study:** Refresh, interactions and reporting limitations.
  - **Study Resource:**
    - [Microsoft: data refresh](https://learn.microsoft.com/en-us/power-bi/connect-data/refresh-data)
    - [visual interactions](https://learn.microsoft.com/en-us/power-bi/create-reports/service-reports-visual-interactions)

- [ ] **Day 2 (1.5h): Test Duplicate and Missing Data in Isolated Copy**
  - **Study:** Power Query quality checks; duplicates and missing values.
  - **Study Resource:** [Microsoft Learn: prepare data in Power BI](https://learn.microsoft.com/en-us/training/paths/prepare-data-power-bi/)
  - **Lab Exercise:** Complete Step 1 in the [Week 15 lab](../labs/phase-03-power-bi.md#week-15--exceptions-and-storytelling).

- [ ] **Day 3 (1.5h): Compare SQL, Excel and BI Results**
  - **Study Resource:**
    - [SQL GROUP BY](https://www.w3schools.com/sql/sql_groupby.asp)
    - [Excel SUMIFS Function](https://www.w3schools.com/excel/excel_sumifs.php)
    - [Microsoft Learn: model data and DAX](https://learn.microsoft.com/en-us/training/paths/model-data-power-bi/)
  - **Lab Exercise:** Complete Step 2 in the [Week 15 lab](../labs/phase-03-power-bi.md#week-15--exceptions-and-storytelling).

- [ ] **Day 4 (3h): Refine Report and Write Business Recommendation**
  - **Study Resource:**
    - [Microsoft Learn: prepare and visualize Power BI data](https://learn.microsoft.com/en-us/training/paths/prepare-visualize-data-power-bi/)
    - [Purdue OWL: memo format and sample](https://owl.purdue.edu/owl/subject_specific_writing/professional_technical_writing/memos/format.html)
  - **Lab Exercise:** Complete Step 3 in the [Week 15 lab](../labs/phase-03-power-bi.md#week-15--exceptions-and-storytelling).

- [ ] **Day 5 (2h): Obtain or Simulate a Reviewer Walkthrough, Document Feedback Honestly**
  - **Study Resource:**
    - [career and interview guide](../04-career-progression.md)
    - [Microsoft: accessible Power BI reports](https://learn.microsoft.com/en-us/power-bi/create-reports/desktop-accessibility-creating-reports)
  - **Lab Exercise:** Review Step 3 in the [Week 15 lab](../labs/phase-03-power-bi.md#week-15--exceptions-and-storytelling) and record results in the [Week 15 log](../logs/week-15.md).

**Deliverables:** Completed [Week 15 lab artifacts](../labs/phase-03-power-bi.md#week-15--exceptions-and-storytelling), project work where assigned, and recorded checks/evidence.

**Self-Check:** Answer the questions in the [Week 15 log](../logs/week-15.md).

## Week 16 - Handoff

**Goal:** Complete the **Handoff** lab and verify its outputs. Follow the [Week 16 lab procedure](../labs/phase-03-power-bi.md#week-16--handoff).

**Learning Outcomes:** Document the model and measures, prepare a walkthrough and package a refreshable report.

**Use Case:** When a teammate must maintain a report, clear model notes, screenshots, and refresh steps let them reproduce a filtered result.

- [ ] **Day 1 (1h): Model and Measures**
  - **Study:** Model and measures.
  - **Study Resource:**
    - [Microsoft Learn: model data and DAX](https://learn.microsoft.com/en-us/training/paths/model-data-power-bi/)
    - [Microsoft DAX reference](https://learn.microsoft.com/en-us/dax/)

- [ ] **Day 2 (1.5h): Draft Setup and Data Dictionary**
  - **Study Resource:**
    - [Microsoft Learn: prepare data in Power BI](https://learn.microsoft.com/en-us/training/paths/prepare-data-power-bi/)
    - [Microsoft: star schemas and grain](https://learn.microsoft.com/en-us/power-bi/guidance/star-schema)
    - [SQLite documentation](https://www.sqlite.org/docs.html)
  - **Lab Exercise:** Complete Step 1 in the [Week 16 lab](../labs/phase-03-power-bi.md#week-16--handoff).

- [ ] **Day 3 (1.5h): Prepare Screenshots and Walkthrough**
  - **Study Resource:** [Microsoft: accessible Power BI reports](https://learn.microsoft.com/en-us/power-bi/create-reports/desktop-accessibility-creating-reports)
  - **Lab Exercise:** Complete Step 2 in the [Week 16 lab](../labs/phase-03-power-bi.md#week-16--handoff).

- [ ] **Day 4 (3h): Rebuild/Refresh and Package SQL, PBIX and Docs**
  - **Study:** Rebuild/refresh and package SQL, PBIX and docs.
  - **Study Resource:** [Microsoft Learn: prepare data in Power BI](https://learn.microsoft.com/en-us/training/paths/prepare-data-power-bi/)
  - **Lab Exercise:** Complete Step 3 in the [Week 16 lab](../labs/phase-03-power-bi.md#week-16--handoff).

- [ ] **Day 5 (2h): Present Two-Minute Summary**
  - **Study Resource:**
    - [career and interview guide](../04-career-progression.md)
    - [Microsoft: accessible Power BI reports](https://learn.microsoft.com/en-us/power-bi/create-reports/desktop-accessibility-creating-reports)
  - **Lab Exercise:** Review Step 3 in the [Week 16 lab](../labs/phase-03-power-bi.md#week-16--handoff) and record results in the [Week 16 log](../logs/week-16.md).

**Deliverables:** SQL, PBIX, screenshots, setup instructions and two-minute walkthrough.  

**Self-Check:** Answer the questions in the [Week 16 log](../logs/week-16.md).


**Exit:** Reproducible report matches Q1 and a filtered slice, explains expense sign, and documents synthetic data, limitations, and findings. Screenshots are a supplement, not a substitute for source files.
