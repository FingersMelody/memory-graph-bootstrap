# memory-lancedb-pro Integration

**EN**: This document explains how to integrate `memory-lancedb-pro` conservatively, starting with recall before broader automation.

**中文**：这份文档说明如何以保守方式接入 `memory-lancedb-pro`，优先做好 recall，再逐步增加自动化。

## Default recommendation

Start with a recall-first setup.

Recommended first pass:
- `autoRecall: true`
- `autoCapture: false`
- `captureAssistant: false`
- `smartExtraction: false`

Enable `autoCapture` only after the user has a base structure and enough real data to evaluate quality.

## Why recall-first

This avoids early memory pollution and lets the user confirm that:
- the plugin loads correctly
- embeddings work
- retrieval works
- injected memories are actually useful

## Good retrieval inputs

Prefer indexing or capturing:
- structured note summaries
- compact project updates
- stable preference statements
- decision summaries
- recurring themes

## Avoid relying on

- full raw chat dumps
- low-value greetings
- speculative statements
- repeated assistant boilerplate

## Jina embedding guidance

If using Jina:
- verify the API key works
- confirm the configured embedding model appears in plugin registration logs
- confirm initialization logs mention embedding OK and retrieval OK

## Verification signals

Healthy logs often include messages like:
- plugin registered
- embedding OK
- retrieval OK
- auto-captured N memories
- injecting N memories into context

## Warning signs

Investigate if you see:
- missing env var errors
- plugin register failure
- embedding initialization failure
- repeated zero-result recall for known captured content
