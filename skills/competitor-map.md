# Skill: competitor-map

Map who competes with `<home vendor>` in each `<product line>`, and how.

## Steps
1. For each product line, list competitors by category: direct, adjacent-platform, oem-hardware, public-cloud, emerging, status-quo-diy. Include the do-nothing option; it is often the real rival.
2. For each `<competitor>`, create or refresh `competitors/<competitor>/profile.md` and `competitors/<competitor>/<product-line>.md` using `templates/kb-entry.md`.
3. In each product-line file capture, with citations:
   - Positioning in their own words (quote briefly, cite)
   - Target buyer and typical deployment
   - Packaging and licensing model (public info only, dated)
   - Strengths: steelman, as their happiest customers would put it
   - Known limitations: only from verifiable sources (docs, release notes, peer reviews), never rumor
   - Recent moves: acquisitions, licensing changes, major releases (dated)
4. Signal strength for each "recent move": weak / moderate / strong, with the reason.
5. Build a summary table per product line: competitor, category, overlap (high/med/low), last refreshed, confidence.
6. Log unknowns in `_meta/gaps.md`.

## Output
- `competitors/` entries plus a per-line map table, saved to `comparisons/<product-line>-landscape.md`.
