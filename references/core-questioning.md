# Core Questioning

Use this reference when deciding whether to ask the user before reviewing or editing a workbook.

## Blocker Definition

A missing answer is a blocker only if proceeding would likely cause one of these failures:

- Wrong output type: review memo, edited workbook, executive summary, data audit, action plan, or full rebuild would require different structure.
- Wrong file role: source data, reference example, reviewer comments, and target output cannot be distinguished.
- Wrong evidence口径: denominator, dedupe rule, time/version range, or source scope affects required counts or percentages.
- Unsupported fact: the recommendation depends on a business, product, process, or capability fact not present in the files.
- Destructive operation: overwrite originals, mutate source evidence, delete sheets, or run costly/long jobs.

## Non-Blockers

Do not stop for these. State an assumption and proceed:

- Exact wording can be refined after a draft.
- Minor formatting preferences are not provided.
- Output filename is missing.
- Ranking weights are incomplete but evidence allows a provisional rank.
- No reference workbook exists; choose the most suitable generic output shape.

## Asking Rules

- Ask at most 3 questions in one turn.
- Prefer yes/no or short-answer questions.
- State why the answer matters.
- If there are more than 3 uncertainties, ask the structural blockers first and defer the rest.

## Permission Rules

- "优化", "整理", "生成", "输出", "落本地", or "给我完整表格" implies permission to create a new artifact.
- Confirm before overwriting original files.
- Confirm before paid, high-volume, or long-running jobs.
- Confirm when the user only asks for analysis/advice and has not requested an artifact.
