# API.md

<!--
Purpose:
This file documents API routes, server actions, external APIs, request/response shapes, and error patterns.

How to use:
Update this whenever an endpoint, server action, webhook, or integration is added or changed.
-->

## API Overview

<!--
Explain whether this project uses REST, GraphQL, server actions, SDK calls, or a mix.
-->

Architecture:

```txt
Client
  -> Server Action / API Route
  -> Service Layer
  -> Database or External API
```

## Authentication

<!--
Explain how API calls are authenticated.
-->

- Auth method:
- Session source:
- Required headers:
- Role checks:

## Error Format

<!--
Standardize errors so UI can handle them consistently.
-->

Example:

```json
{
  "success": false,
  "error": {
    "code": "VALIDATION_ERROR",
    "message": "Invalid input."
  }
}
```

## Success Format

Example:

```json
{
  "success": true,
  "data": {}
}
```

## API Routes

<!--
Copy this template for each route.
-->

### `GET /api/example`

**Purpose:**  
Describe what this endpoint does.

**Auth Required:** Yes/No

**Query Params:**

| Name | Type | Required | Description |
|---|---|---:|---|
| `id` | string | yes | Example ID |

**Response:**

```json
{
  "success": true,
  "data": {}
}
```

**Errors:**

| Code | Meaning |
|---|---|
| `UNAUTHORIZED` | User is not logged in |
| `NOT_FOUND` | Resource does not exist |

---

### `POST /api/example`

**Purpose:**  
Describe what this endpoint creates or changes.

**Auth Required:** Yes/No

**Request Body:**

```json
{
  "name": "Example"
}
```

**Response:**

```json
{
  "success": true,
  "data": {
    "id": "example-id"
  }
}
```

## Server Actions

<!--
If using Next.js server actions, document them here.
-->

| Action | File | Purpose |
|---|---|---|
| `createExample` | `app/actions/example.ts` | Creates an example record |

## Webhooks

<!--
Document Stripe, Shopify, Clerk, Sanity, or other webhooks here.
-->

| Webhook | Provider | Route | Purpose |
|---|---|---|---|
| Example webhook | Provider | `/api/webhooks/example` | Handles event |

## External APIs

<!--
Document third-party services here.
-->

| Service | Purpose | Docs | Env Vars |
|---|---|---|---|
| Example | Example purpose | Example URL | `EXAMPLE_API_KEY` |
