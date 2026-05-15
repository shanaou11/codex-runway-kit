# Atlas Contract

Atlas Memory is the first module in Codex Runway Kit. It is a repo-local continuity convention that keeps the important context for humans and Codex in Markdown files that live in the same Git history as the work.

It is meant to help future sessions restart cleanly. It is not the whole Runway Kit: mission briefs, local law, ATC/Council review, validation, and landing reports are broader runway practices around this continuity layer. Atlas Memory is not meant to make decisions automatically or replace the source files, tests, issues, pull requests, or normal project docs.

## Public contract

An Atlas-enabled repo should make these things easy to find:

- The agent operating rules.
- The main project description.
- A documentation index.
- A start-here map for the repo.
- A next-session handoff.
- A visible work queue.
- Evidence for decisions or changes that need support.
- Reusable prompts for common Codex workflows.

## Mandatory surfaces

The minimal public shape is:

```text
AGENTS.md
README.md
docs/_index.md
Atlas/00-Start Here.md
session/Next session handoff.md
queue/00-work-queue.md
prompts/
```

Use `evidence/` when a change needs supporting notes, investigation output, reproduction details, screenshots, logs, or decision records. A repo may add more docs, indexes, or maps as needed.

## Truth hierarchy

When files disagree, prefer truth in this order:

1. Source code, tests, configuration, and current generated outputs.
2. `AGENTS.md` for local operating rules.
3. Canonical project docs under `docs/`.
4. Atlas maps and session handoffs.
5. Queue notes, scratch notes, and older observations.

Atlas maps route readers to truth. They should not silently override canonical files.

## Update expectations

- Update the smallest useful surface that will help the next reader.
- Keep handoffs current when a session ends with unresolved work.
- Promote repeated lessons into durable docs only after they prove useful.
- Update `docs/_index.md` when adding or moving durable docs.
- Leave clear uncertainty labels when something is inferred, stale, draft, or unverified.

## Boundaries and non-goals

Atlas Memory is not:

- Vector memory, RAG, or chatbot memory.
- A replacement for Git, tests, issues, pull requests, or project documentation.
- An automation system.
- A production tool or CLI.
- A claim about agent identity, consciousness, or personhood.

Atlas Memory should stay boring on purpose: plain files, clear labels, and enough continuity to keep work coherent.
