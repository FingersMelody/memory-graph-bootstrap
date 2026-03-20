# memory-graph-bootstrap

用于构建 **OpenClaw + Obsidian + memory-lancedb-pro** 三层记忆系统的 AgentSkill。

---

## 这个仓库是干什么的

这个 skill 用来帮助设计并落地一套三层记忆架构：

- **热记忆** —— OpenClaw 原生记忆文件
- **图谱层** —— 用 Obsidian 管理结构化笔记
- **检索层** —— 使用 `memory-lancedb-pro` 做 recall 和记忆捕捉

图谱层应该保持精炼，不应该变成检索层的完整镜像。
一个更稳妥的默认原则是“记忆固化”：广泛召回可以留在检索层，只有稳定且高价值的内容才提升到图谱层。

---

## 适合谁

- 想增强 OpenClaw 长期记忆的人
- 想做 Obsidian memory graph 规划的人
- 想接入并调优 `memory-lancedb-pro` 的人
- 想走保守式记忆自动化的人

---

## 不太适合谁

- 只想一键安装、不想做结构设计的人
- 不需要图谱层的用户
- 只想要通用 PKM 系统、与 OpenClaw 无关的场景

---

## 依赖条件

### 核心
- OpenClaw
- 这个 skill 目录本身

### 推荐
- Obsidian —— 用于图谱层
- `memory-lancedb-pro` —— 用于检索层工作流

### 可选
- 比如 **Jina** 这样的 embedding provider
- 用于后续抽取流程的 LLM

> 这个 skill 以架构设计优先，即使依赖还没全部装好，也可以先用来做规划。

---

## 安全说明

本仓库 **不包含**：
- API key
- 私有 vault 数据
- 本地记忆数据库
- 个人配置文件

如果你使用 Jina 或其他 LLM API，请在你自己的本地环境或配置中填写凭据，不要写进这个仓库。

---

## 仓库结构

- `SKILL.md` —— skill 主说明
- `references/architecture.md` —— 记忆架构
- `references/vault-schema.md` —— vault 结构与笔记 schema
- `references/lancedb-integration.md` —— 检索层接入建议
- `references/rollout-plan.md` —— 分阶段实施方案

---

## 如何使用

1. 把这个目录放到 OpenClaw 可加载的 skills 目录中。
2. 当你要设计记忆架构、Obsidian 图谱或检索层接入时使用它。
3. 先做架构和 schema。
4. 基础结构稳定后再接入检索层。
5. 先验收 recall，再逐步增加自动化。
6. 在大规模写入 Obsidian 前，先建立“记忆晋升门槛”。
7. 当图谱开始增长后，加入去重与合并检查。

---

## 设计理念

**先把 recall 做对，再逐步增加自动化。**

优先追求低维护成本：
- 检索层可以保持广度
- 图谱层应该经过过滤并保持结构化
- 在大规模写入 Obsidian 前先建立晋升门槛
- 在图谱变乱之前就安排去重与合并检查
