# AGENTS.md

<!--
Purpose:
This file tells AI coding agents how to work inside this repository.
Every serious repo should have this because agents need rules, boundaries,
commands, coding style, and final-response expectations.

How to use:
Update the project-specific stack, commands, file ownership rules,
and final checklist before asking Codex or any coding agent to work.
-->

## Agent Role

You are working as a production-focused coding agent inside this repository.

Your job is to implement assigned tasks carefully, follow the existing architecture,
avoid unrelated changes, and leave the codebase cleaner than you found it.

## Core Rules

- Read `PROJECT.md`, `TASKS.md`, `ARCHITECTURE.md`, `DESIGN.md`, and `API.md` before coding.
- Work only on the assigned task.
- Do not rewrite unrelated files.
- Do not add new dependencies unless necessary.
- If you add a dependency, explain why.
- Keep files small and focused.
- Prefer reusable components over repeated code.
- Prefer clear names over clever abstractions.
- Do not expose secrets or hardcode API keys.
- Update documentation when behavior changes.

## Code Style

<!--
Customize this section based on your stack.
Example: Next.js, TypeScript, Tailwind, Supabase, Sanity, Shopify, etc.
-->

- Use TypeScript when possible.
- Keep pages/routes light.
- Move business logic into `lib/`, `services/`, `hooks/`, `server-actions/`, or equivalent folders.
- Keep UI components reusable.
- Handle loading, error, and empty states.
- Validate user input.
- Follow existing project patterns before creating new ones.

## File Ownership Rules

<!--
Use this section when multiple agents are working in parallel.
Assign each agent a branch and folder/file ownership zone.
-->

Example:

| Agent | Branch | Allowed Files | Avoid Files |
|---|---|---|---|
| UI Agent | `design/ui-system` | `components/ui/**`, `components/layout/**`, `app/page.tsx` | `lib/db/**`, `api/**` |
| Auth Agent | `feature/auth` | `app/(auth)/**`, `middleware.ts`, `lib/auth/**` | `billing/**`, `cms/**` |
| DB Agent | `feature/database` | `db/**`, `supabase/**`, `lib/db/**` | `components/**` |

## Commands

<!--
Replace these commands with the correct commands for your project.
-->

```bash
# Install dependencies
pnpm install

# Run local development server
pnpm dev

# Lint
pnpm lint

# Typecheck
pnpm typecheck

# Build
pnpm build

# Test
pnpm test
```

## Before Coding

The agent should:

1. Read the relevant docs.
2. Inspect the files related to the assigned task.
3. Create a short implementation plan.
4. Confirm assumptions if the task is unclear.
5. Implement only the requested scope.

## Before Final Response

The agent should run:

```bash
pnpm lint
pnpm typecheck
pnpm build
```

If a command fails, the agent should report the failure clearly and explain what was attempted.

## Final Response Format

Every coding agent should end with:

```md
## Summary
- What changed

## Files Changed
- List of important files

## Commands Run
- Command results

## Manual Testing
- Steps for the user to test

## Known Issues
- Anything unfinished or blocked
```
