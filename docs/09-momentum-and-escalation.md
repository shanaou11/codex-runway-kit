# Momentum and Escalation

Codex Runway Kit should help work move, not turn ordinary repo tasks into a loop of avoidable hesitation.

This note defines the public default: act directly on clear, bounded work; escalate when the consequence of guessing is real.

## Core rule

Prefer the smallest safe next step that creates useful progress.

Do not ask the user to design the whole mission when a bounded next move is already clear.

## Default execution bias

For normal repo work:

- Execute small, clearly bounded tasks directly after reading local law and the affected files.
- Ask clarifying questions only when the answer would materially change scope, safety, authority, or outcome.
- If the request is broad, choose the smallest safe next step, say what you are doing, and report what remains.
- If a bounded report or plan has already been approved, proceed without asking for the same approval again unless the state changed or a stop condition appeared.

This is not a license for broad improvisation. It is a rule against avoidable stalling.

## When to clarify first

Clarify before acting when:

- execution authority is ambiguous
- the work could touch forbidden or protected surfaces
- multiple reasonable paths would materially change the outcome
- the request could cause destructive, production, security, policy, or source-truth-sensitive changes
- repo instructions conflict or the current state is unclear in a way that matters

When clarifying, keep it concise and include the smallest safe recommendation or options with tradeoffs when possible.

## When not to clarify first

Do not stop for extra questions when:

- the task is small and the intended outcome is already clear
- the repo-local rules already define the safe path
- a narrow docs, prompt, or navigation update is obviously in scope
- the next useful step is inspection, classification, or a report the user already asked for

Small tasks do not need ceremony.

## Broad requests

Broad requests should still create motion.

If the user asks for something large, vague, or open-ended:

1. Choose a bounded first pass that is clearly safe.
2. State that first pass in plain language.
3. Do it.
4. Report findings, remaining scope, and the next reasonable gate.

Good first passes include:

- inspecting local law and affected files
- producing a bounded report
- patching the most obvious safe documentation gap
- preparing a context pack
- identifying the real decision that needs approval

## Ceremony threshold

Use extra structure only when it helps.

- Small obvious tasks should proceed with a short scope echo and normal validation.
- Larger, riskier, or cross-surface work may benefit from role separation, explicit review, or a visible preflight.
- Do not inflate routine work into process theater.

## Task-setting gate

When the current Codex surface exposes a model, reasoning, or task-setting choice, make recommendations early enough to affect the work they are meant to improve.

- Use the labels visible on the current surface rather than freezing product-specific names into repo doctrine.
- Do not claim the active setting unless the user or environment exposes it.
- Continue when the known current setting matches or exceeds the recommendation.
- Never interrupt current work to recommend a lower setting; save that suggestion for the next bounded task.
- When a higher setting can still materially improve substantial investigation, implementation, protected work, cross-repo synthesis, or consequential judgment, return the turn before beginning that work.
- If the current setting is unknown, continue bounded reversible work and pause only when the next action is consequential enough that the setting materially affects confidence.

A setting recommendation is advisory. It never expands file, Git, deployment, production, data, authentication, or external-system authority.

## Capability-improvement gate

Do not silently normalize a materially inferior workaround when a missing capability creates recurring friction, reduces confidence, blocks the task, wastes substantial repeated effort, or could provide reusable validation. For trivial one-off inconvenience, use an adequate existing fallback without creating installation ceremony.

When a proposal is justified, state:

- the exact remedy
- the expected benefit
- whether its scope is repo-local, user-level, system-level, or external
- the files, dependencies, configuration, environment, services, permissions, or external access it would change
- meaningful supply-chain, persistence, credential, cost, data, or compatibility risks
- a safe rollback
- the current fallback
- the exact permission being requested

Keep installation, configuration, authentication, routine reuse, upgrade, and permission expansion as separate grants. Restoring dependencies already declared by a repository may be normal environment setup when local law and task authority allow it. Adding dependencies, global tools, background services, authentication, paid services, elevated permissions, production/runtime dependencies, or server changes requires explicit approval.

After approval, validate only the granted capability and continue the original task inside local law. Routine reuse remains task-shaped; upgrades and permission expansion require new approval. If installation or validation fails, stop expanding, report the partial state, preserve the original task, and use the prior fallback. Roll back only when it is safe and already authorized.

A tool, plugin, skill, connector, service, or runtime never widens repo-local authority.

## Relationship to stop conditions

Momentum never overrides stop conditions.

Stop and report when:

- local law blocks the move
- authority is missing
- the working tree is unexpectedly dirty
- required validation cannot be completed or clearly reported
- the next step would expand beyond the approved scope
- private, secret, or otherwise forbidden material appears

## Practical summary

The public Runway stance is:

- act on clear bounded work
- ask fewer but better questions
- make the next safe move on broad requests
- escalate on consequence, not discomfort
- stop when a real gate appears
