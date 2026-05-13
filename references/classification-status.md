# Classification And Status

Use this reference when classifying issues, assigning status, or reconciling priority and release node.

## Three Main Classes

- `体验`: existing capability, but effect, interaction, path, discoverability, or expectation match is weak.
- `功能`: unsupported module-level capability or new workflow.
- `性能`: speed, crash,打不开, 卡顿, instability, conversion failure from runtime/engineering cause.

## Complex Boundary Rules

- 广告: usually commercial/monetization experience. If it blocks task completion, mark `体验`; if asking for new ad control, mark candidate `功能`.
- 订阅/付费/退款: usually monetization experience or policy; do not turn into product feature unless there is a concrete paywall/entitlement change.
- 权限: if OS/platform permission blocks usage, classify by affected flow and mark platform constraint when product control is limited.
- 评分弹窗: existing rating library or trigger timing issue usually `体验`, not `功能`.
- 打印: if current app already prints but users cannot find/use it, `体验`; if no print workflow exists, `功能`.
- 文件找不到/无法保存: classify by actual cause. Save failure may be `性能`; confusing path may be `体验`; missing file-management capability may be `功能`.
- 不会用/找不到入口: usually `体验` unless the requested path does not exist.
- OCR vs AI: treat as separate capabilities unless the product design explicitly binds them.

If the app capability is unknown, use `待确认` instead of guessing.

## Status Labels

Use a small status vocabulary:

- `待确认`: missing product fact, source fact, or data口径.
- `观察`: weak signal, stale issue, low volume, or post-release sample is not enough.
- `排查中`: problem exists but cause/path still needs logs, reproduction, or comparison.
- `计划优化`: cause and direction are known; not necessarily scheduled.
- `已确认需求`: unsupported capability or clear requirement ready for requirement list.
- `优化中`: already in active work or committed near-term plan.
- `已解决`: recent evidence confirms meaningful decline or fix.
- `无优化空间`: external/platform/security/file-system constraint, or product control is low.

## Priority Conflict Order

When signals conflict, use this default order unless the user says otherwise:

1. Explicit leader/business commitment
2. Current high-volume unresolved issue
3. Revenue or conversion impact
4. Major competitor gap with clear user expectation
5. Internal capability already available and low implementation cost
6. Long-term technical foundation work
7. Low-volume or stale observation

## Release Node

- Do not map P0/P1/P2 mechanically to Q2/Q3.
- A near-term node requires evidence, clear action, and feasible capacity.
- One version generally supports one main feature plus limited optimizations unless the user gives a different capacity rule.
- If a high-priority item is delayed, state the dependency or capacity reason.
- If an item is Q3, place it with Q3 items or explain why it appears near Q2 work.

## Long-Term Optimization Wording

Do not write only `持续优化`.

Use:

```text
长期底层优化，当前版本先跟踪 1.3.1 后排版抱怨率是否继续下降
```

or:

```text
Q2 拆分排版异常链路，优先验证字体变化、页面增加、文字缺失
```
