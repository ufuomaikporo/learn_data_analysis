# Phase 5 — Python for Analysts, Weeks 21–26

[Schedule index](README.md) · [Phase 5 lab](../labs/phase-05-python.md) · [Project B](../projects/project-b-excel-python.md)

**Time:** 6 × 9 = 54 hours. **Outcome:** A re-runnable pandas notebook and exported finance report. Primary: [W3Schools Python](https://www.w3schools.com/python/) and [pandas](https://www.w3schools.com/python/pandas/). Supplements: [Udemy Data Analysis with Pandas and Python](https://www.udemy.com/course/data-analysis-with-pandas/), [Python docs](https://docs.python.org/3/) and [pandas docs](https://pandas.pydata.org/docs/user_guide/).

### Weekly study map

| Week | Primary W3Schools topic | Supplement when needed |
|---|---|---|
| 21 | Python variables, numbers, strings, lists, dictionaries and conditions. | Udemy Python introduction; Python docs for environment setup. |
| 22 | Python functions, loops, exceptions and file handling. | Udemy Python foundations; Python docs for CSV and exceptions. |
| 23 | pandas DataFrames, reading CSV, cleaning and missing values. | Udemy pandas DataFrames/cleaning; pandas docs for current parsing behavior. |
| 24 | pandas grouping, merging and pivoting where covered. | Udemy grouping/merging; pandas docs for `merge` validation and aggregation. |
| 25 | pandas analysis and plotting. | Udemy visualization; pandas/Matplotlib documentation for chart labels and saving. |
| 26 | Revisit Python and pandas topics tied to unresolved gaps. | Udemy review; official Python/pandas docs for versions, environment and reproducibility. |

Use tutorial navigation for the topics and selected Udemy sections within the existing weekly hours; do not complete the entire course by default.

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

## Week 21 - Setup and syntax
**Goal:** Set up Python and implement basic finance functions. Follow the [Week 21 lab procedure](../labs/phase-05-python.md#week-21--fundamentals-and-financial-functions).

**Learning Outcomes:** Use basic Python values, collections and conditions to calculate finance measures with explicit signs.

**Use Case:** When a calculation must be repeated, small Python functions can apply finance definitions consistently and make sign handling testable.

- [ ] **Day 1 (1h): Variables, Numbers and Strings**
  - **Study:** Variables, numbers and strings.
  - **Study Resource:**
    - [Python Variables](https://www.w3schools.com/python/python_variables.asp)
    - [Python Numbers](https://www.w3schools.com/python/python_numbers.asp)
    - [Python Strings](https://www.w3schools.com/python/python_strings.asp)

- [ ] **Day 2 (1.5h): Create a Virtual Environment and Notebook**
  - **Study:** Python virtual environments; Jupyter notebooks.
  - **Study Resource:**
    - [Python virtual environments](https://docs.python.org/3/library/venv.html)
    - [JupyterLab notebook documentation](https://jupyterlab.readthedocs.io/en/latest/user/notebook.html)
  - **Lab Exercise:** Complete Step 1 in the [Week 21 lab](../labs/phase-05-python.md#week-21--fundamentals-and-financial-functions).

- [ ] **Day 3 (1.5h): Lists, Dictionaries and Conditions**
  - **Study:** Lists, dictionaries and conditions.
  - **Study Resource:**
    - [Python Lists](https://www.w3schools.com/python/python_lists.asp)
    - [Python Dictionaries](https://www.w3schools.com/python/python_dictionaries.asp)
    - [Python Conditions](https://www.w3schools.com/python/python_conditions.asp)
  - **Lab Exercise:** Complete Step 2 in the [Week 21 lab](../labs/phase-05-python.md#week-21--fundamentals-and-financial-functions).

- [ ] **Day 4 (3h): Implement Finance KPI Functions on Small Examples**
  - **Study Resource:**
    - [Python Functions](https://www.w3schools.com/python/python_functions.asp)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Complete Step 3 in the [Week 21 lab](../labs/phase-05-python.md#week-21--fundamentals-and-financial-functions).

- [ ] **Day 5 (2h): Check Signs and Undefined Denominator**
  - **Study Resource:**
    - [finance KPI definitions and control totals](../data/README.md)
    - [Python Conditions](https://www.w3schools.com/python/python_conditions.asp)
    - [Python built-in constants: None](https://docs.python.org/3/library/constants.html#None)
  - **Lab Exercise:** Complete Step 4 in the [Week 21 lab](../labs/phase-05-python.md#week-21--fundamentals-and-financial-functions) and record results in the [Week 21 log](../logs/week-21.md).

**Deliverables:** Completed [Week 21 lab artifacts](../labs/phase-05-python.md#week-21--fundamentals-and-financial-functions), project work where assigned, and recorded checks/evidence.

**Self-Check:** Answer the questions in the [Week 21 log](../logs/week-21.md).

## Week 22 - Files, validation and errors

**Goal:** Complete the **Files, validation and errors** lab and verify its outputs. Follow the [Week 22 lab procedure](../labs/phase-05-python.md#week-22--files-validation-and-errors).

**Learning Outcomes:** Read CSV files, validate fields and values, and raise useful errors for malformed input.

**Use Case:** When scripts receive CSV files from others, validation can catch missing or malformed values early and explain how to fix them.

- [ ] **Day 1 (1h): Functions, Loops and Exceptions**
  - **Study:** Functions, loops and exceptions.
  - **Study Resource:**
    - [Python Functions](https://www.w3schools.com/python/python_functions.asp)
    - [Python For Loops](https://www.w3schools.com/python/python_for_loops.asp)
    - [Python tutorial: errors and exceptions](https://docs.python.org/3/tutorial/errors.html)

- [ ] **Day 2 (1.5h): A Local CSV Using Python**
  - **Study:** Python file handling; CSV parsing and validation.
  - **Study Resource:**
    - [Python File Handling](https://www.w3schools.com/python/python_file_handling.asp)
    - [Python CSV documentation](https://docs.python.org/3/library/csv.html)
  - **Lab Exercise:** Complete Step 1 in the [Week 22 lab](../labs/phase-05-python.md#week-22--files-validation-and-errors).

- [ ] **Day 3 (1.5h): Validate Headers and Numeric/Date Inputs**
  - **Study:** Validate headers and numeric/date inputs.
  - **Study Resource:**
    - [Python CSV documentation](https://docs.python.org/3/library/csv.html)
    - [Python tutorial: errors and exceptions](https://docs.python.org/3/tutorial/errors.html)
  - **Lab Exercise:** Complete Step 2 in the [Week 22 lab](../labs/phase-05-python.md#week-22--files-validation-and-errors).

- [ ] **Day 4 (3h): Write Explicit Checks with Actionable Errors**
  - **Study Resource:**
    - [Python tutorial: errors and exceptions](https://docs.python.org/3/tutorial/errors.html)
    - [Python CSV documentation](https://docs.python.org/3/library/csv.html)
  - **Lab Exercise:** Complete Step 3 in the [Week 22 lab](../labs/phase-05-python.md#week-22--files-validation-and-errors).

- [ ] **Day 5 (2h): Test Malformed Data in a Copy**
  - **Study Resource:** [Python tutorial: errors and exceptions](https://docs.python.org/3/tutorial/errors.html)
  - **Lab Exercise:** Complete Step 4 in the [Week 22 lab](../labs/phase-05-python.md#week-22--files-validation-and-errors) and record results in the [Week 22 log](../logs/week-22.md).

**Deliverables:** Completed [Week 22 lab artifacts](../labs/phase-05-python.md#week-22--files-validation-and-errors), project work where assigned, and recorded checks/evidence.

**Self-Check:** Answer the questions in the [Week 22 log](../logs/week-22.md).

## Week 23 - pandas ingestion and quality

**Goal:** Complete the **pandas ingestion and quality** lab and verify its outputs. Follow the [Week 23 lab procedure](../labs/phase-05-python.md#week-23--pandas-ingestion-and-quality).

**Learning Outcomes:** Load data into pandas, check types and identify missing or duplicate values without changing the baseline.

**Use Case:** Before analyzing a CSV in pandas, check its columns, data types, missing values, and duplicate keys so bad data does not silently affect results.

- [ ] **Day 1 (1h): DataFrames, read_csv and Types**
  - **Study:** DataFrames, readcsv and types.
  - **Study Resource:**
    - [Pandas DataFrames](https://www.w3schools.com/python/pandas/pandas_dataframes.asp)
    - [Pandas Read CSV](https://www.w3schools.com/python/pandas/pandas_csv.asp)

- [ ] **Day 2 (1.5h): Load and Inspect Fixture**
  - **Study:** pandas read_csv; DataFrames; data types.
  - **Study Resource:**
    - [Pandas DataFrames](https://www.w3schools.com/python/pandas/pandas_dataframes.asp)
    - [Pandas Read CSV](https://www.w3schools.com/python/pandas/pandas_csv.asp)
  - **Lab Exercise:** Complete Step 1 in the [Week 23 lab](../labs/phase-05-python.md#week-23--pandas-ingestion-and-quality).

- [ ] **Day 3 (1.5h): Detect Nulls and Duplicates**
  - **Study Resource:** [Pandas - Cleaning Data](https://www.w3schools.com/python/pandas/pandas_cleaning.asp)
  - **Lab Exercise:** Complete Step 2 in the [Week 23 lab](../labs/phase-05-python.md#week-23--pandas-ingestion-and-quality).

- [ ] **Day 4 (3h): Clean Only an Isolated Faulty Copy and Document Decisions**
  - **Study Resource:** [Pandas - Cleaning Data](https://www.w3schools.com/python/pandas/pandas_cleaning.asp)
  - **Lab Exercise:** Complete Step 3 in the [Week 23 lab](../labs/phase-05-python.md#week-23--pandas-ingestion-and-quality).

- [ ] **Day 5 (2h): Confirm Baseline 12 Unique Rows**
  - **Study:** Confirm baseline 12 unique rows.
  - **Study Resource:**
    - [Pandas - Cleaning Data](https://www.w3schools.com/python/pandas/pandas_cleaning.asp)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Review Step 3 in the [Week 23 lab](../labs/phase-05-python.md#week-23--pandas-ingestion-and-quality) and record results in the [Week 23 log](../logs/week-23.md).

**Deliverables:** Completed [Week 23 lab artifacts](../labs/phase-05-python.md#week-23--pandas-ingestion-and-quality), project work where assigned, and recorded checks/evidence.

**Self-Check:** Answer the questions in the [Week 23 log](../logs/week-23.md).

## Week 24 - Merge, group and reconcile

**Goal:** Complete the **Merge, group and reconcile** lab and verify its outputs. Follow the [Week 24 lab procedure](../labs/phase-05-python.md#week-24--merge-group-and-reconcile).

**Learning Outcomes:** Merge lookup data, group records into KPIs and reconcile results with Excel and SQL.

**Use Case:** When combining finance records with a lookup table, validate the match, summarize results, and compare them with independent totals.

- [ ] **Day 1 (1h): Groupby, Merge and Pivot**
  - **Study:** Groupby, merge and pivot.
  - **Study Resource:**
    - [Pandas DataFrame groupby() Method](https://www.w3schools.com/python/pandas/ref_df_groupby.asp)
    - [Pandas DataFrame merge() Method](https://www.w3schools.com/python/pandas/ref_df_merge.asp)
    - [Reshaping and pivot tables](https://pandas.pydata.org/docs/user_guide/reshaping.html)
    - [Group by: split-apply-combine](https://pandas.pydata.org/docs/user_guide/groupby.html)
    - [Merge, join, concatenate and compare](https://pandas.pydata.org/docs/user_guide/merging.html)

- [ ] **Day 2 (1.5h): Create Segment Lookup and Validate Join**
  - **Study:** pandas merges; lookup validation.
  - **Study Resource:**
    - [Pandas DataFrame merge() Method](https://www.w3schools.com/python/pandas/ref_df_merge.asp)
    - [Merge, join, concatenate and compare](https://pandas.pydata.org/docs/user_guide/merging.html)
  - **Lab Exercise:** Complete Step 1 in the [Week 24 lab](../labs/phase-05-python.md#week-24--merge-group-and-reconcile).

- [ ] **Day 3 (1.5h): Group Budget and Actual by Category/Month/Segment**
  - **Study:** Group budget and actual by category/month/segment.
  - **Study Resource:**
    - [Pandas DataFrame groupby() Method](https://www.w3schools.com/python/pandas/ref_df_groupby.asp)
    - [Group by: split-apply-combine](https://pandas.pydata.org/docs/user_guide/groupby.html)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Complete Step 2 in the [Week 24 lab](../labs/phase-05-python.md#week-24--merge-group-and-reconcile).

- [ ] **Day 4 (3h): Calculate Profit and Favorable Variances**
  - **Study Resource:**
    - [Pandas DataFrame groupby() Method](https://www.w3schools.com/python/pandas/ref_df_groupby.asp)
    - [Group by: split-apply-combine](https://pandas.pydata.org/docs/user_guide/groupby.html)
    - [Reshaping and pivot tables](https://pandas.pydata.org/docs/user_guide/reshaping.html)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Complete Step 3 in the [Week 24 lab](../labs/phase-05-python.md#week-24--merge-group-and-reconcile).

- [ ] **Day 5 (2h): Reconcile Q1, Monthly and January Retail to Excel/SQL**
  - **Study Resource:**
    - [Pandas DataFrame groupby() Method](https://www.w3schools.com/python/pandas/ref_df_groupby.asp)
    - [Group by: split-apply-combine](https://pandas.pydata.org/docs/user_guide/groupby.html)
    - [Excel SUMIFS Function](https://www.w3schools.com/excel/excel_sumifs.php)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Complete Step 4 in the [Week 24 lab](../labs/phase-05-python.md#week-24--merge-group-and-reconcile) and record results in the [Week 24 log](../logs/week-24.md).

**Deliverables:** Completed [Week 24 lab artifacts](../labs/phase-05-python.md#week-24--merge-group-and-reconcile), project work where assigned, and recorded checks/evidence.

**Self-Check:** Answer the questions in the [Week 24 log](../logs/week-24.md).

## Week 25 - Visualize and investigate

**Goal:** Complete the **Visualize and investigate** lab and verify its outputs. Follow the [Week 25 lab procedure](../labs/phase-05-python.md#week-25--visualize-and-investigate).

**Learning Outcomes:** Plot budget-versus-actual results, quantify segment contributions and export a concise report.

**Use Case:** When reporting monthly performance, a labeled chart and segment contributions can show where a variance came from, with limitations stated.

- [ ] **Day 1 (1h): Plotting and Labels**
  - **Study:** Plotting and labels.
  - **Study Resource:** [Chart visualization](https://pandas.pydata.org/docs/user_guide/visualization.html)

- [ ] **Day 2 (1.5h): Plot Monthly Profit and Budget**
  - **Study:** pandas plotting; monthly budget-versus-actual comparisons.
  - **Study Resource:** [Chart visualization](https://pandas.pydata.org/docs/user_guide/visualization.html)
  - **Lab Exercise:** Complete Step 1 in the [Week 25 lab](../labs/phase-05-python.md#week-25--visualize-and-investigate).

- [ ] **Day 3 (1.5h): Calculate Segment-Month Contribution to Variance**
  - **Study Resource:**
    - [Pandas DataFrame groupby() Method](https://www.w3schools.com/python/pandas/ref_df_groupby.asp)
    - [Group by: split-apply-combine](https://pandas.pydata.org/docs/user_guide/groupby.html)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Complete Step 2 in the [Week 25 lab](../labs/phase-05-python.md#week-25--visualize-and-investigate).

- [ ] **Day 4 (3h): Draft Short Report, Chart and Outputs**
  - **Study Resource:**
    - [Chart visualization](https://pandas.pydata.org/docs/user_guide/visualization.html)
    - [Purdue OWL: memo format and sample](https://owl.purdue.edu/owl/subject_specific_writing/professional_technical_writing/memos/format.html)
  - **Lab Exercise:** Complete Step 3 in the [Week 25 lab](../labs/phase-05-python.md#week-25--visualize-and-investigate).

- [ ] **Day 5 (2h): Explain Limits, Test Zero Denominator and Inspect Exported Files**
  - **Study Resource:**
    - [Pandas - Cleaning Data](https://www.w3schools.com/python/pandas/pandas_cleaning.asp)
    - [Python tutorial: errors and exceptions](https://docs.python.org/3/tutorial/errors.html)
    - [Python CSV documentation](https://docs.python.org/3/library/csv.html)
    - [Python Conditions](https://www.w3schools.com/python/python_conditions.asp)
    - [Python built-in constants: None](https://docs.python.org/3/library/constants.html#None)
    - [finance KPI definitions and control totals](../data/README.md)
  - **Lab Exercise:** Review Step 3 in the [Week 25 lab](../labs/phase-05-python.md#week-25--visualize-and-investigate) and record results in the [Week 25 log](../logs/week-25.md).

**Deliverables:** Completed [Week 25 lab artifacts](../labs/phase-05-python.md#week-25--visualize-and-investigate), project work where assigned, and recorded checks/evidence.

**Self-Check:** Answer the questions in the [Week 25 log](../logs/week-25.md).

## Week 26 - Run from scratch

**Goal:** Complete the **Run from scratch** lab and verify its outputs. Follow the [Week 26 lab procedure](../labs/phase-05-python.md#week-26--run-from-scratch).

**Learning Outcomes:** Record dependencies and versions, run a notebook from a clean start and verify its outputs.

**Use Case:** When someone else needs to rerun a notebook, a clean start and recorded setup instructions show whether the results are reproducible.

- [ ] **Day 1 (1h): Environments and Notebook Execution**
  - **Study:** Environments and notebook execution.
  - **Study Resource:**
    - [Python virtual environments](https://docs.python.org/3/library/venv.html)
    - [JupyterLab notebook documentation](https://jupyterlab.readthedocs.io/en/latest/user/notebook.html)

- [ ] **Day 2 (1.5h): Record Versions and Installation Instructions**
  - **Study:** Python environments; Jupyter setup; reproducibility.
  - **Study Resource:**
    - [Python virtual environments](https://docs.python.org/3/library/venv.html)
    - [JupyterLab notebook documentation](https://jupyterlab.readthedocs.io/en/latest/user/notebook.html)
  - **Lab Exercise:** Complete Step 1 in the [Week 26 lab](../labs/phase-05-python.md#week-26--run-from-scratch).

- [ ] **Day 3 (1.5h): Restart Kernel and Run All Cells**
  - **Study:** Restart kernel and run all cells.
  - **Study Resource:** [JupyterLab notebook documentation](https://jupyterlab.readthedocs.io/en/latest/user/notebook.html)
  - **Lab Exercise:** Complete Step 2 in the [Week 26 lab](../labs/phase-05-python.md#week-26--run-from-scratch).

- [ ] **Day 4 (3h): Complete Project B Notebook and Quality Tests on Clean Copies**
  - **Study Resource:** [Pandas - Cleaning Data](https://www.w3schools.com/python/pandas/pandas_cleaning.asp)
  - **Lab Exercise:** Complete Step 3 in the [Week 26 lab](../labs/phase-05-python.md#week-26--run-from-scratch).

- [ ] **Day 5 (2h): Demonstrate Outputs and Complete Phase Gate**
  - **Study Resource:**
    - [Python virtual environments](https://docs.python.org/3/library/venv.html)
    - [JupyterLab notebook documentation](https://jupyterlab.readthedocs.io/en/latest/user/notebook.html)
  - **Lab Exercise:** Review Step 3 in the [Week 26 lab](../labs/phase-05-python.md#week-26--run-from-scratch) and record results in the [Week 26 log](../logs/week-26.md).

**Deliverables:** Versioned setup notes, clean notebook run, outputs and quality-test evidence.  

**Self-Check:** Answer the questions in the [Week 26 log](../logs/week-26.md).


**Exit:** A fresh environment can run the notebook top-to-bottom; explicit quality checks and Q1, monthly, and slice controls pass. Outputs preserve limitations and do not infer causes.
