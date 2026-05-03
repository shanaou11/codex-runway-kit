# Truth and Freshness Labels

Labels make the status of a note obvious without requiring a long explanation.

Use labels where status matters. Do not label every sentence.

## `current`

Use when the note matches the present repo state and has been checked recently.

Good for active rules, current paths, current workflow notes, and handoffs from the latest session.

## `likely-current`

Use when the note probably still applies, but has not been checked recently.

Good for stable guidance that may need a quick confirmation before high-risk work.

## `stale`

Use when the note may no longer match the repo state.

Good for old paths, old assumptions, postponed investigations, or anything that should be rechecked before use.

## `historical`

Use when the note describes what happened in the past but is not active guidance.

Good for completed decisions, migration records, previous approaches, and closed incidents.

## `draft`

Use when the note is proposed, incomplete, or not yet accepted.

Good for candidate rules, rough plans, early docs, and pending decisions.

## `verified`

Use when the claim has supporting evidence, such as a passing test, command output, source file, reviewed issue, or documented decision.

Add the evidence location when useful.

## `unverified`

Use when the claim is plausible but has not been confirmed.

Good for initial observations, suspected causes, or assumptions that should not be promoted yet.

## Combining labels

Labels can be combined when helpful:

- `likely-current, unverified`
- `historical, verified`
- `draft, unverified`

Prefer plain language if a label combination becomes hard to read.
