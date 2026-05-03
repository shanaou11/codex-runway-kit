# Atlas Memory for Codex

A Markdown-native, Git-native continuity layer for repositories that helps humans and Codex keep long-running work coherent across sessions.

## What problem it solves

Long-running repo work often loses context between sessions: what changed, what is still uncertain, which files should be read first, what evidence supported a decision, and what the next agent or human should avoid repeating.

Atlas Memory for Codex gives a repo a small set of durable Markdown surfaces for continuity: operating rules, maps, handoffs, work queues, evidence notes, truth/freshness labels, and reusable Codex prompts.

## What it is

- A public template and framework for repo-local memory.
- A lightweight convention for `AGENTS.md`, Atlas maps, handoffs, queues, evidence, and prompts.
- A way to make Codex sessions easier to restart, review, and hand off.
- Normal Markdown in normal Git history.

## What it is not

- Vector memory, RAG, or chatbot memory.
- AI consciousness, personhood, or identity.
- A clone of another coding-agent product.
- An automation platform.
- A replacement for normal project documentation.
- Production software, a CLI tool, or a package to install.

## Quick start

1. Copy `templates/minimal/` into a repository.
2. Edit `AGENTS.md` with repo-specific operating rules.
3. Fill in `Atlas/00-Start Here.md` with the main read-first map.
4. Keep `session/Next session handoff.md` updated when a work session ends.
5. Use `queue/00-work-queue.md` for active work and unresolved follow-ups.
6. Add evidence notes only when a decision, bug, migration, or high-risk change needs support.

## Minimal file layout

```text
AGENTS.md
README.md
docs/_index.md
Atlas/00-Start Here.md
session/Next session handoff.md
queue/00-work-queue.md
evidence/
prompts/
```

The minimal template in this repo keeps only the starter surfaces. Add `evidence/` and project-specific docs when the work needs them.

## Intended audience

Atlas Memory for Codex is for maintainers, solo builders, teams, and coding agents that need repo continuity without adding a database or external memory service. It is most useful when work spans many sessions, contributors, branches, or decisions.

## Current status

This repo is an early public template/framework. The contract is intentionally small, practical, and expected to evolve as real public examples clarify what is worth keeping.

Start with [docs/_index.md](docs/_index.md) for the public documentation map.
