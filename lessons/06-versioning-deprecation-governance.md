# 06 - Versioning, Deprecation, And Governance

## Core Idea

API change is a product problem. Versioning and deprecation policies protect developer trust while giving the platform room to evolve.

## Governance Rules

- Breaking changes require a new major version or explicit migration path.
- Deprecation notices should include dates, impact, replacement APIs, and support contact.
- High-usage APIs require migration analytics before retirement.
- Docs, SDKs, examples, and changelogs must be updated together.

## Deprecation Timeline

```mermaid
gantt
  title API Deprecation Timeline
  dateFormat  YYYY-MM-DD
  section Lifecycle
  Announce deprecation        :a1, 2026-01-01, 30d
  Migration support           :a2, after a1, 90d
  Freeze new app access       :a3, after a2, 30d
  Retire legacy endpoint      :a4, after a3, 1d
```

