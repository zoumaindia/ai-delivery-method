# Multi-Repo Delivery

Use this workflow when one product is split across multiple repositories, for example:

- frontend repo
- backend repo
- infra repo
- mobile repo
- shared contracts / SDK / design-system repo

The goal is to keep one delivery method without forcing all code into one repository.

## Core model

### 1. Central methodology repo

Use the methodology repo as the team-level source for:

- principles
- templates
- checklists
- starter structure

### 2. Per-repo local context

Each implementation repo should still carry its own local project docs:

- `docs/README.md`
- `docs/CURRENT.md`
- `docs/DECISIONS.md`
- `docs/working-agreement.md`
- `docs/TASKS.md`
- `docs/conventions.md`
- `docs/overview.md`

### 3. Shared product coordination layer

For work that spans repositories, keep one shared execution object:

- a cross-repo task brief
- or a central product/backlog board
- or a coordination repo if the team needs one

The shared layer should capture:

- touched repos
- changed interfaces
- dependency order
- rollout order
- shared decisions

## Default rules for multi-repo work

### Rule 1 — No repo works in isolation on shared flows

If the user flow, API contract, document format, or auth model spans repos, the task must be planned as a cross-repo change.

### Rule 2 — Keep local truth local

Each repo owns its own:

- code truth
- local active state
- local implementation backlog
- local testing guidance

Do not turn the central methodology repo into the active delivery board for every product.

### Rule 3 — Keep shared decisions shared

If a decision changes behavior across repos, capture it in the shared coordination artifact and then update local docs where needed.

### Rule 4 — Verify the interface, not just each repo

Passing local tests in each repo is not enough.

Also verify:

- request/response compatibility
- schema/contract compatibility
- release order
- backward compatibility
- environment/runtime assumptions

## Recommended operating pattern

1. Write a cross-repo task brief.
2. Identify touched repos and impacted repos.
3. Record the contract/interface changes.
4. Decide execution order.
5. Implement repo-local changes.
6. Run repo-local verification.
7. Run cross-repo verification on the shared flow.
8. Update local docs and shared coordination notes.

## Typical multi-repo checks

| Change | Also verify |
|---|---|
| Backend API change | frontend client calls, SDKs, API docs, E2E flow |
| Shared type/schema change | all consumer repos, generated clients, compatibility |
| Auth/role change | frontend nav/guards, backend guards, direct URL access, service-to-service access |
| Document/export change | generation repo, consumer UI, storage/integration behavior |
| Alert/notification change | scheduler/service repo, settings UI, recipient resolution, template compatibility |
| Infra/runtime dependency | deployment repo, runtime config, release checklist |

## Keep it lean

Do not create a heavyweight program-management system by default.

For most teams, the minimum viable multi-repo setup is:

- one central methodology repo
- local docs in each implementation repo
- one cross-repo task brief per shared change
