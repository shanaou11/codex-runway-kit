# File Roles

Atlas Memory works best when each file has a narrow job.

## `AGENTS.md`

The local operating guide for Codex and other agents. It should contain repo-specific rules, read-first instructions, safety boundaries, wording constraints, and required workflows.

Use it for stable, high-value rules. Do not use it as a session diary.

## `README.md`

The public front door. It explains what the project is, who it is for, how to start, and where to read next.

Use it for orientation. Do not overload it with every rule or decision.

## `docs/_index.md`

The documentation map. It lists durable docs and gives readers a short reason to open each one.

Update it when durable docs are added, moved, renamed, or removed.

## `Atlas/00-Start Here.md`

The repo map for fast restart. It should point to the most important files, current work areas, known boundaries, and recent handoff context.

Atlas maps should route readers. They should not duplicate full canonical docs.

## `session/Next session handoff.md`

The current handoff for the next human or Codex session. It should capture what just happened, what remains open, what to read first, and what not to redo.

Keep it short enough to read at the start of a session.

## `queue/00-work-queue.md`

The visible list of active or candidate work. It can include next tasks, blocked tasks, follow-ups, and parking-lot items.

Use it to preserve intent without pretending every idea is committed work.

## `evidence/`

Supporting material for decisions, investigations, migrations, risky edits, or bug reproduction. Evidence can include notes, logs, screenshots, command output summaries, or links to repo artifacts.

Use evidence when a future reader may ask, "Why do we believe this?"

## `prompts/`

Reusable Codex prompts for common workflows, such as starting a session, preparing a context pack, or updating Atlas after work.

The bootstrap prompt is the adoption prompt for adding Atlas Memory surfaces to a target repo. It should make Codex inspect first, preserve existing project identity, adapt from repo evidence, and report what changed.

Prompts should be practical and repo-neutral unless they live inside a specific project.
