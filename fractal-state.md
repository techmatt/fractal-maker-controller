# fractal-state — ckpt 25, 2026-08-01

**Rewritten in full at EVERY distillation — the only doc guaranteed to be.** Holds NO FACTS: status, plan, flags, open/parked, manifest. A fact that needs recording forces its owner doc onto the touched list (fractal-operating).

**This checkpoint = the maneuver-exploration era closed.** Dry run → view screen v2/v3 (v4 measured and rejected) → the supply crawl → four label batches built, verified, UNLABELED. First distillation under the CC-applied-diffs mechanism (fractal-operating).

## THE GOAL (Matt, stated plainly — unchanged)
Two learned functions: **(a) find good minibrots** — a SCREENING problem over maneuver targets — and **(b) find the q4 within a neighbourhood** (guided descent, "nothing specific to do with minibrots"). Full automation the target; manual isolation is scaffolding.

## THE PLAN
**(1–5) ~~done~~ (v8 · re-render/retrain · maneuvers · probe · THE CRAWL) · (6) Matt LABELS the four batches ← next · (7) the linear neighborhood-quality fit + v10 retrain on the new labels — THE FLIP; re-derive t_good + keeper cuts + τ_h together · (8) evaluate the maneuvers (now readable) · (9) THE HUNT — relights emission · (10) guided descent (harness resumes) · (11) one production campaign.**
- Labeling order when Matt sits down: strat_a → strat_b → uniform → exemplar (the confound reads depend on strat coverage; see fractal-corpus/discovery).
- Nothing urgent, no early deliverables. Harness stays SHELVED until step 10.

## STATUS
- **EMISSION IS DARK** (unchanged since the v8 flip) — the hunt relights it; scheduler-off until a v8-era run rebuilds the seed.
- Discovery last ran: the supply crawl (this checkpoint's run; results in fractal-discovery). Batches: 730 rows / 4 registered methods, crops rendered and verified, awaiting labels.
- Suite 1,025 Python + 73 Rust, green. `main` ahead of `origin/main`, unpushed (SSH auth fails on this machine).

## STALENESS FLAGS
- **thresholds:** everything pre-cap-raise still on a moved distribution — `t_good` + keeper cuts + τ_h re-derive TOGETHER at step 7 (`deferred_recalibration.md`).
- **discovery:** economics EMA stale until a v8-era run refreshes it; ring scores pre-2026-07-31 on the old maxiter scale.
- **orchestration:** library seed unavailable in principle — scheduler-off stands.
- **models:** v8 on maneuver views is measured non-separating (fractal-models) — no head reads that population until v10.

## OPEN ITEMS — recorded, not scheduled
`scratch/view_screen_v2_report.md` + `REPORT_composite_v3.md` still in scratch; both justified durable decisions — extract-and-delete pending · the framing sweep never ran on the crawl population · the exemplar labeling leg is the weakest (derivation, not verdict — fractal-corpus) · depth lever = `M_CAP` + root supply, not budget (fractal-discovery) · `coevo/` retirement verdict — Matt's call · `scratch/maneuver_degree_report.md` Part 3 extract-or-delete pending.

## PARKED — named, not half-open
The variety measure (one answer with emission diversity) · composition (the screen's known ceiling; the learned fit inherits the question) · Douady tuning (unblocked, unbuilt) · perturbation in `render-one` · probe as a standing audit · the recolor-batching executor (next cache rebuild) · the wall display's `id_map` rewiring · the deferred-recalibration cluster · wider aug palette set (next rebuild) · mining-gate calibration.

## MANIFEST — replace only files listed as touched; ceilings never increase without Matt
| doc | last touched | wc -c | ceiling |
|---|---|---|---|
| fractal-operating | ckpt 25b (rewrite) | 12,939 | 13,000 |
| fractal-state | ckpt 25 (rewrite) | 4,370 | 6,000 |
| fractal-engine | ckpt 24 | 10,513 | 11,000 |
| fractal-storage | ckpt 24 | 5,759 | 6,000 |
| fractal-orchestration | ckpt 25 (hunks) | 3,599 | 4,000 |
| fractal-models | ckpt 25 (hunks) | 7,503 | 8,000 |
| fractal-thresholds | ckpt 24 | 4,716 | 5,000 |
| fractal-corpus | ckpt 25 (hunks) | 7,863 | 8,000 |
| fractal-discovery | ckpt 25 (rewrite) | 9,032 | 13,000 |
| fractal-emission | ckpt 24 | 5,598 | 6,000 |

⟨FILL⟩ = measured by the apply-prompt after it applies; it replaces each token with `wc -c` of the file it just wrote. fractal-discovery remains the hottest doc and first split candidate at ceiling pressure.
