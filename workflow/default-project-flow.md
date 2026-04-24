# Default Project Flow

Use this flow when starting or running a new AI-assisted software project.

## Phase 1 — Start the project spine

Before writing features, set up the shared project context:

- `docs/README.md`
- `docs/CURRENT.md`
- `docs/DECISIONS.md`
- `docs/working-agreement.md`
- `docs/TASKS.md`
- `docs/conventions.md`
- `docs/overview.md`

Optional wrappers:

- `AGENTS.md`
- `CLAUDE.md`

## Phase 2 — Define the project model

Document the main business objects and relationships early.

For each important object, define:

- what it is
- who uses it
- what it connects to
- what it can impact

This is the basis for cross-object review later.

## Phase 3 — Start delivery with a task brief

For medium or large work, create a task brief before implementation.

The brief should cover:

- goal
- scope
- touched objects
- risks
- open questions
- required tests
- required doc updates

## Phase 4 — Run cross-object impact review

Before coding, identify:

- touched modules
- dependent modules
- likely lifecycle effects
- status/totals/permission/reporting impacts
- required regression checks

## Phase 5 — Execute and verify

For each meaningful task:

- implement
- run builds
- run/update relevant tests
- verify user-facing behavior if applicable
- update docs

## Phase 6 — Capture learnings

After major work, ask:

- what surprised us
- what was missed in planning
- what should become a decision, checklist, or template update

Then update this methodology repo or the project adoption docs.
