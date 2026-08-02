# fractal-state — ckpt 26 (PARTIAL), 2026-08-02

**Rewritten in full at EVERY distillation — the only doc guaranteed to be.** Holds NO FACTS: status, plan, flags, open/parked, manifest. **This is a PARTIAL distillation (Matt-sanctioned): the v10 build prompt is OUTSTANDING at the code CC; only v10-independent docs were emitted. models + thresholds are deliberately untouched — they are the flip's cargo; the flip-era distillation re-touches them and state.**

**This checkpoint = the label-and-fit era closed.** Crawl labeled (730, incl. 81 by Matt's interior rule) → `view_fit` built, beats the hand screen → label-seeded harvest built+run → its 580 labels delivered 23 class-4s = the v10 GO → v10 build launched. Five pre-distill decisions taken; a read-only claim-verification pass ran (findings folded into the docs and the closeout list).

## THE GOAL (Matt, unchanged)
Two learned functions: **(a) find good minibrots** (a SCREENING problem over maneuver targets) and **(b) find the q4 within a neighbourhood** (guided descent). Full automation the target; manual isolation is scaffolding. NEW: the label-seeded loop's measured arithmetic ≈1.5 new goods per good seed — self-sustaining once v10 lets maneuvers trigger on admissions (fractal-discovery).

## THE PLAN
**(1–6) ~~done~~ (v8 · re-render/retrain · maneuvers · the crawl · LABELS · the fit + label-seeded harvest + its labels) · (7) v10 build ← IN FLIGHT (prompt out: cache extend, uniform-90 promoted to EVAL, recipe frozen) · (8) THE FLIP — adopt against the pre-registered bars; re-derive t_good + keeper cuts + τ_h TOGETHER; the flip prompt must CARRY the full procedure (see staleness) · (9) closeout sweep (below) · (10) flip-era distillation (models/thresholds/state) · (11) profiling/optimization · (12) THE LONG HARVEST — absorbs the hunt, relights emission · (13) guided descent (harness resumes; seed library = crawl+harvest rows ≥2) · (14) one production campaign.**

## STATUS
- **EMISSION IS DARK** (unchanged since the v8 flip) — the long harvest relights it; scheduler-off stands.
- Corpus grew +1,310 labeled rows this era (730 crawl / 580 harvest); crawl held zero class-4, harvest held 23 (fractal-discovery owns the numbers).
- `view_fit_v1.1` = sourcing sort key ONLY; `composite_v3` live everywhere else.
- Suite 1,081 Python + 73 Rust green (pre-v10-build).

## STALENESS FLAGS
- **thresholds:** pre-cap-raise moved-distribution caveat stands; **`docs/design/deferred_recalibration.md` is INTENTION-ONLY and scopes a different cluster [verified 2026-08-02, read-only pass] — it names t_good once and keeper cuts never. The flip prompt carries the full t_good+keeper+τ_h re-derivation procedure itself; fix the doc pointer at the flip-era distillation.**
- **models:** v8 measured non-separating on maneuver views until v10; v10 build outstanding. **CLAUDE.md mis-states K history — v8 is the first K=4 head [verified]; closeout fixes.**
- **discovery:** economics EMA stale until a v10-era run.
- **orchestration:** library seed unavailable in principle — self-heals at the long harvest; scheduler-off meanwhile.

## CLOSEOUT SWEEP (one prompt, after the flip)
Delete `coevo/` — all-channels liveness grep first (mechanics only; stop-and-report if a live consumer surfaces), then directory + index line + every mention vanish · extract-and-delete `scratch/view_screen_v2_report.md`, `REPORT_composite_v3.md`, `maneuver_degree_report.md` Part 3 · deliberately live-fire the budget caps (active / wall / STOP-sentinel — three runs, never fired; untested ≠ working) · re-check the blocked ~285 MiB v8/v9 plan-pair deletion after v10's cache extension moved the parity-gate preconditions · **fix `descriptor.py`'s stale `auto_maxiter` mirror (500/8000 vs production 4000/67000) and extend the pin test to cover it — emission intake re-renders at the OLD cap until fixed [verified 2026-08-02]** · CLAUDE.md K-history fix · `load_admitted` docstring `==` → `>=`.

## OPEN ITEMS — recorded, not scheduled
Matt owes: the julia-near-minibrots eyeball test — now load-bearing for the long harvest's julia channel, not just a variety curiosity.

## PARKED — named, not half-open
The variety measure (one answer with emission diversity) · composition (the fit inherits the question) · Douady tuning (unblocked, unbuilt) · perturbation in `render-one` · probe as a standing audit · the recolor-batching executor (unless v10's cache-extend estimate forced it) · wider aug palette set (re-parked at v10: labels were the single variable) · mining-gate calibration (accrues free at releases) · the ~2,004 ranked harvest-queue rows (more label chunks = a build, not a re-run) · fw-scaled precanon radius for dives.

## MANIFEST — replace only files listed as touched; ceilings never increase without Matt
| doc | last touched | wc -c | ceiling |
|---|---|---|---|
| fractal-operating | ckpt 26 (hunks) | 12,918 | 13,000 |
| fractal-state | ckpt 26 (rewrite) | 5,537 | 6,000 |
| fractal-engine | ckpt 24 | 10,513 | 11,000 |
| fractal-storage | ckpt 24 | 5,759 | 6,000 |
| fractal-orchestration | ckpt 25 | 3,599 | 4,000 |
| fractal-models | ckpt 25 | 7,503 | 8,000 |
| fractal-thresholds | ckpt 24 | 4,716 | 5,000 |
| fractal-corpus | ckpt 26 (hunks) | 8,033 | 8,000 |
| fractal-discovery | ckpt 26 (rewrite) | 10,753 | 13,000 |
| fractal-emission | ckpt 26 (hunks) | 5,902 | 6,000 |

⟨FILL⟩ = measured by the apply-prompt after it applies (`wc -c` of the file it just wrote).
