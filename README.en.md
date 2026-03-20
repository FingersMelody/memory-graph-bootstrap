# memory-graph-bootstrap

AgentSkill for building a three-layer OpenClaw memory system with Obsidian and memory-lancedb-pro.

---

## What it does

This skill helps design and roll out a memory stack with three layers:

- **Hot memory** — OpenClaw native memory files
- **Graph layer** — Obsidian vault with structured notes
- **Retrieval layer** — `memory-lancedb-pro` for recall and capture

The graph layer should stay selective. It should not become a full mirror of retrieval memory.
A good default is memory hardening: keep broad recall in retrieval, and promote only durable, high-value items into the graph layer.

---

## Best for

- Long-term memory design for OpenClaw
- Obsidian memory graph planning
- `memory-lancedb-pro` rollout and tuning
- Conservative memory automation

---

## Not ideal for

- One-command installation only
- Users who do not want a graph layer
- Users looking for a general PKM system unrelated to OpenClaw

---

## Requirements

### Core
- OpenClaw
- This skill folder

### Recommended
- Obsidian — for the graph layer
- `memory-lancedb-pro` — for retrieval workflows

### Optional
- An embedding provider such as **Jina**
- An LLM for later extraction workflows

> This skill is architecture-first. It can still be useful before every dependency is installed.

---

## Security

This repository does **not** include:
- API keys
- private user vault data
- local memory databases
- personal config files

If you use providers such as Jina or other LLM APIs, add your own credentials locally in your own environment or config.

---

## Repository layout

- `SKILL.md` — core skill instructions
- `references/architecture.md` — memory architecture
- `references/vault-schema.md` — vault structure and note schema
- `references/lancedb-integration.md` — retrieval integration guidance
- `references/rollout-plan.md` — staged rollout plan

---

## How to use

1. Put this folder where OpenClaw can load skills.
2. Use it when designing memory architecture, Obsidian graphs, or retrieval rollout.
3. Start with architecture and schema first.
4. Add retrieval after the base structure is stable.
5. Validate recall before enabling more automation.
6. Add a promotion gate before writing broadly into Obsidian.
7. Review duplicates after the graph starts to grow.

---

## Design philosophy

**Recall quality first, automation later.**

Prefer a low-maintenance system:
- retrieval can stay broad
- graph notes should stay filtered and structured
- add a promotion gate before broad Obsidian writes
- review duplicates before graph clutter grows
