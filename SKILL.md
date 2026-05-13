---
name: workbook-decision-review
description: Decision-ready workbook review and editing methodology for Chinese product/work reports, especially symptom lists, requirement lists, competitive analysis sheets, leadership comment exports, revised workbooks, and feedback-driven skill evolution. Use when the user sends .xlsx/.csv workbooks or reviewer comments and asks Codex to inspect first, raise necessary questions, optimize a work table, summarize adjustment patterns, preserve source evidence, produce a local workbook, or evolve this skill from post-review modifications.
---

# Workbook Decision Review

## Purpose

Convert raw workbook analysis into decision-ready product planning material. Optimize for what the recipient can decide: problem, evidence, status, priority, next action, and release implication.

## Operating Rules

- Inspect actual files before proposing structure or editing. Do not infer source/reference/target roles from filenames alone.
- Ask only blocker questions. If a missing answer is not a blocker, state the assumption and proceed.
- Do not ask a long intake questionnaire. Ask at most 3 concise questions in one turn.
- Preserve raw evidence. Do not rewrite original comments, counts, labels, versions, timestamps, or source rows to make the output look cleaner.
- If product capability is unknown, mark it `待确认` or ask for the product fact. Do not assume a feature is supported or unsupported.
- Treat a provided reference workbook as the layout authority unless the user asks to redesign.
- If the user says "优化/整理/生成/输出/落本地", treat that as approval to create a new artifact. Confirm only before overwriting originals, destructive edits, paid/long API runs, or ambiguous analysis-only requests.
- Do not turn one-off reviewer wording into a permanent rule during evolution.

## Workflow

1. Inspect workbook sheets, comments, formulas, sample rows, and any reference files.
2. Identify the artifact type: boss report, execution schedule, diagnosis sheet, requirement pool, competitor comparison, or feedback export.
3. Load only the needed reference file:
   - `references/question-gate.md` for ambiguity, blocker decisions, or permission questions.
   - `references/output-shapes.md` when deciding sheet roles, fields, sorting, or final structure.
   - `references/evidence-rules.md` when counts, percentages, dedupe, version trends, stale issues, or source preservation matter.
   - `references/classification-status.md` when assigning `体验 / 功能 / 性能`, complex categories, status, priority, or release node.
   - `references/evolution.md` when the user provides corrections and asks the skill to evolve.
   - `references/feedback-patterns.md` for detailed reusable feedback patterns.
4. State assumptions briefly, ask blockers only if needed, then edit or produce the requested output.
5. Verify at the artifact boundary: source evidence traceability, formula/error checks when applicable, sheet structure, field order, formatting consistency, and whether the output matches the intended recipient.

## Core Row Logic

For each formal symptom or requirement, make the row answer:

1. What exactly is the problem?
2. What evidence proves it matters?
3. Which business boundary does it belong to?
4. What is the current status?
5. What is the next action?
6. Does priority match release capacity?

If any answer cannot be supported, mark the row `待确认`, `观察`, or move it out of the main table instead of fabricating certainty.

## Writing Standard

Use compact Chinese business writing. Prefer `现状 / 判断 / 方案` or `问题 / 证据 / 下一步` over paragraph explanation.

Do not write empty action phrases such as `持续优化`, `提升体验`, `进一步完善`, or `实测后发现`. If long-term optimization is real, name the current stage action and tracked metric.

Example:

```text
现状：1.3.1 优化后排版问题抱怨率由 4.4% 降至 3.7%，下降 16%
判断：仍为 PDF 转 Word Top 问题
方案：Q2 拆分排版异常链路，优先排查字体变化、页面增加、文字缺失
```

## Failure Conditions

Stop or mark uncertainty instead of finalizing when:

- The target artifact type is unclear and would change sheet structure.
- The denominator, dedupe rule, or version range is unclear but percentages/trends are required.
- Source and reference files cannot be distinguished.
- A product capability claim is needed but unsupported by workbook evidence or user context.
- The requested edit would overwrite or mutate source evidence without explicit approval.

## Evolution

When the user provides post-delivery corrections, compare the delivered artifact against corrections first. Update this skill only for durable behavior changes; put detailed reusable rules in references and keep `SKILL.md` lean.
