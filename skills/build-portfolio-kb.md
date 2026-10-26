# Skill: build-portfolio-kb

Build or extend the `<home vendor>` portfolio section of the private KB.

## When to use
- First-time setup, a new `<product line>`, or a major release/rebrand.

## Inputs
- `config/home-vendor.yaml` (product lines and products)
- Optional: one `<product line>` id to limit scope

## Steps
1. Read the config. For each product line in scope, create `portfolio/<product-line>/` with `overview.md`, `capabilities.md`, `metrics.md`, `roadmap.md` from `templates/kb-entry.md`.
2. State search boundaries in `overview.md`: sources searched, date range, exclusions.
3. Gather **primary sources first**: official docs, datasheets, release notes, public pricing/licensing pages, compatibility lists, public filings, published benchmarks (note who ran them).
4. Record each fact as a separate bullet with an inline citation `[S#]` and a Sources table (source, url, date_published, date_retrieved, confidence).
5. Capture the licensing model (per core, per node, per VM, per user, subscription term, bundles) exactly as published. If not public, write "not public" and log it in `_meta/gaps.md`.
6. Roadmap: publicly announced items only, with announcement date. Mark "announced, not GA" clearly.
7. Rate confidence per fact: High / Med / Low. Never fill a field from memory.
8. Append a line to `_meta/changelog.md`.

## Output
- Updated `portfolio/` files and a short summary: what was added, top gaps, lowest-confidence items.

## Do not
- Invent figures, paste marketing copy as fact, or include customer/deal data.
