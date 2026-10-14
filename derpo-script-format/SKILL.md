---
name: derpo-script-format
description: Structure and markup for DerpO video scripts - cold open, sections, skit blocks, B-roll and on-screen cues, claim references, timing. Use when writing or reviewing a script.
---

# DerpO script format

File: `videos/<slug>/script.md`

```
# <Working title>
Pillar: Think | Wrench | Ride   Target length: <min>   Research: research.md

## Cold open (0:00-0:45)
VO: ...
[B-ROLL: what to show]
[ON-SCREEN: text, Barlow Black]

## Section 1: <name> (~mm:ss)
VO: ... [C3]
...

## SKIT: <name>
SETTING: ...
CHARACTERS: ...
DIALOGUE:
NAME: line
(action)
END SKIT

## Outro (~0:30)
VO: ...
```

Rules:
- About 140-150 spoken words per minute; state the estimated runtime at the top.
- Every factual statement carries its claim ID `[Cn]` from research.md.
- Cue lines: `[B-ROLL: ...]`, `[ON-SCREEN: ...]`, `[SFX: ...]`, `[MUSIC: ...]`.
- Cold open ends on an open question the video answers.
- No section without a point; cut anything that doesn't serve the title's promise.
