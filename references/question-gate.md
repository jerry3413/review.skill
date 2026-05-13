# Question Gate

Use this reference when deciding whether to ask before editing a workbook.

## Blocker Definition

A missing answer is a blocker only if proceeding would likely cause one of these failures:

- Wrong artifact structure: boss report vs execution schedule vs diagnosis sheet vs requirement pool.
- Wrong file role: source data, reference workbook, comment export, and target output cannot be distinguished.
- Wrong evidence口径: denominator, dedupe rule, version range, or source scope affects required counts/percentages.
- Unsupported product fact: a row depends on whether the app/internal product/competitor supports a capability.
- Destructive operation: overwrite original files, mutate source evidence, delete sheets, or run a costly/long API workflow.

## Non-Blockers

Do not stop for these. State an assumption and proceed:

- Exact wording can be refined after draft output.
- Minor formatting preferences are not provided.
- Output filename is missing; choose a clear local name.
- Priority weights are incomplete but evidence allows a provisional rank.
- Reference style is absent; use the appropriate output shape.

## Asking Rules

- Ask at most 3 questions in one turn.
- Prefer yes/no or short-answer questions.
- Tie each question to the failure it prevents.
- If there are more than 3 uncertainties, ask the 1-3 structural blockers first and proceed later with assumptions.

## Permission Rules

- "帮我优化/整理/生成/输出/落本地/给我完整表格" means approval to create a new artifact.
- Confirm before overwriting the original workbook.
- Confirm before paid, high-volume, or long-running API calls.
- Confirm when the user only asks for analysis/advice and has not asked for an output artifact.
