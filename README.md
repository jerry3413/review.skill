# Workbook Decision Review Skill

This Codex skill helps turn Chinese product/workbook materials into decision-ready outputs. It is designed for symptom lists, requirement lists, competitive analysis sheets, reviewer comment exports, and revised workbooks.

## What It Does

- Inspects actual workbook files before proposing structure or edits
- Asks only blocker questions instead of long intake questionnaires
- Preserves raw evidence such as comments, counts, versions, labels, and source rows
- Chooses the right output shape for boss reports, execution schedules, diagnosis sheets, requirement pools, and competitor comparisons
- Applies stricter rules for evidence口径, dedupe, version comparison, classification, status, priority, and release nodes
- Evolves from durable reviewer feedback without turning one-off wording changes into permanent rules

## Structure

```text
workbook-decision-review/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── question-gate.md
    ├── output-shapes.md
    ├── evidence-rules.md
    ├── classification-status.md
    ├── evolution.md
    └── feedback-patterns.md
```

`SKILL.md` stays short and acts as the trigger, workflow, and hard-constraint layer. Detailed rules are split into `references/` so Codex loads only what is needed for the current task.

## Installation

Clone or copy this folder into your Codex skills directory:

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/jerry3413/review.skill.git ~/.codex/skills/workbook-decision-review
```

Restart Codex after installation so the skill can be discovered.

## Usage

Use it when asking Codex to work on a spreadsheet or workbook such as:

```text
用 workbook-decision-review 处理这个体征表，先看文件和评论，再决定要问我什么
```

or:

```text
这是领导改完的版本，请对比我之前的输出，总结哪些规则要沉淀到 skill
```

## Evolution Policy

When post-review feedback arrives, classify it first:

- `本次修正`: only fixes the current workbook
- `项目规则`: useful for this product/workbook family
- `长期方法`: reusable across future workbook reviews

Only durable `长期方法` should update the skill. Most detailed updates should go into `references/` instead of expanding `SKILL.md`.
