# Launch Checklist

<!--
Purpose:
Use before launching the product or major feature.
-->

## Product

- [ ] MVP scope complete
- [ ] Out-of-scope items not accidentally added
- [ ] Critical user flows work
- [ ] Copy reviewed
- [ ] Empty/loading/error states reviewed

## Engineering

- [ ] Lint passes
- [ ] Typecheck passes
- [ ] Build passes
- [ ] Tests pass
- [ ] CI passes
- [ ] Production env vars configured
- [ ] Database migrations applied
- [ ] Webhooks configured
- [ ] Domain configured

## Security

- [ ] No secrets in repo
- [ ] Auth works
- [ ] Authorization works
- [ ] Admin routes protected
- [ ] Webhook signatures verified
- [ ] Rate limits added where needed

## UX

- [ ] Mobile tested
- [ ] Tablet tested
- [ ] Desktop tested
- [ ] Accessibility basics checked
- [ ] Forms tested
- [ ] Error messages clear

## Operations

- [ ] Rollback plan documented
- [ ] Error logging checked
- [ ] Analytics checked
- [ ] Support/contact path exists
- [ ] README/SETUP/DEPLOYMENT updated

## Final Smoke Test

1. Visit production homepage
2. Complete primary user flow
3. Complete auth flow if applicable
4. Complete payment flow if applicable
5. Check logs for errors
