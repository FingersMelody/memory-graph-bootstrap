# Three-Layer Memory Architecture

**EN**: This document explains why memory should be split into hot memory, graph memory, and retrieval memory.

**中文**：这份文档解释为什么记忆系统应该拆成热记忆、图谱记忆和检索记忆三层。

## Goal

Combine fast always-loaded memory, human-maintained knowledge structure, and semantic recall.

## Layer 1: Hot memory

Use OpenClaw native files:
- `MEMORY.md`
- `memory/YYYY-MM-DD.md`

### Store here
- stable user preferences
- short high-signal facts
- frequently needed context
- compact summaries of ongoing projects

### Do not store here
- long raw logs
- transient jokes
- duplicate event history
- low-confidence guesses

## Layer 2: Graph layer

Use Obsidian for:
- projects
- topics
- decisions
- systems
- memories
- people
- reviews

### Purpose
- make memory readable
- make memory maintainable
- create links and graph relationships
- support manual review and cleanup
- preserve only higher-signal structured knowledge, not every captured memory

### Important boundary
Do not use the graph layer as a full sync target for retrieval memory.
Retrieval memory can be broad; graph memory should stay selective.
Only promote items into Obsidian when they are stable, important, repeated, user-confirmed, or structurally useful.

## Layer 3: Retrieval layer

Use `memory-lancedb-pro` for:
- semantic recall
- auto-capture
- retrieval injection
- future extraction and memory lifecycle work

### Purpose
- help the agent remember by meaning, not just keywords
- support larger memory volume without stuffing everything into prompt memory

## Core principle

Hot memory is what should always be carried.
Graph memory is what humans should be able to inspect and maintain.
Retrieval memory is what should be searchable and recallable.

Do not use one layer to replace the others.
