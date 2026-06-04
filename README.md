# Goated GitHub Project Template

<!--
Purpose:
Use this repository as the starting template for every serious product, SaaS, internal tool,
client project, or AI-assisted coding project.

This template gives Codex and other coding agents the context they need before they code.
-->

## What This Template Includes

```txt
AGENTS.md
PROJECT.md
TASKS.md
ARCHITECTURE.md
DESIGN.md
API.md
.env.example
README.md
```

## Why This Template Exists

AI coding agents are much better when the repo has clear instructions.

Without documentation, agents guess.

With this template, agents know:

- What the product is
- What the architecture should look like
- What tasks exist
- What files they can touch
- What design direction to follow
- What APIs exist
- What environment variables are needed
- What commands to run before finishing

## Recommended Workflow

### 1. Create a New Repo From This Template

Use this repo as a GitHub template.

Then create a new product repo from it.

### 2. Fill Out the Core Docs

Before writing code, update:

```txt
PROJECT.md
ARCHITECTURE.md
DESIGN.md
TASKS.md
API.md
.env.example
```

Do not skip this step.

The better these files are, the better Codex performs.

### 3. Create Branches for Agents

Example branch structure:

```txt
setup/project-foundation
design/ui-system
feature/auth
feature/database-schema
feature/core-dashboard
feature/payments
feature/cms
chore/tests-ci
```

### 4. Use Git Worktrees for Parallel Agents

Example:

```bash
git checkout main
git pull origin main

git worktree add ../product-foundation -b setup/project-foundation
git worktree add ../product-ui -b design/ui-system
git worktree add ../product-auth -b feature/auth
git worktree add ../product-db -b feature/database-schema
git worktree add ../product-qa -b chore/tests-ci
```

Open each folder separately and run one coding agent per folder.

### 5. Give Each Agent a Focused Task

Use this prompt format:

```md
You are Agent [NAME].

Read:
- AGENTS.md
- PROJECT.md
- TASKS.md
- ARCHITECTURE.md
- DESIGN.md
- API.md

Task:
[Describe one clear task]

Scope:
- Item 1
- Item 2
- Item 3

Out of scope:
- Do not touch unrelated files
- Do not redesign unrelated screens
- Do not add bonus features

Acceptance criteria:
- Criteria 1
- Criteria 2
- Criteria 3
- Build passes

Before final response:
Run:
pnpm lint
pnpm typecheck
pnpm build

Final response:
- Summary
- Files changed
- Commands run
- Manual testing
- Known issues
```

## How to Use With Codex

1. Start with the planning docs.
2. Ask Codex to read the docs before coding.
3. Give one task at a time.
4. Keep branches isolated.
5. Review every diff.
6. Merge only after lint, typecheck, build, and manual testing pass.

## Suggested Agent Setup

| Agent | Purpose |
|---|---|
| Product Architect | Creates project plan and task breakdown |
| Foundation Agent | Sets up repo, tooling, folders, configs |
| UI Agent | Builds design system and app shell |
| Auth Agent | Implements login, signup, protected routes |
| Database Agent | Builds schema, migrations, seed data |
| Feature Agent | Builds one vertical feature slice |
| QA Agent | Adds tests, checks edge cases |
| Deploy Agent | Handles Vercel, env docs, CI/CD |

## Best Practices

- Keep tasks small.
- Use one branch per agent.
- Use one worktree per branch.
- Define acceptance criteria before coding.
- Tell agents what not to touch.
- Do not let agents merge directly into `main`.
- Always review diffs.
- Always run build checks.
- Keep documentation updated.

## New Project Checklist

Before coding:

- [ ] Rename the project in `PROJECT.md`
- [ ] Fill in the product description
- [ ] Define target users
- [ ] Define MVP scope
- [ ] Define out-of-scope features
- [ ] Fill in tech stack
- [ ] Update architecture
- [ ] Add design direction
- [ ] Add API/server action notes
- [ ] Update `.env.example`
- [ ] Break work into tasks
- [ ] Create branches/worktrees
- [ ] Assign agents

Before merging:

- [ ] Code reviewed
- [ ] No unrelated files changed
- [ ] No secrets committed
- [ ] Lint passes
- [ ] Typecheck passes
- [ ] Build passes
- [ ] Tests pass if available
- [ ] Manual testing complete
- [ ] Docs updated

## License

Use this template freely for your own projects.
