---
name: agneros-memory-policy
description: AgnerOS rules for what to remember, where, and how little. Applies on top of para-memory-files. Use whenever you are about to store, recall or synthesize memory.
---

# AgnerOS memory policy

`para-memory-files` is the mechanism. This skill is the policy. Memory is re-read on future runs, so every line you keep costs tokens forever. Keep it small and true.

## Three places, three jobs
| Where | Holds | Who writes |
|---|---|---|
| Company files: `COMPANY.md`, `DECISIONS.md`, repo `docs/`, `channel/` | Shared truth: context, decisions, architecture, runbooks | Board, Holt (DECISIONS), agents via PR (docs) |
| Issues and comments | Task state: what's done, blocked, next | Everyone |
| Your personal memory | Durable lessons only you need | You |

If something belongs in the first two, it does not go in your memory.

## Store
- Board feedback and corrections, as a rule: "Colin: no `latest` tags, pin versions". Highest priority.
- Recurring gotchas: "Nextcloud upgrade needs occ upgrade after container start".
- Stable facts you will need again and that aren't in company files: reliable sources, codebase conventions, service quirks.
- Patterns: "Colin cuts history sections longer than 2 minutes".

## Never store
- Task status or progress (the issue holds it)
- Copies or summaries of COMPANY.md, DECISIONS.md, repo files, research.md
- Secrets, tokens, passwords, internal IPs
- Private details about Colin, his partner, friends or finances
- Raw search results, long quotes, full diffs
- Guesses about what Colin wants. Only what he said or did.

## Cadence and size
- Daily note: only on days you learned something durable. Max 5 lines (Holt), 3 lines (everyone else).
- Weekly synthesis: on your first run 7+ days after the last synthesis, fold daily notes into tacit knowledge, drop what is stale or now covered by company files, archive notes older than 30 days.
- Tacit knowledge stays under ~80 lines. Over that: merge, generalise, delete.

## Recall
- Recall by topic for the issue at hand (targeted qmd query). Don't load all memory "for context".
- Company files beat memory. If memory contradicts `DECISIONS.md` or a repo doc, the file wins: fix your memory.

## Board said "forget"
Delete the fact and anything derived only from it. Don't soften it into "used to".
