# Pre-Merge Checklist

<!--
Purpose:
Run this before merging any branch into main.
-->

## Scope

- [ ] PR matches one task from `TASKS.md`
- [ ] No unrelated files changed
- [ ] No bonus features added
- [ ] Docs updated if needed

## Quality

- [ ] Lint passes
- [ ] Typecheck passes
- [ ] Build passes
- [ ] Tests pass
- [ ] No console errors in manual testing

## Security

- [ ] No secrets committed
- [ ] Server-only keys are not exposed to client
- [ ] Auth checks are server-side
- [ ] Inputs are validated
- [ ] Webhooks verify signatures if applicable

## UX

- [ ] Loading state exists
- [ ] Empty state exists
- [ ] Error state exists
- [ ] Mobile layout checked
- [ ] Tablet layout checked
- [ ] Desktop layout checked
- [ ] Accessibility basics checked

## Review

- [ ] Diff reviewed
- [ ] Screenshots included for UI changes
- [ ] Handoff notes added if useful
- [ ] Reviewer approved
