# Working Agreement

Stable workflow rules for how the team should work in this repo.

## Collaboration rules

- Read startup docs before beginning meaningful work.
- Keep questions concise and practical.
- State assumptions explicitly.
- Describe destructive or high-risk actions plainly before taking them.

## Source-of-truth rules

- Code beats docs when they drift.
- Schema/migrations are the database source of truth.
- Route/handler definitions are the API source of truth.
- Update docs after verifying code truth.

## Delivery rules

- No feature is done in isolation.
- Every backend logic change must have unit or integration coverage.
- Every auth/role change must have permission-focused verification.
- Every changed user flow must have browser verification or a smoke-check update.
- Non-obvious decisions belong in `DECISIONS.md`.

## Definition of done

- [ ] Cross-object impact checked
- [ ] Relevant docs updated
- [ ] Relevant tests added/updated
- [ ] Builds pass
- [ ] User-facing flow verified when applicable

## Safety rules

- Do not overstate verification.
- "Build passes" is not the same as "behavior verified."
- Keep the process lean and proportional to task risk.
