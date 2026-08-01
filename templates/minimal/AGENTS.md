# AGENTS.md

This file tells Codex and other agents how to work in this repo.

## Read first

Before editing, read the compact universal entry set:

1. `README.md`
2. `docs/_index.md`
3. Any file directly affected by the task

Load `Atlas/00-Start Here.md` for navigation or restart routing. Load `session/Next session handoff.md` only for continuation, landing, cleanup, or unresolved prior state.

## Operating rules

- Prefer the repo's existing patterns.
- Keep changes focused on the requested task.
- Mark uncertainty instead of guessing.
- Prefer the smallest safe next step that creates useful progress.
- Keep session-loaded instructions, checked-out files, and fetched remote-tracking authority distinct. If current main differs on `AGENTS.md` or another relevant operating surface, reread current-main authority before setting/runtime advice or subsequent implementation. A fetch updates refs; it does not refresh the worktree.
- Do not ask clarifying questions for every small bounded task when the intended outcome is already clear.
- Ask clarifying questions when the answer would materially change authority, safety, scope, or outcome.
- If a request is broad, choose a bounded first pass, do it, and report what remains.
- Small tasks do not need ceremony.
- Keep universal starter context small. New useful docs remain conditional by default; do not add a mandatory starter file merely because it is important.
- When the current surface exposes a useful task-setting choice, classify settings by each actor's next substantial action and reassess at material phase changes; one role's difficulty does not set another's profile. Use visible labels, do not claim an unexposed setting, continue when sufficient, pause only for a useful escalation, and never interrupt an active role for a downgrade.
- Within an authorized task, prefer bounded nested delegation for separable specialist, checker, and validator work before replacing the coordinator. When nested agents are available, spawning inside the task and selecting an exposed child profile do not require approval for every spawn; each child stays inside the same authority and local law, while child-led recursion remains separately gated. Creating a new top-level task remains an explicit user-requested action.
- When a missing capability creates material or recurring friction, reduces confidence, blocks work, wastes substantial repeated effort, or could create reusable validation, propose the smallest exact remedy with scope, changed state, risk, rollback, fallback, and permission requested. Use an adequate existing fallback quietly for trivial one-off inconvenience.
- Treat installation, configuration, authentication, routine reuse, upgrade, and permission expansion as separate grants. A capability never widens repo-local authority.
- `observe only`, `report only`, `scan`, and `don't change a thing` mean inspect and report without file edits, staging, commits, pushes, merges, or durable capture.
- Do not casually edit safe-boundary areas listed below.
- Update the handoff or queue when useful context would otherwise be lost.
- For non-trivial work, run a closeout learning loop: note any repeatable failure mode, confusion, or risk; add the smallest reasonable prevention when safe; record a visible follow-up when prevention is too large; or say no useful guard was found.
- For non-trivial work, include `Learning loop: none`, `Learning loop: applied guard`, or `Learning loop: parked follow-up` in the final report.
- For non-trivial work, include `Durable capture: chat-only`, `Durable capture: written at [path]`, `Durable capture: queued at [path]`, or `Durable capture: blocked by stop gate` in the final report.
- Record-only durable capture may happen automatically when a repeatable, actionable, future-relevant lesson, decision, or follow-up has a clear approved owner surface and no stop gate applies. Use the smallest appropriate existing durable surface, such as `docs/`, `Atlas/`, `session/Next session handoff.md`, or `queue/00-work-queue.md`. Recording preserves context and does not approve execution, policy, landing, cleanup, publication, or further mutation.
- Do not perform durable capture when the run is explicitly report-only/no-write/no-capture, the owner surface is unclear, the material is sensitive or private, or the capture would broaden repo intent.

## Safe boundaries

Add repo-specific paths here when changes need extra care.

Example:

- `config/`: review behavior changes before committing.
- `schema/`: include validation notes for structural changes.

## Git workflow

Use a branch for changes. Commit and push only when the user asks or when this repo's workflow requires it. Do not merge to the default branch unless explicitly authorized. Report cleanup status and avoid leaving unnecessary branch or handoff debt.
