# AGENTS.md

This file is the operating guide for Codex or any other agent working in this repository.

## Read first

Before making changes, read:

1. `README.md`
2. `docs/_index.md`
3. `docs/00-atlas-contract.md`
4. Any file directly affected by the requested change

For template changes, also inspect the matching files under `templates/minimal/`.

## Public wording

This repository is public. Keep language clear, practical, and conservative.

- Do not overclaim what Atlas Memory does.
- Do not describe it as production software, a CLI, a platform, RAG, vector memory, chatbot memory, or agent consciousness.
- Do not write manifesto-style copy.
- Prefer concise examples that a stranger can understand quickly.

## Examples

Use only fictional or generic examples.

Do not mention non-public repositories, client work, or real non-public project names.

## Documentation rules

- Keep Markdown thin and extensible.
- Link new durable docs from `docs/_index.md`.
- Keep Atlas maps as routing surfaces, not full duplicates of canonical docs.
- Mark uncertainty instead of converting guesses into facts.
- Use truth and freshness labels from `docs/02-truth-and-freshness-labels.md` when a note's status matters.

## Cross-Repo Orchestration / Runway Rules

This repo can participate in autonomous cross-repo Codex orchestration through an external orchestration controller or a local orchestration environment.

- Repo-local `AGENTS.md` rules remain authoritative for this repository's boundaries, source truth, and protected areas.
- Source truth stays in this repo. Cross-repo reports should summarize and point to local docs rather than duplicate them.
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
5. Commit with a clear message.
6. Push the branch to `origin`.

Do not merge to `main` unless the user explicitly asks.
