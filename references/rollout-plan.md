# Rollout Plan

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

Deliverables:
- stable capture behavior
- initial useful recalls

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

## Stage 6 — Optional extraction

Only after recall is stable, consider enabling smart extraction or a separate distillation workflow.

Do this only if the user has:
- a clear need for more automation
- a suitable LLM for extraction
- tolerance for reviewing memory quality
