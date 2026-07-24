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
- Supervisory status recipient and current address:
- Return recipient and current return address:
- Required payload class: answer-only / evidence packet / implementation handoff / decision packet / closeout report
- Receipt required: yes/no, with receipt destination
- Consolidation owner:
- Landing authority: not granted / exact allowed landing action and target
- Landing owner, if landing is authorized:
- Cleanup authority: not granted / exact allowed branch, remote-ref, worktree, or destructive actions
- Cleanup owner:
- Named cleanup objects:

Delegation wait rule:
- After a receiver explicitly accepts delegated execution, the sender pauses that delegated path until the receiver reports. Steering and clarification may continue, but duplicate execution may not. Resume only after the report or an explicit return-for-revision handoff.

Visible Council preflight before edits:
- Mission Chair: restate the mission in plain language.
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
- Treat delegated agents as mission-local role holders. Reuse only the same mission, role, authority, and source boundary after a refresh and contamination check. After delivery, separate work completion from runtime disposal; close or release only when supported and permitted, otherwise report `work complete; disposal unavailable`.
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
  - allowed surfaces
  - forbidden surfaces
  - expected full-work-product recipient
  - expected supervisory status recipient
  - required payload class and receipt expectation
- Keep forbidden surfaces explicit. Include out-of-scope repos, protected files, secrets, private material, production config, generated files, or any area the mission does not authorize.
- Record completion through the named full-payload and/or compact-status route when each role finishes, even if the report is brief.
- Route by semantic dependency: full work product to the return recipient, compact status to the named supervisory status recipient, and landing receipt to the landing owner when applicable.
- If direct delivery is unavailable, relay the original payload losslessly with its Mission ID, origin, payload class, intended recipient, evidence pointers, uncertainty, and current route state.
- If a task address changes, record the route replacement as: Mission ID / old address / new address / replacement time and reason / accepting recipient / undelivered payloads / open questions / receipt state.

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
- Route replacements: none / Mission ID / old address / new address / replacement time and reason / accepting recipient / undelivered payloads / open questions / receipt state
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
