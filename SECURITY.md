# SECURITY.md

<!--
Purpose:
This file defines security rules for the project.
Agents should read this before working on auth, API routes, webhooks, database, or payments.
-->

## Security Principles

- Never commit secrets.
- Never expose server-only keys to the client.
- Validate all user input.
- Check authorization server-side.
- Use least-privilege access.
- Verify webhooks.
- Avoid logging sensitive data.
- Keep dependencies updated.

## Secret Handling

Secrets must go in environment variables.

Do not hardcode:

- API keys
- service role keys
- database URLs
- webhook secrets
- private tokens
- passwords

## Client vs Server Variables

Client-safe variables may start with:

```txt
NEXT_PUBLIC_
```

Server-only variables must not be exposed to browser code.

## Authentication Checklist

- [ ] Protected routes require auth
- [ ] Session is checked server-side
- [ ] Logout clears session
- [ ] Password reset flow works if applicable
- [ ] Admin routes require admin role

## Authorization Checklist

- [ ] Users can only access their own data
- [ ] Admin-only actions are protected
- [ ] API routes check permissions
- [ ] Database policies enforce access rules

## API Security

- [ ] Validate request body
- [ ] Validate query params
- [ ] Rate limit sensitive endpoints if needed
- [ ] Return safe error messages
- [ ] Do not leak internal details

## Webhook Security

- [ ] Verify signature
- [ ] Use raw body if required by provider
- [ ] Make handlers idempotent
- [ ] Log event IDs
- [ ] Do not trust payload blindly

## Dependency Security

Before adding a dependency:

- Check if it is maintained
- Check package popularity/reputation
- Avoid unnecessary packages
- Prefer official SDKs

## Reporting Security Issues

If a vulnerability is found, document:

- What is affected
- How severe it is
- How to reproduce
- Suggested fix
- Whether secrets need rotation
