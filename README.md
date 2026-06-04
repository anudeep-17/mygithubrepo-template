# Goated Codex Repo Template

<!--
Purpose:
Use this repository as a starting point for every serious product, SaaS, internal tool,
client project, or AI-assisted coding project.

This template is designed to make Codex and other coding agents dramatically better by
giving them context, architecture, task boundaries, quality gates, and review rules.
-->

## What This Template Includes

```txt
README.md
AGENTS.md
PROJECT.md
PRD.md
TASKS.md
ARCHITECTURE.md
DESIGN.md
API.md
DECISIONS.md
SETUP.md
DEPLOYMENT.md
SECURITY.md
TESTING.md
CONTRIBUTING.md
CHANGELOG.md
.env.example
.gitignore
CODEOWNERS

.github/
  pull_request_template.md
  ISSUE_TEMPLATE/
    bug_report.md
    feature_request.md
    task.md
  workflows/
    ci.yml

docs/
  prompts/
    architect-agent.md
    foundation-agent.md
    ui-agent.md
    auth-agent.md
    database-agent.md
    feature-agent.md
    review-agent.md
    qa-agent.md
    deploy-agent.md
  handoffs/
    .gitkeep
  checklists/
    pre-merge.md
    launch.md
    security.md
```

## Why This Exists

AI coding agents are only as good as the instructions and constraints inside the repo.

Without structure, agents guess.

With this template, agents understand:

- What the product is
- Who the users are
- What the MVP includes
- What architecture to follow
- What files they can edit
- What design language to use
- What APIs exist
- How to run and test the project
- How to open clean pull requests
- How to hand off work to the next agent

## Recommended Workflow

### 1. Create a New Repo From This Template

Create a new GitHub repository from this template.

### 2. Fill Out the Planning Docs

Before coding, update:

```txt
PROJECT.md
PRD.md
TASKS.md
ARCHITECTURE.md
DESIGN.md
API.md
DECISIONS.md
.env.example
```

### 3. Create One Branch Per Agent

Example:

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

### 4. Use Git Worktrees for Parallel Coding Agents

```bash
git checkout main
git pull origin main

git worktree add ../product-foundation -b setup/project-foundation
git worktree add ../product-ui -b design/ui-system
git worktree add ../product-auth -b feature/auth
git worktree add ../product-db -b feature/database-schema
git worktree add ../product-qa -b chore/tests-ci
```

Open each folder separately and run one agent per folder.

### 5. Use Prompt Files

Copy prompts from:

```txt
docs/prompts/
```

Each prompt is designed for a specific agent role.

## Suggested Agent Roles

| Agent | Purpose |
|---|---|
| Architect Agent | Creates product plan, architecture, and task split |
| Foundation Agent | Sets up project, tooling, folders, configs |
| UI Agent | Builds design system and app shell |
| Auth Agent | Implements login, signup, sessions, protected routes |
| Database Agent | Builds schema, migrations, seed data, data helpers |
| Feature Agent | Builds one vertical product feature |
| Review Agent | Reviews diffs and catches issues |
| QA Agent | Adds tests, checks edge cases, improves quality |
| Deploy Agent | Handles deployment, CI/CD, env docs, production readiness |

## Golden Rules

- Do not ask agents to build the whole product in one prompt.
- Give one agent one clear task.
- Give each agent a branch.
- Give each agent file ownership boundaries.
- Define acceptance criteria before coding.
- Run lint, typecheck, build, and tests before merging.
- Never let agents merge directly into `main`.
- Keep docs updated as the product changes.

## New Project Checklist

- [ ] Rename project in `PROJECT.md`
- [ ] Define users and MVP scope
- [ ] Complete `PRD.md`
- [ ] Complete `ARCHITECTURE.md`
- [ ] Complete `DESIGN.md`
- [ ] Complete `API.md`
- [ ] Fill `.env.example`
- [ ] Break work into `TASKS.md`
- [ ] Create worktrees/branches
- [ ] Assign agents
- [ ] Add CI secrets if needed
- [ ] Start with the Foundation Agent

## License

Use freely for your own projects.
