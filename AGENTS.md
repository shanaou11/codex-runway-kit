# AGENTS.md

This file is the operating guide for Codex or any other agent working in this repository.

## Read first

Before making changes, read the compact universal entry set:

1. `README.md`
2. `docs/_index.md`
3. Any file directly affected by the requested change

Then load only the owner surface needed for the task:

- broader public framing or positioning: `docs/07-codex-runway-kit.md`
- mission briefs, local law, context loading, validation, or landing reports: `docs/08-runway-operations.md`
- Atlas Memory contract or scaffold behavior: `docs/00-atlas-contract.md`
- navigation or restart routing: `Atlas/00-Start Here.md`
- continuation, landing, cleanup, or unresolved prior state: `session/Next session handoff.md`

For template changes, also inspect the matching files under `templates/minimal/`.

## Public wording

This repository is public. Keep language clear, practical, and conservative.

- Do not overclaim what Codex Runway Kit or Atlas Memory does.
- Do not describe it as production software, a CLI, a package, a plugin, a platform, RAG, vector memory, chatbot memory, or agent consciousness.
- Describe skills only as future or draft reusable workflow surfaces unless a finished local skill exists and documents its own installation and use.
- Do not write manifesto-style copy.
- Prefer concise examples that a stranger can understand quickly.
- Frame Atlas Memory as the first module or continuity layer inside the broader Runway Kit, not as the whole product.

## Examples

Use only fictional or generic examples.

Do not mention non-public repositories, organizations, projects, examples, or real non-public project names.

## Documentation rules

- Keep Markdown thin and extensible.
- Link new durable docs from `docs/_index.md`.
- Keep Atlas maps as routing surfaces, not full duplicates of canonical docs.
- Mark uncertainty instead of converting guesses into facts.
- Use truth and freshness labels from `docs/02-truth-and-freshness-labels.md` when a note's status matters.

## Execution stance

- Prefer the smallest safe next step that creates useful progress.
- Keep session-loaded instructions, checked-out files, and fetched remote-tracking authority distinct. If a fetch or live-main comparison shows that `AGENTS.md` or another relevant operating surface differs on the current default branch, reread that current-branch version before setting/runtime advice or subsequent implementation. A fetch does not refresh the worktree.
- Do not ask clarifying questions for every small bounded task when local law and the requested outcome are already clear.
- Ask clarifying questions when the answer would materially change authority, safety, scope, or outcome.
- If a request is broad, choose a bounded first pass, do it, and report what remains.
- If a bounded report or plan has already been approved, proceed without asking for the same approval again unless the state changed or a stop condition appeared.
- Small tasks do not need ceremony.
- Keep universal starter context small. New useful docs remain conditional by default; do not add a mandatory starter file merely because it is important.
- Follow `docs/09-momentum-and-escalation.md` for task-setting and capability-improvement advice. Classify settings by each actor's next substantial action and reassess at material phase changes; one role's difficulty does not set another's profile. Use visible labels, do not claim an unexposed setting, continue when sufficient, pause only for a useful escalation, and never interrupt an active role for a downgrade.
- Within an authorized mission, prefer bounded nested delegation for separable specialist, checker, and validator work before replacing the coordinator. When the runtime supports nested agents, spawning inside the mission and selecting an exposed child profile do not require approval for every spawn; each child remains inside the same authority and local law, while child-led recursion remains separately gated. Creating a new top-level task remains an explicit user-requested action.
- Propose a capability change only for material or recurring friction, reduced confidence, a blocker, substantial repeated effort, or reusable validation. State the exact remedy, scope, changed state, risk, rollback, fallback, and permission requested; do not install, configure, authenticate, upgrade, expand permissions, or add dependencies without the authority required by local law.
- Keep Codex Security and other security review proportional. Ordinary UI, docs, business-rule, cosmetic admin, and low-risk workflow work uses normal implementation and validation. Meaningful authentication, authorization, permission, trust-boundary, secret-handling, custody, or external attack-surface changes receive a focused security diff review, normally as a finishing check; standard and deep scans require an explicit request or separately approved security justification.
- A message, delegation, relay, route replacement, or successor-task handoff changes only the conversation route. It must declare direct/local canonical attachment, an existing named worktree, or explicitly authorized worktree creation and does not itself create, select, move, clean, or remove a Git lane. Stop before repository work when the opened cwd does not match the declared attachment.

## Cross-Repo Orchestration / Runway Rules

This repo can participate in autonomous cross-repo Codex orchestration through an external orchestration controller or a local orchestration environment.

- Repo-local `AGENTS.md` rules remain authoritative for this repository's boundaries, source truth, and protected areas.
- A mission brief may narrow work for a run, but it does not silently replace repo-local law.
- Source truth stays in this repo. Cross-repo reports should summarize and point to local docs rather than duplicate them.
- Target repos, or ground sites, remain the source of truth for their own code, docs, tests, configuration, and local rules.
- Active, dirty, or overlapping sibling lanes are coordination inputs, not an all-lanes-clear gate. Preserve them unchanged and use a separately authorized safe lane; block only unsafe mutation of the selected checkout or an exact prohibited action, then reconcile conflicts during landing.
- The requested autonomy level controls what Codex may do here. Report-only mode must not edit this repo.
- Level 1 low-risk docs hygiene is allowed only when the prompt explicitly selects that level.
- Higher-risk documentation refactors require checker and validator gates plus explicit authorization where local rules require it.
- Protected areas require explicit authorization, including policy-defining docs, public positioning changes, prompt contracts, and any material that would broaden or reinterpret repo intent.

## Git workflow

For repo changes:

1. Confirm the current branch and worktree status.
2. Create or switch to a purpose-named branch before editing.
3. Make focused changes.
4. Run basic validation, including `git diff --check`.
5. For non-trivial work, include a closeout learning loop: note any repeatable failure mode, confusion, or risk discovered; add the smallest reasonable prevention when safe; record a visible follow-up when prevention is too large; or say no useful guard was found.
6. Include `Learning loop: none`, `Learning loop: applied guard`, or `Learning loop: parked follow-up` in the final report for non-trivial work.
7. Include `Durable capture: chat-only`, `Durable capture: written at [path]`, `Durable capture: queued at [path]`, or `Durable capture: blocked by stop gate` in the final report for non-trivial work.
8. Record-only durable capture may happen automatically when a repeatable, actionable, future-relevant lesson, decision, or follow-up has a clear approved owner surface and no stop gate applies. Use the smallest existing surface, such as `docs/`, `Atlas/`, `session/Next session handoff.md`, or `queue/00-work-queue.md`; do not create a new memory surface by default. Recording preserves context and does not approve execution, policy, landing, cleanup, publication, or further mutation.
9. Do not perform durable capture when the run is explicitly report-only/no-write/no-capture, the owner surface is unclear, the material is sensitive or private, or the capture would broaden repo intent.
10. Report cleanup status and avoid leaving unnecessary branch or handoff debt.
11. Commit with a clear message.
12. Push the branch to `origin`.

Do not merge to `main` unless the user explicitly asks.
