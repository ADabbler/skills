# Agent Skills

[English](README.md) · 简体中文

面向编程代理的 [Agent Skills](https://agentskills.io/specification) 集合。

## 安装

需要 Git 和 Node.js 22.20 或更高版本。在要使用技能的项目目录中运行以下命令，按提示选择技能和目标代理。

```sh
npx skills add ADabbler/skills
```

**查看可用技能**

```sh
npx skills add ADabbler/skills --list
```

**安装单项技能**

```sh
npx skills add ADabbler/skills --skill agent-notes
```

默认安装到当前项目。加上 `--global` 可在多个项目中使用。更多选项见[CLI 命令参考](https://github.com/vercel-labs/skills/blob/main/docs/commands.md)和[支持的代理](https://github.com/vercel-labs/skills/blob/main/docs/agents.md#supported-agents)。

## 技能

| 技能 | 使用场景 | 中文说明 |
| --- | --- | --- |
| [`agent-notes`](skills/agent-notes/SKILL.md) | 记录工作上下文与决策、交接任务，或审查与归档项目笔记。 | [中文对照](notes/implemented/2026-11-16-skills-review/agent-notes.zh.md) |
| [`prose-standard`](skills/prose-standard/SKILL.md) | 编写或审查技术文字，保留读者采取行动所需的事实。 | [中文对照](notes/implemented/2026-11-16-skills-review/prose-standard.zh.md) |

安装后，可在任务中按名称指定技能。

- 使用 `agent-notes` 记录这次调查的已确认发现、开放问题和下一步。
- 使用 `prose-standard` 审查这份 API 文档，写清前置条件和失败行为。

## 反馈

欢迎通过 [GitHub Issues](https://github.com/ADabbler/skills/issues) 反馈问题或提出建议。

## 致谢

笔记生命周期和写作规范参考了 [DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness) 与 [write-notes-like-deepseek](https://github.com/czm15053/write-notes-like-deepseek)。具体取舍见[设计笔记](notes/implemented/2026-10-02-agent-notes-architecture.md#上游依据与取舍)。

感谢 [LINUX DO](https://linux.do/) 社区。

## 许可证

本仓库采用 [MIT 许可证](LICENSE)。
