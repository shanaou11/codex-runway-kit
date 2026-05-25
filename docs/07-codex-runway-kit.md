# Codex Runway Kit

Codex Runway Kit is the public umbrella for reusable repo-local workflows that help humans and Codex brief, start, steer, hand off, validate, and review repository work.

It is intentionally modest: Markdown files, Git branches, clear prompts, practical roles, and validation notes. It is not a CLI, package, plugin, hosted service, or production platform.

## The runway loop

The kit is organized around a small loop:

1. Write a mission brief.
2. Read local law in the target repo.
3. Use Atlas Memory to recover context.
4. Work only in the authorized ground site.
5. Use ATC/Council review when role separation helps.
6. Validate with checks appropriate to the repo and risk.
7. Leave a landing report.

See [Runway Operations](08-runway-operations.md) for the public operating pattern.

## How the pieces fit

### Atlas Memory

Atlas Memory is the first module and current foundation layer of the kit. It gives a repository durable continuity surfaces:

- `AGENTS.md` for local operating rules.
- `docs/_index.md` for durable documentation navigation.
- `Atlas/00-Start Here.md` for a fast restart map.
- `session/Next session handoff.md` for current handoff context.
- `queue/00-work-queue.md` for active and parked work.
- `evidence/` when decisions or risky changes need support.
- `prompts/` for repeatable Codex workflows.

Atlas Memory should remain a component inside the kit, not the entire public identity of the repo. It answers "how does this repo remember enough to restart?" while the broader Runway Kit also answers "how do we brief, steer, check, validate, and land the work?"

### Mission Briefs And Local Law

A mission brief defines the immediate run: mission, target repo, branch expectation, allowed writes, forbidden writes, stop conditions, validation, and landing report.

Local law is the target repo's `AGENTS.md` and project documentation. It remains authoritative for that repo. A mission brief narrows the task; it does not override local law unless the maintainer explicitly updates the repo's own rules.

### ATC/Council Workflow

ATC/Council is an optional coordination pattern for larger Codex-assisted runs.

- ATC keeps the mission, scope, authority, stop conditions, and landing report visible.
- Council separates responsibilities so a run can include editing, checking, validation, and recommendation without blurring those jobs together.
- For larger plans, specs, roadmaps, doctrine notes, or module direction, Council can also separate planning and drafting lanes so the artifact skeleton begins while other lanes inspect current state, source truth, structure, sequencing, and risks.
- The workflow can be used by one person, one Codex session, or several manually coordinated sessions.

This is a documentation and prompting pattern. It does not automate orchestration by itself.

The public starter surface is [Codex Prompt: Run ATC/Council Mission](../prompts/codex-run-atc-council-mission.md). Use it for a bounded repo mission after reading local instructions and the relevant repo docs. For bigger artifact-producing work, use [Codex Prompt: Run Review Council Planning + Drafting](../prompts/codex-run-review-council-planning-drafting.md).

### Ground Crew Roles

Ground crew roles are small responsibility labels for practical repo work:

- Reader: gathers local context and repo instructions.
- Editor: makes the focused change.
- Checker: reviews for consistency, public wording, links, and obvious regressions.
- Validator: runs repo-appropriate checks and records what passed or could not be checked.
- Navigator: keeps indexes, maps, and handoffs discoverable.

These roles are optional. Use them when they make the work clearer, and skip them when a small edit does not need ceremony.

### Ground Sites And Landing Reports

A ground site is the target repo where work happens. The target repo remains the source of truth for its own files, tests, configuration, and docs.

Runway work should land with a concise report that names the branch, changed files, validation, risks, and next gate. For public or cross-repo work, the report should also confirm that private material, secrets, and out-of-scope repos were not touched.

### Handoffs, Prompts, And Guardrails

Handoffs keep unfinished work from becoming hidden context. Prompts make common Codex workflows repeatable. Guardrails keep public wording, safe boundaries, evidence, truth labels, and note size from drifting into guesswork or overclaiming.

The kit should prefer short, reusable surfaces over large process documents.

### Future Skills

Future skills may become a reusable workflow surface for Codex-assisted repo work. For now, skills should be described only as draft or future-facing patterns unless a specific finished skill exists in a repo that documents its own installation and use.

## Practical Adoption Order

1. Start with a small mission brief for the next actual task.
2. Add Atlas Memory when the repo needs durable continuity across sessions.
3. Add prompts only for workflows that repeat.
4. Add guardrails where future sessions could cause avoidable damage.
5. Use ATC/Council only when the work is large enough to benefit from role separation.
6. Use Review Council Planning + Drafting when the desired output is a larger plan, spec, roadmap, doctrine note, or module direction.
7. Document future skills as drafts until they are real, tested, and locally supported.
