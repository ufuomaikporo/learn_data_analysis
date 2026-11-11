# Phase 3 — Power BI Modeling and Reporting Solutions

[Solutions index](README.md) · [Phase 3 lab](../labs/phase-03-power-bi.md)

Attempt the lab before consulting these reference results. Adapt table and column names to your model.

## Week 11 — Import and quality

The baseline has 12 rows: six Revenue and six Expense rows. IDs and month/segment/category combinations are unique; the baseline contains no missing dates, categories or amounts.

## Week 12 — Model the grain

A suitable model keeps `Finance` as the fact table at month × segment × category. Use unique `Segment` and `Calendar` dimensions related one-to-many to the fact table with single-direction filters. Use dimension fields for segment/date slicers and avoid ambiguous active filter paths.

## Week 13 — Measures and checks

```DAX
Actual Revenue = CALCULATE(SUM(Finance[actual_cad]), Finance[category] = "Revenue")
Actual Expense = CALCULATE(SUM(Finance[actual_cad]), Finance[category] = "Expense")
Budget Revenue = CALCULATE(SUM(Finance[budget_cad]), Finance[category] = "Revenue")
Budget Expense = CALCULATE(SUM(Finance[budget_cad]), Finance[category] = "Expense")
Actual Profit = [Actual Revenue] - [Actual Expense]
Budget Profit = [Budget Revenue] - [Budget Expense]
Favorable Profit Variance = [Actual Profit] - [Budget Profit]
Revenue Favorable Variance = [Actual Revenue] - [Budget Revenue]
Expense Favorable Variance = [Budget Expense] - [Actual Expense]
Profit Variance % = DIVIDE([Favorable Profit Variance], [Budget Profit])
```

`DIVIDE` returns blank for a zero denominator unless a different alternate result is supplied. Revenue favorable variance is actual revenue minus budget revenue; expense favorable variance is budget expense minus actual expense. These measures apply a category filter inside `CALCULATE`; a category slicer may interact with that filter, so test and document the intended behavior.

## Week 14 — Report design

For January Retail, actual profit is CAD 43,000, budget profit CAD 40,000, and favorable profit variance CAD 3,000. The baseline Q1 controls are in the [data contract](../data/README.md).
