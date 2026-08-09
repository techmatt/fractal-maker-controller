# fractal-thresholds — live cuts & the decode predicate

Changes when: a flip, a re-derivation. **★ Cuts are expressed RELATIVE TO A REFERENCE, never as absolutes** — a float says nothing about which model it describes. **The cap-raise recalibration debt is PAID (2026-08-02): t_good + keeper cuts + τ_h re-derived TOGETHER on v10's scale; the procedure is recorded as a dated record in `docs/design/deferred_recalibration.md`.** Every cut moving down at the flip was calibration (v10's P(≥3) sits lower on the same rows), not quality.

## t_good — ADOPTED on v11's scale (`5438554`; natives `8d5e5e8`)
q3 = the served predicate (below). One instrument per partition, never pooled. **`derive_t_good.select_population` is now the SHARED DEFAULT** — randomized location-grouped holdout, instrument fallback, never pooled (the v11 conformance item; the frozen-slice machinery is off the gate path, kept only for instruments already built).

| partition | v10 | **v11** | cut on | obj | plateau |
|---|---|---|---|---|---|
| mandelbrot | 0.03 | **0.90** | holdout 797[90] | F0.5 | [0.90,0.90] ⚠ 1-step |
| julia:mandelbrot | — | **0.85** | holdout 254[70] | F0.5 | [0.83,0.85] |
| phoenix | — | **0.77** | holdout 113[55] | F0.5 | [0.73,0.77] |
| julia:multibrot3 | 0.27 | **0.26** | **instrument** (census) 54[19] | F2 | [0.24,0.26] |
| julia:multibrot4 | 0.03 | **0.10** | holdout 44[28] | F2 | [0.10,0.10] ⚠ 1-step |
| julia:multibrot5 | 0.06 | **0.39** | holdout 58[28] | F2 | [0.38,0.39] ⚠ 2-step |
| multibrot3/4/5 | UNCAL | **0.61 / 0.85 / 0.61** | holdout 196/151/164 [49/32/38] | F2 | withheld at the flip, ADOPTED 2026-08-08 byte-for-byte |
| phoenix:classic | UNCAL | **UNCAL** (0.50) | 8[1] holdout, 0 instrument | — | below `MIN_POS`; `T_GOOD_UNCALIBRATED`'s last element |

- **★★ READ EVERY MOVE AS POPULATION *AND* HEAD.** mandelbrot 0.03→0.90 says nothing about v11's scale: the cut moved from 526 instrument rows at a 4.9% keeper base to 797 holdout rows at 11.3%, and an F_beta argmax moves with prevalence. **`julia:multibrot3` is the ONE clean head-only read** (same census population as v10): 0.27 → 0.26.
- **★★ THE HOLDOUT IS BIASED EXACTLY AS TRAINING IS** — these precisions are NOT what the gate delivers on a frontier. Accepted as the price of calibrating six previously-uncalibratable partitions; the new `Q4_WATCH` hangs on it (fractal-models).
- **★★ MANDELBROT'S UNDECIDABLE-AT-THE-TOP ERA IS OVER** — the correction sitting's labels made the flat F0.5 curve DECIDABLE (interior argmax, precision 0.781 / recall 0.633, OOF 0.731). **Labels + population, not head drift** — exactly what the old rule predicted: the answer to an undecidable cut is MORE LABELS, never a hand-nudge. Both failure directions still stand (high cut stalls growth, low cut pollutes).
- ⚠ Knife-edge plateaus (1–2 steps) on mandelbrot + julia:multibrot4/5; j:mandelbrot and phoenix are the wide ones. Adopted WITH the flags — run (25)'s release review judges them.
- **★ UNCALIBRATED IS STAMPED, NOT IMPLIED** (`t_good_status`) — a baseline 0.50 and a derived 0.50 are indistinguishable in a config file.
- **★★ `MIN_POS` binds HOLDOUT-**or**-INSTRUMENT per partition, NEVER their union** — holdout-ONLY would have been a regression (j:mb3 has 3 holdout positives ⇒ UNCALIBRATED). **★ `FT2FAM` folds every DERIVED partition into its base** — harmless until the holdout carried phoenix rows, then it cut phoenix on 121 instead of 113 while stamping `phoenix:classic` "no eval rows" about rows in the same file. Both `derive_t_good` and `keeper_cut` now read the partition the eval freeze resolved.
- **★★ The objective principle (protocol §4): recall where supply is scarce, precision where abundant** — re-chosen per flip from CURRENT supply, never copied.
- **★ A built sheet's frozen population must NOT be re-derived from a live t_good table** — `SheetSpec.filter_version` pins it.

## The served predicate — sweep and gate now agree (`5d866cc`)
Production admits via `corn_decode`, which **COUNTS thresholds met** (CORN cumulatives aren't guaranteed monotone — 92/760 v10-slice rows have `p_ge4 > p_ge3`); since 2026-08-02 **the t_good sweep searches that same rule** (the old ∧-rule disagreed at 68/97 grid points; the adopted v10 table is byte-identical under alignment; a non-vacuity fixture pins the disagreement cases).
- **★★ v8'S LIVE MANDELBROT CUT WAS CHOSEN AGAINST A PREDICATE THE GATE NEVER RAN** — served-rule re-derivation moves it 0.85 → 0.14 (8/526 keepers entered on `p_ge4` alone). The v8 artifact is deliberately byte-identical (it records what v8 served). **★ A ROLLBACK RE-DERIVES ITS TABLE, NEVER COPIES IT** — hazard written beside the ladder in the pins module.
- **★ THE SERVED-vs-AND ALIGNMENT GAP STOPPED BEING ZERO** — 34/2,860 rows at the flip, all `served_only`; it was a fact about v10's loose cuts, not an invariant. Now **pinned per version**, with the impossible direction (`and_only`) asserted separately and empty. The native adoption moved it 34 → **39**, attributable to ONLY the two tightened partitions (multibrot3 4→5, multibrot4 2→6) — a pinned measurement is a tripwire that must be re-attributed, not just re-stamped.

## τ_h — re-derived under v11 on the FULL REGISTRY POPULATION (`a03eb49`)
Per-partition **MINIMUM of the harvest-log quantile (left-truncated by construction ⇒ an upper bound) and the untruncated walk-outcome derivation**, each arm cut on its OWN population (keep=0.90). Base = **every run `harvest_log_registry` discovers**, 64,365 rows re-rendered over 21,417 s (~6.0 h) — the registry population IS the population now; the pinned-five era and the ~2× deferral are both closed.

| partition | v10 | **v11** | | partition | v10 | **v11** |
|---|---|---|---|---|---|---|
| mandelbrot | 0.023 | **0.626** | | julia:mandelbrot | 0.413 | **0.848** |
| multibrot3 | 0.369 | **0.595** | | julia:multibrot3 | 0.282 | **0.241** |
| multibrot4 | 0.409 | **0.825** | | julia:multibrot4 | 0.052 | **0.200** |
| multibrot5 | 0.351 | **0.607** | | julia:multibrot5 | 0.070 | **0.361** |

- **★★ THE DELTAS SPLIT IN TWO AND MUST NOT BE READ AS ONE NUMBER.** The five partitions at identical `t_good` across both derivations moved by pure population, and moved SMALL (|Δ| ≤ 0.041). The three natives moved 10–40× more and are **CONFOUNDED** — their `t_good` changed between the runs, so bar and population moved together; **not separable from the committed artifacts** (de-confound = a third derivation at the new `t_good` over the old 3,492-row sample; skipped deliberately).
- **★ It fixed the arm it was aimed at:** mandelbrot's cut rested on **23** passing frames of 300, now **885**, and the value barely moved (0.6329 → 0.6257) — the reassurance a 23-frame quantile could not give. Passers now run 609–11,705 per partition.
- **⚠⚠ multibrot4 LOST ITS WALK ARM** — t_good 0.50→0.85 cut walk passers 15/169 → **2**, under `min_n=5`. The walk ledger is the untruncated population, the only thing bounding the left-truncated harvest estimate from BELOW ⇒ mb4 is an upper bound with nothing under it, and took the table's largest move (0.4743 → 0.8245): the two facts are not independent. The condition the flip had recorded as CLOSED, reopened the same day for a different reason. Remedy = walk rows from the next run.
- **★★ THE POOLED CROSS-FAMILY FALLBACK WAS LIVE AND IS REMOVED** (`allow_pooled=False`): an arm lacking n is recorded UNAVAILABLE and the min is over arms that exist (mb4 pooled would have been 0.292, ~3.5× looser than its own estimate).
- **★ Each log left-truncates at ITS OWN live τ_h** — non-uniform across the enlarged arm; `truncation_record` stamps the per-run levels. The upper-bound direction holds regardless. The adoption-era artifact (3,492 rows) is stamped `record_status` **superseded**, not deleted; `TAU_H_CAMPAIGN_FLOOR` stays retired and empty. ⚠ `tau_h_retained_readout.py` NOT re-run against the enlarged base.

## Keeper cuts (`data/atlas/keeper_cuts.json`, recut at the v11 flip)
REPORT-ONLY floor; a keeper is `label >= 3`; nothing ranks within eligible any more (ranker deleted). **★ The cut takes the DISCOVERY TABLE'S OWN POPULATION** — its `INSTRUMENT` rule ("a partition absent from the map takes every row it has") silently became a POOLED cut the moment the holdout gave those partitions rows (julia:mandelbrot on 302 = 254+48, phoenix on 211 = 113+98). "The precision-weighted twin" always meant the discovery population; it now is one. **★ One-instrument rule enforced in `keeper_cut.load_triples`**: pooling 12 zero-positive mandelbrot rows had moved the v10 cut 5 grid steps and collapsed OOF 0.357 → 0.100.

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
