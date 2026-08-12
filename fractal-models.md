# fractal-models — the instruments

Changes when: retrains, screen work, aug-recipe changes. Thresholds/floors → fractal-thresholds; label corpora → fractal-corpus (stage-1) / fractal-emission (stage-2); view-fit → fractal-discovery.

## Division of labor
| model | judges | scope |
|---|---|---|
| **v11** location head | location potential, pre-color, classes 1–4 | within-family STEER + `GOOD_FLOOR` semantics; NEVER ranks, NEVER allocates cross-family |
| **wallpaper v4b** | finished SMOOTH renders | advisory scoring + annotation; collapses strange ≈0.000, never gates them |
| **mining v3** | finished STRANGE renders, K=3 | advisory scoring + annotation, EXCEPT the mining GATE at `deploy_tail` (fractal-thresholds owns) |
| **pref v3-gvo** | within-location palette preference | colorize-path palette pick; NEVER quality, never cross-location |
| **`view_fit_v1.1`** | maneuver-candidate sourcing order | fractal-discovery owns it |

**Ranker CLOSED, rebuild path DELETED (Matt).** The 379 blind ranker labels stay ORPHANED (untracked joins wiped — fractal-storage), not a rebuild candidate. Steer/rank/select split load-bearing; winner's curse recurs at every level. **"q4" = class 4 on the label scale; there is no separate q4 network and will not be one.**

## v11 — the deployed location head (flipped 2026-08-08)
MobileNetV4 (`mobilenetv4_conv_medium`, 1280-D penultimate), CORN ordinal, multi-family, K per-version from the checkpoint's own `config`. Deploy: 384×224 stretch from 640×360 ss2 `twilight_shifted`, pinned bit-for-bit. Method = `classifier_retrain_protocol.md`. Trained on the `crop-batch` cache, randomized LOCATION-GROUPED splits, 20% eval; baseline = v10 re-scored on identical canonical tiles.
- **Certification [pre-registered]: PASSED on all four arms** — bars + results → `data/v11/{prereg_v11.json, eval_results_v11.json}` — point, don't restate.
- **★★ THREE CHANGES MOVED AT ONCE** (corpus, split method, render recipe) — no arm attributable; a v11−v10 delta prices the BUNDLE.
- **★★ THE MODEL-SELECTION OBJECTIVE IS A CONTROLLED VARIABLE** — freeze selection to the baseline-comparable population; amendment before the re-run. Generalizes to every retrain.
- **★ The ≥3 boundary in the maneuver-view population has no eval instrument anywhere** — the measurement gap.
- **First correction-loop read [human n=500, prefill-anchored — a CEILING]:** correction rate 43.6% (the convergence metric's first datum), concentrated on the 3|4 boundary and downward ⇒ ordering matches Matt, only the class-4 cutpoint was loose. Machine-4 survival ~54% (julia:multibrot4 93% — the one partition where P(≥4)≥0.5 is calibrated; phoenix worst).
- Role limits [human n=81+298+500]: on selected output `p_good` is a badness filter; NEVER allocate across families (family-mean Spearman −0.57).
- **★★ Machine-1 trust is PARTITION-DEPENDENT [human n=870, blind]:** native multibrot 94–100%, phoenix 72% ⇒ auto-discard safe; **julia:mandelbrot 30.9% with 16.5% of machine-1s human-≥3 ⇒ never auto-discard; `phoenix:classic` never-auto-discard (unmeasured).**
- **Rollback ladder = v11 → v10 ONLY** — everything below de-tracked (fractal-storage). Ladder lives in `data/v11/adoption_record.json`, every version token READ off the live pins. Live coupling = `COUPLED_ARTIFACTS` [code: production_pins.py]; the next flip edits `FLIP_HISTORY` only. **★★ Flip-era lesson: check the sites that BUILD a frozen artifact's inputs, not just the loader** — and deleting a retired rung's constants breaks its readers.

## Stage-2 heads (judge finished colored renders; independent of the location head)
| head | pin | state |
|---|---|---|
| wallpaper **v4b** | `wallpaper_pins.HEAD_CKPT_REL` → **`data/wallpaper_head/v4b/seed_1/model_best.pt` — SEED 1** | LIVE (2026-08-11); floors → fractal-thresholds |
| wallpaper **v3** | `data/wallpaper_head/v3/model_best.pt` | PREVIOUS — the rollback rung |
| mining **v3** (`dedup_weighted` arm) | `mining_pins.ACTIVE_MINING_CKPT` → **`data/render_mode_head/v3/model_best.pt`**, K=3 | LIVE (2026-08-11) |
| mining **v1** | `data/render_mode_head/v1/model_best.pt` | PREVIOUS; its gate lock STAYS at v1's path, live again on rollback |
| mining v3 siblings · wallpaper v4 · mining v2 | — | staged/rejected: weights untracked, run records tracked; v4 NOT REVIVABLE |
| pref **v3-gvo** | `queries/scorer/data.ACTIVE_SCORER_DIR` | LIVE, kept pre-trained (Matt); documented rungs v3/v2 DO NOT EXIST on disk |

### The 2026-08-11 flip — both stage-2 heads, from scratch. Era-gate PASSED at run 26.
Adopted on Matt's standard: **comparable-plus-regenerable is sufficient** — the incumbents' anchored advantages were measured to be label-echo, and neither PREVIOUS rung can be rebuilt from its own recorded recipe; **regenerability IS the adoption rationale.** Evidence tables, per-cell CIs, seed bands, and the blind re-verdicts live in **`data/{wallpaper_head/v4b, render_mode_head/v3}/adoption_record.json`** + the committed flip reports — point, don't restate. What survives:
- **The wallpaper pin is SEED 1, not the top-level `v4b/model_best.pt`** (that is seed 0, byte-different). ⚠ **The pick SPENDS the 197-row selection — the BAND is the honest read** (caveat in the adoption record and pin comment).
- **★★ CROSS-SEED COMPARISONS SCORE THE BAND, NEVER THE STAGED PICK ALONE** — a staged pick has sat bottom of its own band on the first held-out population it ever saw.
- **★★ ANCHORED CORRECTION SHEETS MEASURE AGREEMENT WITH THE INCUMBENT, NOT QUALITY** — every rate off one is a CEILING, and a measured anchoring gap NEVER transfers across heads (the v1-era gate-boundary gap dissolved under v3 — fractal-corpus owns the audit). Governing rules = protocol §2a/§2b.
- **Convergence metric, first stage-2 datum [human n=200, sheet F]:** mining v3 88.0% exact, ≥2 flips symmetric ⇒ the head's ordering matches Matt. (v11's stage-1 datum above.)
- **★★ THE WINNER RULE (reusable adoption gate):** a staged head becomes candidate only if (a) no overall pre-declared eval metric significantly worse (95% paired bootstrap) AND (b) the motivating slice significantly better, none worse; no per-slice cherry-picking; declare slices before numbers.
- **★★ CORN scale is train-prior-calibrated** — a retrain moves the whole probability scale ⇒ volume-matched comparison is the only load-bearing cross-head read; flip rule → fractal-thresholds.
- **★ `version_pinned` never covered the stage-2 pins** — marker **`stage2_pinned`** + protocol **§5-0** exist for the next flip.
- **★ The stage-2 trainer baseline already carries `border_crop=0.05` + flips; only COLOUR aug is off** — an "unaugmented" arm is never unaugmented.
- **Never finetune** — v2's small-data damage stands.
- **★ Correction-sheet suggestion cuts:** prior-matched quantile cuts on `1 + Σ marginals`, re-derived per labeled slice (`suggest_tier.fit_cuts`); textbook CORN 0.5 and accuracy-max cutpoints both degenerate — corn_0.5 has beaten the adopted rule on exact agreement and is STILL rejected (it wrecks the prior). **The guard asserts PRIOR REPRODUCTION, not one head's coincidence.**

## The augmentation recipe — v11
**32 tiles/location, EACH AN INDEPENDENT SEEDED DRAW** (no palette × geometry × AA product): palette uniform over the curated 76 **minus the 8 held out as the invariance instrument** · shift ≤5% fw · scale ∈ [0.90,1.10] · AA 50/50 ss1-box / ss2-lanczos3 · JPG quality uniform 60..95 (q60 Matt-eyeballed). Guaranteed FLOOR from the same 32: ≥2 `twilight_shifted` + ≥2 `blue_orange` + ≥1 identity.
- **★★ Never augment in a way that destroys the evidence the label was based on** (off-structure crops corrupted positives for v4→v7).
- Full rebuild ≈ 3 h on `crop-batch` (costs → `docs/design/crop_batch.md`) — no longer a one-way door.
