# fractal-models — the instruments

Changes when: retrains, ranker/screen work, aug-recipe changes. Thresholds/floors → fractal-thresholds; label corpora → fractal-corpus (stage-1) / fractal-emission (stage-2); view-fit → fractal-discovery.

## Division of labor
| model | judges | scope |
|---|---|---|
| **v11** location head | location potential, pre-color, classes 1–4 | within-family STEER + FLOOR + decode-admission; NEVER ranks, NEVER allocates cross-family |
| **wallpaper v3** | finished SMOOTH renders | pool + release gating; collapses strange ≈0.000, never gates them |
| **mining v1** | finished STRANGE renders, K=3 | pool + release gating (enforcing) |
| **pref v3-gvo** | within-location palette preference | colorize-path palette pick; NEVER quality, never cross-location |
| **`view_fit_v1.1`** | maneuver-candidate sourcing order | fractal-discovery owns it |

**Ranker CLOSED — the rebuild path is DELETED (Matt, 2026-08-08); emission is unranked BY DESIGN.**

Steer/rank/select split load-bearing; winner's curse recurs at every level. **"q4" = class 4 on the label scale; there is no separate q4 network and will not be one.**

## v11 — the deployed location head (flipped 2026-08-08)
MobileNetV4 (`mobilenetv4_conv_medium`, 1280-D penultimate), CORN ordinal, multi-family, K per-version from the checkpoint's own `config`. Deploy: 384×224 stretch from 640×360 ss2 `twilight_shifted`, pinned bit-for-bit. Method = `classifier_retrain_protocol.md`. Trained on the `crop-batch` cache (fractal-engine): **361,696 tiles**, randomized LOCATION-GROUPED splits, 20% eval. Baseline = v10 RE-SCORED on the identical v11 canonical tiles — tile-path diagnostic |Δ| ≤ 0.02 held.
- **Certification [pre-registered]:** census / floor / uniform legs NON-INFERIOR · the **q4-uniform leg SEPARATES** · **the 3|4 CUTPOINT TIGHTENED** — predicted class-4 rate lands exactly on the **0.4713** base, ECE **.162 → .130** — and **ORDERING IS NOT DAMAGED** (the v10 correction read's one live defect, and the only one the retrain was aimed at).
- **★★ THREE CHANGES MOVED AT ONCE** — corpus, split method, and render recipe. **No arm is attributable**; a v11−v10 delta prices the BUNDLE, never a component.
- **★★ THE MODEL-SELECTION OBJECTIVE IS A CONTROLLED VARIABLE** — freeze selection to the baseline-comparable population; amendment before the re-run. Generalizes to every retrain (wallpaper v4 selected on pooled-eval AP≥3, stated).
- **★ The ≥3 boundary in the maneuver-view population has no eval instrument anywhere** — that is the measurement gap.
- Class-4 WATCH: v10's retired itself at the flip (census AUC(q4) 0.7273 → 0.7664); a fresh `Q4_WATCH` is attached to the **holdout-is-biased-exactly-as-training-is** caveat on the six newly-calibrated partitions (fractal-thresholds).
- **★★ First correction-loop read [human n=500, prefill-anchored — a CEILING]: correction rate 43.6%** (the convergence metric's first datum), within-one 96.6% (all 17 two-tier moves phoenix or julia:mandelbrot), 75% of corrections downward, **68% on the 3|4 boundary alone** ⇒ v10's ORDERING matches Matt; its CLASS-4 CUTPOINT is loose, and only that. Machine-4 survival 172/320 = 53.8% as human 4 (96.6% as ≥3; misses land at 3): julia:multibrot4 **93%** — the one partition where P(≥4)≥0.5 is calibrated; phoenix **42.5%** worst; the rest ~50–68%. Per-bucket correction rates 34–51%; mandelbrot's floor-bought supply read 19% ≥3 vs 86–99% in ranked buckets.
- Role limits [human n=81+298+500]: on selected output `p_good` is a badness filter; NEVER allocate across families (family-mean Spearman −0.57); over-separates seed fertility.
- **★★ Machine-1 trust is PARTITION-DEPENDENT [human n=870, blind]:** native multibrot 94–100%, phoenix 72% ⇒ auto-discard safe; **julia:mandelbrot 30.9% with 16.5% of machine-1s human-≥3 ⇒ never auto-discard; `phoenix:classic` never-auto-discard (unmeasured).**
- **Rollback ladder = v11 → v10 ONLY** — everything below is de-tracked under the weights retention policy (fractal-storage owns it). **★ A ladder written BY AN ADOPTION is a different object from a build-time note about a flip that hadn't happened** — it lives in `data/v11/adoption_record.json`, every version token READ off the live pins; v11's `build_record.json` adopted nothing and said so. Live coupling = `COUPLED_ARTIFACTS` (7 entries, all stamps v11, walked by `test_coupled_artifacts.py`) [code: production_pins.py]; `test_flip_coherence.py` was never version-specific — the next flip edits `FLIP_HISTORY` only. **★★ Flip-era lesson: check the sites that BUILD a frozen artifact's inputs, not just the loader** — and **deleting a retired rung's constants breaks its readers** (a study importing `V6_CKPT_ROLLBACK` now spells the dead path locally, with why).

## Stage-2 heads (judge finished colored renders; independent of the location head)
| head | pin | state |
|---|---|---|
| wallpaper **v3** | `wallpaper_pins.HEAD_CKPT_REL` → `data/wallpaper_head/v3` | LIVE; gate 0.90 |
| wallpaper **v4** | weights DE-TRACKED 2026-08-08 → `retired_weights\` (unreferenced backup); run record (`config`/`metrics`) stays tracked | NOT ADOPTED and NOT REVIVABLE — **v4b = retrain FROM SCRATCH** when triggered |
| mining **v1** | `mining_pins.ACTIVE_MINING_CKPT` → `data/render_mode_head/v1`, K=3 | LIVE; calibrated 2026-08-06 (fractal-thresholds) |
| mining v2 | weights de-tracked (rejected) | LOST the winner rule; run record tracked — the live gate lock derives from its `report.json` |
| pref **v3-gvo** | `queries/scorer/data.ACTIVE_SCORER_DIR` | LIVE, kept pre-trained (Matt); documented ladder rungs v3/v2 DO NOT EXIST on disk |

- **wallpaper v3 [human, own-era 686-row eval]: a junk filter, not a good-detector** — AP≥2 0.956 / AUC≥3 0.748; at the 0.90 gate a third of passers ≤ tier-2 and 36/90 tier-4s rejected. Fresh era [eval n=357]: AP≥3 0.741 / AUC 0.886; **colorize-path AP≥3 0.939 ≫ pool-draw 0.580 — strongest on production's own coloring path.** Blind-spot list (38 label-≥3 rows at stamped p<0.05) lives in the v4 report.
- **v4 verdict [pre-declared slices]:** wash overall (AP≥3 0.678 vs 0.683); pool_draw improved (vm precision .593→.778; 13/15 eval blind-spot rows raised); **colorize_path regressed** (AP≥3 .939→.867, n=61) — the one production slice. NOT adopted. **★★ CORN scale is train-prior-calibrated: v4's re-stratified sheet moved the whole scale (0.90 fires 1.6% vs v3's 24.7%)** — volume-matched comparison is the load-bearing read; flip rule in fractal-thresholds. v4b: when minibrot-era material reaches intake; pools all batches + a top-slice positives draw.
- **mining v1 [human n=960 correction sitting; 7.1% corrections, 99.8% within-one]:** AUC≥3 0.967 / 0.978 eval; all 15 modes clear chance. v2 finetune post-mortem: 538 rows eroded ≥2 discrimination (small-data finetune damage); 2 of 3 v1-dropped modes have ZERO eval tier-3s (≥3 unmeasurable); `exp_smoothing` nearly all-good (20/27 ≥3) — barely a within-mode task. "Never saw the mode" mattered less than "the mode barely has two classes."
- **★★ THE WINNER RULE (reusable adoption gate):** a staged head becomes the candidate only if (a) no overall pre-declared eval metric significantly worse (95% paired bootstrap) AND (b) the motivating slice significantly better, none worse — the losing head keeps candidacy; no per-slice cherry-picking; declare the slices before the numbers.
- **★ Correction-sheet suggestion cuts:** prior-matched quantile cuts on `1 + Σ marginals`, re-derived per labeled slice (`suggest_tier.fit_cuts`); textbook CORN 0.5 and accuracy-max free cutpoints both degenerate (measured). Reads off corrected labels are CEILINGS (prefill anchoring) — stated, never blocking.
- **pref:** 999 old queries / ≈5,994 tiers survive tracked; joins never in git — orphaned (fractal-storage). A future batch re-points the warmstart pre-selection at v3-gvo (pref-v1 ckpt gone). Re-engagement triggers → fractal-emission.

## v9 — shelved (closed)
Never deployed; its cache was the forward asset, extended byte-identically by v10, and both are now deleted (fractal-storage).

## The augmentation recipe — v11
**32 tiles/location, EACH AN INDEPENDENT SEEDED DRAW** (no palette × geometry × AA product): palette uniform over the curated 76 **minus the 8 held out entirely as the invariance instrument** · shift ≤5% fw · scale ∈ [0.90,1.10] · AA 50/50 ss1-box / ss2-lanczos3 · **JPG quality uniform 60..95** (Matt eyeballed q60 — keeps all location-quality detail; cache mean 65.4 KiB/tile). Guaranteed FLOOR, drawn from the same 32: ≥2 `twilight_shifted` + ≥2 `blue_orange` + ≥1 identity.
- **★★ Never augment in a way that destroys the evidence the label was based on** (off-structure crops corrupted positives for v4→v7).
- **Cost [measured, v11 full rebuild]:** 361,696 tiles / 22.57 GiB / **3.09 h** on `crop-batch` (fractal-engine owns the executor and its per-unit costs) — the rebuild stopped being a one-way door.

## `pref_loc_v1` — the ranker: CLOSED 2026-08-08
No artifact ever existed; `tools/ranker/` + `campaign1_manifest.py` DELETED, closure in `deferred_recalibration.md`. The 379 blind labels stay ORPHANED (their tile→location joins were scratch-only and wiped) — a permanent record of what an untracked join costs, not a rebuild candidate.

## q4 stage-1 screen (G) — superseded at sourcing (kept for its invariants)
**★★ Weak gate, dead ranker** [human n=487, blind]: AUC 0.605 pooled, 0.511 within accepts. Discard junk only; interior clause inert as quality but **KEEP as a 5.3× COMPUTE filter.** Successor invariants: OOD-mask permanent · gate from LABELED precision, p uncalibrated · deterministic seed before weight-stability claims · referee = minibrot-DISJOINT LOMO. ⚠ Nothing sees within-source VARIETY or COMPOSITION — open; no scalar settles a composition call.
