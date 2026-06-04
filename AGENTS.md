# AGENTS.md

<!--
Purpose:
This file gives coding agents the rules of the repository.
Agents should read this before touching code.

Use this file to define:
- coding standards
- commands
- folder ownership
- safety rules
- final response format
- multi-agent workflow
-->

## Agent Mission

You are working inside a production-grade repository.

Your goal is to complete the assigned task with minimal, high-quality changes while following the documented architecture, design system, and task boundaries.

## Required Reading Before Coding

Before making changes, read:

1. `PROJECT.md`
2. `PRD.md`
3. `TASKS.md`
4. `ARCHITECTURE.md`
5. `DESIGN.md`
6. `API.md`
7. `DECISIONS.md`
8. This file

## Core Rules

- Work only on the assigned task.
- Do not modify unrelated files.
- Do not add bonus features.
- Do not rewrite the architecture unless the task explicitly asks for it.
- Do not add dependencies without explaining the reason.
- Do not hardcode secrets or credentials.
- Do not remove existing functionality unless asked.
- Prefer small, reviewable changes.
- Keep files focused and readable.
- Update docs when behavior or setup changes.
- Respect the existing design system.

## Code Quality Rules

- Use TypeScript where applicable.
- Prefer explicit types for public functions.
- Validate user input.
- Handle loading, error, and empty states.
- Keep UI components reusable.
- Move business logic out of route/page files.
- Prefer server-side logic for sensitive operations.
- Avoid duplicating logic.
- Avoid large files.
- Use clear names.

## Multi-Agent Rules

When multiple agents are working in parallel:

- Each agent must work on its own branch.
- Each agent must own a narrow scope.
- Avoid editing files owned by another branch.
- Do not merge directly into `main`.
- Create or update a handoff doc in `docs/handoffs/` when the task is complete.
- If blocked by another task, document the blocker clearly.

## Suggested File Ownership

| Agent | Branch | Allowed Files | Avoid Files |
|---|---|---|---|
| Foundation Agent | `setup/project-foundation` | configs, package files, base folders | feature-specific logic |
| UI Agent | `design/ui-system` | `components/ui/**`, `components/layout/**`, styles | auth, db, payments |
| Auth Agent | `feature/auth` | auth routes, middleware, auth helpers | billing, CMS, unrelated UI |
| Database Agent | `feature/database-schema` | db, migrations, types, data helpers | page redesigns |
| Feature Agent | `feature/name` | assigned feature files | unrelated modules |
| QA Agent | `chore/tests-ci` | tests, CI, test utilities | product behavior changes |
| Deploy Agent | `chore/deployment` | deployment docs, CI/CD, env docs | feature logic |

## Commands

<!--
Update these commands for your actual stack.
-->

```bash
pnpm install
pnpm dev
pnpm lint
pnpm typecheck
pnpm build
pnpm test
```

## Before Coding

The agent should:

1. Inspect the relevant files.
2. Create a short plan.
3. Identify files to edit.
4. Identify risks.
5. Implement only the agreed scope.

## Before Finishing

Run:

```bash
pnpm lint
pnpm typecheck
pnpm build
pnpm test
```

If a command fails, explain why and include the error summary.

## Final Response Format

```md
## Summary
- What changed

## Files Changed
- Important files changed

## Commands Run
- Command and result

## Manual Testing
- Steps performed or recommended

## Handoff Notes
- Anything the next agent should know

## Known Issues
- Anything incomplete or blocked
```
