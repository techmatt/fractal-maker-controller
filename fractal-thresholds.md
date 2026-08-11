# fractal-thresholds — live cuts & the decode predicate

Changes when: a flip, a re-derivation. **★ Cuts are expressed RELATIVE TO A REFERENCE, never as absolutes** — a float says nothing about which model it describes. **The cap-raise recalibration debt is PAID (2026-08-02): t_good + keeper cuts + τ_h re-derived TOGETHER on v10's scale; the procedure is recorded as a dated record in `docs/design/deferred_recalibration.md`.** Every cut moving down at the flip was calibration (v10's P(≥3) sits lower on the same rows), not quality.

## The fixed-cut regime — `floors.py` sole owner (2026-08-09, `551643c`)
ONE quality definition everywhere: fixed cuts on **stored raw P(≥3)**. The per-partition derived-threshold apparatus is deleted (record → fractal-storage); volume-matching is the heir of the ★ rule above.
- **`JUNK_FLOOR` 0.20** — the ONE cut that enforces, at the single site where the colorize pool is drawn.
- **`GOOD_FLOOR` 0.50** — run-side admission, and what "good" means to τ_h.
- **`NOTBAD_CUT` / `GREAT_CUT` 0.50 each** — CORN's own natural cutpoints, never per-family calibrated. They NAME a frame; they never keep one.
- **`THIN_SUPPLY_DIVISOR` 4 · `CLUSTER_CAP` 2 · `ATTEMPT_MULTIPLIER` 4** — emission's selection arithmetic (fractal-emission owns the rules they feed).
- **`good_class(p_good, p_great) → None|3|4`** — the two run-side sites that need a CLASS, not a yes/no: pop-quota currency weighs **a 4 ten times a 3**, and the cloud diagnostic prints a split. **★ `machine_1_discard` reads `canon_nb < NOTBAD_CUT`** — the keep-and-flag catch: the class column can never say 1 again, so reading it would have silently widened "the head is confident this is BAD" onto every class-2.
- **★★ THE VOLUME-MATCHED FLIP RULE.** At a head flip, restate a floor as the score that passes the SAME FRACTION of a fixed reference pool — CORN scales are train-prior-calibrated (fractal-models), so a number carried across heads describes a different population. The whole flip is `ledger_rescore`, then volume-match the two floors, and there is nothing else (`classifier_retrain_protocol.md` §5a/b/c).
- **`corn_decode` survives as a function** for retired readouts only; the counting rule is gone from every run-side site. The rollback-re-derives-its-table hazard died with the table.

## τ_h — walk arm only, re-derived on the fixed cut (`551643c`)
Per-partition quantile of the WALK-OUTCOME arm alone (keep=0.90), "good" = canonical P(≥3) ≥ `GOOD_FLOOR`, **fail-open τ_h = 0.0 below `MIN_N=5`** — the price of a loose arm is visible GPU-minutes, never lost supply. Base `data/atlas/tau_h_base_v11.json`, 1,148 walk rows.

| partition | n_rows | n_good | τ_h |
|---|--:|--:|--:|
| mandelbrot | 356 | 23 | 0.3145 |
| multibrot3 | 239 | 12 | 0.5450 |
| multibrot4 | 169 | 15 | 0.4743 |
| multibrot5 | 135 | **8** | 0.5379 |
| julia:mandelbrot | 102 | 59 | 0.2005 |
| julia:multibrot3 | 54 | 34 | 0.4736 |
| julia:multibrot4 | 54 | 32 | 0.5340 |
| julia:multibrot5 | 39 | 23 | 0.4695 |

Spread flattens to **0.20–0.55**. mb4 is now cut on its OWN 169-row / 15-good arm — the upper-bound-with-nothing-under-it condition is closed. ⚠ **multibrot5 (8), multibrot3 (12), multibrot4 (15) clear `MIN_N` by single digits — read those three as "roughly half", not four significant figures.**
- **★★ NEVER POOL CROSS-FAMILY FOR A MISSING ARM** — mb4 pooled would have been 0.292, ~3.5× looser than its own estimate. The two-arm minimum, the per-run truncation records and `harvest_log_registry` are deleted code.

## Every cut restated at the 2026-08-11 stage-2 flip (old → new)
**⚠⚠ BASE-RATE BANNER — reads on ANY of these entries: absolute rates from PREFILLED correction sheets are AGREEMENT-INFLATED, not base rates** (measured anchoring prices: wallpaper **−0.224** AUC≥3, mining **−0.278** AUC≥2; the four-sheet base-rate comparison is fractal-corpus's). **Every precision column below, and every precision in the gate locks, is a CEILING, not an estimate. The base-rate audit is QUEUED (state §OPEN 1) — do not re-read any calibration here until it lands.**

Reference pools: wallpaper = the (28) six-batch eval union (1,337 rows / 527 locations); mining = the (28) deduplicated eval side (827 rows / 136 locations). Both re-scored under BOTH heads in one pass through the harness that gates with each.

| owner | old | **new** | volume held | precision≥3 old → new |
|---|---:|---:|---|---|
| `wallpaper_pins.GATE_THRESHOLD` (= `floors.WALLPAPER_RELEASE`) | 0.90 | **0.6052** | 416/1337 (31.1%) | 0.798 → 0.748 |
| `floors.WALLPAPER_POOL` | 0.75 | **0.4698** | 503/1337 (37.6%) | 0.748 → 0.706 |
| `mining_pins.MINING_GATE_THRESHOLD` (= `floors.MINING_RELEASE`) | 0.50 | **0.6691** | 129/827 (15.6%) | 0.636 → 0.760 |
| `floors.MINING_POOL` | 0.25 | **0.3402** | 322/827 (38.9%) | 0.534 → 0.525 |
| `suggest_tier.CUTS` (686-row July slice) | (1.017, 2.615, 2.997) | **(1.2573, 2.4007, 2.91)** | prior-matched, n=686 | exact 0.414 → 0.427 |
| `suggest_tier.INTAKE_CUTS` (1,140-row intake) | (1.0119, 2.4663, 3.0012) | **(1.2304, 2.4197, 2.9713)** | prior-matched, n=1140 | exact 0.687 → 0.665 |
| `suggest_tier_mining.CUTS` (960-row fresh sheet) | (1.317, 1.8727) | **(1.6671, 2.352)** | prior-matched, n=960 | exact 0.800 |
| `build_fresh_sheet.SCORE_BINS` top edge | 0.90 | **derived from the gate** | — | — |
| `mining_pins.LOCK_PATH` | `…/v1/mining_gate_lock.json` | **`…/v3/mining_gate_lock.json`** | — | — |

`realized_volume == matched_volume` on all four floors. The mining pair reproduces the committed (28) report exactly (0.636 → 0.760 at n=129), which is the cross-check.
- **★ THE RETIRED FLOORS' ORDER REVERSED** — wallpaper release **0.6052 now sits BELOW** mining **0.6691**. Two tests encoded the old 0.90/0.50 order in a literal; both now DERIVE the straddle from the floors. Nothing about a head's quality follows from which number is larger.
- **`suggest_tier.CUTS` finally has a live deriver (`derive_cuts`)** — its slice's readout had never been stamped anywhere, so the constant was only checkable against prose. BOTH `CUTS` and `INTAKE_CUTS` were re-derived (`build_fresh_sheet` imports `CUTS`, so a future correction sheet reads it).
- **`JUNK_FLOOR` 0.20 was DELIBERATELY NOT RESTATED** — it is read on TWO heads' scales, so a single-head flip has no correct move: matching it to the flipped head corrupts the other reader. Recorded as a residual in protocol §5a and state §OPEN 5, not fixed.

## Keeper cuts + the four stage-2 floors — ANNOTATION-ONLY (2026-08-09)
**⚠⚠ The BASE-RATE BANNER above governs every entry in this section.** Keeper cuts (`data/atlas/keeper_cuts.json`, `model:"v11"`) and the four stamped stage-2 floors (values → the table above) are recorded against every row and gate nothing; a `Floor` offers `annotates()` and cannot cut. Each keeps the head version it was set against: an annotation on the wrong probability scale is as unreadable as a gate on one. The gate-lock records stay TRACKED as provenance and as the scale-comparison input a volume-matched flip reads — the live lock is now `data/render_mode_head/v3/mining_gate_lock.{json,md}`, derived from the flip's own `volume_match_mining.json`; **v1's lock STAYS at v1's path as the rollback record** [eval n=422, 15 modes, ≥3 base 14.9%], plus July's `fresh_sheet_reads.JULY_LOCK` (different population, NOT superseded). **★ Every precision in them is a CEILING, not an estimate** — v1 trained at the sheet's 112 locations AND labels were prefill-anchored; inseparable, stated in the record.

⚠ Sink isolation remains the only wall against smoke contamination — the rule lives in fractal-orchestration.
