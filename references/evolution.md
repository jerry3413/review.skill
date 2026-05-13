# Evolution Workflow

Use this reference only when the user asks the skill to evolve from corrections, reviewer comments, revised workbooks, or post-delivery feedback.

## Feedback Types

Classify every correction before updating the skill:

- `本次修正`: specific row wording, one workbook's data issue, or one-off stakeholder preference.
- `项目规则`: applies to this product/workbook family but not necessarily all future work.
- `长期方法`: reusable behavior rule for future workbook review.

Only `长期方法` should change this skill. `项目规则` can be noted in the current task output or memory if the user explicitly asks. `本次修正` should not be written into the skill.

## Update Rules

- Compare delivered artifact and corrected artifact/comment before editing the skill.
- Extract the smallest durable rule that would have prevented the error.
- Prefer updating reference files over `SKILL.md`.
- Edit `SKILL.md` only when trigger behavior, workflow, hard constraints, or reference routing changes.
- Remove or rewrite conflicting old rules instead of appending repetitive patches.
- Tell the user which rule changed and which file changed.

## Do Not Evolve When

- The correction is only a sentence polish for one row.
- The feedback depends on private context not present in future tasks.
- The user is still discussing whether the correction is valid.
- The rule would make future outputs longer or more rigid without reducing real errors.

## Good Evolution Example

Correction: "这里不是功能，是体验，因为我们已经支持打印，只是入口不清楚"

Durable rule: supported-but-not-found capability belongs to `体验`, not `功能`; unknown support must be `待确认`.

Target file: `classification-status.md`
