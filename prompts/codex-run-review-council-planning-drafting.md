# Codex Prompt: Run Review Council Planning + Drafting

Use this when the requested output is a larger plan, spec, roadmap, doctrine note, module direction, or other durable artifact that benefits from parallel thinking.

This is a prompt-driven workflow. It does not install anything, automate orchestration by itself, or promise that separate agents are available. Label the execution truthfully as actual delegated sessions, manually coordinated sessions, or single-session role-split.

Do not use this prompt for tiny obvious edits.

```text
You are helping run a Review Council Planning + Drafting mission in this repository.

Do not treat this as a CLI, package, automation platform, plugin, hosted service, or finished skill. Work with repo-local files, prompts, and Git.

Mission:
[One or two sentences describing the desired plan, spec, roadmap, doctrine note, or module direction.]

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
[List protected files, folders, secrets, production config, private material, or out-of-scope areas.]

Stop conditions:
- The working tree is dirty before work and the changes are not yours or clearly expected.
- Required repo instructions are missing or conflict with this mission.
- The requested work would touch forbidden surfaces.
- The artifact would require unsupported claims or private context.
- Required validation cannot be completed or clearly reported.
- Secrets or private material appear.
- The work requires strategic judgment beyond the stated authority.

Semantic route:
- Mission owner:
- Requesting task and current address:
- Dispatcher:
- Worker or lane addresses:
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

Council truth labels:
- Council mode: Light Council / Full Council / Parallel Planning + Drafting / single-session role-split.
- Execution shape: actual delegated sessions / manually coordinated sessions / single-session role-split.
- Do not claim actual delegation unless separate sessions, agents, or people produced separate reports.
- Shell parallelism, branch lanes, and role labels are not actual delegation.
- Delegated agents are mission-local role holders. Reuse only the same mission, role, authority, and source boundary after a refresh and contamination check. After report capture, separate work completion from runtime disposal; close or release only when supported and permitted, otherwise report `work complete; disposal unavailable`.

Parallel lanes:
- Vision lane: define the goal, user questions, success shape, and non-goals.
- Current-state lane: inspect local law, existing docs, current strengths, gaps, and overclaims.
- Source-truth lane: separate supported claims from assumptions, unknowns, and claims needing evidence.
- Structure lane: propose the artifact structure, information architecture, or user journey.
- Sequencing lane: turn the direction into phases, independent slices, risks, and stop gates.
- Draft lane: start the artifact skeleton while other lanes investigate.
- Checker lane: challenge overreach, contradictions, public/private boundary issues, and role confusion.
- Validator lane: define and run or record repo-appropriate validation.

Coordinator duties:
1. Inspect local law before assigning lanes.
2. Give each lane a scope, allowed surfaces, forbidden surfaces, and report format.
3. Keep the draft moving while lane reports arrive.
4. Integrate lane findings rather than restarting the artifact from zero.
5. Preserve source truth in the target repo.
6. Label uncertainty instead of inventing facts.
7. Route each full lane report to its semantic return recipient and send only the required compact status to the named supervisory status recipient.
8. If direct delivery is unavailable, relay the original payload losslessly with a separate header containing Mission ID, origin, payload class, destination, and current route state.
9. Record every route replacement as: Mission ID / old address / new address / replacement time and reason / accepting recipient / undelivered payloads / open questions / receipt state.

Lane report format:
- Mission ID:
- Payload class:
- Intended return recipient:
- Supervisory status recipient:
- Report state: complete / partial / blocked
- Delivery state: pending / delivered / acknowledged / blocked
- Receipt state or unresolved delivery gap:
- Strong findings:
- Pushback or caution:
- Recommendation:
- Evidence paths:
- Confidence / uncertainty:

Coordinator synthesis:
- Strong agreement:
- Material disagreement or uncertainty:
- Recommendation:
- Smallest safe next action:
- Validation or documentation impact:

Closeout:
- Branch name:
- Council mode:
- Execution shape:
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

Use this prompt when the thinking itself needs multiple lenses and the output should become a durable artifact.

For bounded repo missions with a smaller edit/check/validate loop, use [Codex Prompt: Run ATC/Council Mission](codex-run-atc-council-mission.md).
