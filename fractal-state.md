# fractal-state — checkpoint 68 (2026-08-22)

## Where we are
Ckpt 68: **run10 DONE** (8h shallow, 55 released, landed 84 min early — pacing terms re-derived, +57.6 active min on re-plan). **THE TWO-PHASE RULING (Matt):** a run builds the POOL (harvest + judged small renders + a ~10-picture DIAGNOSTIC release); the **GALLERY PASS** (`curate gallery` — "emission" is banned vocabulary) is a separate global selection over the whole pool; **nothing released so far is gallery**. Design → `preserve\emission_design.md` (rename pending there and in the v3 article master). Prereqs LANDED: sidecar durable; served-index removed from the run path; `collection` field; `STRANGE_SHARE` 0.6; `MODES_PER_LOCATION` param; pool re-scored (`scores_current`); floor fit COMMITTED — strange 0.685 reproduces, **smooth floor 0.381 recorded, Matt ruled 0.385 (0.005 grid) — not yet applied**. **Frontier sheet (200) labeled + ingested: 43/100 judge-refused novel frames are keepers; planes have zero novel ground; gates placed right.** Site review round 1 applied; From-locations v3 DRAFTED on the two-phase design. Both repos FREE.

## OPEN (ordered)
1. **`gallery_pass_naming_and_floor`** (wallpapers, small): restate `SMOOTH_RELEASE_FLOOR` 0.381 → **0.385** on the 0.005 grid (one grid for both floors; 0.685 untouched); rename the phase GALLERY PASS everywhere the design is cited; `head floor` → `--head` convention. Then edit `preserve\emission_design.md` + `prose\From locations to wallpapers v3.md` for the rename (claude.ai authors).
2. **`embed_admissions`** (wallpapers): one fixed-map neutral render + DINOv2 vector per admitted location over the junk floor (~24.8k); store keyed by location; field discarded; report dimension/geometry/cost/disk. Written FROM the design doc §2.3.
3. **`curate gallery` v0** (wallpapers): slots by mix → 60/40 head split → quality-weighted farthest point + hard radius per partition → per-head floors, P(≥4) sort → full-size for winners, `collection=gallery`; no attempt leg yet; RETRO TABLE of nearest chosen pairs for Matt. Design §2, §4, §6.3.
4. **`gallery_attempts`** (wallpapers): the colorize leg inside the gallery pass — top m locations per chosen point × (2 smooth + 6 strange), knobs; drop 31/32 palette JPEGs after judging. Design §2.5.
5. **Frontier consequences (Matt's calls):** (a) a **c-pool channel for julia/phoenix** — the proven channel serves parameter planes only, so 42 of 43 frontier keepers are labels without a root channel; (b) **location-head retrain** with the 200 new rows — "retrain when a decision needs it": 43% of refused novel ground is good, and the next harvest is that decision; (c) harvest reach — 70.7% of run10's expandable tier never expanded.
6. First real gallery at N≈50 → Matt's hand pass (formal sheet or not — his call) → v3 TODOs filled → figures `emission-*`/`gallery-output` drawn → **From locations to wallpapers PLACED**. Running at scale after.
7. Website, free now: `home-views` GALLERY keep-or-delete (site's only gallery; deleting empties galleries/index — decide what the Galleries link does) · `escape-orbit-race` APNG carries the last reader-facing coordinates (maker unwired from `build`) · README family-spread cost table · pool cap 8→cores · explore-the-set.
8. Native genericity fix (`field::sample` → specialized `iterate::run`; → fractal-engine); Matt: bigger perf work separately. Deep zoom after the perturbation arc.
9. Parked (Matt's call each) → fractal-tutorial §THE REPO.

## CLOSED this era (record = Drive reports)
- launch_run10 + run10_readout — restore found/fixed an empty-directory structural-check bug; seed 20260821; under-fill = strange bar (15/40), location rule cost 20 (3 prior-run); saturation 91.4%, planes 100% discounted; share ran on exhausted julia pools.
- run10_followups — pacing terms (ACTIVE_TO_WALL conditional, release rate read from newest tracked run via new `finished` stamp, re-score scales, ledger term → direct lookup, docstrings); autopsy stratified by fate (54 cards, gate sentences live); 1 smooth + 2 strange attempts per location; plan prints pool state; `--release-workers`.
- retire_repeats — 185→153 served, 32 retired by own-head score (14/15 cross-head groups went smooth; two served smooth rows at P(≥3)≈0.03). Meaningless under the two-phase model; rows stay.
- draw_frontier_labels + ingest (ADDENDUM A) — `run10_novel_ground` registered train-side; result → fractal-discovery.
- audit_emission_split — dependency map → design doc §4; coverage 475/67,586; ledgers NOT gone (archived; `curate ledgers` provenance).
- emission_prereqs — `curation/durability.py` (archived copy + tracked manifest + `curate sidecar save|check|restore`, run-start guard); served index off the run path; `collection` diagnostic/gallery on all 1,050 rows; deep `gallery_*` → `evaluation_*`; `DEFAULT_N` 10; pacing derives attempts from the night's own shape; `scores_current` (identity on 925, 125 retired-head rows gain P(≥4)); `head floor` PAVA fit.
- site_review_round_1 — 12 items; contents summaries in SIGGRAPH register; figure credits/explorer sentence → ↗ icon; captions stripped of coordinates/scores; `escape-families` 15-panel teaser (all detail panels Matt-q4); `family-home-views` FIGURE deleted; merged/redrawn Rendering-fundamentals figures; palettes diversified (3→8 maps); 23 section names lowercased; writing-guidance colon-list principle NARROWED by CC (Matt's Overview wording kept verbatim).
- Corrections landed: ~19 MiB/s bulk figure was the first 300 MiB (sustained cold 28–37) · release 41.9 s/picture was measured with curation on the USB archive (24.9 hot) · "320 attempted" = 160 locations · 5-of-8 ledgers "gone" were on the archive tier.

## SCRATCH/ARTIFACT FLAGS
- DISPOSABLE now: `scratch/run10_repeats.json` · `scratch/run8h_instrumented/` (run10 + readout done) · `artifacts/run10_novel_ground` (labels ingested; the store is the record) · website `scratch/_ss_check.mjs`, `scratch/explorer_bench/`.
- KEEP: `artifacts/curation_backup/` (sidecar archive copy — load-bearing, manifest-tracked) · `artifacts/deep_run1/` + `_gallery/` · `preserve\julia_deep_eyetest\` · `preserve\emission_design.md` (NEW, durable).
- `scratch/run10_readout_report.md` etc. — Drive copies are the record.

## ROSTER — soft size targets
operating 14k · state 6k · tutorial 15k · corpus 7k · discovery 6k · engine 5k. This distillation: state REPLACED · tutorial 9 hunks · corpus 1 hunk · discovery 2 hunks · operating 2 hunks · engine CLEAN. Session estimate at checkpoint: ~150k tokens.
