# Domain: Product Planning Workbooks

Use this optional reference only when the workbook is about product feedback, user review analysis, product planning, competitor research, symptoms/signals, or requirement prioritization.

## Abstract Sheet Aliases

Map local sheet names to generic roles:

- Signal register: raw or summarized user/product issues. Local names may include symptom, signal, feedback, issue, or similar terms.
- Action backlog: items that may enter planning, scheduling, or ownership.
- Benchmark evidence: competitor, market, or external comparison evidence.
- Review evidence: exported comments, reviewer notes, or source feedback.

Do not require these exact names. Use the role implied by columns and content.

## Product Feedback Classification

Classify by user goal, system boundary, responsibility, and actionability.

Common categories:

- Experience: existing capability but poor effect, path, interaction, discoverability, expectation match, or comprehension.
- Capability gap: unsupported workflow, missing module, or new user job.
- Reliability/performance: speed, crash, failure, instability, latency, data loss, or runtime issue.
- Commercial/policy: pricing, subscription, entitlement, refund, advertising, compliance, or platform policy.
- Education/discoverability: users cannot find, understand, or correctly use an existing capability.
- Constraint/no-action: external rule, platform limit, security rule, legal/policy boundary, or low product control.

If current product capability is unknown, mark `待确认` instead of guessing.

## Product Planning Status

Use a compact status vocabulary:

- `待确认`: missing product fact, source fact, or evidence口径.
- `观察`: weak signal, stale signal, low volume, or sample is not enough.
- `排查中`: problem exists but path/cause needs logs, reproduction, or comparison.
- `计划优化`: direction is known but not necessarily scheduled.
- `已确认需求`: capability gap or clear requirement ready for backlog.
- `优化中`: active work or committed near-term plan.
- `已解决`: recent evidence supports meaningful decline or fix.
- `无优化空间`: product control is low or constraints dominate.

## Priority Reasoning

When signals conflict, use this default order unless the user gives another priority model:

1. Explicit business or leadership commitment
2. Current high-volume unresolved issue
3. Revenue, conversion, retention, or operational risk
4. Major competitor or market gap with clear user expectation
5. Existing internal capability or low implementation cost
6. Long-term foundation work
7. Low-volume or stale observation

Do not map priority mechanically to a quarter, sprint, or release. Timing requires evidence, clear action, dependency awareness, and capacity.

## Product Wording

Avoid empty phrases like `持续优化`. If ongoing work is real, name the stage:

```text
现状：处理后核心问题率由 A% 降至 B%，但仍高于阈值
判断：问题仍需保留在观察/排查范围
建议：下一阶段拆分主要子问题，优先验证高频路径
```

## Source Labels

If the workbook has a source column, make the source explain why the item matters:

- high-volume feedback
- recurring recent issue
- competitor benchmark
- user request cluster
- business commitment
- technical dependency

Avoid source labels that only say "feedback table" or "analysis table" without importance.
