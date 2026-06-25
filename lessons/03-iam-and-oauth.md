# 03 - IAM And OAuth

## Core Idea

Identity and access management determines who can do what, on whose behalf, against which resource, under which conditions.

## Building Blocks

- User identity.
- Organization or tenant identity.
- Application identity.
- API keys for app-level access.
- OAuth for delegated access.
- Scopes for permission boundaries.
- Audit logs for accountability.

## OAuth Flow

```mermaid
sequenceDiagram
  participant User
  participant App
  participant Auth as Authorization Server
  participant API
  User->>App: Start integration
  App->>Auth: Request authorization with scopes
  Auth->>User: Consent screen
  User->>Auth: Approve
  Auth->>App: Authorization code
  App->>Auth: Exchange code for token
  App->>API: Call API with access token
  API-->>App: Scoped response
```

## Product Decisions

- Which permissions need explicit consent?
- Which roles can create apps or keys?
- How are tokens revoked?
- What is visible in the audit trail?

