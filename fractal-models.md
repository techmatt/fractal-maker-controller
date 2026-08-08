# fractal-models — the instruments

Changes when: retrains, ranker/screen work, aug-recipe changes. Thresholds/floors → fractal-thresholds; label corpora → fractal-corpus (stage-1) / fractal-emission (stage-2); view-fit → fractal-discovery.

## Division of labor
| model | judges | scope |
|---|---|---|
| **v10** location head | location potential, pre-color, classes 1–4 | within-family STEER + FLOOR + decode-admission; NEVER ranks, NEVER allocates cross-family |
| **wallpaper v3** | finished SMOOTH renders | pool + release gating; collapses strange ≈0.000, never gates them |
| **mining v1** | finished STRANGE renders, K=3 | pool + release gating (enforcing) |
| **pref v3-gvo** | within-location palette preference | colorize-path palette pick; NEVER quality, never cross-location |
| **`pref_loc_v1`** ranker | — | NO ARTIFACT HAS EVER EXISTED; every emission run unranked |
| **`view_fit_v1.1`** | maneuver-candidate sourcing order | fractal-discovery owns it |

Steer/rank/select split load-bearing; winner's curse recurs at every level. **"q4" = class 4 on the label scale; there is no separate q4 network and will not be one.**

## v10 — the deployed location head (flipped 2026-08-02)
MobileNetV4 (`mobilenetv4_conv_medium`, 1280-D penultimate), CORN ordinal, multi-family, K per-version from the checkpoint's own `config`. Deploy: 384×224 stretch from 640×360 ss2 `twilight_shifted`, pinned bit-for-bit. Method = `classifier_retrain_protocol.md`. Trained on the v9-cache extension (201,168 tiles) + 1,310 labels; uniform-90 held out of training AND model selection.
- **Certification [pre-registered]:** census-144 0.742 vs v8 0.751 p=0.79 NON-INFERIOR · floor-526 NON-INFERIOR · uniform-90 both heads separate at ≥2. Palette invariance ρ̄ 0.845 in-band. **★★ THE GAIN WAS ZERO** — appended labels were 100% native-plane while all class-4 eval power is julia:multibrot; instruments couldn't price the intervention.
- **★★ THE MODEL-SELECTION OBJECTIVE IS A CONTROLLED VARIABLE** — freeze selection to the baseline-comparable population; amendment before the re-run. Generalizes to every retrain (wallpaper v4 selected on pooled-eval AP≥3, stated).
- **★ The ≥3 boundary in the maneuver-view population has no eval instrument anywhere** — that, not v8-blindness, is the measurement gap.
- Class-4 WATCH (no gate): AUC 0.813 → 0.728 [n=22, all julia:multibrot] rides `cloud_diagnostic`, self-retiring.
- **★★ First correction-loop read [human n=500, prefill-anchored — a CEILING]: correction rate 43.6%** (the convergence metric's first datum), within-one 96.6% (all 17 two-tier moves phoenix or julia:mandelbrot), 75% of corrections downward, **68% on the 3|4 boundary alone** ⇒ v10's ORDERING matches Matt; its CLASS-4 CUTPOINT is loose, and only that. Machine-4 survival 172/320 = 53.8% as human 4 (96.6% as ≥3; misses land at 3): julia:multibrot4 **93%** — the one partition where P(≥4)≥0.5 is calibrated; phoenix **42.5%** worst; the rest ~50–68%. Per-bucket correction rates 34–51%; mandelbrot's floor-bought supply read 19% ≥3 vs 86–99% in ranked buckets.
- Role limits [human n=81+298+500]: on selected output `p_good` is a badness filter; NEVER allocate across families (family-mean Spearman −0.57); over-separates seed fertility.
- **★★ Machine-1 trust is PARTITION-DEPENDENT [human n=870, blind]:** native multibrot 94–100%, phoenix 72% ⇒ auto-discard safe; **julia:mandelbrot 30.9% with 16.5% of machine-1s human-≥3 ⇒ never auto-discard; `phoenix:classic` never-auto-discard (unmeasured).**
- **Rollback ladder v10 → v8 → v7 → v6 → v5** (v9 is NOT a rung — built, staged, never deployed). **★ The artifact `production_pins` names as the ladder is a frozen PRE-adoption record** (`deployed_now: "v8"`, field `ladder_after_a_v10_adoption`, v8-stamped revert set) — the ladder field is right; its surroundings describe the pre-flip state. Live coupling = `COUPLED_ARTIFACTS` (7 entries, all stamps v10, walked by `test_coupled_artifacts.py`) [code: production_pins.py]. **★ v5–v7 rungs carry NO `config.json`** — K-read falls back to the `.pt`'s internal config dict [census]. **★ A rollback to v8 RE-DERIVES its t_good table, never copies it** (fractal-thresholds owns why). **★★ Flip-era lesson: check the sites that BUILD a frozen artifact's inputs, not just the loader** (`tools/ranker/scorer.PENULTIMATE_CKPT` raises rather than falls back).

## Stage-2 heads (judge finished colored renders; independent of the location head)
| head | pin | state |
|---|---|---|
| wallpaper **v3** | `wallpaper_pins.HEAD_CKPT_REL` → `data/wallpaper_head/v3` | LIVE; gate 0.90 |
| wallpaper **v4** | `data/wallpaper_head/v4` (5 seeds; staged seed 2) | STAGED, NOT ADOPTED; canaried as a pair with v3 |
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
Never deployed; its cache was the forward asset, extended byte-identically by v10. Lesson survives in the aug-recipe rules.

## The augmentation recipe
**24 crops/location: 4 palettes × 3 geometric × 2 AA.** Palettes per LOCATION, per-location seed: `twilight_shifted` + `blue_orange` always · 2 from the 76 curated, **8 held out entirely as the invariance instrument.** Geometry: identity + 2 jittered (shift ≤ 0.11 fw, scale ∈ [0.90,1.10]). AA: ss1 box + ss2 lanczos3. `data_v4.Loc.palette_renders()` derives counts from `aug_roster.json` — a recipe change is data.
- **★★ Never augment in a way that destroys the evidence the label was based on** (off-structure crops corrupted positives for v4→v7).
- ⚠ Wider palette set (32–64/location): parked TWO builds — genuinely next rebuild.
- **Costs [measured, v10 extend]:** 30,408 tiles / 7.52 h; appended maneuver material ~9× v9 per-tile (interior mass). Full rebuild ≈ 11–13 h; recolor-batching executor (fractal-engine) would cut the appended half ~4×.

## `pref_loc_v1` — the ranker: NO ARTIFACT HAS EVER EXISTED (falsified 2026-08-05)
`data/ranker/**` zero commits ever; `--intake-floor` raises naming the absent artifact. 379 blind labels survive; their tile→location joins were scratch-only and wiped (campaign1's circular). Path back = re-collect + RE-BASE the bar (`deferred_recalibration.md` § Ranker rebuild) — a v11-prep decision; candidate alternative: let the retrained wallpaper head's score order within partition, deleting the rebuild entirely. **HARD SCOPE stands: never frontier priority, dive-start, scheduling, or any discovery decision.**

## q4 stage-1 screen (G) — superseded at sourcing (kept for its invariants)
**★★ Weak gate, dead ranker** [human n=487, blind]: AUC 0.605 pooled, 0.511 within accepts. Discard junk only; interior clause inert as quality but **KEEP as a 5.3× COMPUTE filter.** Successor invariants: OOD-mask permanent · gate from LABELED precision, p uncalibrated · deterministic seed before weight-stability claims · referee = minibrot-DISJOINT LOMO. ⚠ Nothing sees within-source VARIETY or COMPOSITION — open; no scalar settles a composition call.
