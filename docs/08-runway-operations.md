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

A landing report should make the end state easy to review:

- Run location.
- Target repo.
- Branch.
- Commit hash, if committed.
- Push status, if pushed.
- Files changed.
- Docs added, if any.
- Validation performed.
- Boundary checks and anything intentionally not changed.
- Remaining risks, unknowns, or next gates.

The landing report is not a replacement for a pull request, release note, or issue. It is the compact handoff that lets the next reader see what happened.

## Current status

Real today:

- Public docs, templates, and prompts.
- A minimal Atlas Memory starter layout.
- A reusable ATC/Council prompt for bounded missions.
- Public doctrine for local law, mission briefs, ground sites, validation, and landing reports.

Not claimed today:

- A finished CLI, package, plugin, automation platform, hosted service, or production orchestration product.
- Automatic cross-repo execution.
- External memory, vector memory, or RAG.
- Access to any external non-public workflow repository.
