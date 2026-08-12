# fractal-thresholds — live cuts & floors

Changes when: a flip, a re-derivation. **★ Cuts are expressed RELATIVE TO A REFERENCE, never as absolutes** — a float says nothing about which model it describes. Cap-raise recalibration debt PAID (2026-08-02, record → `docs/design/deferred_recalibration.md`). **The base-rate audit LANDED 2026-08-11** (population verdict → fractal-corpus); no banner remains, but the standing rule holds everywhere: a rate off a prefilled sheet is a CEILING.

## The fixed-cut regime — `floors.py` sole owner (2026-08-09, `551643c`)
ONE quality definition everywhere: fixed cuts on **stored raw P(≥3)**. The per-partition derived-threshold apparatus is deleted (record → fractal-storage).
- **`JUNK_FLOOR` 0.20** — enforces at ONE site since 2026-08-11: `ranked_intake`, on the LOCATION head's scale. **Fresh run-side supply always clears it** (run-side admission already requires `GOOD_FLOOR`) — it only ever bites the LEGACY ledgers. The mining-scale read at `deploy_tail` was REPOINTED at the gate (Matt's resolution of the crossover inversion) [code: `test_floors`' caller-census + source tests]. **PERMANENTLY SHARED-SCALE stands as a statement about what 0.20 MEANS** — never restated at any single-head flip — even with one live reader.
- **`GOOD_FLOOR` 0.50** — run-side admission, and what "good" means to τ_h.
- **`NOTBAD_CUT` / `GREAT_CUT` 0.50 each** — CORN's own natural cutpoints, never per-family calibrated. They NAME a frame; they never keep one.
- **`THIN_SUPPLY_DIVISOR` 4 · `CLUSTER_CAP` 2 · `ATTEMPT_MULTIPLIER` 4** — emission's selection arithmetic (fractal-emission owns the rules they feed).
- **`good_class(p_good, p_great) → None|3|4`** — pop-quota currency weighs a 4 ten times a 3; the cloud diagnostic prints a split. **★ `machine_1_discard` reads `canon_nb < NOTBAD_CUT`** — the class column can never say 1 again, so reading it would silently widen "confidently BAD" onto every class-2.
- **★★ TWO RESTATEMENT MODES, choose by evidence class.** (1) **Volume-matched** (head flips): restate a floor as the score passing the SAME FRACTION of a fixed reference pool — CORN scales are train-prior-calibrated (fractal-models); `classifier_retrain_protocol.md` §5a/b/c. (2) **Human-derived crossover** (label audits): isotonic P(≥boundary)=0.5 on a labeled sheet — §5a's midpoint convention is REUSABLE, its volume invariant is NOT: the volume change IS the finding (2026-08-11: 4.6× at the gate). **★ The cut lands at the MIDPOINT** between the k-th and (k+1)-th score, and the two stage-2 gate sites disagree (`emit_v1` `>`, `MiningScorer.gate` `>=`) — re-count realized volume under the ROUNDED constant at each site's own operator.
- `corn_decode` survives as a function for retired readouts only.

## τ_h — walk arm only, on the fixed cut (`551643c`)
Per-partition quantile of the WALK-OUTCOME arm alone (keep=0.90), "good" = canonical P(≥3) ≥ `GOOD_FLOOR`, **fail-open τ_h = 0.0 below `MIN_N=5`** — the price of a loose arm is visible GPU-minutes, never lost supply. Values + per-partition n → **`data/atlas/tau_h_base_v11.json`** (1,148 walk rows; spread ~0.20–0.55). ⚠ **Three multibrot arms clear `MIN_N` by single digits — read those as "roughly half", not four significant figures.**
- **★★ NEVER POOL CROSS-FAMILY FOR A MISSING ARM** — a pooled mb4 would have been ~3.5× looser than its own-arm estimate.

## The mining gate — HUMAN-DERIVED (2026-08-11)
- **`MINING_GATE_THRESHOLD` 0.0949** = sheet F's crossover `[human n=200, prefill-anchored — ceiling]`; owner `mining_gate` → `MiningScorer.gate` (`>=`). **THE GATE ACTS:** `deploy_tail.alloc_input` draws through `scorer.gate` — the one stage-2 site where a mining cut genuinely filters; `floors.MINING_RELEASE` still annotates only. The pre-repoint pool is a strict SUBSET of the new one — the change only recovers gate-good rows.
- **`floors.MINING_POOL` 0.0** — pool everything the gate could pass (Matt).
- **Lock = `data/render_mode_head/v3/mining_gate_lock_2026-08-11.{json,md}` — REGENERATION-VERIFIED** [code: `lock_mining_gate.py` verify + `test_mining_gate_lock`]: never hand-edit; decision prose enters via `LockSpec` fields and `--write`. The repoint decision + refused alternatives live in its "What this cut forced elsewhere".
- **★ THE LIVE VALUE IS THE END OF A COMMITTED `superseded_by` CHAIN** [code: `adopt_head.AdoptSpec.superseded_by`; `test_volume_match`] — each record starts where the previous ended. Rollback rung named by `mining_pins.MINING_LOCK_ROLLBACK` (the flip's volume-matched lock — retained, no longer re-verified; same status as v1's).
- Wallpaper floors: volume-match restated at the 2026-08-11 flip, unchanged since (evidence in the flip records). Nothing about a head's quality follows from which floor is numerically larger — tests DERIVE any straddle, never encode one.
- **`suggest_tier.CUTS` has a live deriver (`derive_cuts`)**; `INTAKE_CUTS` served explicitly with `INTAKE_DERIVATION` stamped (`1ac30c5`). Mining CUTS re-derived including sheet F: immaterial shift, NOT adopted.
- **v1's gate lock STAYS at v1's path** as a rollback record [eval n=422, 15 modes], plus July's `fresh_sheet_reads.JULY_LOCK` (different population, NOT superseded). Every precision in any lock is a CEILING.

## Keeper cuts + stage-2 floors — annotation status
Keeper cuts (`data/atlas/keeper_cuts.json`, `model:"v11"`) and the stage-2 floors are recorded against every row; a `Floor` offers `annotates()` and cannot cut — **the mining GATE (above) is the one deliberate exception, owned by `MiningScorer.gate`, not a `Floor`.** Each annotation keeps the head version it was set against — an annotation on the wrong probability scale is as unreadable as a gate on one. Gate-lock records stay TRACKED as provenance and as the scale-comparison input any restatement reads.

⚠ Sink isolation remains the only wall against smoke contamination — rule lives in fractal-orchestration.
