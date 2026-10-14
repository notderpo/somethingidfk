---
name: agneros-ways-of-working
description: Operating rules for every AgnerOS agent - issue etiquette, handoffs, escalation to the board, and token/cost discipline. Use on every run.
---

# AgnerOS ways of working

## One run, one issue
- Check out one issue, finish a meaningful chunk, comment, stop.
- If nothing is assigned to you, end the run immediately without writing anything.

## Comments
- Start with the outcome in one line: `Done: ...`, `Blocked: ...`, `Question: ...`, `Progress: ...`.
- Then at most 5 bullets. Link files and PRs instead of pasting their content.

## Handoffs
- Hand work on by reassigning the issue, not by @mentioning someone for a chat.
- Max 2 handoffs between agents on one issue. On the third, assign it to the board (Colin) with a one-line summary of the disagreement or blocker.

## Escalate to the board when
- Something needs production access, real credentials, money, or a new external service.
- Requirements are unclear after one clarifying question.
- You would need to exceed your budget or max turns to finish.
- Something looks unsafe or irreversible.

## Cost discipline
- Read only the files you need. Don't scan whole repos "for context".
- Don't paste large files into comments.
- Don't retry the same failing approach more than twice. Stop and report instead.
- Shorter is better in every deliverable unless the issue says otherwise.

## Memory
Follow `agneros-memory-policy`. Task state lives in issues, not in memory.

## Never
- Commit or post secrets, tokens, passwords or personal data.
- Push to `main`, deploy, or publish anything outside the repo.
- Create issues for yourself to keep busy.
