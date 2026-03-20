# Vault Schema

**EN**: This document defines a practical Obsidian vault structure, note types, and routing rules for memory systems.

**中文**：这份文档定义了一套适合记忆系统的 Obsidian vault 结构、笔记类型和分流规则。

## Recommended vault structure

```text
OpenClaw-Memory-Vault/
  00-Inbox/
  01-Daily/
  02-People/
  03-Projects/
  04-Topics/
  05-Decisions/
  06-Memories/
  07-Systems/
  08-Reviews/
  99-Templates/
```

## Core note types

### Daily
Use as the raw input layer.

Suggested sections:
- 今日事件 / Events
- 项目更新 / Project Updates
- 关键决策 / Key Decisions
- 候选长期记忆 / Candidate Long-Term Memories
- 后续行动 / Next Steps

### Project
Use for active work with goals and state.

Suggested sections:
- Goal
- Why
- Current Status
- Key Decisions
- Blockers
- Next Steps

### Topic
Use for recurring themes and domain knowledge.

Suggested sections:
- Summary
- Key Ideas
- Open Questions
- Related Notes

### Decision
Use when the user made a meaningful choice.

Suggested sections:
- Decision
- Context
- Alternatives Considered
- Why This Choice
- Consequences

### System
Use for methods, workflows, and architecture.

Suggested sections:
- Purpose
- Structure
- Rules
- Workflow
- Future Improvements

## Frontmatter guidance

Prefer a small stable schema:

```yaml
---
type: project | topic | decision | system | memory | person | daily
created: YYYY-MM-DD
updated: YYYY-MM-DD
summary: one-line summary
status: active | accepted | archived
tags:
  - ...
---
```

## Naming rules

- Keep file names stable
- Use one main note per concept when possible
- Prefer readable titles over clever short names
- Use date-prefixed names for decisions and daily notes

## Routing rule

- raw information goes to Daily first
- stable information gets promoted into structured notes
- only the highest-signal stable items belong in `MEMORY.md`
