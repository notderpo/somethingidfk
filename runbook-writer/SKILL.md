---
name: runbook-writer
description: Fixed format for per-service runbooks in agner-cloud-stacks (<service>/README.md), written so they can be pasted into AFFiNE. Use when documenting a service.
---

# Runbook format

`<service>/README.md`:

```
# <Service>
Purpose: <one line>  
URL: <url> (public | NetBird-only)  
Auth: Pocket ID OIDC | NetBird-only | own login (explain why)  
Compose: /opt/stacks/<service>/compose.yaml  

## Data
- Volumes / paths and what lives there
- What must be backed up, and how to restore it

## Config
- Key env variables (see .env.example)
- OIDC client settings in Pocket ID (callback URL, scopes)

## Operations
- Start / stop / logs (Arcane and CLI)
- Update procedure (tag bump, migrations, breaking-change check)

## Known issues
- <gotchas, workarounds>
```

Rules: facts only from the repo and the issue. Unknowns go under "Known issues" as `TODO (Colin): <question>`. Keep it under one screen where possible.
