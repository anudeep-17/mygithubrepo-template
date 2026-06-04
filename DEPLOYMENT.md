# DEPLOYMENT.md

<!--
Purpose:
This file explains how to deploy the project safely.
Use this for Vercel, Netlify, Railway, Render, AWS, or any other host.
-->

## Deployment Provider

- Provider:
- Production URL:
- Preview URL:
- Dashboard URL:

## Build Settings

```txt
Install command:
Build command:
Output directory:
Node version:
```

## Environment Variables

Add these in the deployment provider:

```txt
NEXT_PUBLIC_APP_URL=
DATABASE_URL=
AUTH_SECRET_KEY=
```

Use `.env.example` as the source of truth.

## Deployment Steps

1. Push changes to GitHub.
2. Open pull request.
3. Wait for CI to pass.
4. Review changes.
5. Merge to main.
6. Confirm production deployment.
7. Run smoke tests.

## Preview Deployments

Each PR should create a preview deployment when supported.

## Production Checklist

- [ ] CI passed
- [ ] Environment variables added
- [ ] Database migrations complete
- [ ] Webhooks configured
- [ ] Domain configured
- [ ] Smoke test complete
- [ ] Rollback plan known

## Rollback Plan

- Revert the PR
- Redeploy previous build
- Restore database backup if needed
- Disable broken feature flag if available

## Smoke Test

After deployment:

1. Visit homepage
2. Test login/auth flow
3. Test main product flow
4. Test admin flow if applicable
5. Check error logs
6. Check analytics/events if applicable
