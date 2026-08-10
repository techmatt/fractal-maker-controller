# fractal-state — ckpt 37, 2026-08-10

**Rewritten in full at EVERY distillation — the only doc guaranteed to be.** Holds NO FACTS: status, plan, flags, open/parked, roster.

**This checkpoint = the selection-restructure / run-25 era (~1 day):** Matt's over-design verdict — derived per-partition thresholds as ENFORCING FROZEN STATE were the root cause of the recurring "zero supply / impossible by construction" failures — drove a five-prompt restructure (`b474154` → `32d2d2c` → `551643c` → sat-memory → `e3dd2bc`): selection became READ-TIME and rank-based · all enforcement floors became annotations · one quality definition (fixed cuts on raw P(≥3)) replaced the t_good/decode-predicate apparatus everywhere (net −4,395 lines) · saturation memory (24) landed · run (25), the first production run under the new stack, completed clean and PASSED its era gate (below-floor bet vindicated; classic supply solved; one aimed problem: busy strange renders).

## THE GOAL (Matt) — one amendment
Two learned functions: **(a) find good minibrots** and **(b) find the q4 within a neighbourhood**. **(b) has NO scheduled supervised build** — the descent harness moved to FUTURE IDEAS (Matt: no manual descent labels; nothing that forces framework-wide retraining); (b) is served implicitly by the dive leg + the correction loop's 3|4 sharpening. End-state unchanged: fully unsupervised/progressive wallpaper generation. Correction loop the mechanism; per-sitting correction rate the convergence metric (first datum 43.6%, v10-era); era gate the standing human act.

## THE PLAN — ckpt-37 queue (Matt-approved order)
*(This era: restructure DONE · (24) DONE · (25) DONE + era gate PASSED.)*
**(26) slot-guarantee fix** — 1 release slot per partition with floor-passing supply, remainder by mix; small prompt, before run 26. **(27) sittings:** wallpaper ~960 — ~300 minibrot-centered (v4b's motivating slice) · ~150 below-retired-floor stratum · ~75 top-slice positives · ~40/partition floor · phoenix:classic take-all · remainder proportional; stratify by partition/score/source-vein only, NEVER palette; strata take what supply allows — PLUS a mining correction sheet oversampling high-scoring BUSY fancy-mode passers. **(28) retrains under the winner rule, both FROM SCRATCH:** mining (motivating slice: busy false-positives on fancy modes) · wallpaper v4b (motivating slice: minibrot-centered; pools all batches + top-slice draw). Flips are cheap now: `ledger_rescore` + volume-match the two floors. **Next emission** unions run-25's 1,987 forward rows + drops the redundant `rescored_v11` overlay. **Then the convergence/tutorial turn.**

## STATUS
- **v11 LIVE**; ladder v11 → v10 only. Stage-2: wallpaper v3 + mining v1 + pref v3-gvo LIVE as **advisory scorers — no head enforces anything**.
- **Selection regime:** read-time ranked per partition on stored raw P(≥3); constants (all `floors.py`, all coarse): `JUNK_FLOOR` 0.20 (one site: colorize-pool draw) · `GOOD_FLOOR` 0.50 · `NOTBAD_CUT`/`GREAT_CUT` + `good_class` · `THIN_SUPPLY_DIVISOR` 4 · `CLUSTER_CAP` 2 · `ATTEMPT_MULTIPLIER` 4. All legacy floors/keeper cuts annotation-only. τ_h walk-arm-only, fail-open below min_n. Sat memory LIVE (k=0.30, strength 1.0).
- Supply: 1,477 mined / 1,285 above junk floor / 881 admitted; +1,987 run-25 rows pending union. classic 23 admitted. Seed **v2 KEPT** (v3 registered, NOT adopted — revisit after the sitting).
- Workflow: drive-sync exchange; **ALL prompts — CC and session/distillation — go through `prompts\`**. Suite green (2507).

## FLAGS (new this era)
- **Busy strange renders from fancy modes** (era-gate verdict): mining-head weakness — busyness/composition is the never-measured axis; remedy = (27)+(28); busy rows are the RECOLOR quadrant, never drops.
- **Classic release paradox:** 23 above-floor rows, 0 slots — release_mix apportionment at N=12 zeroes 4 partitions structurally; fix approved FOR NOW = (26). **STANDING CONCERN: release-composition governance** (hand-tuned ratio table at small N) — recurs whenever N or partition count changes.
- τ_h small-n on multibrot3/4/5 (8–15 good rows — "roughly half") · mb4 walk arm still thin (39 checks run 25; fail-open, accumulates) · legacy orchestrator minis UNVERIFIED vs new semantics (Matt dropped; fix-forward if ever used for A/B) · bulk store has NO size watch (`size_guard` walks repo only; durable fix = in-run pruner in `steered_frontier`).

## OPEN — recorded, not scheduled
label-run target semantics · mandelbrot price rests on 3 samples · phoenix units-weighted EMA step (next allocator touch) · dive top-vs-control unread (6/28 run 25) · `emission_selector` z-plane `VIEWPORT_K`/`ZOOM_RATIO` uncalibrated · eval slice lacks parameter axes; classic viewport instrument NOT_DRAWN, fail-closed · opaque-export guard gap · frozen-record hazard sites (re-count post-deletion) · namespace-package migration · `LS.FIELDS` at `bulk()`.
*(Closed this era: t_good/decode/served-vs-AND apparatus (deleted) · ranker-era prose · mb4 τ_h upper-bound flag (own-arm now) · phoenix:classic zero-supply (`KNOWN_EMPTY` empty) · knife-edge plateaus (cuts deleted) · native-τ_h de-confound + `tau_h_retained_readout` re-run (moot) · release-no-mix-term (apportionment landed).)*

## PARKED — named, not half-open
color-space cool-lean · two dead strange modes · `render_release` unbounded end-to-end · pref re-collection (two triggers) · uniform draws · refill knobs near limits · variety measure · composition-as-general-measure (the busy slice is now AIMED via (27); the general measure stays parked) · Douady tuning · perturbation in `render-one` · probe as standing audit · ∂M-distance-scaled c-floor · lever-2 · deep-render tier.
**FUTURE IDEAS (Matt-gated):** descent harness (supervised) + its cheap fallbacks (dive rungs near high-P(≥4); multi-start local descent on the existing head) · **phoenix fast-render** (no f64 smooth lane for the memory-term recurrence + interior burn at the Ushiki point; profile first, then attracting-cycle bailout + specialized kernel behind a pixel-diff parity harness; absorbs the Rust-kernel-profiling + phoenix-render-cost parked items) · root-draw saturation discount + rejection-sampler re-tune (ONE decision) · release-composition redesign.

## ROSTER — soft size targets (unchanged; targets move only with Matt)
operating 13k · state 6k · engine 11k · storage 6k · orchestration 4k · models 8k · thresholds 5k · corpus 8k · discovery 13k · emission 6k
