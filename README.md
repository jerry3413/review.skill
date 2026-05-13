# Workbook Decision Review Skill

语言：中文 | [English](README.en.md)

这是一个通用 AI Agent 指令包，用于把中文产品/工作表格整理成可决策的输出，适合处理体征表、需求表、竞品分析表、领导/同事评论导出、以及修改后的工作簿。

## 功能

- 先检查真实工作簿文件，再决定结构或修改方式
- 只提出阻塞问题，避免一上来问长清单
- 保留原始证据，例如评论、计数、版本、标签、来源行
- 根据目标选择输出形态：老板汇报版、执行排期版、问题诊断版、需求池版、竞品对比版
- 对证据口径、去重、版本前后对比、分类、状态、优先级和排期节点使用更严格的规则
- 可以根据长期有效的复盘反馈进化，但不会把一次性的文字修改沉淀成永久规则

## 目录结构

```text
workbook-decision-review/
├── SKILL.md
└── references/
    ├── question-gate.md
    ├── output-shapes.md
    ├── evidence-rules.md
    ├── classification-status.md
    ├── evolution.md
    └── feedback-patterns.md
```

`SKILL.md` 保持短小，只负责触发、主流程和硬约束。更细的规则拆到 `references/`，让 Agent 在具体任务中按需读取，避免一次性加载过多上下文。

## 安装

把这个仓库克隆或复制到任意 Agent 能读取的位置：

```bash
git clone https://github.com/jerry3413/review.skill.git
```

对于任何 AI Agent，把 `SKILL.md` 作为入口指令，并允许它按需读取 `references/` 下的文件。如果你的平台有自己的 skill/plugin 目录，把整个文件夹放进去并保持目录结构即可。

## 使用示例

处理工作簿时可以这样说：

```text
用 workbook-decision-review 处理这个体征表，先看文件和评论，再决定要问我什么
```

或者在收到修改版之后：

```text
这是领导改完的版本，请对比我之前的输出，总结哪些规则要沉淀到 skill
```

## 进化策略

收到复盘反馈时，先把反馈分成三类：

- `本次修正`：只修当前这份工作簿
- `项目规则`：适用于当前产品或这类工作簿
- `长期方法`：可复用于未来工作簿 review

只有长期有效的 `长期方法` 才应该更新 skill。大多数细节规则应写进 `references/`，不要不断膨胀 `SKILL.md`。
