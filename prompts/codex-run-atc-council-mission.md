# Codex Prompt: Run ATC/Council Mission

Use this when a repo task is large enough to benefit from a short preflight, clear role separation, and a visible closeout.

This is a prompt-driven workflow. It does not install anything, automate orchestration by itself, or replace the repo's normal docs, tests, issues, pull requests, or maintainer judgment.

```text
You are helping run a small ATC/Council mission in this repository.

Do not treat this as a CLI, package, automation platform, plugin, hosted service, or finished skill. Work with repo-local files, prompts, and Git.

Mission:
[One or two sentences describing the work.]

Target repo:
[Current repo path or repo name.]

Target branch:
[Branch name, or "create a focused branch".]

Authority:
[Observe only / edit allowed / commit allowed / push allowed.]
Do not merge to main unless explicitly authorized.

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

Visible Council preflight before edits:
- Mission Chair: restate the mission in plain language.
- State Keeper: read the current branch, worktree status, local instructions, README, docs index, and directly affected files.
- Blast Radius Officer: list allowed and forbidden surfaces.
- Implementation Planner: choose the smallest useful execution phase.
- Checker: state what will be challenged during review.
- Validator: state what validation evidence will be collected.
- Authority: state whether to execute, report first, or stop.

Execution:
1. Inspect before editing.
2. Make the smallest useful repo-local change.
3. Keep examples fictional or generic.
4. Preserve existing project identity and source truth.
5. Update navigation when adding durable docs or prompts.
6. Run repo-appropriate validation, including git diff --check when Git is available.

Closeout:
- Branch name:
- Files changed:
- Validation performed:
- Summary of what changed:
- Checker verdict:
- Validator verdict:
- Stop conditions or next gate:
- Recommended next phase:
- Uncertainty or gated follow-up:
- Committed: yes/no, with commit hash if yes
- Pushed: yes/no, with remote branch if yes
```

## When to use it

Use this prompt for work that is bigger than a tiny cleanup but smaller than a full project plan: adding a doc, preparing a context pack, reviewing a risky edit, or coordinating a focused repo change.

For first-time adoption, start with [Bootstrap Atlas Memory](codex-bootstrap-atlas-memory.md). Atlas Memory is the first concrete module in Codex Runway Kit; this ATC/Council prompt is an optional coordination surface to use after the repo has enough local context to steer from.
