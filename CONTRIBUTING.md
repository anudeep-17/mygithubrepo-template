# CONTRIBUTING.md

<!--
Purpose:
This file explains how work should be contributed to the repo.
It helps humans and agents follow a clean GitHub workflow.
-->

## Branching Strategy

Use one branch per task.

Recommended names:

```txt
setup/project-foundation
design/ui-system
feature/auth
feature/database-schema
feature/core-dashboard
chore/tests-ci
fix/bug-name
```

## Commit Style

Use clear commit messages.

Examples:

```txt
feat: add auth pages
fix: handle empty menu state
docs: update setup guide
chore: add ci workflow
test: add dashboard tests
```

## Pull Request Rules

Every PR should:

- Link to a task in `TASKS.md`
- Be focused on one scope
- Include screenshots for UI changes
- Include test results
- Avoid unrelated file changes
- Update docs if needed

## Review Checklist

- [ ] Code matches the task
- [ ] No unrelated files changed
- [ ] No secrets committed
- [ ] Error/loading/empty states handled
- [ ] Responsive layout checked
- [ ] Lint passes
- [ ] Typecheck passes
- [ ] Build passes
- [ ] Tests pass
- [ ] Docs updated

## Multi-Agent Workflow

When using coding agents:

1. Create a separate branch/worktree for each agent.
2. Give the agent one task.
3. Give the agent file ownership boundaries.
4. Review the diff before merging.
5. Ask a review agent to inspect the branch if needed.
6. Merge only after checks pass.

## Merge Strategy

Prefer squash merge for clean history unless the project needs detailed commit history.
