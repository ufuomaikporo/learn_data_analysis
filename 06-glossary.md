# Glossary

[Overview](README.md) · [Data contract](data/README.md) · [Schedules](weekly-schedules/README.md)

Plain-language definitions for terms used throughout the roadmap. Examples refer to the fictional finance dataset unless noted otherwise.

## Data basics

| Term | Plain-language meaning |
|---|---|
| Dataset | A collection of related information, usually organized into rows and columns. |
| Fixture | A small, fixed sample dataset for learning and testing. This roadmap's finance data is fictional. |
| Row / record | One item in a dataset. In the finance file, a row contains the figures for one month, one segment and one category. |
| Field / column | One kind of information recorded for each row, such as `month` or `actual_cad`. |
| Data type | The kind of value a field should contain, such as a date, text, whole number or decimal number. |
| Row grain (grain) | What one row represents. Here, one row represents one specific combination of month, segment and category, with a budget and actual amount for that combination. Grain matters because combining data at the wrong level can duplicate or misstate totals. |
| Data dictionary | A list describing each field, its meaning, data type and any rules it must follow. |
| CSV | A plain-text file format that stores values separated by commas; it can be opened in spreadsheet and data tools. |
| CAD | Canadian dollars, the currency used for the amounts in the finance dataset. |
| DataFrame | A table of rows and columns used by the Python pandas library. |

## Finance and checking results

| Term | Plain-language meaning |
|---|---|
| KPI | Key Performance Indicator: a measure used to track performance, such as revenue, expense or profit. |
| Budget / actual | Budget is the planned amount; actual is the amount recorded for the period. |
| Finance variance | The difference between actual and budget. The data contract defines the exact formulas and signs for each measure. |
| Favorable / unfavorable variance | A favorable difference is better than budget; an unfavorable one is worse. Higher revenue and lower expense are favorable in this roadmap. |
| Denominator | The bottom part of a fraction. For percentage variance, the budget is the denominator; if it is zero, the percentage is undefined. |
| Control total | A known total used to check whether a calculation or report is correct. |
| Reconciliation | Comparing results calculated in separate ways or tools, then investigating any differences. |
| Data quality check | A test for issues such as missing values, duplicate rows, invalid values or unexpected totals. |

## Statistics

| Term | Plain-language meaning |
|---|---|
| Population / sample | The population is the full group you want to understand; a sample is the smaller set of observations you actually analyze. |
| Distribution | How values are spread across a dataset, including where values cluster and how far they vary. |
| Mean / median | The mean is the arithmetic average; the median is the middle value after sorting. The median is less affected by extreme values. |
| Statistical variance | A measure of how spread out values are. This is different from finance variance, which compares actual with budget. |
| Outlier | A value unusually far from most other values; it should be checked, not automatically removed. |
| Correlation / causation | Correlation means two things vary together; it does not prove that one caused the other. |
| Confidence interval | A range that expresses uncertainty around an estimate from a sample. |
| Regression | A method for describing or estimating relationships between variables; a regression result alone does not prove cause and effect. |

## Analysis and data models

| Term | Plain-language meaning |
|---|---|
| Filter | A way to show only rows that meet selected conditions, such as one month or segment. |
| Aggregation | Combining many rows into a summary using a calculation such as sum, count or average. |
| Query | A set of instructions asking a database for selected or summarized data. |
| GROUP BY | A SQL instruction that groups rows by selected fields before calculating a summary for each group. |
| Window function | A SQL calculation that uses related rows while keeping each row visible in the result. |
| Lookup table | A small table that provides extra information for a code or value, such as a segment name and its description. |
| Key | A value used to identify a row or connect related tables. |
| Primary key | A field, or combination of fields, that uniquely identifies each row in its table. |
| Foreign key | A field whose value refers to a key in another table, connecting the two tables. |
| Join | A way to combine rows from tables using matching key values. |
| Left join | A join that keeps every row from the first table and adds matching information from the second; unmatched rows are still kept. |
| One-to-many relationship | A connection where one row in a lookup table can match several rows in a detail table; for example, one segment can appear in many months and categories. |
| Fact table | A table of measurable amounts or events, such as the budget and actual figures in the finance dataset. |
| Dimension | A descriptive table used to group or filter facts, such as a calendar or segment list. |
| Star schema | A data model with a central fact table connected to descriptive dimension tables. |
| PivotTable | An Excel feature that summarizes data by categories, such as profit by month or segment. |
| Dashboard | A report that brings together key measures and visuals to help someone monitor or explore results. |
| Measure | A calculation in Power BI, such as total revenue, that can update when report filters change. |

## Tools and methods

| Term | Plain-language meaning |
|---|---|
| SQL | A language for retrieving and summarizing data stored in relational databases. |
| pandas | A Python library for working with table-shaped data, including DataFrames. |
| Power BI | A Microsoft tool for building data models and interactive reports. |
| Power Query | An Excel and Power BI tool for importing, reshaping and cleaning data through repeatable steps. |
| DAX | The formula language used to define calculations and measures in Power BI. |
