# Codex Runway Kit

Codex Runway Kit is the public umbrella for reusable repo-local workflows that help humans and Codex start, steer, hand off, and review repository work.

It is intentionally modest: Markdown files, Git branches, clear prompts, practical roles, and validation notes. It is not a CLI, package, plugin, hosted service, or production platform.

## How the pieces fit

### Atlas Memory

Atlas Memory is the first module and current foundation of the kit. It gives a repository durable continuity surfaces:

- `AGENTS.md` for local operating rules.
- `docs/_index.md` for durable documentation navigation.
- `Atlas/00-Start Here.md` for a fast restart map.
- `session/Next session handoff.md` for current handoff context.
- `queue/00-work-queue.md` for active and parked work.
- `evidence/` when decisions or risky changes need support.
- `prompts/` for repeatable Codex workflows.

Atlas Memory should remain a component inside the kit, not the entire public identity of the repo.

### ATC/Council Workflow

ATC/Council is an optional coordination pattern for larger Codex-assisted runs.

- ATC keeps the mission, scope, authority, stop conditions, and landing report visible.
- Council separates responsibilities so a run can include editing, checking, validation, and recommendation without blurring those jobs together.
- The workflow can be used by one person, one Codex session, or several coordinated sessions.

This is a documentation and prompting pattern. It does not automate orchestration by itself.

### Ground Crew Roles

Ground crew roles are small responsibility labels for practical repo work:

- Reader: gathers local context and repo instructions.
- Editor: makes the focused change.
- Checker: reviews for consistency, public wording, links, and obvious regressions.
- Validator: runs repo-appropriate checks and records what passed or could not be checked.
- Navigator: keeps indexes, maps, and handoffs discoverable.

These roles are optional. Use them when they make the work clearer, and skip them when a small edit does not need ceremony.

### Handoffs, Prompts, And Guardrails

Handoffs keep unfinished work from becoming hidden context. Prompts make common Codex workflows repeatable. Guardrails keep public wording, safe boundaries, evidence, truth labels, and note size from drifting into guesswork or overclaiming.

The kit should prefer short, reusable surfaces over large process documents.

### Future Skills

Future skills may become a reusable workflow surface for Codex-assisted repo work. For now, skills should be described only as draft or future-facing patterns unless a specific finished skill exists in a repo that documents its own installation and use.

## Practical Adoption Order

1. Start with Atlas Memory.
2. Add prompts only for workflows that repeat.
3. Add guardrails where future sessions could cause avoidable damage.
4. Use ATC/Council only when the work is large enough to benefit from role separation.
5. Document future skills as drafts until they are real, tested, and locally supported.
