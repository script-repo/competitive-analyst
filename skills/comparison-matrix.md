# Skill: comparison-matrix

Produce a normalized, cited comparison of `<home vendor>` `<product line>` vs one or more `<competitor>`s.

## Steps
1. **Scope**: product line, competitors, audience (exec / technical / pricing), use case, deployment size. Write it at the top.
2. **Check the KB**. Refresh any entry older than its staleness threshold before using it (run `refresh-kb` on just those entries).
3. **Normalize** into `templates/comparison-matrix.md` rows: capabilities, outcomes, TCO, licensing model, performance, scale, ops effort, ecosystem, support, roadmap.
4. For each cell: the finding, citation `[S#]`, confidence H/M/L. Empty is allowed: write "not found".
5. **TCO and pricing**: only from published prices or clearly labelled estimates. For estimates, show the formula, inputs, sources, and a sensitivity range (e.g. ±20% on the largest inputs). Compare like for like (same workload, term, support tier). Segment; don't average across very different buyers.
6. **Performance**: cite who ran the test, the configuration, and the date. Vendor-run benchmarks are Med at best.
7. **Verdict per row**: win / contested / lose for `<home vendor>`, with one-line rationale. Be willing to mark "lose".
8. **Overall confidence** cannot exceed the weakest source that a key conclusion depends on.
9. Save to `comparisons/<product-line>-vs-<competitor>.md`; list open gaps at the end.
