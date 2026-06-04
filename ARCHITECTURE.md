# ARCHITECTURE.md

<!--
Purpose:
This file explains how the system is structured.
Agents should read this before making architecture or implementation decisions.

How to use:
Keep this updated when you add major folders, services, integrations, database tables, or data flow changes.
-->

## Architecture Overview

<!--
Describe the system at a high level.
-->

Example:

```txt
User Interface
  -> App Routes / Pages
  -> Server Actions / API Routes
  -> Services / Lib Layer
  -> Database / CMS / External APIs
```

## Folder Structure

<!--
Update this to match your repo.
-->

```txt
app/
  # Routes, layouts, pages, API routes

components/
  # Reusable UI and feature components

lib/
  # Shared utilities, clients, helpers

services/
  # Business logic and external service wrappers

hooks/
  # React hooks

types/
  # Shared TypeScript types

db/
  # Database schema, migrations, seed files

docs/
  # Extra documentation
```

## Data Flow

<!--
Explain how data moves through the app.
-->

Example:

```txt
Client Component
  -> Server Action
  -> Validation
  -> Database Query
  -> Response
  -> UI Update
```

## Frontend Architecture

<!--
Explain UI patterns, component strategy, routing strategy, state management, etc.
-->

- Routing:
- Components:
- State management:
- Forms:
- Validation:
- Error handling:

## Backend Architecture

<!--
Explain API routes, server actions, service layer, background jobs, etc.
-->

- API pattern:
- Server actions:
- Services:
- Background jobs:
- Error handling:

## Database Architecture

<!--
List tables or collections when known.
-->

| Table/Collection | Purpose | Notes |
|---|---|---|
| `users` | User profile data | Example |
| `items` | Main app records | Example |

## Authentication

<!--
Explain how users log in and how protected routes work.
-->

- Auth provider:
- Session strategy:
- Protected routes:
- Roles/permissions:

## External Integrations

<!--
Add all external services here.
-->

| Service | Purpose | Environment Variables |
|---|---|---|
| Example Service | Example purpose | `EXAMPLE_API_KEY` |

## Security Notes

<!--
Agents should pay attention to this section.
-->

- Never expose server-only secrets to the browser.
- Validate all user input.
- Use least-privilege API keys.
- Protect admin routes.
- Avoid logging sensitive data.

## Performance Notes

<!--
Add important performance decisions here.
-->

- Cache where appropriate.
- Avoid unnecessary client components.
- Keep images optimized.
- Minimize large dependencies.

## Architecture Decisions

<!--
Add important technical decisions with reasons.
-->

### Decision 001: [Decision Name]

**Decision:**  
Describe the decision.

**Reason:**  
Explain why this was chosen.

**Tradeoffs:**  
Explain what this makes better or worse.
