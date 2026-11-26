# Agent Skills

English · [简体中文](README.zh-CN.md)

A collection of [Agent Skills](https://agentskills.io/specification) for coding agents.

## Install

With Git and Node.js 22.20 or later, run this from the project where you want to use the skills. Choose the skills and target agents when prompted.

```sh
npx skills add ADabbler/skills
```

**List available skills**

```sh
npx skills add ADabbler/skills --list
```

**Install one skill**

```sh
npx skills add ADabbler/skills --skill agent-notes
```

Installation is project-local by default. Add `--global` to make the skills available across your projects. See the [CLI reference](https://github.com/vercel-labs/skills/blob/main/docs/commands.md) and [supported agents](https://github.com/vercel-labs/skills/blob/main/docs/agents.md#supported-agents).

## Skills

| Skill | When to use it | Chinese guide |
| --- | --- | --- |
| [`agent-notes`](skills/agent-notes/SKILL.md) | Record working context and decisions, hand off a task, or review and archive project notes. | [中文对照](notes/implemented/2026-11-16-skills-review/agent-notes.zh.md) |
| [`prose-standard`](skills/prose-standard/SKILL.md) | Write or review technical prose while preserving the facts readers need to act. | [中文对照](notes/implemented/2026-11-16-skills-review/prose-standard.zh.md) |

After installation, you can ask your agent to use a skill by name.

- Use `agent-notes` to record confirmed findings, open questions, and the next step from this investigation.
- Use `prose-standard` to review this API documentation. Keep the prerequisites and failure behavior clear.

## Feedback

Share feedback or report a problem in [GitHub Issues](https://github.com/ADabbler/skills/issues).

## Acknowledgments

The note lifecycle and writing guidance draw on [DeepSeek Harness](https://github.com/deepseek-ai/deepseek-harness) and [write-notes-like-deepseek](https://github.com/czm15053/write-notes-like-deepseek). See which practices the skills adopt in the [design notes (Chinese)](notes/implemented/2026-10-02-agent-notes-architecture.md#上游依据与取舍).

Thanks to the [LINUX DO](https://linux.do/) community.

## License

This repository is licensed under the [MIT License](LICENSE).
