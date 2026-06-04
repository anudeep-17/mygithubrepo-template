# Security Checklist

<!--
Purpose:
Use this checklist for auth, API, payments, database, and production readiness.
-->

## Secrets

- [ ] No secrets committed
- [ ] `.env.example` contains names only
- [ ] Server-only keys do not use public prefixes
- [ ] Production secrets are set in deployment provider
- [ ] Old exposed secrets rotated if needed

## Authentication

- [ ] Private pages require auth
- [ ] Session checked server-side
- [ ] Logout works
- [ ] Password reset works if applicable
- [ ] Auth errors are safe and clear

## Authorization

- [ ] Users can only access their own data
- [ ] Admin actions require admin role
- [ ] API routes enforce permissions
- [ ] Database policies enforce permissions

## Input Validation

- [ ] Request body validated
- [ ] Query params validated
- [ ] Form inputs validated
- [ ] File uploads restricted if applicable
- [ ] Error messages do not leak internals

## API

- [ ] Sensitive endpoints are protected
- [ ] Webhooks verify signatures
- [ ] Webhook handlers are idempotent
- [ ] Rate limits added where needed
- [ ] Logs avoid sensitive data

## Dependencies

- [ ] Dependencies are necessary
- [ ] Packages are maintained
- [ ] Lockfile committed
- [ ] No suspicious packages added

## Production

- [ ] HTTPS enabled
- [ ] Domain configured
- [ ] Security headers considered
- [ ] Error logging active
- [ ] Backup/rollback plan exists
