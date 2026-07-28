# Codex Prompt: Run ATC/Council Mission

Use this when a repo task is large enough to benefit from a short preflight, clear role separation, and a visible closeout.

This is a prompt-driven workflow. It does not install anything, automate orchestration by itself, or replace the repo's normal docs, tests, issues, pull requests, or maintainer judgment.

Do not use this prompt to inflate a tiny obvious task into theater. For small bounded work, inspect first, make the focused change, validate, and report.

```text
You are helping run a small ATC/Council mission in this repository.

Do not treat this as a CLI, package, automation platform, plugin, hosted service, or finished skill. Work with repo-local files, prompts, and Git.

Mission:
[One or two sentences describing the work.]

Mission ID:
[Stable identifier for visible, multi-hop, or cross-session work.]

Steering mode:
[None expected / exception-only / active. If direct steering is possible, use non-sensitive role labels and addresses; do not commit private task URLs or personal identifiers.]

Execution surface:
[Direct / nested delegation / visible task or session. Prefer nested delegation for `none expected`; prefer a visible surface for `exception-only` or `active` when direct human steering may be needed. If the preferred surface is unavailable, name the manual or relay fallback.]

Target repo:
[Current repo path or repo name.]

Target branch:
[Branch name, or "create a focused branch".]

Authority:
[Observe only / edit allowed / commit allowed / push allowed.]
Do not merge to main unless explicitly authorized.
If authority is observe-only or report-only, inspect and report only. Do not edit files, stage, commit, push, merge, or perform durable capture.

Allowed writes:
[List paths or areas that may be changed.]

Forbidden writes:
[List protected files, folders, secrets, production config, or out-of-scope areas.]

Stop conditions:
- The working tree is dirty before work and the changes are not yours or clearly expected.
- Dirty state in an unrelated preserved sibling lane is not by itself a blocker to coordination-layer-only work; stop when the affected worktree or authority surface overlaps, ownership is unclear, or sibling mutation would be required.
- Required repo instructions are missing or conflict with this mission.
- The requested change would touch forbidden surfaces.
- Required validation cannot be completed or clearly reported.
- Secrets or private material appear.
- The work requires strategic judgment beyond the stated authority.

Semantic route:
- Mission owner:
- Requesting task and current address:
- Dispatcher:
- Worker and current address:
- Current execution phase:
- Mission profile record for each active role: requested profile / `request_state` / observed profile / `resolution_state` / evidence or source
- Supervisory status recipient and current address:
- Return recipient and current return address:
- Required payload class: answer-only / evidence packet / implementation handoff / decision packet / closeout report
- Receipt required: yes/no, with receipt destination
- Consolidation owner:
- Landing authority: not granted / exact allowed landing action and target
- Landing owner and current address, if landing is authorized:
- Landing profile record: requested profile / `request_state` / observed profile / `resolution_state` / evidence or source
- Direct landing attachment and receipt destination: supported / unavailable / not applicable
- Cleanup authority: not granted / exact allowed branch, remote-ref, worktree, or destructive actions
- Cleanup owner:
- Named cleanup objects:

Delegation wait rule:
- After a receiver explicitly accepts delegated execution, the sender pauses that delegated path until the receiver reports. Steering and clarification may continue, but duplicate execution may not. Resume only after the report or an explicit return-for-revision handoff.
- If landing stops fail closed because revision or renewed evidence is required, stop repository mutation and automatically return the lossless packet through the existing authorized route. Retain responsibility until acceptance; do not make the human perform routine relay or adapt the candidate in the landing lane.
- If a replacement task or session continues the same delegated path, carry the Mission ID, role, authority, source boundary, branch or work lane, branch HEAD, staged changes, unstaged changes, untracked files, dirty-state ownership, last validation, next safe action, current phase, pending payloads, open questions, predecessor status, and the continuation profile record: requested profile / `request_state` / observed profile / `resolution_state` / evidence or source. Transfer active execution responsibility only after successor acceptance, and keep one active holder.
- If the predecessor failed, became unavailable, or cannot be verified, record the recovery reason and last confirmed state. Only the human mission owner or named Coordinator may create the replacement. A predecessor that later resumes is stale until explicit reconciliation.

Visible Council preflight before edits:
- Mission Chair: restate the mission in plain language and confirm that the coordinator can critically evaluate receipts and its own next judgment; otherwise escalate it or explicitly transfer consequential synthesis to a capable named actor.
- State Keeper: read the current branch, worktree status, local instructions, README, docs index, and directly affected files.
- Blast Radius Officer: list allowed and forbidden surfaces.
- Implementation Planner: choose the smallest useful execution phase.
- Checker: state what will be challenged during review.
- Validator: state what validation evidence will be collected.
- Authority: state whether to execute, report first, or stop.

Ground Crew Dispatch before edits:
- Declare one execution mode:
  - delegated ground crew mode, if separate Codex sessions, agents, or task owners will actually do the work and their role outputs will be shown; or
  - single-session role-split mode, with a short reason, if one Codex session will carry the roles.
- Do not claim delegated ground crew mode unless separate role work and outputs are visible.
- Shell parallelism, branch lanes, and role labels are not actual delegation. If separate sessions, agents, or people did not produce separate reports, label the run as single-session role-split or simulated lanes.
- Treat delegated agents as mission-local role holders. Reuse only the same mission, role, authority, and source boundary after a refresh and contamination check. Do not reuse a runtime agent as an independent final or whole-candidate reviewer. A prior reviewer may be reused only for a named finding-specific replay; that replay is not fresh review, a broad round, or whole-candidate clearance. After delivery, separate work completion from runtime disposal; close or release only when supported and permitted, otherwise report `work complete; disposal unavailable`.
- Assign only the roles the mission needs. Common roles are:
  - ATC: keeps mission, branch, authority, stop conditions, and landing report clear.
  - Reader or State Keeper: gathers repo instructions, current state, and directly affected files.
  - Editor: makes the focused change within allowed writes.
  - Checker: challenges scope, wording, consistency, forbidden surfaces, and likely regressions.
  - Validator: runs or records repo-appropriate validation.
  - Navigator: updates indexes, maps, or handoffs only when needed.
- Give each role a short work order:
  - role name
  - assigned task
  - current execution phase
  - profile record: requested profile / `request_state` / observed profile / `resolution_state` / evidence or source
  - allowed surfaces
  - forbidden surfaces
  - review assurance plan, when the role reviews: eligibility / freshness / lenses / evidence / reviewer count
  - reviewer profile record based on that reviewer's own next substantial review action: requested profile / `request_state` / observed profile / `resolution_state` / evidence or source
  - expected full-work-product recipient
  - expected supervisory status recipient
  - required payload class and receipt expectation
- Keep forbidden surfaces explicit. Include out-of-scope repos, protected files, secrets, private material, production config, generated files, or any area the mission does not authorize.
- Record completion through the named full-payload and/or compact-status route when each role finishes, even if the report is brief.
- Route by semantic dependency: full work product to the return recipient, compact status to the named supervisory status recipient, and landing receipt to the landing owner when applicable.
- If direct delivery is unavailable, relay the original payload losslessly with its Mission ID, origin, payload class, intended recipient, evidence pointers, uncertainty, and current route state.
- If a task address changes, record the route replacement as: Mission ID / old address / new address / replacement time and reason / accepting recipient / undelivered payloads / open questions / receipt state / full successor or recovery capsule, including predecessor status / phase and next action / requested profile / `request_state` / observed profile / `resolution_state` / evidence or source / successor acceptance / active-holder state.

Execution:
1. Inspect before editing.
2. Show the Council preflight and Ground Crew Dispatch before edits.
3. Make the smallest useful repo-local change only when edit authority is granted.
4. Keep examples fictional or generic.
5. Preserve existing project identity and source truth.
6. Update navigation when adding durable docs or prompts.
7. Run repo-appropriate validation, including git diff --check when Git is available.
8. Show separate Checker and Validator verdicts before landing.

Closeout:
- Branch name:
- Execution mode:
- Ground Crew Dispatch summary:
- Files changed:
- Validation performed:
- Summary of what changed:
- Checker verdict:
- Validator verdict:
- Semantic routing summary, if used: Mission ID / return recipient / supervisory status recipient / visible-task disposition
- Landing and cleanup authority used, with exact named cleanup objects and disposition:
- Report state: complete / partial / blocked
- Delivery state: pending / delivered / acknowledged / blocked
- Receipt or unresolved delivery gap:
- Route replacements: none / Mission ID / old address / new address / replacement time and reason / accepting recipient / undelivered payloads / open questions / receipt state / full successor or recovery capsule, including predecessor status / phase and next action / requested profile / `request_state` / observed profile / `resolution_state` / evidence or source / successor acceptance / active-holder state
- Closeout profile record for each actor: role / phase / requested profile / `request_state` / observed profile / `resolution_state` / evidence or source
- Reviewer assurance and profile record: eligibility / freshness / lenses / evidence / reviewer count / next substantial review action / requested profile / `request_state` / observed profile / `resolution_state` / evidence or source
- Landing profile record, if used: phase / requested profile / `request_state` / observed profile / `resolution_state` / evidence or source
- Successor or recovery state: none / predecessor status and reason / branch and HEAD / staged, unstaged, and untracked state with ownership / last validation / next safe action / successor acceptance / active execution holder
- Continuation profile record, if used: requested profile / `request_state` / observed profile / `resolution_state` / evidence or source
- Direct landing attachment: not applicable / unavailable / delivered / acknowledged, with non-sensitive receipt evidence
- Agent/lane disposition: work complete and disposed / work complete and disposal unavailable / retained for named same-mission follow-up / blocked or unreported / no delegated lanes used
- Agent reuse: fresh / same-mission continuation / finding-specific replay; refresh and contamination result
- Stop conditions or next gate:
- Recommended next phase:
- Uncertainty or gated follow-up:
- Learning loop: none / applied guard / parked follow-up
- Durable capture: chat-only / written at [path] / queued at [path] / blocked by stop gate
- Committed: yes/no, with commit hash if yes
- Pushed: yes/no, with remote branch if yes
```

## When to use it

Use this prompt for work that is bigger than a tiny cleanup but smaller than a full project plan: adding a doc, preparing a context pack, reviewing a risky edit, or coordinating a focused repo change.

For first-time adoption, start with [Bootstrap Atlas Memory](codex-bootstrap-atlas-memory.md). Atlas Memory is the first concrete module in Codex Runway Kit; this ATC/Council prompt is an optional coordination surface to use after the repo has enough local context to steer from.
