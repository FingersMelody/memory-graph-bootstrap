# memory-graph-bootstrap

**EN**: A public AgentSkill for designing a three-layer memory system with OpenClaw core memory, an Obsidian graph, and `memory-lancedb-pro` retrieval.

**中文**：这是一个公开的 AgentSkill，用来帮助用户设计一套三层记忆系统：OpenClaw 原生记忆、Obsidian 图谱层，以及 `memory-lancedb-pro` 检索层。

## Who this is for / 适合谁

**EN**
- People who want better long-term memory in OpenClaw
- People who want to combine Obsidian with AI memory
- People who want `memory-lancedb-pro` without going straight into aggressive automation

**中文**
- 想增强 OpenClaw 长期记忆的人
- 想把 Obsidian 和 AI 记忆结合起来的人
- 想接入 `memory-lancedb-pro`，但不想一上来就全自动化的人

## Who this is not for / 不太适合谁

**EN**
- People who only want a one-command installer
- People who do not want to design a memory structure
- People who are not using Obsidian and do not want a graph layer

**中文**
- 只想要一键安装、不想设计结构的人
- 不想做记忆分层的人
- 不使用 Obsidian，也不需要图谱层的人

## What is inside / 仓库内容

- `SKILL.md` — core skill instructions / skill 主说明
- `references/architecture.md` — three-layer architecture / 三层记忆架构
- `references/vault-schema.md` — vault structure and schema / vault 结构与 schema
- `references/lancedb-integration.md` — retrieval integration guidance / 检索层接入建议
- `references/rollout-plan.md` — staged rollout plan / 分阶段实施方案

## How to use / 如何使用

**EN**
1. Put this folder where your OpenClaw skills can be loaded.
2. Trigger it when working on memory architecture, Obsidian memory graphs, or `memory-lancedb-pro` rollout.
3. Start with architecture and schema first.
4. Add retrieval after the base structure exists.

**中文**
1. 把这个目录放到 OpenClaw 可加载的 skills 目录中。
2. 当你要做记忆架构设计、Obsidian memory graph、或 `memory-lancedb-pro` 接入时触发它。
3. 先做架构和 schema。
4. 在基础结构稳定后再接入检索层。

## Design philosophy / 设计理念

**EN**: Recall quality first, automation later.

**中文**：先把 recall 做对，再逐步增加自动化。
