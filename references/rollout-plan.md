# Rollout Plan

**EN**: This document gives a staged rollout path from architecture design to retrieval validation and later automation.

**中文**：这份文档给出了一条分阶段实施路径：从架构设计开始，到检索验收，再到后续自动化。

## Stage 1 — Architecture

Define:
- what the user wants to remember
- what should always be hot memory
- what belongs in Obsidian
- what should be recallable but not always injected

Deliverables:
- memory goals
- three-layer architecture choice
- basic routing rules

## Stage 2 — Vault setup

Create:
- vault directory structure
- note templates
- naming conventions
- example notes

Deliverables:
- usable Obsidian vault skeleton
- at least one example project, topic, decision, and system note

## Stage 3 — Retrieval integration

Install and configure `memory-lancedb-pro`.

Start conservatively:
- recall on
- capture off at first
- assistant capture off
- extraction off

Deliverables:
- plugin loaded
- embeddings verified
- retrieval verified

## Stage 4 — Controlled automation

After some real usage:
- enable auto-capture if retrieval quality is acceptable
- review what gets stored
- adjust capture rules if memory gets noisy
- add a promotion gate so only selected items can enter the graph layer

Suggested promotion signals:
- user explicitly says it is important
- the same fact appears repeatedly
- the item is a project, decision, system rule, or durable preference
- the item clearly improves future collaboration

Deliverables:
- stable capture behavior
- initial useful recalls
- a clear memory hardening rule for Obsidian promotion

## Stage 5 — Validation and tuning

Test questions such as:
- what project am I working on?
- what system are we building?
- what preference did I mention before?
- what decision did we make earlier?

Measure:
- relevance
- noise
- duplication
- usefulness in context

## Stage 6 — Dedupe and merge

After the graph has real content, add a dedupe / merge review step.

Look for:
- duplicate notes with slightly different names
- repeated decisions stored twice
- project or topic notes that should be merged
- overlapping summaries that reduce graph quality

Possible future implementation:
- scripted similarity checks
- scheduled review tasks
- AI-assisted merge suggestions with human review

## Stage 7 — Optional extraction

Only after recall is stable, consider enabling smart extraction or a separate distillation workflow.

Do this only if the user has:
- a clear need for more automation
- a suitable LLM for extraction
- tolerance for reviewing memory quality
