# Weekly Self-Check Answers

[Solutions index](README.md) · [Weekly logs](../logs/README.md) · [Weekly schedules](../weekly-schedules/README.md)

Try to answer the questions before reading this guide. These are sample explanations, not scripts to memorize; a different answer is acceptable when it is accurate and well supported. The fourth answer gives a real-world example of applying that week's concepts as a data analyst.

## Week 1 Self-Check Answers

1. **Row grain:** The grain describes what one record represents. Confirming it before summarizing helps avoid counting the same business event more than once.
2. **Finance measures:** Revenue is income earned and expense is a cost. Profit is revenue minus expense; budget is the plan and actual is what was recorded.
3. **Clarifying scope:** Check the data contract, then confirm the period, currency, included segments, and field definitions with the data owner if anything remains unclear. Comparisons are unreliable when those scopes or meanings differ.
4. **Real-world application:** Confirming row grain prevents double-counting, and keeping expenses as positive costs makes the profit and favorable-variance calculations clear. For example, for January Retail, actual profit is CAD 105,000 revenue minus CAD 62,000 expense, or CAD 43,000; compare it with CAD 40,000 budget profit to report a CAD 3,000 favorable variance.

## Week 2 Self-Check Answers

1. **Formula choice:** `SUMIFS` adds values that meet criteria; `XLOOKUP` finds a matching key and returns related information, such as a label.
2. **Favorable signs:** Higher revenue is favorable, while lower expense is favorable. Higher profit than budget is favorable when using the roadmap's KPI contract.
3. **Zero denominator:** A percentage with a zero budget denominator is undefined, not zero. Label it as undefined or not applicable so readers do not mistake it for no variance.
4. **Real-world application:** These tools make recurring budget-versus-actual summaries consistent and traceable. For example, use SUMIFS to total actual revenue by segment, XLOOKUP to add its description, and the agreed variance rule to label performance; report a zero-budget percentage as undefined.

## Week 3 Self-Check Answers

1. **Repeatable cleaning:** Power Query is useful when the same import and cleaning steps need to be refreshed. Manual edits may suit a one-time task, but should not replace or obscure the source.
2. **PivotTables:** A PivotTable groups and summarizes source rows by selected fields. Reconciliation with formulas can reveal an incorrect source range, field, or calculation.
3. **Charts and exceptions:** A line chart can show change over time; a bar chart can compare segments. Label units and periods, and show data exceptions rather than silently excluding them.
4. **Real-world application:** Together, these tools support repeatable preparation, summaries, communication, and visible quality checks. For example, refresh a monthly CSV with Power Query, summarize by segment in a PivotTable, chart the trend, and flag malformed amounts instead of silently changing them.

## Week 4 Self-Check Answers

1. **Clarifying a request:** Confirm audience, period, units, scope, and KPI definitions before calculating so the answer matches the decision being requested.
2. **Variance contribution:** Revenue changes affect profit in the same direction; expense increases reduce profit. The defined revenue and expense contributions should reconcile to the profit variance.
3. **Findings and causes:** The figures show what changed, not why. Possible causes require supporting detail, such as pricing, volume, timing, or expense-category data.
4. **Real-world application:** Clarifying scope and reconciling KPIs helps ensure an answer fits the decision and is supported by evidence. For example, before reporting quarterly profit variance, confirm the period, currency, segments, and definitions, reconcile totals, and identify price or volume as follow-up questions rather than proven causes.

## Week 5 Self-Check Answers

1. **Schema and types:** Inspecting fields and types helps ensure filters, comparisons, dates, and calculations behave as intended rather than treating numbers or dates as text.
2. **Query clauses:** `SELECT` chooses columns, `WHERE` filters rows, and `ORDER BY` sorts the returned rows.
3. **Adapting a query:** Translate the question into the needed columns, row conditions, and sort order; change only the relevant clauses and check that the result still has the expected meaning.
4. **Real-world application:** Inspecting fields and types helps prevent queries from filtering or sorting dates and amounts incorrectly. For example, to answer a January expense request, verify the date and amount columns, select needed fields, filter the month and segment, and sort the result by date.

## Week 6 Self-Check Answers

1. **Grouping:** Group by the dimensions needed for the question and aggregate revenue separately from expense; combining them prematurely obscures their meanings.
2. **NULL and zero:** `NULL` means a value is unknown or absent; zero is a known numeric value. Treating them as equivalent can distort totals and conclusions.
3. **Finance calculations:** Use the KPI contract: profit is revenue minus expense, with expenses stored as positive costs. Apply the specified favorable-variance direction after aggregation.
4. **Real-world application:** These concepts produce meaningful summaries without confusing unknown values with known zeroes. For example, group revenue and expenses by month, calculate profit under the KPI contract, and flag a missing expense rather than treating it as zero and overstating profit.

## Week 7 Self-Check Answers

1. **Join keys:** Use fields that identify matching entities and check uniqueness on the lookup side. The relationship's cardinality determines whether a join is safe.
2. **Join types:** An inner join keeps only matching rows; a left join keeps every row from the left table and shows missing right-side matches.
3. **Join errors:** Duplicate lookup keys can multiply fact rows, while unmatched keys can omit descriptive information or rows in an inner join. Compare key uniqueness, row counts, and totals before and after joining.
4. **Real-world application:** Checking key uniqueness and choosing the right join protects row counts and totals. For example, before adding segment names to finance facts, confirm the lookup has one row per segment, use a left join to preserve every fact, and review unmatched keys and reconciled totals.

## Week 8 Self-Check Answers

1. **Quality checks:** Check row counts, required values, valid ranges or formats, duplicate IDs, and duplicate business keys before relying on an analysis.
2. **Subqueries:** A subquery creates an intermediate result that the outer query can filter or summarize, making it useful for isolating groups that meet an exception condition.
3. **Visible exceptions:** Dropping a bad row or replacing a missing amount with zero changes the evidence. Report the problem and make any remediation explicit and traceable.
4. **Real-world application:** Quality checks and subqueries make exceptions easier to find and investigate before reporting. For example, query month-segment-category groups with duplicate counts, separately identify missing amounts, and send an exception list instead of silently dropping or replacing records.

## Week 9 Self-Check Answers

1. **CTEs:** A common table expression names an intermediate result, making a multi-step query easier to read, test, and reuse.
2. **Window functions:** `GROUP BY` reduces rows to groups; a window function calculates across related rows while keeping row-level detail. Running and prior-period values are useful for ordered comparisons.
3. **Ordering and partitions:** A partition defines which rows are compared together, and ordering defines their sequence. The first period has no prior-period value, so that comparison is undefined.
4. **Real-world application:** CTEs make analysis steps readable, while windows compare rows without losing their detail. For example, calculate monthly profit in a CTE and use LAG by segment ordered by month to show prior-month profit; mark the first month as having no prior value.

## Week 10 Self-Check Answers

1. **Reproducibility:** A handoff needs the setup and import steps, scripts, inputs, versions, and expected checks so another person can rerun it from a clean database.
2. **Dates and percentages:** Parse dates consistently and handle a zero denominator as undefined rather than reporting a misleading numeric percentage.
3. **SQL handoff:** State the question and definitions, provide the query and run instructions, and show checks that connect the result to trusted controls.
4. **Real-world application:** Consistent dates, explicit undefined percentages, and documented setup help others trust and rerun an analysis. For example, provide a colleague with the import steps, SQL, date/KPI definitions, and control totals for a quarterly report, including how zero-budget percentages are handled.

## Week 11 Self-Check Answers

1. **Power Query:** It is useful when the same import and transformation steps recur for new files, because the query can be refreshed instead of repeated manually.
2. **Column types:** Correct types are needed for date filtering, numeric calculations, and reliable joins; incorrect types can silently change results.
3. **Safe refresh:** Keep the source file unchanged, refresh the separate query, then check row counts, types, and errors to confirm the refresh behaved as expected.
4. **Real-world application:** Repeatable transformations and correct types reduce manual rework while preserving traceability. For example, refresh a monthly CSV query, inspect date and amount conversion errors, compare row counts and totals, and leave the received source file untouched.

## Week 12 Self-Check Answers

1. **Fact grain:** Grain states what one fact row represents. Define it before modeling so keys and totals have a clear meaning.
2. **Relationships:** Dimension tables usually filter related fact rows through defined one-to-many relationships. Incorrect or ambiguous directions can produce confusing or repeated totals.
3. **Testing filters:** Compare row counts and known control totals before and after applying date or segment filters; investigate any unexpected duplication or change.
4. **Real-world application:** A clear grain and correctly keyed relationships prevent filters from multiplying or omitting amounts. For example, if a segment slicer doubles a Power BI total, check fact grain, dimension-key uniqueness, and relationship cardinality before changing the visual.

## Week 13 Self-Check Answers

1. **Measures:** A measure is calculated in response to the report's current filters, so it is useful for reusable totals such as actual, budget, profit, and variance.
2. **Filter context:** Date and segment selections change which rows contribute to a measure. Test the same measure under known slices to confirm it responds correctly.
3. **Zero denominator:** Guard percentage calculations and return blank or another clearly labeled undefined result when the denominator is zero; do not imply the percentage is zero.
4. **Real-world application:** Reusable measures keep calculations consistent as report filters change. For example, create revenue, expense, profit, and variance measures that recalculate by month and segment, and return blank or undefined for a percentage with a zero budget denominator.

## Week 14 Self-Check Answers

1. **Visual choice:** Lines are useful for trends over time; bars are useful for comparing categories or segments. Choose the visual that makes the question easiest to answer.
2. **Labels and slicers:** Titles, units, and visible filter selections tell readers what the displayed values represent and which records are included.
3. **Accessibility and blanks:** Check readable labels, contrast, keyboard or screen-reader support where available, and distinguish missing values from actual zeros.
4. **Real-world application:** Appropriate visuals and clear labels help stakeholders interpret results accurately and accessibly. For example, use a line chart for monthly profit and bars for segment comparisons, show currency and selected period, and check contrast and blank-value behavior before sharing.

## Week 15 Self-Check Answers

1. **Refresh and exceptions:** A refresh test checks that new input follows the intended steps; exception tests show whether invalid or missing data is surfaced safely.
2. **Cross-tool reconciliation:** Compare the same periods, segments, and KPI definitions across tools. Differences can reveal inconsistent filters, transformations, or formulas.
3. **Supported claims:** Report observed values and patterns. A small or summarized dataset does not establish a cause without additional evidence.
4. **Real-world application:** These practices help catch data or transformation errors and prevent unsupported explanations. For example, after a refresh, compare Power BI and SQL at the same grain and KPI definitions, investigate mismatches, and report only what the data supports.

## Week 16 Self-Check Answers

1. **Documentation:** Record the data grain, source, measure definitions, assumptions, and refresh steps so a teammate can understand and maintain the report.
2. **Reproducible handoff:** A clean refresh and walkthrough should let another person reproduce the report without relying on hidden files or undocumented actions.
3. **Verification:** Reconcile a filtered result to its source controls and explain what the report shows, how filters affect it, and what remains uncertain.
4. **Real-world application:** Clear documentation and clean reruns make reports maintainable when ownership changes. For example, document a report's sources, grain, relationships, measures, and refresh steps so a teammate can load next quarter's file and verify filtered totals against controls.

## Week 17 Self-Check Answers

1. **Mean and median:** The mean uses every value and is sensitive to extreme values; the median is the middle value and is often more representative for skewed data.
2. **Spread and outliers:** Spread describes how varied the observations are; an outlier is unusually far from the rest and may reflect a real event or a data issue.
3. **Sample unit:** State what each observation represents. A small, designed practice dataset is not a representative sample of a larger population.
4. **Real-world application:** These concepts describe typical values and variation without overstating what a sample represents. For example, when monthly variances contain extreme values, compare mean and median, inspect the outlier, and state that a six-observation fixture does not represent all businesses.

## Week 18 Self-Check Answers

1. **Association:** A plot or correlation can describe the direction or strength of a pattern, but cannot by itself show that one variable caused another.
2. **Confounding:** A confounder is another factor related to both measures that can create or distort their observed association.
3. **Further evidence:** Investigate plausible confounders and collect relevant detail over time; a well-designed experiment or other suitable study may be needed for causal claims.
4. **Real-world application:** They help analysts describe patterns without mistaking them for explanations. For example, if training hours and sales move together, report the association and request store-size or seasonality data before claiming that training caused higher sales.

## Week 19 Self-Check Answers

1. **Population and selection:** Define who the conclusion is about and how observations were selected. A biased or narrow sample may not represent that population.
2. **Confidence intervals:** An interval is produced by a method with assumptions about sampling and the data. Its reliability depends on whether those assumptions and the sampling design are reasonable.
3. **Generalization:** A convenience sample or a tiny, non-random fixture cannot support a reliable claim about a broader population; use a suitable sampling plan and adequate data.
4. **Real-world application:** These concepts clarify whether an estimate can represent the group a decision concerns. For example, before generalizing a voluntary satisfaction survey to all clients, examine who responded and whether selection bias makes its confidence interval unrepresentative.

## Week 20 Self-Check Answers

1. **Regression:** A regression describes how an outcome is associated with one or more predictors under a model. Check whether the model's assumptions fit the data before interpreting it.
2. **Interpretation:** Association describes a relationship; prediction estimates an outcome for new inputs; causation claims that changing one factor changes another and needs stronger evidence.
3. **Decision evidence:** Check model assumptions, data relevance, and possible confounders; validate on suitable data before relying on the result for a business decision.
4. **Real-world application:** Regression can describe or predict patterns, but its assumptions and purpose must be checked before guiding decisions. For example, a sales-versus-marketing model may identify an association to investigate, but alone cannot prove that increasing marketing spend will cause sales to rise.

## Week 21 Self-Check Answers

1. **Python structures:** Lists hold ordered items, dictionaries map keys to values, conditions choose actions, and functions package reusable steps.
2. **Finance functions:** Keep expenses as positive costs, calculate profit as revenue minus expense, and apply the documented favorable-variance signs consistently.
3. **Undefined percentages:** If the denominator is zero, the percentage is undefined. Return `None` or another explicit missing result rather than zero.
4. **Real-world application:** Small functions and explicit conditions make repeated calculations consistent and easier to test. For example, reuse a function for favorable expense variance and have it return an undefined percentage when the budget is zero rather than reporting zero percent.

## Week 22 Self-Check Answers

1. **Input validation:** Validate headers and parse dates and amounts before calculation so malformed text is not mistaken for valid data.
2. **Useful errors:** Identify the row and field, describe the invalid value or expected form, and tell the user what needs attention.
3. **Recovery:** Preserve the original value, report the error, and correct or reject the row through a documented decision; never silently convert a malformed amount to zero.
4. **Real-world application:** Validation catches malformed inputs before they create misleading analysis and tells someone how to fix them. For example, report the row and amount column containing `N/A`, preserve the original CSV, and rerun the script on a corrected copy.

## Week 23 Self-Check Answers

1. **Pandas inspection:** Check columns, shape, and data types after loading; explicitly parse dates when later operations depend on date behavior.
2. **Missing and duplicate values:** Missing values can make calculations incomplete, and duplicate keys can multiply rows during joins or double-count results.
3. **Baseline protection:** Stop or flag analysis when required checks fail. Test the unclean fixture separately and leave the clean baseline unchanged.
4. **Real-world application:** Inspecting a DataFrame before analysis reveals problems that could invalidate calculations or joins. For example, check a monthly file's shape, types, missing amounts, and key uniqueness, then investigate failed checks on a separate copy before producing results.

## Week 24 Self-Check Answers

1. **Validated merge:** A many-to-one validation confirms that each fact row matches at most one lookup row; an indicator can reveal unmatched rows.
2. **Grouping:** Group or pivot by the required dimensions, aggregate revenue and expense separately, and then derive profit and variance using the agreed definitions.
3. **Reconciliation:** Compare the same slices and definitions in Excel, SQL, and Python; matching controls help confirm the transformation and calculation are consistent.
4. **Real-world application:** Validated joins and consistent aggregation protect finance totals across tools. For example, merge segment descriptions as many-to-one, group revenue and expense separately by month and segment, then reconcile profit with Excel and SQL controls.

## Week 25 Self-Check Answers

1. **Performance chart:** A time-series chart can compare actual and budget profit by month. Include dates, currency units, and clear labels so values are interpretable.
2. **Contributions:** A segment's contribution is its actual profit minus budget profit; segment contributions should reconcile to the total profit variance.
3. **Report limits:** State what the chart and calculations show, identify missing context, and avoid presenting a possible cause as a proven explanation.
4. **Real-world application:** A useful chart and contribution analysis show where a change occurred while clear caveats prevent unsupported conclusions. For example, plot monthly profit variance, compare segment contributions, and tell the manager that the summarized values do not establish why the variance occurred.

## Week 26 Self-Check Answers

1. **Fresh kernel:** Restarting and running every cell in order reveals reliance on hidden variables or outputs left over from an earlier interactive session.
2. **Setup information:** Record interpreter and package versions, installation and launch commands, working directory, inputs, and output locations.
3. **Clean-run evidence:** Confirm the run completes without errors and creates the documented outputs; record the checks actually performed.
4. **Real-world application:** Clean runs expose hidden dependencies and make analysis reproducible for teammates. For example, restart a notebook kernel, run every cell in order, record package versions and input paths, and confirm the expected report files were created.

## Week 27 Self-Check Answers

1. **End-to-end audit:** Check the data import, scripts, model, and report together because an error in an early step can affect every downstream result.
2. **Model behavior:** Relationship cardinality and filter propagation determine which fact rows contribute; incorrect settings can omit or multiply amounts.
3. **Defect handling:** Prioritize by effect on correctness or delivery, fix the cause, rerun affected checks, and document remaining risks.
4. **Real-world application:** Auditing these parts together helps locate the cause of wrong totals and focus fixes on the highest-impact risk. For example, investigate a dashboard total increase by checking source row counts, key uniqueness, relationship cardinality, and control totals, then retest the correction.

## Week 28 Self-Check Answers

1. **Useful README:** Explain the audience, question, source, grain, definitions, tools, run steps, findings, and limitations.
2. **Project packaging:** Organized files, readable visuals, and reconciliation evidence help another person understand and maintain the work.
3. **Safe sharing:** Test the documented clean run and confirm the project contains only synthetic or otherwise authorized data before publishing.
4. **Real-world application:** A well-packaged project lets another person understand, reproduce, and safely review the analysis. For example, provide a README with the source, grain, definitions, setup, and checks, then verify the project runs and contains no private or unauthorized data before sharing.

## Week 29 Self-Check Answers

1. **Cross-tool checks:** Comparing the same slice in Excel, Python, and SQL can reveal inconsistent calculations, filters, or transformations.
2. **KPI consistency:** Use the same definitions, sign conventions, and denominator rules in every tool or results will not be comparable.
3. **Hand calculation:** Trace one result to its source rows and calculate it independently; this can catch an error shared by multiple automated outputs.
4. **Real-world application:** Independent checks help distinguish a true finding from a shared coding or definition error. For example, when SQL disagrees with Excel and Python on profit variance, compare filters and sign conventions and trace one segment-month result to its source rows by hand.

## Week 30 Self-Check Answers

1. **Variance contributions:** Calculate each month-segment contribution using actual versus budget profit and confirm the contributions add to the total variance.
2. **Edge cases:** Use a separate test copy for missing or duplicate rows and a separate zero-denominator case so tests do not alter the clean baseline.
3. **Evidence-led memo:** Separate measured findings from possible explanations, state limitations, and request the additional information needed to investigate further.
4. **Real-world application:** These practices validate both ordinary results and exceptions while keeping findings separate from possible causes. For example, test a duplicate key in a separate copy, label a zero-budget percentage undefined, and reconcile valid segment contributions before writing the memo.

## Week 31 Self-Check Answers

1. **Environment record:** Document versions, dependencies, working directory, input paths, output paths, and commands needed to run the project.
2. **Clean setup:** A fresh environment exposes missing dependencies, hard-coded paths, or hidden notebook state that may not appear on the original machine.
3. **Sharing checks:** Verify links and source descriptions, and remove confidential or unauthorized data before sharing outputs.
4. **Real-world application:** A reproducible, safe handoff reduces setup delays and prevents accidental disclosure. For example, have a reviewer on another computer follow the documented versions, paths, and run steps, then verify outputs and confirm the files contain no private data.

## Week 32 Self-Check Answers

1. **Project explanation:** Clearly state the question, approach, checks, finding, limitation, and next step for each project.
2. **Feedback:** Label external reviewer feedback separately from self-review, then record which useful suggestions were addressed.
3. **Readiness:** Publish when the work is reproducible, accurate, clearly explained, and uses data that is safe to share; otherwise address the open issues first.
4. **Real-world application:** Clear communication and review make analysis more useful and reveal gaps before publication. For example, revise a confusing chart after reviewer feedback, rerun the project's checks, and publish only when another person can understand and reproduce it.

## Week 33 Self-Check Answers

1. **SQL choices:** Use joins to combine related tables, grouping to summarize, and window functions to compare ordered rows while retaining detail.
2. **Finance interpretation:** Lower actual expense than budget is favorable when expenses are positive costs. A percentage with a zero budget denominator is undefined.
3. **Practice gaps:** Record errors and time separately; use repeated mistakes to choose a targeted practice task rather than treating speed alone as success.
4. **Real-world application:** Combining the right SQL operations answers multi-level questions while a quick check protects accuracy. For example, group results by quarter and segment, use a window for month-over-month change, apply the expense variance sign correctly, and verify one total against a control.

## Week 34 Self-Check Answers

1. **Filter context:** Relationships carry date and segment selections to fact rows; measures recalculate over the rows that remain in context.
2. **Pandas operations:** `groupby` summarizes groups and `merge` matches keys. Check key uniqueness and missing matches to prevent inflated or incomplete results.
3. **Troubleshooting:** Check refresh errors at the source and transformation steps; inspect missing values and duplicate keys before changing the model or calculation.
4. **Real-world application:** Checking models and joins explains why equivalent reports can differ under filters. For example, compare a DAX measure under a segment slicer with a pandas merge validated as many-to-one, ensuring both use the same period, grain, and KPI definitions.

## Week 35 Self-Check Answers

1. **KPI definitions:** State what revenue and expense mean, how profit is calculated, and which variance sign indicates a favorable result.
2. **Context and cause:** The figures describe the measured variance but may not explain why it happened; pricing, volume, timing, or expense detail may be missing.
3. **Stakeholder follow-up:** Ask a focused question that obtains the missing detail needed for the next analysis, and label unverified explanations as hypotheses.
4. **Real-world application:** Consistent definitions make the result interpretable, while focused questions avoid presenting a guess as a cause. For example, explain an unfavorable expense variance using actual and budget amounts, then request price, volume, or timing detail before attributing it to a cause.

## Week 36 Self-Check Answers

1. **Reproducibility:** Follow the setup from a clean copy, rerun the analysis, and verify the rubric's controls and outputs.
2. **Role alignment:** Compare demonstrated skills with current job requirements and describe project work honestly as independent practice.
3. **Next steps:** Choose applications and learning goals that address the most relevant gaps, and set milestones that can be reviewed during the next 90 days.
4. **Real-world application:** Comparing role needs with verifiable evidence helps prioritize learning and support accurate applications. For example, if target postings require SQL joins not shown in your portfolio, build and document a tested join exercise while applying to roles that fit your current skills.
