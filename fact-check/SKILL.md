---
name: fact-check
description: Research and fact-checking method for DerpO - claims table with IDs, sources, confidence, and handling of regulations, specs and sales numbers. Use for research and whenever a script states a fact.
---

# Fact-check

File: `videos/<slug>/research.md`

```
# Research: <topic>
## Summary (5 lines max)
## Timeline
| Year | Event | Claim ID |
## Claims
| ID | Claim | Source (link) | Source type | Confidence |
## Contested / uncertain
## Open questions (for Colin)
```

Source type: primary (manufacturer, regulator, official results, registry) / secondary (trade press, reputable media) / tertiary (wiki, forums - pointer only, never sole source).

Confidence:
- **High**: primary source, or two independent secondary sources.
- **Medium**: one reputable secondary source.
- **Low**: anything else. Low claims don't go into scripts as fact; they can be framed as "reportedly" only with Colin's OK.

Specific rules:
- Regulations (licence categories like A2, emissions norms): cite the regulation text and its effective date; note Swiss vs EU differences.
- Specs (hp, kg, prices): note model year and market; specs differ by region.
- Sales and market numbers: name the registry/source, region and year. Never round in a misleading way.
- Quotes: exact wording, speaker, date, link. No paraphrase in quote marks.
