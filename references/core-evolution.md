# Core Evolution

Use this reference only when the user asks the method to evolve from corrections, revised workbooks, reviewer comments, or post-delivery feedback.

## Feedback Types

Classify every correction before updating the method:

- `本次修正`: specific wording, row-level correction, or one workbook's data issue.
- `项目规则`: applies to this project or workbook family, but may not generalize.
- `长期方法`: reusable behavior rule for future workbook review.

Only `长期方法` should change the general method. `项目规则` belongs in project-specific notes if the user asks. `本次修正` should not become a rule.

## Anti-Overfitting Rule

Never promote a concrete workbook example directly into a long-term rule.

Convert it into:

- Abstract principle
- Applicable condition
- Boundary or counterexample

Example:

```text
Concrete correction: "This row should not be scheduled because it only appears in old data."
Durable rule: "When evidence is stale, preserve it as context but do not place it in active planning unless recent evidence returns."
Condition: use when time/version fields exist.
Boundary: if the issue has explicit business priority, keep it but mark the evidence gap.
```

## Update Rules

- Compare delivered artifact and correction before editing the method.
- Extract the smallest durable rule that would have prevented the error.
- Prefer updating reference files over `SKILL.md`.
- Edit `SKILL.md` only when trigger behavior, workflow, hard constraints, or reference routing changes.
- Remove or rewrite conflicting old rules instead of appending patches.
- Tell the user which rule changed and which file changed.

## Do Not Evolve When

- The correction is only sentence polish.
- The feedback depends on private context not present in future tasks.
- The user is still deciding whether the correction is valid.
- The rule would make future outputs longer or more rigid without preventing real errors.
