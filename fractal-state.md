# fractal-state — checkpoint 112 (2026-09-06)

## Where we are
THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE: (1) the LOCATION hunt · (2) the WALLPAPER hunt · (3) the final curation SOLVE + release render. `MODE_POLICY` is the one place a mode carries a standing; Matt iterates from pictures, not counts. Phase 3 is Matt's eye on the final seating. **NO PUBLISHING OF ANY KIND until Matt raises it — never ask, never list it.**

**STANDING DIRECTION (Matt, ckpt 111, unchanged): QUALITY OF THE n=1000 GALLERY.** Thin themes are DE-PRIORITIZED and the thin-theme goal is a THEMED-PASS goal — the colour ceiling exists so no colour dominates, not so any cell gets a share, and no cell is owed seats. Mine until the pool is healthy across palettes, modes, locations and families → solve at whatever n → mine longer if a gallery comes up short. Busy-over-sparse is INTENTIONAL. τ 0.90× stands. The angle modes are OFF the mining goals; `curvature` is UNMINED.

**★ NO MORE SPECIAL-CASING THIN COLOUR (Matt, ckpt 112).** `stratum_score`, `thin_cells()`, `expressed.json`, the census and its drift guard are all DELETED. The colour ceiling is the one colour constraint and it acts as a hard rule at the seat. The term's anatomy is recorded in `curation/rank_key.py` so nobody re-derives it: three levels, the colour level worth `-0.002 [-0.007,+0.004]`, the composite level `-0.012 [-0.019,-0.006]` — a mode indicator wearing a colour term's name. The composite signal is gone UNREPLACED, deliberately.

**This era (ckpt 111→112, one day).** The retention keep went 3 → 5 with the free-slot function beside it; the slow lane ran green for the first time since the render cache closed; the two retired score artifacts were dropped; two file guards were resolved; the locations page was placed at v7; a two-arm pilot mine priced breadth against the near band; `stratum_score` was removed entirely; and the `gallery_grade` store was built, labelled by Matt across three sittings, and ingested at 1,000 rows. Ledger 284,517 → **308,419**.

**Records.** Unchanged from ckpt 109 except as noted. Published, and the four the site stands on: `20260902T161757Z` · `20260902T164622Z` · `20260904T023748Z` · `20260904T233233Z`. `20260906T133236Z` is the post-mine n=1000 record the browse page, the census rig and the whole `gallery_grade` draw stand on — TENTATIVE, keep it.

## IN FLIGHT ACROSS THIS BOUNDARY — none.

## QUEUED IN DRIVE `prompts\` — none.

## NEXT CHECKPOINT GOAL
**Train the fine-tier head on Matt's 1,000 `gallery_grade` labels.** Settled already, do not re-decide:
- A SEPARATE network, same architecture, initialized from the shipped judge's weights. NEVER a shared trunk — a moved trunk is a judge flip, which empties the pool and forces a full rescore.
- Fit on the **640 candidate column**, accepting the label-quality cost, because that is where it serves. The two geometries correlate at r = 0.696 over the thousand, and the 640 readings are the more compressed of the two.
- The standing training recipe unchanged: 80/20 grouped by lineage, early stop on AP(≥3) with AUC(≥3) fallback, patience 6, cap 20, three seeds, ship the best by stopping-slice AP. **Stratify the split by batch** — the three sittings disagree at p = 2.6e-05.
- How much trunk to unfreeze is decided by EXPERIMENT (frozen · last block · more), not by argument.
- Applied to SEATING ORDER only, never to retention. The ceiling contains a colour-biased ranking at the seat; `_prune_ranks` has no such containment and deletes permanently.
- It is the SECOND STAGE OF A CASCADE behind `p_ge4`, never a standalone scalar: its output is undefined on rows that never clear the bar. That is the shape it takes if it succeeds the rank key.
- The store is NEVER eval-eligible. Its population is 700 seats + 300 runners-up with NO colour-ceiling representation, so it is a ranker among rows at one location and nothing may claim more. 373 rows carry `leveled`; ~5 `itinerary` rows are crossovers.

## OPEN (ordered) — Matt raises each
1. **The long leg.** RULED (Matt, ckpt 112): **75% of wallclock on arm A (places), 25% on arm B (free slots)**. Arm B exhausts its BAND, not its clock — it consumed the pool's whole accumulated band in under four engine-hours — so B's unspent time must fall back to A rather than idle. Measured steady state was 11.5 : 1 A:B; 25% is deliberately above it. Prices → `curation/MEASUREMENTS.md`.
2. **The rank key no longer beats the judge.** On the current corpus the fitted key reads `d = -0.0071` smooth, `-0.0028` strange: nothing over `p_ge4` on either kind, and it is the corpus rather than any one column (the incumbent's own smooth AUC went 0.671 → 0.831). Retiring it is Matt's stated intent once the fine-tier head lands; `population.jsonl` and its 1 MiB allowlist line retire with it, as does the unreplaced composite signal.
3. **`render_train.population` was corrected to 11,849** (117 renders had sat in both stores and were counted twice). **No retrain was run.** The shipped render judge was fitted on the uncorrected population.
4. **Records-only picture retention.** The sweep premise is dead — only two of the five sweepers touch the pool and those are the incremental ones — so the cost is one-off at build. What survives is **regeneration determinism**: signatures invalidate on picture identity, and a regenerated picture that is not byte-identical re-costs its row. Direction → `preserve\retention_design.md`.
5. **`carriers.jsonl`** sits at 65.9% of the 1 MiB history guard, 4.3 drops away, after `fields` and `mean` came off and are derived at the read. `family` is held in reserve. **It is a cross-repo seam**: the website's `builder/palettes.py:carriers()` derives the same two columns and holds the header's dominance sentence to its two thresholds.
6. **`itinerary.jsonl`'s guard** was raised to 786,432 (it sits at 62%). The real horizon is roughly nine drops, which is a design question rather than a constant.
7. **Website** (Matt's pace). **Per-page status, masters, sweep state, figure holds and review rounds live in `docs/page-review.md` — cite it, never restate it here.** The locations page is placed at v7 and its **caption round is OPEN and UNSTARTED**; captions live on the page and not in the master, so that round either travels as exact hunks or brings captions into the master first. Two rounds still named and unscheduled: `color-palettes` (its *Leveling* section becomes *Autolevel*, a URL change) and a re-base onto a newer record. Stale figures and prose are NOT tracked or refreshed until "ready for publishing".
8. **The reframe channel's cadence.** Label-bound rather than clock-bound; a short follow-on after a sitting, never a night. Sizing → `curation/MEASUREMENTS.md`.

Parked → `preserve\parked.md`: augment at n=2000; the rung-frame overwrite; the `mine` leg's autolevel stamp gap; medium refactors; the `tia` bound question; the `rank_key` composition-versus-quality trade; **the `groups.jsonl` re-cut** (Matt ruled ckpt 112: do not build the axis).

## STATUS / KNOWN REDS
None known. Fast lane 3,843 passed / 123 deselected, 117.68 s; `cargo test` 216 passed; `ruff` clean over 403 files. Website `builder check` 17 green, 47 JS tests. ⚠ Fast-lane WALL times taken this era are not comparable readings — three `label serve` processes were up for most of it; the counts are the comparable figures.

## RULINGS THIS ERA
→ `preserve\settled_rulings.md §ckpt 112`.

## KEEP LIST
Drive `prompts\`: wipe everything. `reports\`: wipe everything. Wallpapers `scratch/`: KEEP `overnight_8h_0905/census/` and `probe_spiral/` (Matt's); WIPE everything else. **WIPE `artifacts/sheet/n1000_0906_{1,2,3}`** (554 MB, regenerable from the join on the row) and the three raw drops in `labels/`. Website `scratch/`: KEEP `_modes_render_times.py`, the walk-descent figure rig, and `three_bands/pick_seats.py`.

## OWED
Nothing.

## SCRATCH/ARTIFACT FLAGS
Standing KEEP: `artifacts/curation/candidate_ledger/` · the FIVE Durables · `neutral_embeddings.jsonl` · `artifacts/curation/` HOT · live release rows · `artifacts/reframe_g1…g10` · `artifacts/curation/tentative/<stamp>/` — every record (prune-protected) · `artifacts/votes/` kits · `artifacts/curation/growth/20260902T150756Z/` · `data/coloring/texture_flat.jsonl` · `data/spiral/` · `models/spiral/` · `models/render/` weights-v6 beside v5 · `artifacts/render_folds/` · `artifacts/top_slice_probe/`. **★ NEW: `artifacts/gallery_grade/n1000_0906/*/plan.jsonl`** — a graded row carries `leveled` as a BOOLEAN and never a path, so these plans are the only thing that can rebuild the 373 levelled pictures as they were judged; not regenerable, 736 KB. **★ Every `gallery_grade` row's picture and `.leveled/` colormap is protection-held until the head is fit** — 233 of the 300 runners-up were unprotected and prunable, and they are the hard negatives. **★ `.leveled/` DIRECTORIES ARE NOT SWEEPABLE** (→ fractal-engine). ARCHIVED (RESTORE before reuse): unchanged from ckpt 106. Walk ledgers: `discovered_priors` reads BOTH tiers while a harvest defaults to hot, so every header records which it read.

## CLOSED (records wiped — verdicts in the docs and settled_rulings)
BUILD_ckpt112_retention_freeslots_and_TODOs_0906 · SMALL_ckpt112_guards_and_expressed_staleness_0906 · BUILD_ckpt112_gallery_grade_sheets_0906 · PLACE_finding_good_locations_v7_0906 · MINE_ckpt112_two_arm_pilot_0906 · ADOPT_ckpt112_expressed_rate_threshold_0906 · REMOVE_ckpt112_stratum_score_0906 · FIX_ckpt112_website_carriers_and_prose_0906 · PROMOTE_ckpt112_leveled_check_and_docs_0906 · FOLLOWUP_ckpt112_identity_pin_rehome_dedup_0906 · INGEST_ckpt112_gallery_grade_labels_0906 · PROTECT_ckpt112_gallery_grade_keys_0906.

## PARKED / SETTLED
→ `preserve\parked.md`, `preserve\settled_rulings.md`, `preserve\sourcing_channel_laws.md`, `preserve\retention_design.md`, `preserve\solver_design.md`.
