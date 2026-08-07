# fractal-thresholds — live cuts & the decode predicate

Changes when: a flip, a re-derivation. **★ Cuts are expressed RELATIVE TO A REFERENCE, never as absolutes** — a float says nothing about which model it describes. **The cap-raise recalibration debt is PAID (2026-08-02): t_good + keeper cuts + τ_h re-derived TOGETHER on v10's scale; the procedure is recorded as a dated record in `docs/design/deferred_recalibration.md`.** Every cut moving down at the flip was calibration (v10's P(≥3) sits lower on the same rows), not quality.

## t_good — ADOPTED on v10's scale (`db914df`)
q3 = the served predicate (below). One instrument per partition, never pooled.

| partition | obj | t_good | prec | rec | F_OOF | plateau |
|---|---|---|---|---|---|---|
| mandelbrot | F0.5 | **0.03** | 0.366 | 0.577 | 0.357 | 1 step |
| julia:multibrot3 | F2 | **0.27** | 0.594 | 1.000 | 0.841 | 6 steps |
| julia:multibrot4 | F2 | **0.03** | 0.533 | 1.000 | 0.791 | 2 steps |
| julia:multibrot5 | F2 | **0.06** | 0.704 | 0.864 | 0.789 | 4 steps |
| julia:mandelbrot · phoenix | — | 0.50 | — | — | — | UNCALIBRATED — uniform instrument short of `MIN_POS`; **draws DEMOTED to contingency (Matt, 2026-08-06)** — v11 calibrates via randomized location-grouped split; buy uniform rows only on observed live miscalibration |
| phoenix:classic | — | 0.50 | — | — | — | UNCALIBRATED — positives below `MIN_POS`; the sitting reservation accrues them (fractal-corpus); classic supply reads `t_good_for("phoenix:classic")` [code] |
| multibrot3/4/5 | — | 0.50 | — | — | — | UNCALIBRATED — unbiased rows exist, ZERO positives; more ∂M-shell buys 0 expected positives — needs a DIFFERENT draw (fractal-corpus) |

- **★★ The objective principle (protocol §4): recall where supply is scarce, precision where abundant** — re-chosen per flip from CURRENT supply, never copied.
- **★★ MANDELBROT IS UNDECIDABLE AT THE TOP.** v10's F0.5 curve is flat and low (precision ≈0.35 everywhere below t=0.7); the argmax falls to the grid floor on a 1-step plateau; F0.5 and F2 pick the SAME t (under v8: 0.85 vs 0.14 — the objective was load-bearing and now is not). Paired on the identical 526 rows: admits 2.28% → 7.79%, precision 0.333 → 0.366 — **the cut has NEVER bought precision under either head. The failure mode runs BOTH directions: a high cut quietly stalls library growth; a low cut pollutes it.** Answer = MORE LABELS (the ranked harvest queue is the ready supply), never a hand-nudge.
- ⚠ Small-n plateau flags stand on all three julia:multibrot cuts — OOF is the honest column.
- **★ UNCALIBRATED IS STAMPED, NOT IMPLIED** (`t_good_status`) — a baseline 0.50 and a derived 0.50 are indistinguishable in a config file.
- **★★ `MIN_POS` binds on the frozen EVAL SLICE, never corpus positives** [read 2026-08-05: all five uncal partitions clear corpus counts; none has eval-slice positives]. The v10 slice = `data/v10/eval_scores_v10.jsonl`, three frozen sources (loose0_v3_floor / prospect_census / maneuver_uniform_v1); `q4_uniform_eval_v1` is eval-eligible in the batch registry — the mechanism that admits it at the next version's slice build — but outside the frozen list. The ckpt-33 rule "a staged cut derived on any biased population is NOT adoptable" is **superseded (Matt, 2026-08-06): randomized location-grouped splits are the calibration default at v11**; the frozen-slice machinery stays for instruments already built.

## The served predicate — sweep and gate now agree (`5d866cc`)
Production admits via `corn_decode`, which **COUNTS thresholds met** (CORN cumulatives aren't guaranteed monotone — 92/760 v10-slice rows have `p_ge4 > p_ge3`); since 2026-08-02 **the t_good sweep searches that same rule** (the old ∧-rule disagreed at 68/97 grid points; the adopted v10 table is byte-identical under alignment; a non-vacuity fixture pins the disagreement cases).
- **★★ v8'S LIVE MANDELBROT CUT WAS CHOSEN AGAINST A PREDICATE THE GATE NEVER RAN** — served-rule re-derivation moves it 0.85 → 0.14 (8/526 keepers entered on `p_ge4` alone). The v8 artifact is deliberately byte-identical (it records what v8 served). **★ A ROLLBACK TO v8 MUST RE-DERIVE ITS TABLE, NOT COPY IT** — hazard written beside the ladder in the pins module.

## τ_h — re-derived under v10 (`398d3cf`)
Per-partition **MINIMUM of the harvest-log quantile (left-truncated by construction ⇒ an upper bound) and the untruncated walk-outcome derivation**, each arm cut on its OWN population (3,492 re-scored rows, keep=0.90):

| partition | v8 (retired) | **v10** | | partition | v8 | **v10** |
|---|---|---|---|---|---|---|
| mandelbrot | 0.704 | **0.023** | | julia:mandelbrot | 0.349 | **0.413** |
| multibrot3 | 0.417 | **0.369** | | julia:multibrot3 | 0.381 | **0.282** |
| multibrot4 | 0.550 | **0.409** | | julia:multibrot4 | 0.200 | **0.052** |
| multibrot5 | 0.438 | **0.351** | | julia:multibrot5 | 0.199 | **0.070** |

- **★★ THE POOLED CROSS-FAMILY FALLBACK WAS LIVE AND IS REMOVED** (`allow_pooled=False`): with native-multibrot pass counts collapsed under min_n=5, the old code served mb3/mb5 a pooled quantile ~9× looser than their own harvest estimates. An arm that lacks n is recorded UNAVAILABLE; the min is over arms that exist.
- ⚠ mb3/mb5 rest on the harvest arm ALONE — an upper bound with nothing below it. **Log discovery LANDED (`8165555`): `harvest_log_registry` replaces the retired `HARVEST_RUNS` hand list — writing to the registered store IS registering [code: rests on `discovery_sinks` class resolution; scratch refused; campaign1 (all pre-geometry) and phoenix rows excluded by construction].** Discovered population ≈ 2× the pinned five (mb4 454→1,587, mb3 1,683→4,504); **the adopted arms will NOT reproduce on it (8.4% sample overlap) — a re-derivation is a NEW derivation + flip AND a full re-render (~2,400 harvest + 1,100 walk rows × 2 arms; the rederive cache is gone). DEFERRED deliberately (2026-08-05), not by omission.** New confound: each log left-truncates at ITS OWN live τ_h — the truncation level is non-uniform across the enlarged arm; the upper-bound direction holds.
- `TAU_H_CAMPAIGN_FLOOR` stays retired and empty; mechanism tested by injection only.

## Keeper cuts (`data/atlas/keeper_cuts.json`, `model:"v10"`)
REPORT-ONLY floor; ranker orders within eligible; a keeper is `label >= 3`. Recut: mandelbrot **0.03** (OOF 0.357) · j:mb3 **0.47** (0.528) · j:mb4 **0.55** (0.667) · j:mb5 **0.55** (0.667). **★ One-instrument rule now enforced in `keeper_cut.load_triples`** (generalizing the julia census-only rule): pooling 12 zero-positive mandelbrot rows had moved the cut 5 grid steps and collapsed OOF 0.357 → 0.100.

## Stage-2 cuts — `floors.py` sole owner; ALL FOUR ENFORCING (2026-08-06)

| floor | value | stamp | basis |
|---|--:|---|---|
| wallpaper_pool | 0.75 | v3 | module literal (permissive inventory bar) |
| wallpaper_release | 0.90 | v3 | IS `wallpaper_pins.GATE_THRESHOLD` — imported, never copied |
| mining_pool | 0.25 | v1 | measured: prec 75.7% [64.5–84.2] @ recall 84.1% |
| mining_release | 0.50 | v1 | measured: prec **97.0%** [84.7–99.5] @ recall 50.8% — **ENFORCING** (report-only until 2026-08-06) |

- Basis = `data/render_mode_head/v1/mining_gate_lock.json` [eval n=422, 15 modes, ≥3 base 14.9%]. **★ Every precision is a CEILING, not an estimate** — v1 trained at the sheet's 112 locations AND labels were prefill-anchored; inseparable, stated in the record. `read_lock` + `Floor.gate` refuse on pin/stamp mismatch [code: tools/emission/floors.py, tools/mining/lock_mining_gate.py]; the ladder is frozen WHOLE (both boundaries) so alternative cuts stay answerable without crops; none of the 70/80/90% precision targets clears its Wilson LOWER bound at n=422 — the reason nothing else moved. July's lock (0.548/0.195 @0.50, base .139, genuinely held-out, inputs gone) survives as prose in `fresh_sheet_reads.JULY_LOCK` — different population, NOT superseded.
- **★★ A stage-2 flip re-derives its gate at a VOLUME-MATCHED operating point on the new head's own scale** — CORN marginals calibrate to the train prior (fractal-models). Never copy a threshold across heads.
- First production run: realized fire rates 1.2–1.3× the lock's, inside CIs [unlabeled — no precision info].

## Decode-version predicate — version-general (HIGH-touch)
`corpus_common`: `is_decoded_by`, `is_current_decoded`, `current_rows_only`, `require_current`, `StaleDecodeError`. **Mixed-decode readouts are poison.** Admissible pool = current-decoded ledgers; a t_good flip retro-re-decodes by arithmetic on stored raw probabilities — stale rows die by the predicate, nothing hand-deleted. **Firewall verified live at the v10 flip: 313 v8 rows would have admitted; `load_admitted` returns 0.**
- **★ What it CANNOT catch: freshly-written rows that are wrong** — smoke/test rows are current-decode and admissible; sink isolation (fractal-orchestration) is a hard requirement, not hygiene. ⚠ Its cost: each flip makes the library seed unreconstructable until the next real run (fractal-orchestration).
