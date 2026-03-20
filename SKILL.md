---
name: memory-graph-bootstrap
description: Design and bootstrap a three-layer memory system for OpenClaw using core memory files, an Obsidian knowledge graph, and memory-lancedb-pro retrieval. Use when the user wants to improve long-term memory, build an Obsidian memory graph, connect Obsidian with AI memory, set up memory-lancedb-pro, define memory schemas, or design recall and auto-capture workflows. Best for architecture design, vault schema planning, phased rollout, conservative memory automation, and recall validation.
---

# Memory Graph Bootstrap

Design memory systems in three layers:

1. **Hot memory** — `MEMORY.md` and `memory/YYYY-MM-DD.md`
2. **Graph layer** — Obsidian vault with structured notes and links
3. **Retrieval layer** — `memory-lancedb-pro` for recall, capture, and semantic search

Default to **balanced automation**:
- enable recall first
- add auto-capture only after the base structure exists
- delay smart extraction until retrieval quality is stable

## Workflow

### 1. Place the user in a rollout stage
Classify the request into one of these stages:

- **Stage A — idea only**: user wants a better memory system but has no structure yet
- **Stage B — graph design**: user wants an Obsidian vault, note schema, and linking rules
- **Stage C — retrieval integration**: user wants to install or configure `memory-lancedb-pro`
- **Stage D — validation / tuning**: user wants to verify recall, capture quality, or automation boundaries

If unclear, ask only the minimum needed to place the user in one stage.

### 2. Recommend the default architecture
Unless the user has a strong reason otherwise, recommend:

- hot memory in OpenClaw native files
- Obsidian as the human-maintained graph layer
- `memory-lancedb-pro` as the retrieval layer

Keep the roles separate. Do not collapse everything into one layer.

### 3. Design before automation
Before enabling aggressive automation, define:

- vault directory structure
- core note types
- frontmatter schema
- naming conventions
- memory routing rules

Read `references/vault-schema.md` when designing the vault.
Read `references/architecture.md` when explaining the three-layer model.

### 4. Roll out in this order
Use this rollout sequence by default:

1. clarify memory goals
2. design the vault structure
3. create note templates
4. define routing and distillation rules
5. install / configure `memory-lancedb-pro`
6. enable recall first
7. enable auto-capture later
8. consider smart extraction only after retrieval is stable

Read `references/rollout-plan.md` for a detailed staged plan.

### 5. Use conservative retrieval defaults
When configuring `memory-lancedb-pro`, prefer:

- `autoRecall: true`
- `autoCapture: false` initially
- `captureAssistant: false`
- `smartExtraction: false` initially

Enable broader automation only after the user has real notes and can evaluate noise versus value.

Read `references/lancedb-integration.md` when planning or reviewing plugin setup.

### 6. Validate with concrete recall questions
After setup, test with questions like:

- what project am I working on?
- what memory system are we building?
- what preference did I mention before?
- what decision did we make earlier?

Judge the system by:
- relevance
- duplication
- noise
- usefulness in context

## Output expectations

When helping the user, prefer to produce:

- a recommended architecture
- a minimal vault structure
- a small set of note templates
- explicit routing rules for what belongs in each layer
- a phased rollout plan
- a verification checklist for recall quality

## Important rules

- Do not recommend storing everything in `MEMORY.md`
- Do not recommend using only a vector database without a human-readable structure
- Do not enable aggressive auto-capture by default
- Do not treat Obsidian as a dump of raw chat logs
- Prefer summaries and structured notes over raw transcript storage
- Prefer improving recall quality before adding more automation

## What this skill does not cover

This skill does **not** focus on:
- model switching
- provider relay setup
- unrelated personal knowledge management systems
- replacing the official plugin documentation

Its job is to help build a durable, maintainable, and recall-friendly memory system.
