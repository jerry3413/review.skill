# Core Evidence

Use this reference when source preservation, counts, percentages, dedupe, time ranges, or auditability matter.

## Source Preservation

- Preserve original comments, values, counts, dates, versions, labels, and source rows.
- If rewriting wording for a decision table, keep a traceable source column, source sheet, source row, source id, or evidence note.
- Do not merge, delete, rename, or overwrite source evidence in the original workbook unless explicitly asked.
- Prefer writing derived summaries to a new workbook or new sheet.

## Evidence口径

Before presenting a number as evidence, identify:

- Source row count
- Deduped unit count, if dedupe is used
- Denominator for each percentage
- Included/excluded sheets or filters
- Time or version range, when relevant
- Treatment of empty, invalid, duplicated, or merged rows

If the口径 is unknown and affects a decision, mark `口径待确认` or ask.

## Dedupe

- Deduplicate only when duplicate rows would inflate the decision.
- Preserve raw count separately when dedupe changes the result.
- State whether ranking uses raw rows, unique records, unique users, unique comments, or another unit.

## Before/After Or Time Comparison

When comparing periods or versions, use the same unit and denominator where possible.

Report:

- Before value or rate
- After value or rate
- Absolute change
- Relative change
- Sample size caveat if the periods are imbalanced

If sample sizes differ heavily, prefer rate comparison and add a caution.

## Stale Evidence

Treat evidence as stale when it is concentrated in old periods and absent or sharply reduced recently.

Default handling:

- Main decision output: mark `观察` or remove from active plan
- Notes: preserve historical context when useful
- Source data: never delete only because it is stale

## Low-Signal Detail

Do not silently drop low-signal detail. Demote it to notes or observation unless strict pruning is requested.

Low-signal candidates:

- Tiny wording tweaks
- Very low count with no business, user, risk, or operational signal
- No clear action or unsupported inference
- Already addressed and not recurring
