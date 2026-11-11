# Phase 2 — SQL and Finance Queries Solutions

[Solutions index](README.md) · [Phase 2 lab](../labs/phase-02-sql.md)

Try each exercise before using these examples. Adapt names and formatting to your own database and record the actual checks you ran.

## Week 5 — Create and import

```sql
CREATE TABLE finance (
  record_id INTEGER PRIMARY KEY,
  month TEXT NOT NULL,
  segment TEXT NOT NULL,
  category TEXT NOT NULL CHECK (category IN ('Revenue', 'Expense')),
  budget_cad REAL NOT NULL CHECK (budget_cad >= 0),
  actual_cad REAL NOT NULL CHECK (actual_cad >= 0),
  UNIQUE (month, segment, category)
);
.import --csv --skip 1 'data\finance_monthly.csv' finance
SELECT COUNT(*) AS row_count FROM finance;
SELECT * FROM finance
WHERE month = '2025-01-01' AND segment = 'Retail';
```

The baseline import contains 12 rows. The January Retail slice contains one Revenue row and one Expense row.

## Week 6 — Group and reconcile

Example monthly/segment aggregation:

```sql
SELECT
  month,
  segment,
  SUM(CASE WHEN category = 'Revenue' THEN actual_cad ELSE 0 END) AS actual_revenue,
  SUM(CASE WHEN category = 'Expense' THEN actual_cad ELSE 0 END) AS actual_expense,
  SUM(CASE WHEN category = 'Revenue' THEN budget_cad ELSE 0 END) AS budget_revenue,
  SUM(CASE WHEN category = 'Expense' THEN budget_cad ELSE 0 END) AS budget_expense
FROM finance
GROUP BY month, segment
ORDER BY month, segment;
```

Subtract expense from revenue for profit. For full Q1, actual revenue is CAD 599,000, actual expense CAD 342,000, actual profit CAD 257,000, and favorable profit variance CAD 10,000. The data contract lists the budget and category-level controls.

## Week 7 — Keys and joins

The baseline left join returns 12 fact rows, with no unmatched segments. In the isolated unknown-segment test, an inner join drops the unmatched fact while a left join preserves it with NULL lookup fields. A duplicate lookup key can multiply fact rows; enforce uniqueness instead.

For a percentage with a zero denominator, `NULLIF(denominator, 0)` prevents a divide-by-zero result; the resulting NULL means undefined, not zero.

## Week 8 — Data-quality checks and subqueries

The clean baseline passes the documented row, key, amount, category, lookup and date checks. When staging the provided unclean fixture, the checks should surface its seeded exceptions; see the [shared data-quality fixture answer key](finance-data-quality-fixture.md) for the exact issue inventory. Keep all test records out of baseline analysis.

## Week 9 — CTE and window calculations

```sql
WITH monthly AS (
  SELECT
    month,
    SUM(CASE WHEN category = 'Revenue' THEN actual_cad ELSE 0 END)
      - SUM(CASE WHEN category = 'Expense' THEN actual_cad ELSE 0 END) AS actual_profit,
    SUM(CASE WHEN category = 'Revenue' THEN budget_cad ELSE 0 END)
      - SUM(CASE WHEN category = 'Expense' THEN budget_cad ELSE 0 END) AS budget_profit
  FROM finance
  GROUP BY month
)
SELECT
  month,
  actual_profit,
  budget_profit,
  SUM(actual_profit) OVER (
    ORDER BY month ROWS BETWEEN UNBOUNDED PRECEDING AND CURRENT ROW
  ) AS running_actual_profit,
  LAG(actual_profit) OVER (ORDER BY month) AS previous_month_profit
FROM monthly
ORDER BY month;
```

| Month | Actual profit CAD | Budget profit CAD | Running actual profit CAD | Previous-month actual profit CAD |
|---|---:|---:|---:|---:|
| January | 77,000 | 75,000 | 77,000 | NULL |
| February | 83,000 | 82,000 | 160,000 | 77,000 |
| March | 97,000 | 90,000 | 257,000 | 83,000 |

January's previous-month value is NULL because the ordered result has no earlier month.
