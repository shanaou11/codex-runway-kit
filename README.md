# Codex Runway Kit

A practical Markdown-native, Git-native kit for making Codex-assisted repository work easier to start, steer, hand off, and review.

## What problem it solves

Codex-assisted repo work often needs more than one prompt. Context has to be found, boundaries have to be respected, unfinished work has to be handed off, and larger efforts need a simple way to coordinate readers, editors, checkers, and validators.

Codex Runway Kit gives a repo a small set of reusable public patterns for that work: Atlas Memory, ATC/Council coordination, ground crew roles, handoffs, prompts, guardrails, and future draft workflow surfaces.

## What it is

- A public template and documentation kit for repo-local Codex workflows.
- A lightweight convention for `AGENTS.md`, Atlas maps, handoffs, queues, evidence notes, prompts, and review gates.
- A way to make Codex sessions easier to restart, steer, check, validate, and hand off.
- A place for small reusable workflow surfaces that may later become prompts, templates, or draft skills.
- Normal Markdown in normal Git history.

## Core layers

- **Atlas Memory:** the first concrete module. It keeps repo-local continuity in Markdown through operating rules, maps, handoffs, queues, evidence notes, truth/freshness labels, and reusable prompts.
- **ATC/Council workflow:** an optional coordination pattern for larger runs. ATC keeps the mission, scope, stop conditions, and landing report clear; Council roles split work across implementation, checking, validation, and recommendation.
- **Ground crew roles:** small role labels for practical repo work, such as reader, editor, checker, validator, and navigator. They are meant to clarify responsibility, not create ceremony.
- **Handoffs and prompts:** reusable session-start, context-pack, bootstrap, and update prompts that help Codex and humans restart with less context loss.
- **Guardrails:** plain-language boundaries for public wording, safe editing, truth labels, note size, and promotion of temporary observations into durable docs.
- **Future skills:** draft reusable workflow surfaces may be documented here over time. They should be treated as future-facing patterns, not finished installable products.

## What it is not

- Vector memory, RAG, or chatbot memory.
- AI consciousness, personhood, or identity.
- A clone of another coding-agent product.
- An automation platform.
- A replacement for normal project documentation, tests, issues, or pull requests.
- Production software, a CLI tool, a package, a plugin, or a hosted platform.

## Quick start

### Option A: Ask Codex to adopt Atlas Memory

Atlas Memory is the best starting point because it is the current concrete module in the kit.

1. Open Codex in the target repository.
2. Paste or reference [prompts/codex-bootstrap-atlas-memory.md](prompts/codex-bootstrap-atlas-memory.md).
3. Let Codex inspect the repo before editing.
4. Have Codex adapt the minimal Atlas Memory surfaces to the repo using observable evidence.
5. Review the branch, files changed, assumptions, and validation results before merging.

This is a prompt-driven Markdown workflow. It does not auto-install itself, add a CLI, or replace the target repo's existing docs.

### Option B: Install manually

1. Copy `templates/minimal/` into a repository.
2. Edit `AGENTS.md` with repo-specific operating rules.
3. Fill in `Atlas/00-Start Here.md` with the main read-first map.
4. Keep `session/Next session handoff.md` updated when a work session ends.
5. Use `queue/00-work-queue.md` for active work and unresolved follow-ups.
6. Add evidence notes only when a decision, bug, migration, or high-risk change needs support.

### Option C: Use the broader runway pattern

For larger work, combine Atlas Memory with a light ATC/Council run:

1. Define the mission, scope, authority, and stop conditions.
2. Paste or adapt [prompts/codex-run-atc-council-mission.md](prompts/codex-run-atc-council-mission.md) for a visible preflight and closeout.
3. Assign practical ground crew roles such as editor, checker, validator, and navigator.
4. Work on a branch and keep changes focused.
5. Validate the result with repo-appropriate checks.
6. Land with a concise run report: branch, files changed, validation, risks, and recommended next phase.

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

Codex Runway Kit is for maintainers, solo builders, teams, and coding agents that need practical continuity and review structure without adding a database or external memory service. It is most useful when work spans many sessions, contributors, branches, decisions, or review gates.

## Current status

This repo is an early public template and workflow kit. Atlas Memory is the first concrete module. The broader ATC/Council, ground crew, guardrail, prompt, and future-skill surfaces are intentionally small and expected to evolve as public examples clarify what is worth keeping.

Start with [docs/_index.md](docs/_index.md) for the public documentation map.
