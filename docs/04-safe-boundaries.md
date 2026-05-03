# Safe Boundaries

Some parts of a repository should not be casually edited. Atlas Memory makes those areas visible so a future human or Codex session knows when to slow down.

Safe boundaries are not permanent locks. They are review signals.

## What to mark

Mark areas where casual edits could cause hidden damage, such as:

- Data migrations.
- Authentication or permission rules.
- Billing or payment flows.
- Generated files.
- Deployment configuration.
- Shared schemas.
- Public API contracts.
- Large archived docs.

Use fictional or generic examples in public templates.

## How to define a boundary

For each boundary, describe:

- Path or surface.
- Why it matters.
- What kind of changes are safe.
- What kind of changes need review.
- Suggested validation.

Example:

```md
### `config/deploy.example.yml`

Status: current

Do not casually edit deployment examples. Small comment fixes are fine. Behavioral changes should include a note in `docs/deployment.md` and a validation summary.
```

## Where to put boundaries

- Put stable repo-wide boundaries in `AGENTS.md`.
- Put detailed explanation in canonical docs under `docs/`.
- Put temporary caution in the session handoff or queue.

## What not to do

- Do not mark the whole repo as sensitive.
- Do not use boundaries to avoid normal maintenance.
- Do not promote a one-time concern into `AGENTS.md` unless it is likely to stay useful.
