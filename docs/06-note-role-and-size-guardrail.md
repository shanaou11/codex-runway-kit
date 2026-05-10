# Note Role and Size Guardrail

Use this guardrail when deciding whether a Markdown note is still doing one clear job.

Core principle:

> One note, one job. Line count is a warning signal, not the real rule.

This is a review aid, not a hard law. A long note is not automatically wrong. Reassess when note size starts to hide the note's role, weaken navigation, or reduce reviewer confidence.

Split by role first. Use line count only as a review trigger.

## Role rule

Navigation notes route; evidence notes explain; handoffs transfer; queues prioritize; prompts instruct.

If a note is doing more than one of those jobs, split the jobs unless there is a strong reason to keep them together.

## Soft thresholds

| Note type | Smooth target | Reassess around | Split unless justified |
| --- | ---: | ---: | ---: |
| Atlas / navigation / index note | 50-250 lines | 300-400 | 500+ |
| Handoff / queue / prompt note | 80-250 lines | 300-500 | 700+ |
| Evidence pack / investigation note | 300-900 lines | 1,200 | 1,500+ |
| Archive / raw witness note | no strict limit | role-based | only if navigation suffers |

Treat these as triggers for review, not mechanical limits.

## Note roles

- Atlas map: routes readers to the right files and current surfaces; it should not become a recap archive.
- Index or navigation note: points to relevant notes and canonical docs; it should avoid duplicating long summaries from child notes.
- Queue: prioritizes pending work; it should not become a design doc or a second handoff.
- Handoff: transfers current state to the next session; it should not turn into a stale backlog or a long historical recap.
- Prompt: instructs one bounded task; it should not become policy, changelog, and launcher in one file.
- Evidence pack: explains findings, reasoning, and support for a change or conclusion.
- Policy: states stable operating rules that may need reuse across sessions or repos.
- Archive or raw witness note: preserves source material where custody matters more than compactness.

## Reassess or split when

- The note has too many unrelated sections.
- It repeats long summaries already present in child notes.
- It contains multiple competing lists or sources of truth.
- It carries stale historical recap inside an active handoff.
- It mixes policy, task execution, and changelog.
- Readers must scroll through archive or history before finding the route.
- The note's role is unclear without prior context.

## Raw witness or custody-sensitive exception

Do not apply mechanical splitting to raw witness or custody-sensitive material.

- Source-preserving raw notes can stay long when integrity matters more than compactness.
- Journal-style or witness-style entries should not be split just to satisfy Codex.
- Atlas and workflow notes can still use this guardrail normally.
- Raw material should be judged by custody and voice, not line count.
