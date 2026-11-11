# Phase 5 — Python and pandas Solutions

[Solutions index](README.md) · [Phase 5 lab](../labs/phase-05-python.md)

Use these results to check your own calculations after attempting the exercises. Keep the clean fixture separate from intentionally faulty test copies.

## Week 21 — Fundamentals and financial functions

For January Retail, actual profit is CAD 43,000 and favorable profit variance is CAD 3,000. A revenue increase improves favorable variance; an expense increase reduces it. A percentage with a zero denominator should be represented as undefined (for example, `None`), not as zero.

## Week 23 — pandas ingestion and quality

The baseline has 12 rows, six Revenue rows and six Expense rows. It has no missing values, invalid categories, non-month-start dates, duplicate IDs or duplicate business keys.

## Week 25 — Visualize and investigate

| Month | Segment | Favorable profit variance CAD |
|---|---|---:|
| January | Retail | 3,000 |
| January | Business | -1,000 |
| February | Retail | -1,000 |
| February | Business | 2,000 |
| March | Retail | 3,000 |
| March | Business | 4,000 |

The contributions sum to CAD 10,000. State any zero-denominator percentage as undefined, not zero.
