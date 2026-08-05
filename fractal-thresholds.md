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
| julia:mandelbrot · phoenix | — | 0.50 | — | — | — | UNCALIBRATED — eval instruments exist since 2026-08-03 (fractal-corpus); calibrate at the next version |
| phoenix:classic | — | 0.50 | — | — | — | UNCALIBRATED — positives below `MIN_POS`; the sitting reservation accrues them (fractal-corpus); classic supply reads `t_good_for("phoenix:classic")` [code] |
| multibrot3/4/5 | — | 0.50 | — | — | — | UNCALIBRATED (unbiased rows exist, ZERO keeper positives — stamped as its own case) |

- **★★ The objective principle (protocol §4): recall where supply is scarce, precision where abundant** — re-chosen per flip from CURRENT supply, never copied.
- **★★ MANDELBROT IS UNDECIDABLE AT THE TOP.** v10's F0.5 curve is flat and low (precision ≈0.35 everywhere below t=0.7); the argmax falls to the grid floor on a 1-step plateau; F0.5 and F2 pick the SAME t (under v8: 0.85 vs 0.14 — the objective was load-bearing and now is not). Paired on the identical 526 rows: admits 2.28% → 7.79%, precision 0.333 → 0.366 — **the cut has NEVER bought precision under either head. The failure mode runs BOTH directions: a high cut quietly stalls library growth; a low cut pollutes it.** Answer = MORE LABELS (the ranked harvest queue is the ready supply), never a hand-nudge.
- ⚠ Small-n plateau flags stand on all three julia:multibrot cuts — OOF is the honest column.
- **★ UNCALIBRATED IS STAMPED, NOT IMPLIED** (`t_good_status`) — a baseline 0.50 and a derived 0.50 are indistinguishable in a config file.

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
- ⚠ mb3/mb5 rest on the harvest arm ALONE — an upper bound with nothing below it (sheds-admissions direction). **The "self-heals" claim was FALSE (falsified 2026-08-04): `tau_h_rederive.HARVEST_RUNS` is a 5-entry hand list (campaign1/2 + julia_parent_probe); no 2026-08-03+ log has ever entered a derivation.** Decided fix (Matt): log discovery from registered run dirs, built PRE-RELAUNCH — new logs improve n; the left-truncation confound stands regardless. The harvest arm excludes campaign1's pre-geometry checks (fractal-orchestration owns the count).
- `TAU_H_CAMPAIGN_FLOOR` stays retired and empty; mechanism tested by injection only.

## Keeper cuts (`data/atlas/keeper_cuts.json`, `model:"v10"`)
REPORT-ONLY floor; ranker orders within eligible; a keeper is `label >= 3`. Recut: mandelbrot **0.03** (OOF 0.357) · j:mb3 **0.47** (0.528) · j:mb4 **0.55** (0.667) · j:mb5 **0.55** (0.667). **★ One-instrument rule now enforced in `keeper_cut.load_triples`** (generalizing the julia census-only rule): pooling 12 zero-positive mandelbrot rows had moved the cut 5 grid steps and collapsed OOF 0.357 → 0.100.

## Decode-version predicate — version-general (HIGH-touch)
`corpus_common`: `is_decoded_by`, `is_current_decoded`, `current_rows_only`, `require_current`, `StaleDecodeError`. **Mixed-decode readouts are poison.** Admissible pool = current-decoded ledgers; a t_good flip retro-re-decodes by arithmetic on stored raw probabilities — stale rows die by the predicate, nothing hand-deleted. **Firewall verified live at the v10 flip: 313 v8 rows would have admitted; `load_admitted` returns 0.**
- **★ What it CANNOT catch: freshly-written rows that are wrong** — smoke/test rows are current-decode and admissible; sink isolation (fractal-orchestration) is a hard requirement, not hygiene. ⚠ Its cost: each flip makes the library seed unreconstructable until the next real run (fractal-orchestration).
