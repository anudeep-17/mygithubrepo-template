# TASKS.md

<!--
Purpose:
This file breaks the product into clear tasks that can be assigned to humans or coding agents.

How to use:
Each task should have a branch, scope, acceptance criteria, and clear ownership.
For multi-agent work, do not let two agents own the same files at the same time.
-->

## Task Status Legend

- `todo` — Not started
- `doing` — In progress
- `review` — Needs review
- `done` — Complete
- `blocked` — Blocked

## Recommended Branch Naming

```txt
setup/project-foundation
design/ui-system
feature/auth
feature/database-schema
feature/core-dashboard
feature/payments
feature/cms
chore/tests-ci
fix/bug-name
```

## Task Board

| Status | Task | Branch | Owner | Notes |
|---|---|---|---|---|
| todo | Project foundation | `setup/project-foundation` | Foundation Agent | Setup app, tooling, folders |
| todo | Design system | `design/ui-system` | UI Agent | Components, layout, visual system |
| todo | Authentication | `feature/auth` | Auth Agent | Login, signup, protected routes |
| todo | Database schema | `feature/database-schema` | DB Agent | Tables, policies, seed data |
| todo | Core dashboard | `feature/core-dashboard` | Dashboard Agent | Main app experience |
| todo | Tests and CI | `chore/tests-ci` | QA Agent | Lint, tests, GitHub Actions |

## Task Template

<!--
Copy this block for every real task.
-->

### Task: [Task Name]

**Status:** todo  
**Branch:** `feature/example-branch`  
**Owner:** Agent or person name  

#### Goal

Describe the task in one sentence.

#### Scope

- Item 1
- Item 2
- Item 3

#### Out of Scope

- Item that should not be touched
- Item that belongs to another branch

#### Files Allowed

```txt
app/example/**
components/example/**
lib/example/**
```

#### Files to Avoid

```txt
app/billing/**
lib/payments/**
```

#### Acceptance Criteria

- Criteria 1
- Criteria 2
- Criteria 3
- Build passes

#### Test Plan

```bash
pnpm lint
pnpm typecheck
pnpm build
pnpm test
```

#### Manual Testing Steps

1. Step one
2. Step two
3. Step three

#### Notes

Add important context here.
