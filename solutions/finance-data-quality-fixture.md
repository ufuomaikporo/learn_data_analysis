# Data fixtures — worked checks

[Data contract](../data/README.md) · [Unclean practice data](../data/finance_monthly_unclean.csv) · [Clean baseline](../data/finance_monthly.csv)

Try the data-quality labs before consulting these answers.

## Clean baseline checks

The clean fixture has 12 unique IDs and 12 unique month/segment/category combinations; six Revenue and six Expense rows; no missing dates, categories, or amounts; and only valid month-start dates and nonnegative amounts. By month, actual profit is **77,000 / 83,000 / 97,000** and budget profit is **75,000 / 82,000 / 90,000**, respectively.

## Unclean fixture checks

The unclean fixture contains 13 rows and the same six columns as the clean baseline. Its issues are:

| Row / record | Issue | Expected comparison with the clean baseline |
|---|---|---|
| Second occurrence of `record_id` 1 | Duplicate ID and duplicate month/segment/category key | Keep one occurrence; the clean baseline has one such row. |
| `record_id` 6 | Missing `actual_cad` | The clean fixture has `64,000`; in a real workflow, confirm a missing amount with its source rather than assuming or imputing it. |
| `record_id` 7 | Invalid date (`2025-02-30`) | The clean fixture has `2025-02-01`; validate dates instead of coercing invalid dates silently. |
| `record_id` 8 | Invalid category (`Other`) | The clean fixture has `Expense`. |
| `record_id` 9 | Nonnumeric `budget_cad` (`not_available`) | The clean fixture has `120,000`. |
| `record_id` 10 | Negative `actual_cad` | The clean fixture has `73,000`; expenses are stored as positive costs under this data contract. |

After documenting each detection and remediation decision, compare the result with [finance_monthly.csv](../data/finance_monthly.csv): it should contain 12 rows, 12 unique IDs, 12 unique business keys, valid month-start dates, allowed categories, and nonnegative numeric amounts. The clean file is a reference for this synthetic exercise, not evidence that a real missing or invalid value may be safely replaced.
