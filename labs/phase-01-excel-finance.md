# Phase 1 Lab — Excel and Finance

[Schedule](../weekly-schedules/phase-01-excel-finance.md) · [Data contract](../data/README.md) · [Worked solutions](../solutions/phase-01-excel-finance.md)

Create a separate workbook. Treat all provided CSVs as read-only, and save any cleaned or test data as clearly named copies in the workbook or an output folder. Use these sheets to keep the work organized:

| Sheet | What to put there |
|---|---|
| `Source` | An unchanged copy of the input CSV data, formatted as a table named `Finance`. Keep the original values intact; put any cleaned or test data in a separate, clearly named area or copy. |
| `Dictionary` | A field dictionary listing each column, its meaning, data type, and any relevant rule or assumption. Include the row grain (one month, segment, and category) and the reporting currency (CAD). |
| `Checks` | Data-quality checks and their results: row and unique-ID counts, data types, blank cells, expected date range, and month/segment/category combinations. Compare results with the [data contract](../data/README.md) and record exceptions and how you handled them. |
| `Analysis` | The calculations used to answer the exercises, such as budget and actual revenue, expenses, profit, and favorable variance. Show formulas or other calculation steps and retain the January Retail hand check with its source rows. |
| `Summary` | A short, readable statement of the key findings, scope, assumptions, and limitations. Distinguish what the data shows from what cannot be concluded, such as cash flow or the causes of a variance. |

You can use Excel for the web for the core exercises or Excel desktop. The Power Query exercise has a manual web alternative below; consult the [resource map](../02-courses-and-reading.md) for feature and license differences.

## Week 1 — Setup and finance foundations

1. In `Source`, import [finance_monthly.csv](../data/finance_monthly.csv) as a structured table called `Finance`, preserving the input values. In `Dictionary`, record the row grain—one month, one segment and one category—and reporting currency. Check date and amount types in `Checks`. See the [glossary](../06-glossary.md#data-basics) if needed.
2. In `Dictionary`, define revenue, expenses as positive costs, profit, budget and actual. Explain there why profit differs from cash flow and why these data do not constitute a complete income statement.
3. In `Checks`, count rows, IDs, empty cells and month/segment/category combinations. Compare the results and date range with the data contract; show exceptions instead of hiding them.
4. In `Analysis`, manually calculate January Retail actual revenue and expense, budget and actual profit, and favorable profit variance. Keep the source rows or their identifiers with the calculation as a hand check.
5. In `Summary`, write a short note describing assumptions, the hand-check result, and any remaining data limitations. Save the workbook with the `Source`, `Dictionary`, `Checks`, `Analysis`, and `Summary` sheets.

## Week 2 — Formula-driven analysis

1. In `Analysis`, use `SUMIFS` on the `Source` table to calculate revenue and expense for budget and actual, first for Q1 then by month and segment. Calculate profit using the KPI contract, and verify criteria ranges against the original data.
2. In `Analysis`, use the [KPI contract](../data/README.md) to add favorable variance for Revenue, Expense and Profit. In `Checks`, verify the signs with one favorable and one unfavorable example.
3. In `Analysis`, add category and profit percentage variance using the relevant budget denominator from the contract. Guard against zero denominators and label the result as undefined; record the zero-denominator check in `Checks`.
4. In `Dictionary`, import [segment_lookup.csv](../data/segment_lookup.csv) as a separate lookup table and use XLOOKUP to retrieve a segment description. In `Checks`, demonstrate a missing lookup as a visible exception, not an unexplained blank; use a test-only value without changing the CSV.
5. In `Checks`, compare Q1 values with the independent controls in the [data contract](../data/README.md). In `Analysis`, hand-check one monthly result against its source rows and perform a test-only zero-denominator calculation; record that the percentage is undefined in `Checks`.

## Week 3 — Power Query, pivots, and exceptions

1. **Power Query route:** Create a separate query from the `Source` data; explicitly set date, text, and numeric types, and inspect errors. In `Checks`, document the applied steps and results; refresh without altering `Source`. **Free web alternative if you cannot create a query:** Open a copy of the CSV in Excel for the web and copy it to a clearly named separate worksheet. Inspect dates, text and numeric values, and document corrections and the 12-row count in `Checks`. This is manual cleaning, not a Power Query refresh or evidence of Power Query experience. Keep the original file untouched.
2. In `Analysis`, build PivotTables by month, segment and category. Ensure the source is the intended table, then verify summed values against the formula calculations; record reconciliation results in `Checks`. Derive profit separately; do not sum Revenue and Expense into a single revenue total.
3. In `Analysis`, create a monthly budget-versus-actual profit chart and a segment variance view; include currency, date range and a descriptive title.
4. Import [finance_monthly_unclean.csv](../data/finance_monthly_unclean.csv) into a clearly named separate query or worksheet, not `Source`. In `Checks`, create checks that visibly identify data-quality issues and record your handling decision; do not repair by silently replacing a missing amount with zero. Keep the clean [finance_monthly.csv](../data/finance_monthly.csv) unchanged and use it only as a validation reference.
5. In `Checks`, return to the unmodified baseline and confirm totals. In `Summary`, record the error, handling decision, and what cannot be inferred from this small dataset.

## Week 4 — Management handoff

### Fictional stakeholder request

You are an analyst supporting a finance manager. The manager sends you this request:

> Please review our January–March 2025 financial results against budget. Did we make more or less profit than planned? How much of the difference came from revenue and expenses? Which month and business segment should we look at more closely? Please send me a short summary and tell me what you would investigate next.

The manager has supplied the fictional dataset. Your role is to clarify the request, check the data, answer the questions using evidence, and communicate what the data can and cannot tell you.

### Analyst tasks

1. **Clarify the request.** In `Summary`, write down the reporting period, audience, units and segments. For this exercise, the simulated manager confirms: include January–March 2025, both Retail and Business, and amounts in CAD; compare actual with budget. In `Dictionary`, record the definitions: profit means revenue minus expense, and a positive favorable variance means better than budget. Use the [data contract](../data/README.md) for the exact signs. If a real request is unclear, ask the stakeholder instead of assuming; do not invent a response from a real person.
2. **Check the data and calculate the answer.** In `Checks`, confirm 12 rows, unique keys, no missing amounts and the correct period. In `Analysis`, calculate Q1 budget and actual revenue, expense and profit, and show favorable variance for each. In `Checks`, compare the totals against the data contract. Trace at least one result in `Analysis` to its `Source` rows. If a check fails, investigate and resolve it before reporting.
3. **Identify useful follow-up questions.** In `Analysis`, answer: Which month had the largest favorable profit variance? How much did each segment contribute to the quarterly profit variance? For the largest month, compare the segments. Note that a segment's contribution is its actual profit minus its budget profit; segment contributions should add to the total profit variance.
4. **Separate findings from explanations.** In `Summary`, list at least two questions for a real finance manager or data owner, such as whether the difference came from pricing, sales volume, or a timing shift, and what expense details are available. The dataset shows *what* changed, not *why*; label these as questions, not established causes.
5. **Prepare the management memo.** Write your own or adapt the [sample solution](../solutions/phase-01-excel-finance.md#week-4--management-handoff). Verify every figure in `Analysis` and `Checks` first; include the question, overall result, revenue and expense contributions, a month/segment finding, data limitations and a specific next action. Put the memo in `Summary` or a separate document. A drafted template is acceptable, but you are responsible for checking and explaining it.
6. **Reproduce and hand off.** Reopen or rebuild from a clean input copy and rerun the checks in `Checks`. If you used Power Query, refresh it; if using free Excel for the web without Power Query, re-import or copy the clean data into a separate worksheet and rerun the formulas in `Analysis` and PivotTable checks. Document what you actually tested in `Checks` and do not overwrite `Source`. Review the [phase gate](../05-study-tracker.md) and save the workbook, memo, screenshots and check results for Project B.
