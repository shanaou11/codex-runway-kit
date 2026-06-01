# Runway Operations

Codex Runway Kit treats repository work as a bounded mission: brief it, read local law, work at the ground site, check it, validate it, and leave a landing report.

This is a public documentation pattern. It does not require access to any private atlas, orchestration server, plugin, package, or CLI.

## Mission briefs

A mission brief is the smallest useful instruction for a Codex-assisted run.

Good briefs usually include:

- Mission: what outcome is being requested.
- Target repo: the repo where work should happen.
- Branch expectation: whether to create a branch, reuse one, commit, push, or stop before publishing.
- Allowed writes: files or areas that may be edited.
- Forbidden writes: protected paths, secrets, production config, private material, or out-of-scope repos.
- Stop conditions: events that should make Codex stop and report.
- Validation: checks that should be run or explicitly marked unavailable.
- Landing report: what the final report must include.

The brief does not replace the target repo's own instructions. It narrows the task and makes authority visible.

## Momentum and escalation

Runway work should not stall on ordinary tasks.

- For small, clearly bounded work, inspect the local rules and affected files, then proceed directly.
- Ask clarifying questions when the answer would materially change safety, authority, scope, or outcome.
- If the request is broad, choose the smallest safe next step that makes useful progress, do it, and report what remains.
- After a bounded report or plan is approved, proceed without re-asking for the same approval unless the state changed or a stop condition appeared.

Small tasks do not need ceremony. Escalate on consequence, not on discomfort.

For the fuller public rule set, see [Momentum and Escalation](09-momentum-and-escalation.md).

## Local law

Local law is the target repo's operating guidance. In this kit, `AGENTS.md` is the primary local-law surface for Codex and other agents.

Use `AGENTS.md` for stable rules such as:

- Read-first files.
- Public wording constraints.
- Protected or high-care areas.
- Branch, commit, push, and merge rules.
- Required validation.
- How to update handoffs, queues, or indexes.

Local law should stay practical. One-time task notes belong in a mission brief, queue, or handoff rather than becoming permanent repo rules.

## Atlas Memory

Atlas Memory is the first concrete module inside the broader Runway Kit. It keeps continuity close to the repo through plain Markdown:

- `AGENTS.md` for local law.
- `docs/_index.md` for durable documentation navigation.
- `Atlas/00-Start Here.md` for fast restart routing.
- `session/Next session handoff.md` for current handoff context.
- `queue/00-work-queue.md` for active and parked work.
- `evidence/` when claims or decisions need support.
- `prompts/` for repeatable Codex workflows.

Atlas Memory is a routing and continuity layer. It should summarize and point to source truth rather than copying large source material into new places.

## ATC/Council review

ATC/Council is a lightweight review pattern for missions that are large, ambiguous, cross-surface, or risky enough to benefit from visible role separation.

Common roles:

- ATC or Mission Chair: keeps the mission, authority, stop conditions, and landing report clear.
- State Keeper or Reader: reads current repo state and local law before edits.
- Blast Radius Officer: names allowed and forbidden surfaces.
- Editor: makes the focused change.
- Checker: challenges scope, wording, consistency, and overreach.
- Validator: runs or records repo-appropriate checks.
- Navigator: updates indexes, maps, and handoffs when needed.

Small edits do not need ceremony. Use Council language when it clarifies responsibility, not as theater.

### Review Council planning and drafting

When the expected output is a durable plan, spec, roadmap, doctrine note, or module direction, use Review Council as a planning pattern rather than only an edit/check/validate pattern.

The useful move is non-linear work: one lane can start the artifact skeleton while other lanes inspect current state, source truth, structure, sequencing, risks, and validation. The coordinator integrates reports as they arrive instead of waiting for every discovery pass to finish before drafting begins.

Common planning lanes:

- Vision: goal, user questions, success shape, and non-goals.
- Current state: existing docs, implementation, strengths, gaps, and overclaims.
- Source truth: supported claims, assumptions, missing evidence, and uncertainty.
- Structure: document shape, information architecture, or user journey.
- Sequencing: phases, independent slices, risks, and stop gates.
- Drafting: artifact skeleton and integration notes.
- Checker: overreach, contradictions, and public/private boundary issues.
- Validator: repo-appropriate validation and closeout evidence.

Label execution honestly. Actual delegated work means separate sessions, agents, or people produced separate reports. Manually coordinated sessions should say so. A single Codex session can still use role-split thinking, but it should not claim actual delegation. Shell parallelism, branch lanes, and role labels are not actual delegation.

Delegated lanes should also be cleaned up intentionally. When a delegated session or agent has reported and no explicit follow-up is queued, close or release that lane after capturing its output. Leave a lane idle only with a named reason such as an expected follow-up, integration pause, file arrival, or active branch/artifact. Final synthesis should state agent or lane cleanup status.

The reusable public prompt is [Codex Prompt: Run Review Council Planning + Drafting](../prompts/codex-run-review-council-planning-drafting.md).

## Ground sites and source truth

A ground site is the target repo where the actual work lives. When a mission spans steering notes and a target repo, the target repo remains the source of truth for its own code, docs, tests, configuration, and local rules.

Reusable runway practice should:

- Edit only the authorized ground site.
- Keep source truth in the target repo.
- Summarize and link rather than duplicating large source material.
- Avoid moving private or sensitive context into public docs.
- Report uncertainty instead of inventing repo facts.

## Validation and landing reports

Validation should match the repo and risk level. For docs-only work, lightweight validation may be enough: `git status`, final diff review, `git diff --check`, and any available Markdown checks. For code or higher-risk work, use the repo's tests, linters, builds, or manual checks.

Non-trivial work should also include a closeout learning loop. Before calling the run done, ask whether the work revealed a repeatable failure mode, delay, confusion, or risk. Add the smallest reasonable prevention when it fits the task, such as a focused check, clearer instruction, template note, validation step, or parked follow-up. If no useful guard was found, say that briefly instead of inventing extra process.

For stronger closeout discipline, use two visible final-report lines:

- `Learning loop: none`, `Learning loop: applied guard`, or `Learning loop: parked follow-up`.
- `Durable capture: chat-only`, `Durable capture: written at [path]`, `Durable capture: queued at [path]`, or `Durable capture: blocked by stop gate`.

Use `none` only when the run did not reveal a repeatable failure mode, delay, confusion, or risk. Use `applied guard` when the prevention was added in the same run. Use `parked follow-up` when the prevention is too large or needs a later decision.

Durable capture should stay small and repo-local. Use an existing owner surface such as local law, docs, Atlas maps, the next-session handoff, the work queue, a template, or a prompt. Do not create a new memory surface by default. Do not capture when the run is report-only, the owner surface is unclear, the material is sensitive or private, or the capture would broaden the repo's intent.

A landing report should make the end state easy to review:

- Run location.
- Target repo.
- Branch.
- Cleanup status for branches, handoffs, delegated lanes, or parked follow-ups.
- Commit hash, if committed.
- Push status, if pushed.
- Files changed.
- Docs added, if any.
- Validation performed.
- Boundary checks and anything intentionally not changed.
- Learning loop and durable capture status for non-trivial work.
- Remaining risks, unknowns, or next gates.

The landing report is not a replacement for a pull request, release note, or issue. It is the compact handoff that lets the next reader see what happened.

## Current status

Real today:

- Public docs, templates, and prompts.
- A minimal Atlas Memory starter layout.
- A reusable ATC/Council prompt for bounded missions.
- A reusable Review Council Planning + Drafting prompt for larger artifact-producing work.
- Public doctrine for local law, mission briefs, ground sites, validation, and landing reports.

Not claimed today:

- A finished CLI, package, plugin, automation platform, hosted service, or production orchestration product.
- Automatic cross-repo execution.
- External memory, vector memory, or RAG.
- Access to any external non-public workflow repository.
