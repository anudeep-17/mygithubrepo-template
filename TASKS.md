# TASKS.md

<!--
Purpose:
This file breaks the product into clear work items.
Use it to assign tasks to coding agents or humans.

Good tasks have:
- one owner
- one branch
- clear scope
- files allowed
- acceptance criteria
- test plan
-->

## Status Legend

- `todo`
- `doing`
- `review`
- `done`
- `blocked`

## Branch Naming

```txt
setup/project-foundation
design/ui-system
feature/auth
feature/database-schema
feature/core-feature
feature/payments
feature/cms
chore/tests-ci
fix/bug-name
```

## Task Board

| Status | Task | Branch | Owner | Notes |
|---|---|---|---|---|
| todo | Product architecture | `docs/product-architecture` | Architect Agent | Complete docs before coding |
| todo | Project foundation | `setup/project-foundation` | Foundation Agent | Tooling, folders, config |
| todo | Design system | `design/ui-system` | UI Agent | Components and layout |
| todo | Authentication | `feature/auth` | Auth Agent | Login/signup/session |
| todo | Database schema | `feature/database-schema` | Database Agent | Schema, policies, seed |
| todo | Core feature | `feature/core-feature` | Feature Agent | Main product workflow |
| todo | QA and CI | `chore/tests-ci` | QA Agent | Tests and GitHub Actions |
| todo | Deployment | `chore/deployment` | Deploy Agent | Production readiness |

## Task Template

### Task: [Task Name]

**Status:** todo  
**Branch:** `feature/example`  
**Owner:** Agent/person  

#### Goal

One-sentence description of the goal.

#### Scope

- Item 1
- Item 2
- Item 3

#### Out of Scope

- Item 1
- Item 2

#### Files Allowed

```txt
path/example/**
```

#### Files to Avoid

```txt
path/unrelated/**
```

#### Acceptance Criteria

- [ ] Criteria 1
- [ ] Criteria 2
- [ ] Criteria 3
- [ ] Lint passes
- [ ] Typecheck passes
- [ ] Build passes

#### Test Plan

```bash
pnpm lint
pnpm typecheck
pnpm build
pnpm test
```

#### Manual Testing

1. Step one
2. Step two
3. Step three

#### Handoff Notes

Add anything the next agent should know.
