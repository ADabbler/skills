# 技能职责与设计依据

Status: implemented

`agent-notes` 用于维护工作笔记，`prose-standard` 用于编写和审查技术文字。英文源文件位于仓库的 `skills/` 中。

## 决定与入口

| Skill | 职责 | 入口 |
| --- | --- | --- |
| `agent-notes` | 精简记录、上下文延续、决定归属与生命周期整理 | [技能](../../skills/agent-notes/SKILL.md) · [UI 元数据](../../skills/agent-notes/agents/openai.yaml) |
| `prose-standard` | 事实完整性、读者视角、表达精简与会话痕迹审查 | [技能](../../skills/prose-standard/SKILL.md) · [UI 元数据](../../skills/prose-standard/agents/openai.yaml) |

## 理由与职责边界

笔记创建、更新与清理需要共享状态和保留判断，因此集中在 `agent-notes`。工作记录可以只服务于当前任务，长期保留以其对后续工作的用途为准。

`prose-standard` 可独立安装和使用，适用于文档、代码注释、提示词、诊断信息和界面文案等技术文字的编写与审查。处理工作笔记时，也可与 `agent-notes` 配合使用。

## 上游依据与取舍

上游核对日期为 2026-11-17，以下链接固定到已读取的提交。

| 来源 | 核对结果与采用范围 |
| --- | --- |
| [DeepSeek Harness：笔记整理](https://github.com/deepseek-ai/deepseek-harness/blob/39163dd30f703a79079e2d2446545cff3c453738/.agents/skills/dsh-archive-agent-notes/SKILL.md) | 按未来决策价值保留、归档和去重，区分当前指导与历史证据 |
| [表达规范](https://github.com/deepseek-ai/deepseek-harness/blob/39163dd30f703a79079e2d2446545cff3c453738/.agents/skills/dsh-prose-standard/SKILL.md) · [会话痕迹](https://github.com/deepseek-ai/deepseek-harness/blob/39163dd30f703a79079e2d2446545cff3c453738/.agents/skills/dsh-trim-cot-leakage/SKILL.md) | 保留必要事实与约束，按读者用途处理会话痕迹；英文界面文案采用 sentence case，项目已有风格优先 |
| [文档组织](https://github.com/deepseek-ai/deepseek-harness/blob/39163dd30f703a79079e2d2446545cff3c453738/.agents/skills/dsh-doc-writing/SKILL.md) | 按读者和文档用途组织内容；不采用 DSH 专用的双语配对、站点和固定模板要求 |
| [write-notes-like-deepseek](https://github.com/czm15053/write-notes-like-deepseek/blob/72573a5b179de7798bbb7c4aeacdc0df6bf62439/skills/write-notes-like-deepseek/SKILL.md) | 无真实备选时不编造。其 [quality-gate](https://github.com/czm15053/write-notes-like-deepseek/blob/72573a5b179de7798bbb7c4aeacdc0df6bf62439/skills/write-notes-like-deepseek/references/quality-gate.md) 要求至少两个备选，[归档示例](https://github.com/czm15053/write-notes-like-deepseek/blob/72573a5b179de7798bbb7c4aeacdc0df6bf62439/skills/write-notes-like-deepseek/references/archiving.md)与保留规则存在冲突，不采用其数量和分类要求 |

文档按读者、目标与用途组织，不要求固定问答或大纲审批流程。[Agent Skills 规范](https://agentskills.io/specification)与 [Skill Creator](https://github.com/openai/skills/blob/49f948faa9258a0c61caceaf225e179651397431/skills/.system/skill-creator/SKILL.md) 提供技能结构、按需加载与校验方法的参考。

## 验证范围

已核对技能结构、界面元数据、本地引用及中英文对照一致性；未进行独立模型场景验证。
