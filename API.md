# API.md

<!--
Purpose:
This document tracks API routes, server actions, webhooks, external APIs,
request/response shapes, and error formats.
-->

## API Strategy

<!--
Example: REST API routes, Next.js server actions, GraphQL, SDK calls, or mixed.
-->

Current approach:

```txt
Client
  -> Server Action / API Route
  -> Service Layer
  -> Database or External API
```

## Authentication

- Auth method:
- Session source:
- Required headers:
- Role checks:

## Standard Success Response

```json
{
  "success": true,
  "data": {}
}
```

## Standard Error Response

```json
{
  "success": false,
  "error": {
    "code": "ERROR_CODE",
    "message": "Human-readable error message"
  }
}
```

## API Routes

### `GET /api/example`

**Purpose:**  
Describe endpoint.

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
| `UNAUTHORIZED` | User is not authenticated |
| `NOT_FOUND` | Resource not found |

---

### `POST /api/example`

**Purpose:**  
Describe endpoint.

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

| Action | File | Purpose |
|---|---|---|
| `createExample` | `app/actions/example.ts` | Creates example data |

## Webhooks

| Provider | Route | Purpose | Verification |
|---|---|---|---|
| Example | `/api/webhooks/example` | Handles event | Signature check |

## External APIs

| Service | Purpose | Env Vars |
|---|---|---|
| Example | Example service | `EXAMPLE_API_KEY` |
