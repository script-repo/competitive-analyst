# Routine: weekly analyst and news refresh

- Schedule: weekly, e.g. Monday 08:00 local time
- Skills used: analyst-tracker, refresh-kb

## Steps
1. Search for new analyst editions and public placement announcements for each `<product line>` in config.
2. Search news, release notes, and pricing/licensing pages for `<home vendor>` and each configured `<competitor>` since the last run.
3. Log new items as KB entries (`type: news` or `analyst`), with dates and confidence; rate signal strength (weak/moderate/strong).
4. Flag comparisons and battlecards affected by any strong signal as "needs review".
5. Produce a short digest: new analyst items, notable competitor moves, deliverables needing review, new gaps. Save to `deliverables/briefs/weekly-YYYY-MM-DD.md`.

## Guardrails
- Draft only; do not send or post the digest. A human decides distribution.
- Paywalled reports: title/firm/date only.
