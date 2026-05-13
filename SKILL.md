---
name: workbook-decision-review
description: General workbook review and improvement methodology for AI agents working with spreadsheets, workbook comments, reviewer revisions, and decision-support tables. Use when the user asks the agent to inspect workbook files, identify problems, ask only necessary questions, preserve source evidence, produce issues and recommendations, improve a workbook, or evolve the method from durable post-review feedback.
---

# Workbook Decision Review

## Purpose

Turn workbook material into decision-ready output without losing source evidence. Optimize for clear answers to: what changed, what matters, what is uncertain, what should be done next, and what evidence supports that judgment.

## Operating Rules

- Inspect actual workbook files before proposing structure or edits.
- Do not infer source, reference, or target roles from filenames alone.
- Ask only blocker questions. If a missing answer is not a blocker, state the assumption and proceed.
- Ask at most 3 concise questions in one turn.
- Preserve raw evidence. Do not rewrite original values, comments, counts, labels, dates, versions, or source rows to make the output look cleaner.
- If a factual claim is needed but not supported by files or user context, mark it `待确认` or ask.
- Treat a provided reference workbook as the layout authority unless the user asks to redesign.
- If the user asks to optimize, organize, generate, export, or create an output, treat that as approval to create a new artifact. Confirm before overwriting originals, destructive edits, paid or long-running jobs, or ambiguous analysis-only requests.
- Do not turn one-off reviewer wording into a permanent rule during evolution.

## Workflow

1. Inspect sheets, headers, sample rows, comments, formulas, hidden/merged areas, and any reference files.
2. Identify the work mode:
   - Review only: output issues and recommendations.
   - Improve artifact: edit or create a cleaner workbook.
   - Evolve method: compare feedback and update reusable rules.
3. Load only the needed reference:
   - `references/core-questioning.md` for blocker questions and permission boundaries.
   - `references/core-evidence.md` for source preservation, counts, percentages, dedupe, time/version ranges, and traceability.
   - `references/core-output.md` for issue/recommendation output, workbook shapes, field choices, and final formatting.
   - `references/core-evolution.md` for feedback-driven method updates and anti-overfitting rules.
   - `references/domain-product-planning.md` only when the workbook is specifically about product feedback, product planning, competitor research, symptoms/signals, or requirement prioritization.
4. State assumptions briefly, ask blockers only if needed, then produce the requested review, recommendation, or workbook artifact.
5. Verify at the artifact boundary: evidence traceability, calculations when applicable, structure, field order, formatting consistency, and fit for the intended recipient.

## Universal Row Logic

For each row that becomes a decision item, answer:

1. What is the issue or signal?
2. What evidence supports it?
3. What decision or action does it affect?
4. What is the current status?
5. What is uncertain?
6. What is the recommended next step?

If any answer cannot be supported, mark uncertainty instead of fabricating certainty.

## Review Output Mode

When the user asks "怎么看", "有什么问题", "给建议", or "review", do not edit first. Output:

```text
问题：
- ...

风险：
- ...

建议：
- ...

是否建议修改：
- 是/否，原因
```

## Writing Standard

Use compact business writing. Prefer `现状 / 判断 / 建议` or `问题 / 证据 / 下一步` over paragraph explanation.

Do not write empty action phrases such as `持续优化`, `提升体验`, or `进一步完善`. If ongoing work is real, name the current-stage action and tracked metric.

Generic pattern:

```text
现状：某指标在处理前为 A%，处理后为 B%，变化 C%
判断：问题仍高于处理阈值 / 已低于观察阈值
建议：下一阶段拆分主要子问题，优先验证高频路径
```

## Failure Conditions

Stop or mark uncertainty instead of finalizing when:

- Target output type is unclear and would change structure.
- Source and reference files cannot be distinguished.
- A denominator, dedupe rule, or time/version range is required but unknown.
- A factual capability/status claim is needed but unsupported.
- The requested edit would overwrite or mutate source evidence without explicit approval.

## Evolution

When the user provides post-delivery corrections, compare the delivered artifact against corrections first. Update this method only for durable behavior changes. Never promote a concrete workbook example directly into a long-term rule; first abstract it into principle, condition, and boundary.
