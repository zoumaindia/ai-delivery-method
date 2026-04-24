# AI Delivery Method

A lightweight, tool-neutral framework for teams using AI in software delivery.

This repo is designed to help teams start new projects with:

- shared context that does not depend on chat history
- explicit planning and decision capture
- cross-object impact review before work is declared complete
- layered verification instead of "looks done"
- reusable templates that work across Claude, Codex, Cursor, ChatGPT, and non-AI workflows
- support for both single-repo and multi-repo product setups

## Core idea

Every meaningful change should follow this chain:

**Context -> Impact Review -> Plan -> Execute -> Verify -> Capture Learnings**

That keeps AI-assisted work from becoming siloed, fragile, or dependent on one person's memory.

## What this repo contains

- `principles/`
  Non-negotiable delivery principles
- `workflow/`
  Default workflow for new projects and new tasks
- `templates/`
  Reusable project docs and execution templates
- `checklists/`
  Definition of done, release, and review checklists
- `project-starter/`
  Starter structure for a new software project
- `tool-wrappers/`
  Thin examples for `AGENTS.md` and `CLAUDE.md`
- `examples/`
  Example adoption notes for a real team or repo

## Who this is for

- product and engineering teams using AI tools for delivery
- founders and operators who want one repeatable method across projects
- teams switching between agents or IDEs without losing process discipline

## Design goals

- tool-neutral first
- lean by default
- scalable from one repo to many
- reusable across stacks
- easy to improve over time

## Suggested usage

1. Copy `project-starter/` into a new project.
2. Fill the startup docs before feature work begins.
3. Use `templates/task-brief.md` for medium or large work.
4. Use `templates/cross-object-impact-review.md` before implementation.
5. Update `CURRENT.md`, `DECISIONS.md`, and `TASKS.md` as work progresses.
6. Feed new learnings back into this methodology repo.

## Single-repo vs multi-repo

This method supports both:

- **single-repo projects**
  One repo contains the app or service plus its delivery docs.
- **multi-repo products**
  Frontend, backend, mobile, infra, or shared-contract repos are separate, but the same planning and verification method is used across all of them.

For multi-repo setups:

- keep this methodology repo as the team-level framework
- keep local startup docs inside each implementation repo
- use a shared product/task brief when work crosses repositories
- verify interface contracts, release order, and cross-repo regression impact explicitly

See:

- `workflow/multi-repo-delivery.md`
- `templates/cross-repo-task-brief.md`
- `examples/multi-repo-adoption.md`

## What this is inspired by

This repo is informed by practical AI-assisted delivery patterns and by public work such as:

- spec-driven planning structures
- engineering workflow playbooks
- git-native requirements and decision capture

The goal here is not to copy a public framework verbatim, but to adapt the strongest ideas into a lightweight team operating method.

## Versioning

Method improvements should be recorded in `version-history.md`.

Keep the core method stable, and evolve templates and checklists as learnings become durable.
