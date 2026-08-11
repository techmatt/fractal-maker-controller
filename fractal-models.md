# fractal-models — the instruments

Changes when: retrains, ranker/screen work, aug-recipe changes. Thresholds/floors → fractal-thresholds; label corpora → fractal-corpus (stage-1) / fractal-emission (stage-2); view-fit → fractal-discovery.

## Division of labor
| model | judges | scope |
|---|---|---|
| **v11** location head | location potential, pre-color, classes 1–4 | within-family STEER + `GOOD_FLOOR` semantics (thresholds); NEVER ranks, NEVER allocates cross-family |
| **wallpaper v4b** | finished SMOOTH renders | advisory scoring + annotation (enforcement retired 2026-08-09); collapses strange ≈0.000, never gates them |
| **mining v3** | finished STRANGE renders, K=3 | advisory scoring + annotation (enforcement retired 2026-08-09) |
| **pref v3-gvo** | within-location palette preference | colorize-path palette pick; NEVER quality, never cross-location |
| **`view_fit_v1.1`** | maneuver-candidate sourcing order | fractal-discovery owns it |

**Ranker CLOSED — the rebuild path is DELETED (Matt, 2026-08-08); emission is unranked BY DESIGN.**

Steer/rank/select split load-bearing; winner's curse recurs at every level. **"q4" = class 4 on the label scale; there is no separate q4 network and will not be one.**

## v11 — the deployed location head (flipped 2026-08-08)
MobileNetV4 (`mobilenetv4_conv_medium`, 1280-D penultimate), CORN ordinal, multi-family, K per-version from the checkpoint's own `config`. Deploy: 384×224 stretch from 640×360 ss2 `twilight_shifted`, pinned bit-for-bit. Method = `classifier_retrain_protocol.md`. Trained on the `crop-batch` cache (fractal-engine): **361,696 tiles**, randomized LOCATION-GROUPED splits, 20% eval. Baseline = v10 RE-SCORED on the identical v11 canonical tiles — tile-path diagnostic |Δ| ≤ 0.02 held.
- **Certification [pre-registered]:** census / floor / uniform legs NON-INFERIOR · the **q4-uniform leg SEPARATES** · **the 3|4 CUTPOINT TIGHTENED** — predicted class-4 rate lands exactly on the **0.4713** base, ECE **.162 → .130** — and **ORDERING IS NOT DAMAGED** (the v10 correction read's one live defect, and the only one the retrain was aimed at). Per-arm cert bars + results live in `data/v11/{prereg_v11.json, eval_results_v11.json}` (committed) — point, don't restate.
- **★★ THREE CHANGES MOVED AT ONCE** — corpus, split method, and render recipe. **No arm is attributable**; a v11−v10 delta prices the BUNDLE, never a component.
- **★★ THE MODEL-SELECTION OBJECTIVE IS A CONTROLLED VARIABLE** — freeze selection to the baseline-comparable population; amendment before the re-run. Generalizes to every retrain (wallpaper v4 selected on pooled-eval AP≥3, stated).
- **★ The ≥3 boundary in the maneuver-view population has no eval instrument anywhere** — that is the measurement gap.
- **★★ First correction-loop read [human n=500, prefill-anchored — a CEILING]: correction rate 43.6%** (the convergence metric's first datum), within-one 96.6% (all 17 two-tier moves phoenix or julia:mandelbrot), 75% of corrections downward, **68% on the 3|4 boundary alone** ⇒ v10's ORDERING matches Matt; its CLASS-4 CUTPOINT is loose, and only that. Machine-4 survival 172/320 = 53.8% as human 4 (96.6% as ≥3; misses land at 3): julia:multibrot4 **93%** — the one partition where P(≥4)≥0.5 is calibrated; phoenix **42.5%** worst; the rest ~50–68%. Per-bucket correction rates 34–51%; mandelbrot's floor-bought supply read 19% ≥3 vs 86–99% in ranked buckets.
- Role limits [human n=81+298+500]: on selected output `p_good` is a badness filter; NEVER allocate across families (family-mean Spearman −0.57); over-separates seed fertility.
- **★★ Machine-1 trust is PARTITION-DEPENDENT [human n=870, blind]:** native multibrot 94–100%, phoenix 72% ⇒ auto-discard safe; **julia:mandelbrot 30.9% with 16.5% of machine-1s human-≥3 ⇒ never auto-discard; `phoenix:classic` never-auto-discard (unmeasured).**
- **Rollback ladder = v11 → v10 ONLY** — everything below is de-tracked under the weights retention policy (fractal-storage owns it). **★ A ladder written BY AN ADOPTION is a different object from a build-time note about a flip that hadn't happened** — it lives in `data/v11/adoption_record.json`, every version token READ off the live pins; v11's `build_record.json` adopted nothing and said so. Live coupling = `COUPLED_ARTIFACTS` (7 entries, all stamps v11, walked by `test_coupled_artifacts.py`) [code: production_pins.py]; `test_flip_coherence.py` was never version-specific — the next flip edits `FLIP_HISTORY` only. **★★ Flip-era lesson: check the sites that BUILD a frozen artifact's inputs, not just the loader** — and **deleting a retired rung's constants breaks its readers** (a study importing `V6_CKPT_ROLLBACK` now spells the dead path locally, with why).

## Stage-2 heads (judge finished colored renders; independent of the location head)
| head | pin | state |
|---|---|---|
| wallpaper **v4b** | `wallpaper_pins.HEAD_CKPT_REL` → **`data/wallpaper_head/v4b/seed_1/model_best.pt`** | LIVE (flipped 2026-08-11); gate + pool floor restated by volume-match → fractal-thresholds |
| wallpaper **v3** | `data/wallpaper_head/v3/model_best.pt` | **PREVIOUS** — the rollback rung |
| wallpaper **v4** | weights DE-TRACKED 2026-08-08 → `retired_weights\` (unreferenced backup); run record (`config`/`metrics`) stays tracked | NOT ADOPTED and NOT REVIVABLE |
| mining **v3** (`dedup_weighted` arm) | `mining_pins.ACTIVE_MINING_CKPT` → **`data/render_mode_head/v3/model_best.pt`**, K=3 | LIVE (flipped 2026-08-11); gate + pool floor restated by volume-match → fractal-thresholds |
| mining **v1** | `data/render_mode_head/v1/model_best.pt` | **PREVIOUS** — the rollback rung; its `mining_gate_lock.json` STAYS at v1's path as the record of what 0.50/0.25 bought there and goes live again on rollback |
| mining v3 siblings `v3_aug` / `v3_augx` / `v3_uniform` / `v3_ap2` | — | staged-not-adopted: weights UNTRACKED, run records tracked |
| mining v2 | weights de-tracked (rejected) | LOST the winner rule; run record tracked (the live gate lock no longer derives from it — fractal-storage) |
| pref **v3-gvo** | `queries/scorer/data.ACTIVE_SCORER_DIR` | LIVE, kept pre-trained (Matt); documented ladder rungs v3/v2 DO NOT EXIST on disk |

### The 2026-08-11 flip — both stage-2 heads, from scratch
**Adopted on Matt's standard: comparable-plus-regenerable is sufficient**, the incumbents' anchored advantages having been measured as label-echo. Both PREVIOUS rungs are anchored-era heads that cannot be rebuilt from their own recorded recipe; **regenerability IS the adoption rationale.** Adoption records → `data/{wallpaper_head/v4b,render_mode_head/v3}/adoption_record.json`, written by `tools/scoring/adopt_head.py`, **every version token and cut READ off its owner**; `known_flip_cost` records what the un-rewritten stage-2 score carriers were judged against (fractal-operating).
- **The wallpaper pin is SEED 1, not the top-level `v4b/model_best.pt`** — that is seed 0, the staged max on the (28) pooled eval, and is byte-different. Seed 1 picked on best blind sheet-D AUC≥4 **0.609** of {0.572, 0.609, 0.557, 0.585, 0.512}, band **0.567 ± 0.032**, all five above v3's 0.510. ⚠ **The pick SPENDS the 197-row selection** — sheet D was the only unanchored read of that population, so 0.609 is now a selected maximum, not a held-out number; **the BAND is the honest read** (caveat carried in the adoption record and the pin comment).
- **★★ CROSS-SEED COMPARISONS SCORE THE BAND, NEVER THE STAGED PICK ALONE.** Sheet D's staged pick is seed 0 and it is the WORST of the five on AUC≥3 (**0.622** against a **0.697 ± 0.053** band) — selected on the (28) pooled eval, bottom of its own band on the first held-out population it had ever seen.
- **★ `version_pinned` NEVER COVERED THE STAGE-2 PINS**, and listing it before this flip listed the wrong set: the flip went red in **10 tests across 6 files**, every one a hardcoded outgoing value — exactly the failure that marker class exists to catch. New marker **`stage2_pinned` (56 tests)** + `classifier_retrain_protocol.md` **§5-0**.

**Sheet D re-verdict [blind, n=197, `2026-08-11_wallpaper_blind_minibrot_v1`]** — motivating verdict NO (clause (a) PASS / (b) FAIL); all four measurable cells straddle 0, so **at n=197 the slice cannot separate the two heads**:

| cell | v4b − v3 Δ (95% paired bootstrap) |
|---|---|
| AUC≥3 | [−0.341, +0.034] |
| AP≥3 | [−0.024, +0.007] |
| AUC≥4 | [−0.018, +0.141] |
| AP≥4 | [−0.016, +0.116] |

**v3 IS AT CHANCE where this population actually differs — AUC≥4 0.510 / AP≥4 0.480 against a 48.7% tier-4 base rate** — while all five v4b seeds beat it. Volume-matched at the deployed gate (v3 passes 111/197): precision≥3 **0.991 vs 0.982**, tier-4 share **52.3% vs 54.1%**; **at top-10% volume v4b is 1.000 / 75% tier-4 against v3's 0.950 / 45%.** Anchoring price ΔAUC≥3 **−0.224** (blind 0.741 vs anchored 0.965 on the 89-row sheet-A arm).

**Sheet E re-verdict [blind, n=150, `2026-08-11_render_mode_blind_v1`]** — CONTESTED-CELL SURVIVAL, the headline: of the **40** clause-(a) cells the five staged arms failed on the ANCHORED corpus, **2 survive (5%)** unanchored — `v3_aug` on `direct_trap_lines.auc_ge3` (Δ median −0.348, CI [−0.667,−0.042]) and `v3_augx` on `direct_trap_ring.auc_ge2` (−0.122, [−0.267,−0.013]). Of the other 38: **26 measured and no longer significantly worse · 7 dissolve but sit under the 20-row floor · 5 unmeasurable (one class only).** Per arm **v3 0/7 · v3_aug 1/8 · v3_augx 1/9 · v3_uniform 0/8 · v3_ap2 0/8** — three of five pass clause (a) outright. With 21 cells × 5 arms at 95%, ~2–3 one-sided crossings are expected by luck alone ⇒ **the 2 survivors are at multiplicity noise**, and neither is on a cell that failed for more than one arm. Every arm's pooled Δ straddles 0 on all four metrics. Anchoring price ΔAUC≥2 **−0.278** (blind 0.676 vs anchored 0.953 on the 827-row pooled eval); ΔAUC≥3 only −0.021 — **the inflation is concentrated at exactly the ≥2 boundary every staged arm "lost" on.** ⇒ **the (28)/(28b) per-mode clause-(a) rejections are NOT ESTABLISHED either way**; the correction loop is the safety net.

**The five mining arms [eval slice identical across arms: 827 rows (973 before near-dup dedup) / 136 locations / 214 good; baseline = v1 re-scored on the same crops through the same scorer]** — the `verdict` column is the ANCHORED read, superseded blind:

| arm | geometry | weights | objective | staged AP≥3 | 5-seed AP≥3 | 5-seed AUC≥3 | 5-seed AUC≥2 | verdict |
|---|---|---|---|---:|---|---|---|---|
| `dedup_weighted` | border 0.05/edge + flips (v1 recipe) | 1/group_size | `ap_ge3` | 0.679 | 0.654 ± 0.026 | 0.861 ± 0.005 | 0.918 ± 0.014 | v1 keeps (a ✗/b ✓) |
| `aug_gentle` | axis 0.03/axis + flips | 1/group_size | `ap_ge3` | 0.682 | 0.650 ± 0.022 | 0.860 ± 0.008 | 0.917 ± 0.009 | v1 keeps (a ✗/b ✓) |
| `aug_strong` | border 0.10/edge + axis 0.03/axis + flips | 1/group_size | `ap_ge3` | 0.689 | 0.651 ± 0.027 | 0.862 ± 0.013 | 0.917 ± 0.008 | v1 keeps (a ✗/b ✓) |
| `uniform` | border 0.05/edge + flips (v1 recipe) | UNIFORM | `ap_ge3` | 0.664 | 0.649 ± 0.008 | 0.858 ± 0.005 | 0.911 ± 0.015 | v1 keeps (a ✗/b ✓) |
| `ap2_selected` | border 0.05/edge + flips (v1 recipe) | 1/group_size | `ap_ge2` | 0.601 | 0.611 ± 0.020 | 0.846 ± 0.012 | 0.930 ± 0.002 | v1 keeps (a ✗/b ✓) |

**★★ THE FIVE-NULL SAGA — one paragraph, closed.** Every dial was a null and **the failure set never moved**: geometry across a **4× range** · near-dup weighting on and off (lifting it made pooled ≥2 *worse*, −0.019 → −0.061; UNIFORM also tightened the seed band 3× to ±0.008 while widening best-epoch scatter to 1–17) · the selection objective (the `ap_ge2` arm: the ≥2 regression did NOT close — same sign, same magnitude, CI still excluding 0 — and the ≥3 gain evaporated, 5-seed AP≥3 0.654 → 0.611). Four cells fail in ALL FIVE arms (`pooled.auc_ge2`, `curv_linear.auc_ge2`, `direct_trap_lines.auc_ge3`, `direct_trap_ring.auc_ge2`); every arm's best-epoch median is 6–10 of 40, the early-selection signature unmoved. **The mechanism was EVAL ANCHORING, not training** — sheet E dissolved 38 of those 40 rejections. **★ Trainer aug recipe fact: the stage-2 baseline already carries `border_crop=0.05` + h/v flips; only COLOUR aug is off** ⇒ an "unaugmented" arm was never unaugmented.

- **wallpaper v3 (PREVIOUS) [human, own-era 686-row eval]: a junk filter, not a good-detector** — AP≥2 0.956 / AUC≥3 0.748; at the 0.90 gate a third of passers ≤ tier-2 and 36/90 tier-4s rejected. Fresh era [eval n=357]: AP≥3 0.741 / AUC 0.886; **colorize-path AP≥3 0.939 ≫ pool-draw 0.580 — strongest on production's own coloring path.** Blind-spot list (38 label-≥3 rows at stamped p<0.05) lives in the v4 report. **The bet is settled: 33 of 48 run-25 candidates below the retired floors competed and were ALL fine to emit ⇒ the "0.90 as a good-detector" era is formally CLOSED** — consistent with its own AP≥2-vs-AUC≥3 numbers.
- **v4 verdict [pre-declared slices]:** wash overall (AP≥3 0.678 vs 0.683); pool_draw improved (vm precision .593→.778; 13/15 eval blind-spot rows raised); **colorize_path regressed** (AP≥3 .939→.867, n=61) — the one production slice. NOT adopted. **★★ CORN scale is train-prior-calibrated: v4's re-stratified sheet moved the whole scale (0.90 fires 1.6% vs v3's 24.7%)** — volume-matched comparison is the load-bearing read; flip rule in fractal-thresholds.
- **mining v1 (PREVIOUS) [human n=960 correction sitting; 7.1% corrections, 99.8% within-one]:** AUC≥3 0.967 / 0.978 eval; all 15 modes clear chance. v2 finetune post-mortem: 538 rows eroded ≥2 discrimination (small-data finetune damage); 2 of 3 v1-dropped modes have ZERO eval tier-3s (≥3 unmeasurable); `exp_smoothing` nearly all-good (20/27 ≥3) — barely a within-mode task. "Never saw the mode" mattered less than "the mode barely has two classes." **★★ Era verdict (Matt, run-25 sheet review): BUSY/COMPOSITION FALSE-POSITIVES ON THE FANCY MODES** — good locations, over-busy presentation; the old "nothing sees variety or composition" gap made concrete. That is the PRE-DECLARED motivating slice for the from-scratch retrain (never finetune — v2's small-data damage stands).
- **★★ THE WINNER RULE (reusable adoption gate):** a staged head becomes the candidate only if (a) no overall pre-declared eval metric significantly worse (95% paired bootstrap) AND (b) the motivating slice significantly better, none worse — the losing head keeps candidacy; no per-slice cherry-picking; declare the slices before the numbers.
- **★ Correction-sheet suggestion cuts:** prior-matched quantile cuts on `1 + Σ marginals`, re-derived per labeled slice (`suggest_tier.fit_cuts`); textbook CORN 0.5 and accuracy-max free cutpoints both degenerate (measured). Reads off corrected labels are CEILINGS (prefill anchoring) — stated, never blocking. **Postscript under v4b: `corn_0.5` now BEATS the adopted exact rule on exact agreement (0.452 vs 0.427; under v3 it was 0.376 vs 0.414) and is STILL rejected** — it puts 167 rows at tier 1 against a true 116 and 29 at tier 4 against a true 90. **★ The guard test that asserted `exact > corn_0.5.exact` encoded one head's coincidence as the rule's justification; it now asserts PRIOR REPRODUCTION**, which is what the module's own objective is.
- **pref:** 999 old queries / ≈5,994 tiers survive tracked; joins never in git — orphaned (fractal-storage). A future batch re-points the warmstart pre-selection at v3-gvo (pref-v1 ckpt gone). Re-engagement triggers → fractal-emission.

## The augmentation recipe — v11
**32 tiles/location, EACH AN INDEPENDENT SEEDED DRAW** (no palette × geometry × AA product): palette uniform over the curated 76 **minus the 8 held out entirely as the invariance instrument** · shift ≤5% fw · scale ∈ [0.90,1.10] · AA 50/50 ss1-box / ss2-lanczos3 · **JPG quality uniform 60..95** (Matt eyeballed q60 — keeps all location-quality detail; cache mean 65.4 KiB/tile). Guaranteed FLOOR, drawn from the same 32: ≥2 `twilight_shifted` + ≥2 `blue_orange` + ≥1 identity.
- **★★ Never augment in a way that destroys the evidence the label was based on** (off-structure crops corrupted positives for v4→v7).
- **Cost [measured, v11 full rebuild]:** 361,696 tiles / 22.57 GiB / **3.09 h** on `crop-batch` (fractal-engine owns the executor and its per-unit costs) — the rebuild stopped being a one-way door.

## `pref_loc_v1` — the ranker: CLOSED 2026-08-08
No artifact ever existed; `tools/ranker/` + `campaign1_manifest.py` DELETED, closure in `deferred_recalibration.md`. The 379 blind labels stay ORPHANED (their tile→location joins were scratch-only and wiped) — a permanent record of what an untracked join costs, not a rebuild candidate.

## q4 stage-1 screen (G) — superseded at sourcing (kept for its invariants)
**★★ Weak gate, dead ranker** [human n=487, blind]: AUC 0.605 pooled, 0.511 within accepts. Discard junk only; interior clause inert as quality but **KEEP as a 5.3× COMPUTE filter.** Successor invariants: OOD-mask permanent · gate from LABELED precision, p uncalibrated · deterministic seed before weight-stability claims · referee = minibrot-DISJOINT LOMO. ⚠ Nothing sees within-source VARIETY or COMPOSITION — open; no scalar settles a composition call.
