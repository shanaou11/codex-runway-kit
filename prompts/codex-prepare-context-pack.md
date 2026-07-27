# Codex Prompt: Prepare Context Pack

Use this when handing work to another Codex session, reviewer, or human maintainer.

```text
Prepare a concise context pack for the current repo work.

Include:
- task goal
- Mission ID, role, and work lane when continuation or recovery is involved
- current branch and HEAD
- staged changes, unstaged changes, untracked files, and their ownership
- changed files or expected change areas
- mission profile record: current phase / requested profile / `request_state` / observed profile / `resolution_state` / evidence or source
- reviewer profile record for each reviewer: next substantial review action / requested profile / `request_state` / observed profile / `resolution_state` / evidence or source
- landing profile record when landing is authorized: next substantial landing action / requested profile / `request_state` / observed profile / `resolution_state` / evidence or source
- current execution address, predecessor status, and replacement reason when a successor is needed
- active execution holder and successor acceptance state
- continuation profile record when a successor is needed: requested profile / `request_state` / observed profile / `resolution_state` / evidence or source
- read-first files
- active decisions and open questions
- relevant evidence and last validation
- safe boundaries or files that need extra care
- return recipient, supervisory status recipient, and landing recipient when semantic routing is used
- direct landing attachment and receipt state when supported and authorized
- next safe action

Use only repo evidence. Mark assumptions as unverified. Only the human mission owner or named Coordinator may create a failed-task replacement, and a later-resuming predecessor stays stale until explicit reconciliation. Keep sensitive task URLs and identifiers out of durable repo notes. Keep the pack short enough to paste into a new session.
```
