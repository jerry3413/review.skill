# Evidence Rules

Use this reference when counts, percentages, source preservation, version comparison, or stale issues matter.

## Source Preservation

- Preserve original comments, raw counts, versions, timestamps, labels, and source rows.
- If rewriting wording for a decision table, keep a traceable source column, source sheet, source row, or evidence note.
- Do not merge, delete, or rename source evidence in the original workbook unless explicitly asked.
- Prefer writing derived summaries to a new workbook or new sheet.

## Count And Percentage口径

Before calculating or presenting percentages, identify:

- Source row count
- Deduped comment/user count, if dedupe is used
- Denominator used by each percentage
- Version/date range
- Whether empty/invalid/duplicated rows are excluded

If any of these are unknown, mark the percentage `口径待确认` or ask if it is a blocker.

## Dedupe Rules

- Deduplicate only when the task asks for user/comment-level analysis or duplicate comments would inflate product priority.
- Preserve raw count separately when dedupe changes the result.
- State whether ranking uses raw rows or deduped comments.

## Version Before/After

For optimized issues, compare:

- Pre-release count or rate
- Post-release count or rate
- Same denominator type where possible
- Absolute change and relative reduction
- Whether post-release sample size is large enough to trust

If sample sizes differ heavily, prefer rate comparison and add `样本量差异，需继续观察`.

## Historical Or Stale Issues

Treat an issue as stale when it is mostly from old versions and absent or sharply reduced in recent versions.

Default handling:

- Main table: remove or mark `观察`
- Requirement list: do not schedule unless recent evidence returns
- Notes: keep the historical context if it explains a past optimization

Do not delete stale evidence from source data.

## Low-Value Detail

Do not drop low-volume or one-off issues silently. Demote them to notes/observation unless the user asks for strict pruning.

Low-value candidates:

- Tiny wording tweaks
- Very low count with no revenue, boss, competitor, or technical signal
- No clear action or unsupported inference
- Already fixed and not recurring in recent versions
