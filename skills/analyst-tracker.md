# Skill: analyst-tracker

Track industry analyst evaluations relevant to each `<product line>`.

## Source types
- Gartner: Magic Quadrant, Critical Capabilities, Peer Insights
- IDC: MarketScape, market share trackers
- Forrester: Wave
- GigaOm: Radar
- Others as configured

## Steps
1. For each product line, identify the relevant report families and their latest editions.
2. Log each edition in `analysts/analyst-report-log.md` using `templates/analyst-report-log.md`: firm, exact title, publication date, market covered, where `<home vendor>` and each `<competitor>` were placed **as publicly disclosed**, the public source of that disclosure (vendor press release, firm's public page), and date retrieved.
3. Paywalled content: cite **title, firm, and date only**. Do not reproduce text, charts, scores, or rankings that are not publicly released. Vendor reprints may be cited by title and date; do not copy them into the KB.
4. Note edition-to-edition movement only when both editions' placements are publicly sourced.
5. Peer-review platforms: record aggregate rating, review count, and retrieval date; ratings drift, so always date them.
6. Flag any placement claim you cannot trace to a public source as Low confidence, or omit it.

## Output
- Updated log, plus a short "what changed" note per product line.
