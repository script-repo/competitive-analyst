# Routine: monthly KB staleness sweep

- Schedule: monthly, e.g. first business day, 09:00 local time
- Skill used: refresh-kb

## Steps
1. Scan all KB entries; compare `date_retrieved` with `staleness_days` thresholds in config.
2. List stale entries by product line and type; refresh the highest-impact ones first (anything cited by a current battlecard or comparison).
3. Check for broken URLs and missing frontmatter fields (source, url, date_published, date_retrieved, confidence).
4. Review `_meta/gaps.md`: close answered gaps, re-prioritize the rest.
5. Write `_meta/staleness-report.md`: counts, refreshed items, still-stale items, deliverables needing review.

## Guardrails
- Never update a fact without a new citation. Downgrade confidence rather than guess.
