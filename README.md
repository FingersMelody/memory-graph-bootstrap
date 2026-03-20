# memory-graph-bootstrap

Build a three-layer memory system for OpenClaw.
为 OpenClaw 构建一套三层记忆系统。

**Language / 语言**
- [English](./README.en.md)
- [中文](./README.zh.md)

---

## Overview / 概览

This repository contains an AgentSkill for designing and rolling out a three-layer memory architecture with:
这个仓库包含一个 AgentSkill，用于设计和落地一套三层记忆架构，包括：

- OpenClaw hot memory / OpenClaw 热记忆
- Obsidian graph layer / Obsidian 图谱层
- `memory-lancedb-pro` retrieval layer / `memory-lancedb-pro` 检索层

> The graph layer should stay selective. It should not become a full mirror of retrieval memory.  
> 图谱层应该保持精炼，不应该变成检索层的完整镜像。

---

## Repository layout / 仓库结构

- `SKILL.md`
- `references/architecture.md`
- `references/vault-schema.md`
- `references/lancedb-integration.md`
- `references/rollout-plan.md`

---

## Security / 安全说明

This repository does **not** include API keys, private vault data, local memory databases, or personal config files.
本仓库 **不包含** API key、私有 vault 数据、本地记忆数据库或个人配置文件。
