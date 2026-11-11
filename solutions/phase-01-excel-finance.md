# Phase 1 — Excel and Finance Solutions

[Solutions index](README.md) · [Week 4 lab and stakeholder request](../labs/phase-01-excel-finance.md#week-4--management-handoff)

## Week 1 — Setup and finance foundations

For the January Retail hand check, actual revenue is CAD 105,000 and actual expense is CAD 62,000, so actual profit is CAD 43,000. Budget profit is CAD 40,000; favorable profit variance is CAD 3,000.

## Week 4 — Management handoff

The figures below use the fictional [finance dataset](../data/finance_monthly.csv) and its [KPI definitions](../data/README.md). Check them in your workbook before using the memo.

### 1. Clarify the request

The simulated manager confirmed the scope: January–March 2025; Retail and Business; CAD; actual compared with budget. Profit is revenue minus expense. For favorable variance, higher revenue and lower expense are favorable. The audience is the finance manager and the output is a short summary with an investigation request.

In a real engagement, confirm unresolved definitions and scope with the stakeholder rather than assuming a reply.

### 2. Check and analyze the data

Check 12 unique rows, the expected date range, complete amounts and unique month/segment/category combinations. Then calculate:

| Q1 metric | Budget CAD | Actual CAD | Favorable variance CAD |
|---|---:|---:|---:|
| Revenue | 585,000 | 599,000 | 14,000 |
| Expense | 338,000 | 342,000 | -4,000 |
| Profit | 247,000 | 257,000 | 10,000 |

Revenue contributes $14,000 favorably; the $4,000 increase in expense contributes $4,000 unfavorably. Together, $14,000 − $4,000 = $10,000 favorable profit variance. For example, January Retail actual profit is $105,000 − $62,000 = $43,000, compared with budget profit of $100,000 − $60,000 = $40,000; its favorable variance is $3,000.

### 3. Investigate month and segment

| Period | Retail favorable profit variance CAD | Business favorable profit variance CAD | Total CAD |
|---|---:|---:|---:|
| January | 3,000 | -1,000 | 2,000 |
| February | -1,000 | 2,000 | 1,000 |
| March | 3,000 | 4,000 | 7,000 |
| **Q1** | **5,000** | **5,000** | **10,000** |

March has the largest monthly favorable profit variance, $7,000. In March, Business contributes $4,000 and Retail $3,000. Both segments contribute $5,000 across Q1.

### 4. Separate findings from explanations

Possible questions for the data owner include: Did price or sales volume change? Were revenue or expenses shifted between months? Which products or expense categories drove the change? These are questions, not conclusions: the synthetic data does not contain enough detail to establish a cause.

### 5. Sample management memo

**To:** Finance Manager  
**Subject:** Q1 2025 actual performance versus budget

Actual profit for January–March was **$257,000**, compared with a budget of **$247,000**: a **$10,000 favorable variance**. Revenue was $14,000 higher than budget, while expenses were $4,000 higher than budget; the expense increase is an **unfavorable** contribution, leaving the $10,000 favorable profit variance.

March had the largest monthly favorable profit variance at **$7,000**. Within March, the Business segment contributed $4,000 and Retail contributed $3,000. Across the full quarter, each segment contributed $5,000 of the favorable profit variance.

These are fictional, summarized figures for three months; they do not establish the causes of the variances or represent a complete income statement. I recommend asking the data owner for revenue and expense detail, then investigating whether pricing, volume, timing or other factors explain the March result.

### 6. Reproduce and hand off

Keep the workbook, memo and evidence of the actual checks performed. Repeat the checks using a clean input copy and, if you used Power Query, refresh the query. If you used the free web alternative, re-import or copy the clean data into a separate worksheet and rerun the formula and PivotTable checks. Record any differences rather than claiming an unperformed refresh or review.
