# ARCHITECTURE.md

<!--
Purpose:
This document explains how the system is structured.
Agents should use this as the source of truth for architecture.
-->

## System Overview

```txt
Client/UI
  -> Routes / Pages
  -> Server Actions or API Routes
  -> Service Layer
  -> Database / CMS / External APIs
```

## Folder Structure

```txt
app/
  # routes, layouts, pages, API routes

components/
  # reusable UI and feature components

lib/
  # shared helpers, clients, utilities

services/
  # business logic and external service wrappers

hooks/
  # reusable client hooks

types/
  # shared TypeScript types

db/
  # schema, migrations, seed files

docs/
  # project documentation
```

## Architectural Principles

- Keep route files light.
- Put business logic in services or server actions.
- Keep UI reusable and composable.
- Keep secrets server-side.
- Validate inputs at the boundary.
- Prefer explicit data flow.
- Avoid hidden global state.

## Frontend Architecture

- Framework:
- Routing:
- Styling:
- Component library:
- Forms:
- Client state:
- Server state:
- Error handling:

## Backend Architecture

- API style:
- Server actions:
- Validation:
- Service layer:
- Background jobs:
- Logging:
- Error handling:

## Database Architecture

| Table/Collection | Purpose | Notes |
|---|---|---|
| `users` | User profile/account data | Example |
| `items` | Main product data | Example |

## Auth Architecture

- Provider:
- Session strategy:
- Protected routes:
- User roles:
- Admin permissions:

## Data Flow

### Example Flow

```txt
User submits form
  -> Form validation
  -> Server action/API route
  -> Service function
  -> Database write
  -> UI refresh/toast
```

## External Services

| Service | Purpose | Env Vars |
|---|---|---|
| Example | Example purpose | `EXAMPLE_API_KEY` |

## Security Architecture

- Authentication required for private routes.
- Authorization checked server-side.
- Webhooks must verify signatures.
- Secrets must never be exposed to client code.
- Input validation required before writes.

## Performance Architecture

- Optimize images.
- Cache read-heavy data where safe.
- Avoid unnecessary client components.
- Split large components.
- Avoid heavy dependencies unless justified.

## Known Tradeoffs

- Tradeoff 1:
- Tradeoff 2:
- Tradeoff 3:
