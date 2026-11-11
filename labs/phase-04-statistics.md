# Phase 4 Lab — Statistics and Investigation

[Schedule](../weekly-schedules/phase-04-statistics.md) · [Data contract](../data/README.md) · [Worked solutions](../solutions/phase-04-statistics.md)

Use a separate workbook or calculator file, and keep the provided CSVs read-only; save calculations and charts separately from the source data. Each observation for the main analysis is one **segment-month**, not an individual transaction. The fixture is deliberately synthetic, not a random sample of businesses or periods.

## Week 17 — Descriptive statistics

1. Calculate actual profit, budget profit and favorable profit variance for each month-segment pair.
2. Calculate mean, median, minimum, maximum and range of the resulting variances. Reconcile their sum to the data contract.
3. Create a labeled dot or bar chart. Explain what mean and median summarize and why an apparent outlier in six designed values is not proof of an anomaly in a population.
4. Trace one result back to its two source rows and record the calculation.

## Week 18 — Relationships and alternative explanations

1. Plot budget against actual separately for Revenue and Expense. State the number of observations and common units, and explain why mixing categories changes the question.
2. Describe the observed pattern visually. If computing correlation, state the sample size, formula and its sensitivity; a shared trend, small sample and other confounders can mislead.
3. Write at least two possible explanations for a variance and a data request that could distinguish them. Label both explanations hypotheses, not causes established by the fixture.

## Week 19 — Sampling and confidence

1. Use a textbook confidence-interval example with a specified sample, population target and assumptions; reproduce its calculation and explain the interpretation and conditions in your own words.
2. Identify why the designed, tiny, non-random fixture does not justify a confidence interval for real companies or future months. More precision in a calculation cannot repair a poor sampling design.
3. Propose a target population, sampling method, sample unit, date range, missing-data policy and minimum information needed before attempting inference. Do not assign an unsupported sample size or claim this is a validated design.

## Week 20 — Regression and decision memo

1. Work a textbook regression example and identify outcome, predictors, slope, residuals and assumptions. Distinguish an association from a causal or out-of-sample predictive claim.
2. Do not fit and promote a model from the six synthetic observations as a meaningful forecast. Explain limitations of extrapolation and small samples.
3. Write one page: business question, observed calculation, comparison, plausible explanations, uncertainties, decision/request and additional data. Link values to your workbook and label the dataset fictional.
4. Present the result; log actual feedback or a self-review and complete the [phase gate](../05-study-tracker.md).
