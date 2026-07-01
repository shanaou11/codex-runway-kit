# Codex Runway Kit

A practical Markdown-native, Git-native framework for directing Codex-assisted repository work through mission briefs, local law, Atlas Memory, ATC/Council review, ground-site discipline, handoffs, validation, and landing reports.

## What problem it solves

Codex-assisted repo work often needs more than one prompt. Context has to be found, local boundaries have to be respected, unfinished work has to be handed off, and larger efforts need a simple way to coordinate readers, editors, checkers, and validators.

Codex Runway Kit gives a repo a small set of reusable public patterns for that work. The kit helps a human or agent say what mission is being flown, which repo is the ground site, what local law applies, what may be changed, how the work will be checked, and what landing report should be left behind.

## What it is

- A public template and documentation kit for repo-local Codex workflows.
- A lightweight convention for mission briefs, `AGENTS.md`, Atlas maps, handoffs, queues, evidence notes, prompts, review gates, validation, and landing reports.
- A way to make Codex sessions easier to start, restart, steer, check, validate, and hand off.
- A place for small reusable workflow surfaces that may later become prompts, templates, or draft skills.
- Normal Markdown in normal Git history.

## Core layers

- **Mission brief:** the short instruction that defines the goal, target repo, authority, allowed writes, forbidden writes, stop conditions, validation, and reporting expectations.
- **Local law:** the repo's own `AGENTS.md` and project docs. Local law controls what Codex may do in that repo.
- **Atlas Memory:** the first concrete module. It keeps repo-local continuity in Markdown through operating rules, maps, handoffs, queues, optional evidence notes, truth/freshness labels, and repeatable prompts when useful.
- **ATC/Council workflow:** an optional coordination pattern for larger runs. ATC keeps the mission, scope, stop conditions, and landing report clear; Council roles split work across implementation, checking, validation, recommendation, and larger planning or drafting when useful.
- **Ground sites:** target repositories where work happens. The kit encourages the steering context to summarize and point rather than copy source truth away from the ground site.
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

### Option A: Run a small mission brief

Use this when the target repo already has enough instructions to work safely.

1. Open Codex in the target repository.
2. Read the repo's `AGENTS.md`, `README.md`, and docs index if present.
3. Give Codex a short mission brief:
   - mission goal
   - target repo
   - branch expectation
   - allowed writes
   - forbidden writes
   - validation required
   - landing report required
4. Keep work on a branch and validate before landing.
5. End with a concise landing report: branch, files changed, validation, risks, and next gate.

The [Runway Operations](docs/08-runway-operations.md) doc gives a reusable public shape for mission briefs, local law, ground sites, validation, and landing reports.

### Option B: Ask Codex to adopt Atlas Memory

Atlas Memory is the best starting point because it is the current concrete module in the kit.

1. Open Codex in the target repository.
2. Paste or reference [prompts/codex-bootstrap-atlas-memory.md](prompts/codex-bootstrap-atlas-memory.md).
3. Let Codex inspect the repo before editing.
4. Have Codex adapt the minimal Atlas Memory surfaces to the repo using observable evidence.
5. Review the branch, files changed, assumptions, and validation results before merging.

This is a prompt-driven Markdown workflow. It does not auto-install itself, add a CLI, or replace the target repo's existing docs.

### Option C: Install manually

1. Copy `templates/minimal/` into a repository.
2. Edit `AGENTS.md` with repo-specific operating rules.
3. Fill in `Atlas/00-Start Here.md` with the main read-first map.
4. Keep `session/Next session handoff.md` updated when a work session ends.
5. Use `queue/00-work-queue.md` for active work and unresolved follow-ups.
6. Add evidence notes only when a decision, bug, migration, or high-risk change needs support.
7. Add reusable prompts only when the repo has Codex workflows worth repeating.

### Option D: Use the broader runway pattern

For larger work, combine Atlas Memory with a light ATC/Council run:

1. Define the mission, scope, authority, and stop conditions.
2. Paste or adapt [prompts/codex-run-atc-council-mission.md](prompts/codex-run-atc-council-mission.md) for a visible preflight and closeout.
3. Assign practical ground crew roles such as editor, checker, validator, and navigator.
4. Work on a branch and keep changes focused.
5. Validate the result with repo-appropriate checks.
6. Land with a concise run report: branch, files changed, validation, risks, and recommended next phase.

When the output is a larger plan, spec, roadmap, doctrine note, or module direction, use [prompts/codex-run-review-council-planning-drafting.md](prompts/codex-run-review-council-planning-drafting.md) instead. It keeps planning lanes, source-truth checks, sequencing, drafting, checker, and validator work visible without claiming automation that the kit does not provide.

## What is real today

Real today:

- Public Markdown docs and templates.
- Reusable prompt files for bootstrap, session start, context packs, Atlas updates, and ATC/Council missions.
- A public Review Council Planning + Drafting prompt for larger artifact-producing work.
- A minimal Atlas Memory starter layout.
- Public doctrine for mission briefs, local law, ATC/Council review, ground sites, validation, and landing reports.

Draft or future-facing:

- Packaged skills, plugins, CLIs, automation controllers, or hosted services.
- Any claim that this kit automatically orchestrates work across repositories.
- Any claim that Atlas Memory is external memory, vector memory, RAG, or a replacement for project source truth.

## Minimal file layout

```text
AGENTS.md
README.md
docs/_index.md
Atlas/00-Start Here.md
session/Next session handoff.md
queue/00-work-queue.md
```

The minimal template in this repo keeps only the starter surfaces. Add `evidence/` when a decision or risky change needs support, and add `prompts/` when the repo has repeatable Codex workflows.

## Intended audience

Codex Runway Kit is for maintainers, solo builders, teams, and coding agents that need practical continuity and review structure without adding a database or external memory service. It is most useful when work spans many sessions, contributors, branches, decisions, or review gates.

## Current status

This repo is an early public template and workflow kit. Atlas Memory is the first concrete module, but the public frame is broader: reusable runway practice for briefing, steering, checking, validating, and landing Codex-assisted repo work. The ATC/Council, ground crew, guardrail, prompt, and future-skill surfaces are intentionally small and expected to evolve as public examples clarify what is worth keeping.

Start with [docs/_index.md](docs/_index.md) for the public documentation map.
