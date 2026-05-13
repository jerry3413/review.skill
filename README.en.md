# Workbook Decision Review Skill

Language: [中文](README.md) | English

This is a general AI agent methodology package for reviewing spreadsheets, workbook comments, revised files, and decision-support tables. It is not a fixed template. It helps an agent identify the goal, preserve evidence, and then output issues, risks, recommendations, or an improved workbook.

## What It Does

- Inspects actual workbook files before proposing structure or edits
- Asks only blocker questions instead of long intake questionnaires
- Preserves source evidence such as original values, comments, counts, dates, versions, labels, and source rows
- Chooses the right output mode: issues and recommendations, action plan, diagnosis sheet, evidence appendix, or improved workbook
- In review mode, outputs both an overall judgment and locatable detailed findings, ideally tied to sheet, row, column, cell, or range
- Applies stricter rules for evidence口径, dedupe, time/version ranges, source traceability, and uncertainty
- Evolves from durable reviewer feedback without turning one-off wording changes into permanent rules

## Structure

```text
workbook-decision-review/
├── SKILL.md
└── references/
    ├── core-questioning.md
    ├── core-evidence.md
    ├── core-output.md
    ├── core-evolution.md
    └── domain-product-planning.md
```

`SKILL.md` is the entry and hard-constraint layer. `references/` is the progressive disclosure layer, so an agent reads only what is needed.

`domain-product-planning.md` is an optional domain extension for product feedback, user reviews, competitor research, and requirement prioritization workbooks.

## Installation

Clone or copy this repository anywhere your agent can read.

```bash
git clone https://github.com/jerry3413/review.skill.git
```

For any AI agent, provide `SKILL.md` as the entry instruction and allow it to read files under `references/` on demand. If your platform has a skill/plugin directory, place this folder there and keep the same structure.

## Usage

Review only:

```text
Use workbook-decision-review to inspect this workbook and give issues and recommendations. Do not edit files yet.
```

Improve a workbook:

```text
Use workbook-decision-review to process this workbook. Inspect files and comments first, ask only blocker questions if needed, then output an improved version.
```

Evolve from feedback:

```text
This is the revised version. Compare it with the previous output and decide which feedback is one-off correction and which should become long-term method.
```

## Evolution Policy

When post-review feedback arrives, classify it first:

- `本次修正`: only fixes the current workbook
- `项目规则`: useful for this project or workbook family
- `长期方法`: reusable across future workbook reviews

Only durable `长期方法` should update the method package. Never promote concrete workbook terms, versions, products, or fields directly into long-term rules; abstract them into principle, applicable condition, and boundary first.
