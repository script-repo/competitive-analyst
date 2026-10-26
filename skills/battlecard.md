# Skill: battlecard

Turn a comparison matrix into a one-page field battlecard. Substance, not FUD.

## Prerequisite
- A current `comparisons/<product-line>-vs-<competitor>.md`. If missing or stale, run `comparison-matrix` first.

## Steps
1. Fill `templates/battlecard.md`.
2. **Their best case** first: the strongest honest argument for `<competitor>`.
3. **Zones**: where `<home vendor>` wins, where it is contested, where it loses. Use the matrix verdicts.
4. **Fact / Impact / Action** for each differentiator: a cited fact, why it matters to this buyer, what the seller should do or show.
5. **Discovery questions**: neutral questions that surface requirements where `<home vendor>` is strong (e.g. "How do you handle X at Y scale today?"). No trick questions; no disparagement.
6. **Objection handling**: likely objection, the root concern behind it, a cited response.
7. **Counter-move check**: for each key argument, the competitor's likely rebuttal and your answer (a quick war-game).
8. **Do not say**: claims that are unverified, outdated, or FUD.
9. Mark INTERNAL. Include Sources and last-refreshed date. Save to `deliverables/battlecards/`.
