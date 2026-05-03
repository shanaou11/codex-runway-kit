# Variable Rigor

Not every change needs the same amount of Atlas updating. Use the smallest level that keeps the next session coherent.

## Level 1: small edit or hotfix

Use for typo fixes, small doc edits, narrow code fixes, or low-risk updates.

Expected updates:

- Update the touched file.
- Add a queue or handoff note only if follow-up remains.
- Run the smallest relevant validation.

Usually not needed:

- New evidence files.
- New durable docs.
- New `AGENTS.md` rules.

## Level 2: feature or workflow change

Use for new features, changed workflows, new templates, new docs, or changes that affect how people use the repo.

Expected updates:

- Update the canonical doc or template.
- Update `docs/_index.md` if durable docs changed.
- Update `Atlas/00-Start Here.md` if the repo map should route to the new surface.
- Update the handoff when unresolved work remains.
- Run relevant validation and summarize it.

Consider:

- Add evidence when the change depends on investigation or non-obvious behavior.
- Add or update prompts when the workflow will repeat.

## Level 3: architecture, migration, evidence, or high-risk change

Use for architecture decisions, migrations, high-risk edits, broad reorganizations, safety boundaries, or changes whose reasoning must survive review.

Expected updates:

- Update canonical docs.
- Add evidence or a decision note.
- Update Atlas maps and indexes.
- Update the work queue and next-session handoff.
- Include risks, rollback notes, or review points where useful.
- Run broader validation.

Consider:

- Promote a stable lesson into `AGENTS.md` only if it is likely to remain valuable across many future sessions.

## Default rule

If unsure, choose the lower level, then add one targeted note where the next reader would otherwise lose time.
