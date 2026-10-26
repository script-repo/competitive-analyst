# Skill: refresh-kb

Refresh stale or targeted KB entries.

## Inputs
- A list of entries, a product line, a competitor, or "all stale" (uses `staleness_days` from config).

## Steps
1. Find entries whose `date_retrieved` exceeds the threshold for their type, or that are listed in `_meta/gaps.md`.
2. Re-open each cited URL. If it changed, update the fact, `date_retrieved`, and confidence. If it is gone, find a replacement primary source or downgrade confidence and note "source unavailable as of <date>".
3. Search for newer sources: release notes, pricing/licensing changes, analyst editions, major announcements.
4. Never silently overwrite: keep a dated "Previously" line when a fact changes materially.
5. Re-check any comparison or deliverable that cites a changed entry; flag it "needs review".
6. Update `_meta/changelog.md` and `_meta/staleness-report.md`.

## Output
- Summary: refreshed, changed, still stale, new gaps, deliverables needing review.
