# Synthetic Finance Dataset and Controls

[Overview](../README.md) · [Glossary](../06-glossary.md) · [Portfolio projects](../projects/README.md)

Use [finance_monthly.csv](finance_monthly.csv) as a **fictional learning fixture**, not real financial or banking data. It has 12 rows for January–March 2025. In plain language, each row represents one month, one business segment and one category (Revenue or Expense); this description of what a row represents is called its **row grain**. Each row has one budget amount and one actual amount for that combination. All amounts are nonnegative CAD; expense is a positive cost, not a signed negative. Dates are the first day of the reporting month. No customer, account, transaction, credit, or cash-flow data is present, so do not claim customer, delinquency, cash-flow, or bank-transaction findings from it.

| Field | Type | Definition / constraint |
|---|---|---|
| `record_id` | integer | Unique row identifier |
| `month` | ISO date | Month start; three months |
| `segment` | text | Retail or Business, fictional business lines |
| `category` | text | Revenue or Expense |
| `budget_cad` | number | Monthly budget, CAD |
| `actual_cad` | number | Monthly actual, CAD |

## KPI contract

- **Revenue:** Sum amounts in Revenue rows. Calculate separately for budget and actual.
- **Expense:** Sum amounts in Expense rows. Expense is stored as a positive cost. Calculate separately for budget and actual.
- **Profit:** Revenue minus expense, calculated separately for budget and actual.
- **Raw variance:** Actual minus budget for each category.
- **Favorable variance:** For Revenue, actual minus budget; for Expense, **budget minus actual**. A positive value is favorable.
- **Favorable profit variance:** Actual profit minus budget profit. A positive value is favorable. Do not combine Revenue and Expense as if both were revenue.
- **Percentage variance by category:** Raw variance divided by that category's budget.
- **Profit variance percentage:** (Actual profit − budget profit) divided by budget profit.
- **Zero denominator:** If the relevant budget denominator is zero, return blank/undefined, not zero. State which percentage measure you are reporting.
- **Scope:** These are management-reporting measures, not a full income statement. They exclude tax, balance sheet, cash flow, FX and unrepresented costs. All data is fictional; no causation can be established.

## Independent control totals

| Full Q1 2025, both segments | Budget CAD | Actual CAD | Favorable variance CAD |
|---|---:|---:|---:|
| Revenue | 585,000 | 599,000 | 14,000 |
| Expense | 338,000 | 342,000 | -4,000 |
| Profit | 247,000 | 257,000 | 10,000 |

Keep raw inputs read-only and create separate output copies. For expected baseline validation checks and monthly profit results, see the [worked data-fixture checks](../solutions/finance-data-quality-fixture.md) after attempting the labs.

## Clean project data and unclean practice data

Use the clean [finance_monthly.csv](finance_monthly.csv) as the input for both portfolio projects and for cross-tool reconciliation. The separate [finance_monthly_unclean.csv](finance_monthly_unclean.csv) is a deliberately altered practice fixture for data-quality labs and isolated project tests; it is not a second project dataset and must not be used to calculate the project findings. Preserve both source files unchanged.

## Join practice lookup

Use the separate [segment_lookup.csv](segment_lookup.csv) as portable lookup/dimension input for XLOOKUP, SQL joins, pandas merges, and Project A. It represents a small extract from segment master data: in production, this reference data would usually be maintained as a source-system or warehouse table, but it may be exported as a separate CSV when working with file-based data. For SQL practice, import it into a `segment_lookup` table in the same SQLite database as the finance facts; do not create a separate database just for this table. It contains one row for each valid `segment` and a `segment_description`; it is not a copy of the finance facts. The expected join is many fact rows to one lookup row, so preserve `segment` uniqueness. This small exercise joins on the segment value; production models commonly use a stable segment code or dimension ID. For unmatched-key and duplicate-key tests, alter only a clearly named test copy, not this file.
