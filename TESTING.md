# TESTING.md

<!--
Purpose:
This file tells humans and agents how to verify quality.
Keep testing expectations clear and repeatable.
-->

## Testing Philosophy

Every change should be tested at the right level:

- Unit tests for pure logic
- Integration tests for data/API behavior
- E2E tests for critical user flows
- Manual testing for UX and visual checks

## Required Checks Before Merge

```bash
pnpm lint
pnpm typecheck
pnpm build
pnpm test
```

## Manual Test Checklist

- [ ] Page loads without console errors
- [ ] Loading state works
- [ ] Empty state works
- [ ] Error state works
- [ ] Mobile layout works
- [ ] Tablet layout works
- [ ] Desktop layout works
- [ ] Form validation works
- [ ] Success toast/message works
- [ ] Failure toast/message works

## Critical User Flows

Document the flows that must always work.

### Flow 1: [Flow Name]

1. Step one
2. Step two
3. Step three
4. Expected result

## Test Data

Document test users, sample records, and seed data here.

## Accessibility Checks

- [ ] Keyboard navigation
- [ ] Focus states
- [ ] Alt text
- [ ] Color contrast
- [ ] Semantic headings
- [ ] Labels for inputs

## Visual QA

For UI changes, include screenshots in the PR.

Check:

- spacing
- alignment
- mobile responsiveness
- font consistency
- hover/focus states
- empty/loading/error states
