# fractal-thresholds — live cuts & floors

Changes when: a flip, a re-derivation. **★ Cuts are expressed RELATIVE TO A REFERENCE, never as absolutes** — a float says nothing about which model it describes. The cap-raise recalibration debt is PAID (2026-08-02, record → `docs/design/deferred_recalibration.md`); every cut moving down at that flip was calibration, not quality.

**⚠⚠ BASE-RATE BANNER — reads on EVERY calibration in this doc:** absolute rates from PREFILLED correction sheets are AGREEMENT-INFLATED, not base rates (measured anchoring prices → fractal-models; four-sheet population comparison → fractal-corpus). **Every precision recorded at a gate lock is a CEILING, not an estimate. The base-rate audit is QUEUED (state §OPEN 1) — do not re-read any calibration here until it lands.**

## The fixed-cut regime — `floors.py` sole owner (2026-08-09, `551643c`)
ONE quality definition everywhere: fixed cuts on **stored raw P(≥3)**. The per-partition derived-threshold apparatus is deleted (record → fractal-storage); volume-matching is the heir of the ★ rule above.
- **`JUNK_FLOOR` 0.20** — the ONE cut that enforces, at the single site where the colorize pool is drawn. **PERMANENTLY SHARED-SCALE (`8496aec`):** it is read on TWO heads' scales (`ranked_intake` on location, `deploy_tail` on mining), so it is never restated at any single-head flip — matching it to the flipped head corrupts the other reader. `test_floors.py` pins both declarations; §5a step 2 names `GOOD_FLOOR` + the four stamped floors as the restatement set.
- **`GOOD_FLOOR` 0.50** — run-side admission, and what "good" means to τ_h.
- **`NOTBAD_CUT` / `GREAT_CUT` 0.50 each** — CORN's own natural cutpoints, never per-family calibrated. They NAME a frame; they never keep one.
- **`THIN_SUPPLY_DIVISOR` 4 · `CLUSTER_CAP` 2 · `ATTEMPT_MULTIPLIER` 4** — emission's selection arithmetic (fractal-emission owns the rules they feed).
- **`good_class(p_good, p_great) → None|3|4`** — the two run-side sites needing a CLASS: pop-quota currency weighs a 4 ten times a 3; the cloud diagnostic prints a split. **★ `machine_1_discard` reads `canon_nb < NOTBAD_CUT`** — the class column can never say 1 again, so reading it would silently widen "confidently BAD" onto every class-2.
- **★★ THE VOLUME-MATCHED FLIP RULE.** At a head flip, restate a floor as the score passing the SAME FRACTION of a fixed reference pool — CORN scales are train-prior-calibrated (fractal-models). The whole flip is `ledger_rescore` (stage-1 only), then volume-match the floors, and nothing else (`classifier_retrain_protocol.md` §5a/b/c). **★ The new cut lands at the MIDPOINT** between the k-th and (k+1)-th score — a report's `cut_at` is the k-th and admits k under `>=` but k−1 under `>`, **and the two stage-2 gate sites disagree** (`emit_v1` `>`, `MiningScorer.gate` `>=`); re-count realized volume under the ROUNDED constant, never the swept one.
- `corn_decode` survives as a function for retired readouts only; the counting rule is gone from every run-side site.

## τ_h — walk arm only, on the fixed cut (`551643c`)
Per-partition quantile of the WALK-OUTCOME arm alone (keep=0.90), "good" = canonical P(≥3) ≥ `GOOD_FLOOR`, **fail-open τ_h = 0.0 below `MIN_N=5`** — the price of a loose arm is visible GPU-minutes, never lost supply. Values + per-partition n → **`data/atlas/tau_h_base_v11.json`** (1,148 walk rows; spread ~0.20–0.55). ⚠ **Three multibrot arms clear `MIN_N` by single digits — read those as "roughly half", not four significant figures.**
- **★★ NEVER POOL CROSS-FAMILY FOR A MISSING ARM** — a pooled mb4 would have been ~3.5× looser than its own-arm estimate.

## The 2026-08-11 stage-2 flip — restated cuts
All four stage-2 floors + both suggestion-cut sets were restated by volume-match in one pass; live values live at their owners (**`floors.py`**, `wallpaper_pins`, `mining_pins`, `suggest_tier{,_mining}.py`) and the evidence lives in the flip records — **`data/render_mode_head/v3/mining_gate_lock.{json,md}`** (derived from the flip's own `volume_match_mining.json`) + the committed volume-match reports. `realized_volume == matched_volume` on all four floors; the mining pair reproduces the committed retrain report exactly, which is the cross-check.
- **★ THE RETIRED FLOORS' ORDER REVERSED** — wallpaper release now sits BELOW mining release. Two tests that encoded the old order in a literal now DERIVE the straddle. Nothing about a head's quality follows from which number is larger.
- **`suggest_tier.CUTS` finally has a live deriver (`derive_cuts`)**; BOTH `CUTS` and `INTAKE_CUTS` were re-derived, and `build_fresh_sheet` now takes its cut set explicitly with `INTAKE_DERIVATION` stamped into `batch.json` (`1ac30c5`).
- **v1's gate lock STAYS at v1's path** as the rollback record [eval n=422, 15 modes], plus July's `fresh_sheet_reads.JULY_LOCK` (different population, NOT superseded). Every precision in a lock is a CEILING (v1 trained at the sheet's locations AND labels were prefill-anchored; inseparable, stated in the record).

## Keeper cuts + the four stage-2 floors — ANNOTATION-ONLY (2026-08-09)
Keeper cuts (`data/atlas/keeper_cuts.json`, `model:"v11"`) and the four stamped stage-2 floors are recorded against every row and gate nothing; a `Floor` offers `annotates()` and cannot cut. Each keeps the head version it was set against — an annotation on the wrong probability scale is as unreadable as a gate on one. Gate-lock records stay TRACKED as provenance and as the scale-comparison input a volume-matched flip reads.

⚠ Sink isolation remains the only wall against smoke contamination — rule lives in fractal-orchestration.
