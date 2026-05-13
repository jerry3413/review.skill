# Workbook Decision Review Skill

语言：中文 | [English](README.en.md)

这是一个通用 AI Agent 工作簿 review 方法包，用于处理表格、工作簿评论、修改版文件和决策支持型表格。它的目标不是套用某个固定模板，而是帮助 Agent 先识别目标、保留证据，再输出问题、风险、建议或改好的工作簿。

## 功能

- 先检查真实工作簿文件，再决定结构或修改方式
- 只提出阻塞问题，避免一上来问长清单
- 保留原始证据，例如原始值、评论、计数、日期、版本、标签、来源行
- 按任务选择输出模式：问题与建议、执行计划、诊断表、证据附录、改好后的工作簿
- Review 模式默认输出“总体判断 + 细项问题”，细项问题要尽量定位到 sheet、行、列、单元格或范围
- 对证据口径、去重、时间/版本区间、来源追溯和不确定性标注使用更严格的规则
- 可以根据长期有效的复盘反馈进化，但不会把一次性的文字修改沉淀成永久规则

## 目录结构

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

`SKILL.md` 是入口和硬约束层。`references/` 是渐进式披露层，Agent 只在需要时读取对应文件。

其中 `domain-product-planning.md` 是可选领域扩展，只在处理产品反馈、用户评论、竞品研究、需求优先级等工作簿时使用。

## 安装

把这个仓库克隆或复制到任意 Agent 能读取的位置：

```bash
git clone https://github.com/jerry3413/review.skill.git
```

对于任何 AI Agent，把 `SKILL.md` 作为入口指令，并允许它按需读取 `references/` 下的文件。如果你的平台有自己的 skill/plugin 目录，把整个文件夹放进去并保持目录结构即可。

## 使用示例

只 review，不修改文件：

```text
用 workbook-decision-review 看一下这个工作簿，有什么问题和建议，先不要改文件
```

改工作簿：

```text
用 workbook-decision-review 处理这个工作簿，先检查文件和评论，必要时只问阻塞问题，然后输出改好的版本
```

根据反馈进化：

```text
这是别人改完的版本，请对比我之前的输出，判断哪些是本次修正，哪些能沉淀成长期方法
```

## 进化策略

收到复盘反馈时，先把反馈分成三类：

- `本次修正`：只修当前这份工作簿
- `项目规则`：适用于当前项目或这类工作簿
- `长期方法`：可复用于未来工作簿 review

只有长期有效的 `长期方法` 才应该更新方法包。不能把具体工作簿里的词、版本、产品、字段原样沉淀为长期规则，必须先抽象成原则、适用条件和边界。
