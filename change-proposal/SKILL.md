---
name: change-proposal
description: How to propose any change to agner.cloud or Colin's apps as a pull request with risk rating, deploy steps, verification and rollback. Use whenever opening a PR.
---

# Change proposal (PR format)

Branch: `aos-<issue-number>-<short-slug>`. Never push to `main`.

PR description:

```
## What and why
<2-3 sentences, link the issue>

## Risk: low | medium | high
low = docs/monitoring only; medium = config change, restart needed; high = data migration, auth change, anything touching Pocket ID, NetBird, Cloudflare Tunnel or backups.

## Deploy steps (for Colin)
1. <exact commands or Arcane actions>

## Verification
- <exact checks: URL, command, expected output>

## Rollback
1. <exact steps back to the previous state, including data if relevant>

## Secrets / env changes
- <new variables, where Colin should put the real values (1Password)>
```

Rules:
- If you can't write a real rollback, the risk is high. Say so.
- Keep PRs small: one service or one feature per PR.
- After opening: comment the PR link on the issue and reassign to Platform Lead.
