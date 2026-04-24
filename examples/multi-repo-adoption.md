# Multi-Repo Adoption Example

## Example setup

Product split into:

- `product-frontend`
- `product-backend`
- `product-infra`

Team also maintains:

- `ai-delivery-method` as the central methodology repo

## How to use the method

### Central repo responsibilities

The methodology repo stores:

- principles
- templates
- checklists
- starter pack

It does **not** become the day-to-day backlog for the product.

### Frontend repo responsibilities

Keep local docs such as:

- `docs/README.md`
- `docs/CURRENT.md`
- `docs/TASKS.md`
- `docs/DECISIONS.md`

Frontend-specific changes are tracked and verified there.

### Backend repo responsibilities

Keep the same local structure.

Backend-specific rules, migrations, test expectations, and active work stay local to that repo.

### Shared product work

If a feature changes the shared user flow between frontend and backend:

1. create a cross-repo task brief
2. list both repos as touched
3. define the API/interface change
4. define release order
5. implement locally in each repo
6. run repo-local tests
7. run shared E2E or smoke verification on the end-to-end flow

## Example scenario

### Change

Add a new billing status that changes:

- backend API payloads
- frontend status rendering
- export/download labels

### Correct method

- write one cross-repo task brief
- update backend repo docs and tests
- update frontend repo docs and tests
- verify the API contract and the browser flow together
- capture any shared decision in the coordination artifact and local `DECISIONS.md` files as needed

### Wrong method

- backend changes first without notifying frontend
- frontend updates later based on chat context only
- no explicit release order
- no shared flow verification

That is exactly the kind of siloed AI-assisted work this method is meant to prevent.
