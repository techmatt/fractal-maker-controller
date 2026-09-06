# fractal-state — checkpoint 111 (2026-09-06)

## Where we are
THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE: (1) the LOCATION hunt · (2) the WALLPAPER hunt · (3) the final curation SOLVE + release render. `MODE_POLICY` is the one place a mode carries a standing; Matt iterates from pictures, not counts. Phase 3 is Matt's eye on the final seating — no label-feedback loop, not tracked. **NO PUBLISHING OF ANY KIND until Matt raises it — never ask, never list it.**

**STANDING DIRECTION (Matt, ckpt 111): QUALITY OF THE n=1000 GALLERY.** The thin themes are DE-PRIORITIZED and the thin-theme goal is a THEMED-PASS goal, never a general-gallery one — the colour ceiling exists so no colour dominates, not so any cell gets a share, and no cell is owed seats. Otherwise the simple loop still holds: mine until the pool is healthy across palettes, modes, locations and families → solve at whatever n → mine longer if a gallery comes up short. Busy-over-sparse is INTENTIONAL. τ 0.90× stands. The angle modes are OFF the mining goals; `curvature` is UNMINED.

**★ SEQUENCE MATTERS AND MINING COMES LAST.** Retention is NOT retroactive, so mining before the keep changes buys pool whose deeper rows are already discarded. Order: `RETAIN_PER_PAIR` 3 → 5 and the free-slot function → mining → re-sweep K. The near-band manifest is inverted until the free-slot fix lands, so a mine before it throws away its cheapest arm.

**This era (ckpt 110→111, one day): one overnight leg, then a long investigation and no second leg.** The `color_mass` grid closed (the drop's 120 maps, full 18-mode grid) and an overnight thin-theme mine added 41,365 candidates; ledger 261,616 → 284,517, pool 214,059 → 236,960. Everything after that was measurement: two retention audits, a record-anatomy audit, a K sweep, a geometry de-confound, a ranker experiment, a regime guard and a pre-closeout pass. **Three things were investigated and CLOSED against: the colour retention key, the penultimate-activation ranker, and (for now) a label-geometry second score.**

**Records.** Unchanged from ckpt 109 except the night's own. Published, and the four the site stands on: `20260902T161757Z` · `20260902T164622Z` · `20260904T023748Z` · `20260904T233233Z`. `20260906T133236Z` is the post-mine n=1000 step-N record the browse page and the census rig stand on — TENTATIVE, keep it. The four K-sweep rungs are DELETED. Deleting a record releases its seats.

## IN FLIGHT ACROSS THIS BOUNDARY — none.

## QUEUED IN DRIVE `prompts\` — none.

## NEXT CHECKPOINT GOAL
Matt names it at the top of the next checkpoint. Nothing is assumed or scheduled here.

## OPEN (ordered) — Matt raises each
1. **`RETAIN_PER_PAIR` 3 → 5 — DECIDED, UNBUILT (Matt, ckpt 111).** Wants the free-slot function with it, since keep 5 redefines a free slot everywhere. Evidence and the shape tables → `preserve\retention_design.md`.
2. **The free-slot function.** Nothing computes free slots; the arithmetic is by hand in leg rigs, which is how `thin2_b_near` was built exactly backwards. The rule is in `curation/README.md` now.
3. **A slow lane has not run against the current tree.** Skipped at ckpt 111 on Matt's call; none of the `test_render_*` or `test_finished_train` files have run since the render cache was closed, which is what they read.
4. **`stratum_score` — traced, no position taken.** Thin colour is pruned first AND seated last off one mapping; the term is fitted, not a bug. Three things sit under it → fractal-tutorial §Selection. Whether any of it should change is Matt's.
5. **Records-only picture retention — parked on ONE question:** do the five whole-store sweepers run incrementally or re-sweep? ~30 min read-only. Everything else about the direction survives → `preserve\retention_design.md`.
6. **Drop the two retired score artifacts (Matt approved, ckpt 111)** — 142 MB, half the sidecar, breaks no read and no test, and includes the rows backing gallery1 and gallery4.
7. **`groups.jsonl` re-cut, with the `color_mass` file split in the SAME pass**, on an axis stable under renumbering — never on group id. `itinerary.jsonl` sits at 93% of its per-file guard; it splits rather than becoming a Durable. Recipe → `palettes/README.md`.
8. **`carriers.jsonl` size guard** — reached by the drop AFTER next. Options → `palettes/README.md`.
9. **Website** (Matt's pace). **Per-page status, masters, sweep state, figure holds and review rounds live in `docs/page-review.md` — cite it, never restate it here.** Two rounds named and unscheduled: `color-palettes` (its *Leveling* section becomes *Autolevel*, a URL change because of the `#leveling` fragment) and a re-base onto a newer record. Stale figures and prose are NOT tracked or refreshed until "ready for publishing".
10. **`color_mass` cost** — the close ran 1.84× cheaper than this repo's carried price, unevenly by mode. Reading → `palettes/README.md`.
11. **The reframe channel's cadence.** Label-bound rather than clock-bound: drains in well under an hour and refills only as the label stores grow. A short follow-on after a sitting, never a night. Sizing → `curation/MEASUREMENTS.md`.

Parked → `preserve\parked.md`: augment at n=2000; the rung-frame overwrite; the `mine` leg's autolevel stamp gap; medium refactors; the `tia` bound question; the `rank_key` composition-versus-quality trade (Matt has other plans).

## STATUS / KNOWN REDS
None known. Fast lane green at 3,796 passed / 121 deselected, 113.49 s; `cargo test` 216 passed; `ruff` clean over 400 files. Website `builder check` 17 green, 47 JS tests. ⚠ The fast-lane WALL times recorded across this era are not comparable readings — a render leg and a second prompt shared the box for most of it; the counts are the comparable figures.

## RULINGS THIS ERA
→ `preserve\settled_rulings.md §ckpt 111`.

## KEEP LIST
Drive `prompts\`: wipe everything. `reports\`: wipe everything. Wallpapers `scratch/`: KEEP `overnight_8h_0905/census/` (the balance-census rig the ceilings are read from) and `probe_spiral/` (Matt's); WIPE everything else, including `measure_geometry_pilot/`, `measure_geometry_cand/` and `smoke_location_0906/`. Website `scratch/`: KEEP `_modes_render_times.py`, the walk-descent figure rig, and `three_bands/pick_seats.py`.

## OWED
Nothing.

## SCRATCH/ARTIFACT FLAGS
Standing KEEP: `artifacts/curation/candidate_ledger/` · the FIVE Durables · `neutral_embeddings.jsonl` · `artifacts/curation/` HOT · live release rows · `artifacts/reframe_g1…g10` · `artifacts/curation/tentative/<stamp>/` — every record (prune-protected) · `artifacts/votes/` kits · `artifacts/curation/growth/20260902T150756Z/` · `data/coloring/texture_flat.jsonl` · `data/spiral/` · `models/spiral/` · `models/render/` weights-v6 beside v5 · `artifacts/render_folds/` · `artifacts/top_slice_probe/` (the ranker sheet Matt read; disposable once he says so). **★ `.leveled/` DIRECTORIES ARE NOT SWEEPABLE** (→ fractal-engine). ARCHIVED (RESTORE before reuse): unchanged from ckpt 106. Walk ledgers: `discovered_priors` reads BOTH tiers while a harvest defaults to hot, so every header records which it read.

## CLOSED (records wiped — verdicts in the docs and settled_rulings)
SWEEP_color_mass_and_MINE_thin_themes_0906 · SHOW_n1000_gallery_0906 (+addendum1) · AUDIT_top_slice_ranker_0906 · AUDIT_retention_key_and_depth_0906 · AUDIT_record_anatomy_and_picture_retention_0906 · SWEEP_K_allowance_0906 · CLEANUP_sweepK_records_0906 · CLEANUP_sweepK_finish_0906 · MEASURE_geometry_deconfound_and_price_0906 · MEASURE_colour_key_supply_0906 · DROP_leveled_directories_0906 · EXPERIMENT_top_slice_ranker_0906 · GUARD_score_regime_0906 · PRE_CLOSEOUT_wallpapers_ckpt111_0906.

## PARKED / SETTLED
→ `preserve\parked.md`, `preserve\settled_rulings.md`, `preserve\sourcing_channel_laws.md`, `preserve\retention_design.md`.
