# Core Output

Use this reference when choosing output structure, field names, sorting, or final presentation.

## Output Modes

### Issues And Recommendations

Use when the user asks for review, critique, "怎么看", "有什么问题", or "给建议".

Format:

```text
总体判断：
- one short paragraph or 2-3 bullets explaining the main pattern

细项问题：
- [P1/P2/P3] Location: sheet/row/column/cell or affected range; issue; evidence; recommendation

风险：
- consequence if unchanged

总体建议：
- concrete change

是否建议修改：
- yes/no and reason
```

Lead with the highest-impact pattern, then give detailed findings. Do not bury the answer in background. The overall judgment explains the pattern; detailed findings identify the fix points.

Detailed findings must be actionable and locatable:

- Include sheet + row, column, cell, or affected range when workbook files are available.
- If the issue is structural and spans many rows, name the sheet, field, and repeated pattern.
- If only a screenshot or text excerpt is available, use the visible field name, item name, or quoted cell text as the location clue.
- If location cannot be known from the available material, say `位置待确认` and explain what is missing.
- Avoid only giving global critique; every major critique should point to where the user can fix it.

### Executive Summary

Goal: help a recipient decide quickly.

Recommended fields:

- Topic / issue
- Evidence
- Judgment
- Status
- Recommendation
- Next checkpoint

Rules:

- Keep only high-signal items in the main view.
- Use concise cells.
- Put details and raw evidence in supporting sheets or notes.

### Action Plan

Goal: decide what to do next.

Recommended fields:

- Item
- Category
- Evidence/source
- Priority
- Owner/function if known
- Timing/checkpoint
- Status
- Notes

Rules:

- Priority and timing must be explainable.
- If priority and timing conflict, state the reason.
- Do not force every candidate into a near-term plan.

### Diagnosis Sheet

Goal: isolate a problem or data issue.

Recommended fields:

- Issue
- Scope
- Evidence
- Hypothesis
- Validation step
- Current status
- Open question

Rules:

- Keep uncertain causes as hypotheses.
- Separate "needs investigation" from "confirmed action".
- Do not claim root cause without evidence.

### Evidence Appendix

Goal: preserve auditability.

Recommended fields:

- Source sheet
- Source row/id
- Original text/value
- Derived label
- Evidence note
- Included/excluded flag

Rules:

- Keep original values intact.
- Use this sheet to support rewritten summary language.

## Field Naming

Prefer generic field names unless the user's reference workbook requires specific labels.

Examples:

- Signal / Issue
- Evidence
- Judgment
- Recommendation
- Status
- Priority
- Timing
- Source
- Notes

## Sorting

Default sort order:

1. Active high-impact unresolved issues
2. Confirmed action items
3. Items needing clarification
4. Observations
5. Low-signal or stale items

## Formatting Defaults

- Keep one idea per cell when possible.
- Main-table cells must optimize for scanability: use one sentence when possible, 1-2 lines by default, and no background explanation unless it changes the decision.
- If `issue + evidence + next step` can be expressed directly, do not split it into multiple explanatory sentences.
- Use compact multi-line cells only when a row needs evidence + judgment + next step.
- Keep count and percentage formats consistent.
- Use visual emphasis to support scanning, not decoration.
- Follow the reference workbook's formatting when one is provided.
