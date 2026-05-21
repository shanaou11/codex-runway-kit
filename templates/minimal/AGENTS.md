# AGENTS.md

This file tells Codex and other agents how to work in this repo.

## Read first

Before editing, read:

1. `README.md`
2. `docs/_index.md`
3. `Atlas/00-Start Here.md`
4. `session/Next session handoff.md`
5. Any file directly affected by the task

## Operating rules

- Prefer the repo's existing patterns.
- Keep changes focused on the requested task.
- Mark uncertainty instead of guessing.
- Prefer the smallest safe next step that creates useful progress.
- Do not ask clarifying questions for every small bounded task when the intended outcome is already clear.
- Ask clarifying questions when the answer would materially change authority, safety, scope, or outcome.
- If a request is broad, choose a bounded first pass, do it, and report what remains.
- Small tasks do not need ceremony.
- Do not casually edit safe-boundary areas listed below.
- Update the handoff or queue when useful context would otherwise be lost.

## Safe boundaries

Add repo-specific paths here when changes need extra care.

Example:

- `config/`: review behavior changes before committing.
- `schema/`: include validation notes for structural changes.

## Git workflow

Use a branch for changes. Commit and push only when the user asks or when this repo's workflow requires it.
