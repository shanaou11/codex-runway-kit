# Codex Prompt: Bootstrap Atlas Memory

Paste this into Codex while working inside the repository where you want to add Atlas Memory.

```text
You are helping add Atlas Memory to this repository as a prompt-driven Markdown continuity framework.

Do not treat this as a CLI, package, automation platform, installer, or external memory service. Work only with repo-local Markdown and Git.

Goal:
Inspect this repo, then create or adapt a small Atlas Memory scaffold so future humans and Codex sessions can restart work with less context loss.

Required behavior:
1. Inspect the repository before editing.
   - Confirm the current branch and worktree status.
   - List the existing top-level files and folders.
   - Read existing guidance before changing it, especially `AGENTS.md`, `README.md`, `docs/`, `Atlas/`, `session/`, and `queue/` if present.
   - Detect whether this appears to be an empty/new repo or an existing/mature repo.

2. Preserve existing content.
   - Do not overwrite `AGENTS.md`, `README.md`, `docs/`, `Atlas/`, `session/`, or `queue/` blindly.
   - If a file exists, merge in the smallest useful Atlas Memory additions while preserving project identity and useful content.
   - Update `README.md` only if appropriate, and do not replace the project's existing purpose, usage, or status.

3. Create missing Atlas Memory surfaces from the minimal public shape:
   - `AGENTS.md`
   - `README.md`, only when appropriate
   - `docs/_index.md`
   - `Atlas/00-Start Here.md`
   - `session/Next session handoff.md`
   - `queue/00-work-queue.md`

4. Adapt content to this repo using only observable repo evidence.
   - Use existing files, package metadata, tests, docs, configuration, and Git status as evidence.
   - Mark assumptions as `draft` or `unverified`.
   - Keep wording conservative and practical.
   - Use fictional or generic examples only.
   - Do not mention private/internal examples, client work, or real non-public project names.

5. Evidence folder:
   - Add `evidence/` only when useful for this repo right now, such as for decision notes, investigation output, migration notes, reproduction details, or validation summaries.
   - If you do not add it, say why.

6. Git workflow:
   - Create or use a focused branch for the changes unless the repo instructions say otherwise.
   - Run basic validation appropriate to the repo. At minimum, check Git status, obvious Markdown links, and `git diff --check`.
   - Commit and push only if this repo's workflow allows it or I explicitly asked you to commit and push.

Atlas Memory file roles:
- `AGENTS.md`: stable operating rules for Codex and other agents.
- `README.md`: project front door; preserve the existing project identity.
- `docs/_index.md`: navigation for durable docs.
- `Atlas/00-Start Here.md`: fast restart map.
- `session/Next session handoff.md`: current handoff for the next session.
- `queue/00-work-queue.md`: active, blocked, and later work.
- `evidence/`: optional support for decisions or claims that need evidence.

Relay back using this format:
- Branch name:
- Files created:
- Files modified:
- Existing files preserved:
- Assumptions made:
- Validation run:
- Recommended next review points:
- Committed: yes/no, with commit hash if yes
- Pushed: yes/no, with branch or remote if yes
- Evidence folder: added/not added, with reason
```
