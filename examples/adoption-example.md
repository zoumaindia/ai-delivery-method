# Example Adoption Pattern

## Central methodology repo

Use this repo as the team-level source for:

- delivery principles
- shared templates
- checklists
- starter docs

## Per-project adoption

For each project:

1. copy the `project-starter/` into the new repo
2. fill the startup docs
3. add thin tool wrappers only if needed
4. keep the backlog and active state inside the project repo
5. feed stable learnings back into the central methodology repo

## Multi-repo adoption

If one product spans multiple repos:

1. keep this repo as the central methodology source
2. keep startup docs and active backlog local to each implementation repo
3. use a shared cross-repo task brief whenever a change spans interfaces or flows
4. verify release order and end-to-end behavior explicitly

See `examples/multi-repo-adoption.md`.

## Upgrade loop

When a repeated failure or blind spot is discovered:

- decide whether it should become a rule, checklist item, or template change
- update this methodology repo
- tag or version the change
- notify the team to adopt it in active projects
