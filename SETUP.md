# SETUP.md

<!--
Purpose:
This file explains how to run the project locally.
Keep README clean and put detailed setup steps here.
-->

## Prerequisites

Install:

- Node.js:
- pnpm:
- Git:
- Database CLI:
- Optional tools:

## Install Dependencies

```bash
pnpm install
```

## Environment Variables

Copy:

```bash
cp .env.example .env.local
```

Then fill in the values.

## Local Development

```bash
pnpm dev
```

Open:

```txt
http://localhost:3000
```

## Database Setup

<!--
Customize this section for Supabase, Prisma, Drizzle, Postgres, MongoDB, etc.
-->

```bash
# Example
pnpm db:migrate
pnpm db:seed
```

## CMS Setup

<!--
Customize if using Sanity, Contentful, Shopify, Payload, etc.
-->

Add CMS setup instructions here.

## Payment Setup

<!--
Customize if using Stripe, Lemon Squeezy, Shopify, etc.
-->

Add payment setup instructions here.

## Email Setup

Add email provider setup instructions here.

## Common Errors

### Error: Missing Environment Variable

Fix:

```bash
cp .env.example .env.local
```

Then fill required values.

### Error: Dependency Install Failed

Fix:

```bash
rm -rf node_modules pnpm-lock.yaml
pnpm install
```

## Useful Commands

```bash
pnpm dev
pnpm lint
pnpm typecheck
pnpm build
pnpm test
```
