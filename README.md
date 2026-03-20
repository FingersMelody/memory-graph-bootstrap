# memory-graph-bootstrap

Build a three-layer memory system for OpenClaw.
为 OpenClaw 构建一套三层记忆系统。

---

## What this skill does / 这个 skill 是干什么的

This skill helps design and roll out a memory stack with three layers:
这个 skill 用来帮助设计并落地一套三层记忆架构：

- **Hot memory** — OpenClaw native memory files  
  **热记忆**：OpenClaw 原生记忆文件
- **Graph layer** — Obsidian vault with structured notes  
  **图谱层**：用 Obsidian 管理结构化笔记
- **Retrieval layer** — `memory-lancedb-pro` for recall and capture  
  **检索层**：使用 `memory-lancedb-pro` 做 recall 和记忆捕捉

---

## Best for / 适合场景

- Long-term memory design for OpenClaw  
  OpenClaw 长期记忆设计
- Obsidian memory graph planning  
  Obsidian memory graph 规划
- `memory-lancedb-pro` rollout and tuning  
  `memory-lancedb-pro` 接入与调优
- Conservative memory automation  
  保守式记忆自动化

---

## Not ideal for / 不太适合

- One-command installation only  
  只想一键安装，不想做结构设计
- Users who do not want a graph layer  
  不需要图谱层的用户
- Users looking for a general PKM system unrelated to OpenClaw  
  只想要通用知识管理系统、与 OpenClaw 无关的场景

---

## Requirements / 依赖条件

### Core / 核心
- OpenClaw
- This skill folder / 这个 skill 目录本身

### Recommended / 推荐
- Obsidian — for the graph layer / 用于图谱层
- `memory-lancedb-pro` — for retrieval workflows / 用于检索层

### Optional / 可选
- An embedding provider such as **Jina**  
  比如 **Jina** 这样的 embedding provider
- An LLM for later extraction workflows  
  用于后续抽取流程的 LLM

> This skill is architecture-first. It can still be useful before every dependency is installed.  
> 这个 skill 以架构设计优先，即使依赖还没全部装好，也可以先用来做规划。

---

## Security / 安全说明

This repository does **not** include:
本仓库 **不包含**：

- API keys
- private user vault data
- local memory databases
- personal config files

If you use providers such as Jina or other LLM APIs, add your own credentials locally in your own environment or config.
如果你使用 Jina 或其他 LLM API，请在你自己的本地环境或配置中填写凭据，不要写进这个仓库。

---

## Repository layout / 仓库结构

- `SKILL.md` — core skill instructions / skill 主说明
- `references/architecture.md` — memory architecture / 记忆架构
- `references/vault-schema.md` — vault structure and note schema / vault 结构与笔记 schema
- `references/lancedb-integration.md` — retrieval integration guidance / 检索层接入建议
- `references/rollout-plan.md` — staged rollout plan / 分阶段实施方案

---

## How to use / 如何使用

1. Put this folder where OpenClaw can load skills.  
   把这个目录放到 OpenClaw 可加载的 skills 目录中。
2. Use it when designing memory architecture, Obsidian graphs, or retrieval rollout.  
   当你要设计记忆架构、Obsidian 图谱或检索层接入时使用它。
3. Start with architecture and schema first.  
   先做架构和 schema。
4. Add retrieval after the base structure is stable.  
   基础结构稳定后再接入检索层。
5. Validate recall before enabling more automation.  
   先验收 recall，再逐步增加自动化。

---

## Design philosophy / 设计理念

**Recall quality first, automation later.**  
**先把 recall 做对，再逐步增加自动化。**
