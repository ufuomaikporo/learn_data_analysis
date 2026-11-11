# Phase 1 Lab — Excel and Finance

[Schedule](../weekly-schedules/phase-01-excel-finance.md) · [Data contract](../data/README.md) · [Worked solutions](../solutions/phase-01-excel-finance.md)

Create a separate workbook. Treat all provided CSVs as read-only, and save any cleaned or test data as clearly named copies in the workbook or an output folder. Suggested sheets: `Source`, `Dictionary`, `Checks`, `Analysis`, `Summary`. You can use Excel for the web for the core exercises or Excel desktop. The Power Query exercise has a manual web alternative below; consult the [resource map](../02-courses-and-reading.md) for feature and license differences.

## Week 1 — Setup and finance foundations

1. Import [finance_monthly.csv](../data/finance_monthly.csv) into a structured table called `Finance`. Check that dates are dates, amounts are numbers, and IDs are unique. Record the row grain—what one row represents; for this file, one month, one segment and one category—and the reporting currency. See the [glossary](../06-glossary.md#data-basics) if needed.
2. Document revenue, expenses as positive costs, profit, budget and actual. Explain why profit differs from cash flow and why these data do not constitute a complete income statement.
3. Count rows, IDs, empty cells and month/segment/category combinations. Check the expected counts and date range against the data contract. Show exceptions instead of hiding them.
4. Manually calculate January Retail actual revenue and expense, budget and actual profit, and favorable profit variance. Record the source rows and calculation as a hand check.
5. Save the workbook, the field dictionary and a short note describing assumptions and the hand check.

## Week 2 — Formula-driven analysis

1. Use `SUMIFS` on the structured table to calculate revenue and expense for budget and actual, first for Q1 then by month and segment. Calculate profit using the KPI contract, and verify criteria ranges against the original data.
2. Use the [KPI contract](../data/README.md) to add favorable variance for Revenue, Expense and Profit. Check the signs with one favorable and one unfavorable example.
3. Add category and profit percentage variance using the relevant budget denominator from the contract. Guard against zero denominators and label the result as undefined.
4. Import [segment_lookup.csv](../data/segment_lookup.csv) into the `Dictionary` sheet and use XLOOKUP to retrieve a segment description. Demonstrate a missing lookup as a visible exception, not an unexplained blank; use a test-only value without changing the CSV.
5. Compare Q1 values with the independent controls in the [data contract](../data/README.md), and hand-check one monthly result against its source rows. In a test-only calculation, set a denominator to zero and verify the percentage is undefined.

## Week 3 — Power Query, pivots, and exceptions

1. **Power Query route:** Import the CSV into a separate query; explicitly set date, text, and numeric types, and inspect errors. Document each applied step; refresh without altering the raw file. **Free web alternative if you cannot create a query:** Open a copy of the CSV in Excel for the web and copy its contents to a separate worksheet in the workbook. Inspect dates, text and numeric values, document any corrections and verify 12 rows. This is manual cleaning, not a Power Query refresh or evidence of Power Query experience. Keep the original file untouched.
2. Build PivotTables by month, segment and category. Ensure the source is the intended table, then verify summed values against the formula sheet. Derive profit separately; do not sum Revenue and Expense into a single revenue total.
3. Create a monthly budget-versus-actual profit chart and a segment variance view; include currency, date range and a descriptive title.
4. Import [finance_monthly_unclean.csv](../data/finance_monthly_unclean.csv) into a clearly named separate query or worksheet. Create checks that visibly identify data-quality issues; do not repair by silently replacing a missing amount with zero. Keep the clean [finance_monthly.csv](../data/finance_monthly.csv) unchanged and use it only as a validation reference after documenting your decisions.
5. Return to the unmodified baseline and confirm totals. Record the error, handling decision, and what cannot be inferred from this small dataset.

## Week 4 — Management handoff

### Fictional stakeholder request

You are an analyst supporting a finance manager. The manager sends you this request:

> Please review our January–March 2025 financial results against budget. Did we make more or less profit than planned? How much of the difference came from revenue and expenses? Which month and business segment should we look at more closely? Please send me a short summary and tell me what you would investigate next.

The manager has supplied the fictional dataset. Your role is to clarify the request, check the data, answer the questions using evidence, and communicate what the data can and cannot tell you.

### Analyst tasks

1. **Clarify the request.** Before calculating, write down the reporting period, audience, units, segments and definitions you intend to use. For this exercise, the simulated manager confirms: include January–March 2025, both Retail and Business, and amounts in CAD; compare actual with budget. Profit means revenue minus expense. A positive favorable variance means better than budget. Use the [data contract](../data/README.md) for the exact signs. If a real request is unclear, ask the stakeholder instead of assuming; do not invent a response from a real person.
2. **Check the data and calculate the answer.** Confirm 12 rows, unique keys, no missing amounts and the correct period. Calculate Q1 budget and actual revenue, expense and profit; show favorable variance for each. Check the totals against the data contract. Trace at least one result to its source rows. If a check fails, investigate and resolve it before reporting.
3. **Identify useful follow-up questions.** Use your workbook to answer: Which month had the largest favorable profit variance? How much did each segment contribute to the quarterly profit variance? For the largest month, compare the segments. Note that a segment's contribution is its actual profit minus its budget profit; segment contributions should add to the total profit variance.
4. **Separate findings from explanations.** The dataset shows *what* changed, not *why*. List at least two questions for a real finance manager or data owner, such as whether the difference came from pricing, sales volume, or a timing shift, and what expense details are available. Label these as questions, not established causes.
5. **Prepare the management memo.** Write your own or adapt the [sample solution](../solutions/phase-01-excel-finance.md#week-4--management-handoff). Verify every figure in the workbook first; include the question, overall result, revenue and expense contributions, a month/segment finding, the data limitations and a specific next action. Use the `Summary` sheet or a separate document. A drafted template is acceptable, but you are responsible for checking and explaining it.
6. **Reproduce and hand off.** Reopen or rebuild from a clean input copy and rerun the checks. If you used Power Query, refresh it; if using free Excel for the web without Power Query, re-import or copy the clean data into a separate worksheet and rerun the formulas and PivotTable checks instead. Document what you actually tested and do not overwrite raw input. Review the [phase gate](../05-study-tracker.md) and save the workbook, memo, screenshots and check results for Project B.
