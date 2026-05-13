# Output Shapes

Use this reference when deciding workbook structure, fields, and sorting.

## Shape Selection

Choose one primary shape before editing. Do not force every workbook into the same style.

### Boss Report

Goal: quick decision and quarterly/leadership visibility.

Recommended fields:

- 模块/问题
- 条数
- 反馈占比
- 当前判断
- 状态
- 下一步/版本节点

Rules:

- Keep only high-signal issues in the main table.
- Sort by business importance: unresolved high-volume issues, leader focus, major competitor gaps, then observations.
- Use short cells; avoid long evidence dumps.

### Execution Schedule

Goal: decide what enters a version.

Recommended fields:

- 分类
- 需求内容
- 优先级
- 来源
- 节点
- 备注

Rules:

- `来源` must explain why the item matters, such as `功能Top1`, `体验Top4`, `竞品对比（Battery）`.
- `节点` is expected delivery or validation timing, not the discovery date.
- If priority and node conflict, explain the dependency or capacity reason in `备注`.

### Diagnosis Sheet

Goal: help product/development/test isolate a problem.

Recommended fields:

- 问题
- 影响范围/版本
- 证据
- 可能原因
- 排查动作
- 当前状态
- 负责人/协作方 if known

Rules:

- Keep uncertain causes as hypotheses.
- Separate `排查中` from `计划优化`.
- Do not send issues to development/testing without evidence or a reproducible direction.

### Requirement Pool

Goal: hold candidate requirements before scheduling.

Recommended fields:

- 需求
- 用户场景
- 来源证据
- 竞品/内部能力
- 价值判断
- 技术状态
- 暂定优先级
- 处理状态

Rules:

- Allow `待确认` and `观察`.
- Do not force every candidate into a release node.

### Competitor Comparison

Goal: prove gap or opportunity.

Recommended fields:

- 竞品标识
- 关键数据
- 用户喜欢
- 用户抱怨
- 用户建议
- 我方差距/机会
- 可转需求

Rules:

- Use stable competitor identifiers: brand, developer, icon-derived name.
- Name the exact competitor when the plan depends on it.
- Do not add country parameters to links unless needed for the recipient.

## Sheet Role Rules

- `体征list`: symptom evidence, judgment, status, and next direction.
- `需求list`: only schedulable or near-schedulable items.
- `竞品对比`: opportunity proof, not generic market notes.
- `评论导出`: reviewer evidence; do not treat it as final structure.

## Formatting Defaults

- Sort quantity lists descending when they imply priority.
- Keep count formats consistent within a module.
- Make quarter colors visibly distinct.
- Use no final Chinese full stop in compact planning cells unless the reference workbook does.
