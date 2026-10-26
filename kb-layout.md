# Recommended private KB layout

Keep this folder **private and local**. Never commit it to a public repo.

```
<kb path>/competitive-kb/
  config/
    home-vendor.yaml            # copied from config/home-vendor.example.yaml
  portfolio/                    # one folder per <home vendor> product line
    <product-line>/
      overview.md               # what it is, packaging, licensing model
      capabilities.md           # cited capability entries
      metrics.md                # TCO/perf/scale evidence, each with confidence
      roadmap.md                # publicly announced roadmap only, dated
  competitors/                  # one folder per competitor
    <competitor>/
      profile.md                # company/portfolio overview, sources
      <product-line>.md         # how this competitor competes in that line
      pricing-licensing.md      # public pricing/licensing evidence, dated
  analysts/
    analyst-report-log.md       # every report: firm, title, date, placements (public only)
    <firm>/                     # notes from public summaries, title/date citations
  comparisons/
    <product-line>-vs-<competitor>.md   # comparison matrices (templates/comparison-matrix.md)
  deliverables/
    briefs/
    battlecards/
    exports/                    # PDF/Pages renders
  _meta/
    gaps.md                     # questions not yet answered
    staleness-report.md         # output of the monthly sweep
    changelog.md                # what changed and when
```

## Conventions

- File names: lowercase, hyphenated. Dates: ISO `YYYY-MM-DD`.
- Every factual file uses `templates/kb-entry.md` frontmatter.
- Staleness defaults (override in config): pricing/licensing 90 days, capabilities 180 days, analyst positions until the next edition, roadmap 90 days.
- Deliverables link back to KB entries rather than restating unsourced facts.
- Mark anything with customer or deal context `visibility: internal` and keep it out of `deliverables/exports/` meant for sharing.
