# fractal-state — checkpoint 106 (2026-09-04)

## Where we are
THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE: (1) the LOCATION hunt · (2) the WALLPAPER hunt · (3) the final curation SOLVE + release render. `MODE_POLICY` is the one place a mode carries a standing; Matt iterates from pictures, not counts. Phase 3 is Matt's eye on the final seating — no label-feedback loop, not tracked.

**STANDING DIRECTION (Matt): THE SIMPLE LOOP.** Mine until the pool is healthy across palettes, modes, locations and families → solve at whatever n → if a gallery comes up short, mine longer until it looks good to Matt's eye. General mining = breadth to OPEN places (full roster; breadth has no per-mode weight), the near band ONCE over the night's own places (`--near-places`), the dear kinds on the floor draw; phoenix planes at SECONDS shares (`phoenix:classic` 3%, `phoenix` 15% — acting since ckpt 105, never yet run as a full night). **K stands; the spiral cap is 10% and is now the DEFAULT; no walk downweight for spirals.** `--draw-cells` is a composition instrument for n≤1000 only (ruled ckpt 106). **No mining for a while (Matt, 2026-09-04).**

**THE SOLVE FILLS THE GALLERY (ckpt 106).** `curate solve run` = view → seed → 1-swap → augmenting chains (depth 2) → 1-swap → record, `--augment on` by default. n=750 and n=1000 fill outright (911 → 1,000 at n=1000; shortfall back to 0, sum above the incumbent, worst seated 0.188 → 0.122), 110 s. n=2000 unmeasured with the shipped stage (prototype: +309 of 379, 26 min, budget expected to bind). Every earlier seat count (947, 930, 911, 1,621…) is a pre-augment number.

This era (ckpt 105→106, one day): eighteen prompts, all reported and absorbed. The rare-cell mine read (aim is an n=1000 artefact; near band is the seat-buyer); `exp_smoothing` evaluated, dropped to niche, its stranded rows restocked as `smooth` (`curate remode`), deleted from the site; solve bound + profile → four speedups (275 → 119 s at n=2000) → augment pass built and shipped; nested verbs as real subparsers; spiral cap default; CLAUDE.md rules-only; Rendering Modes page final (v3 + wording fix, judge tier table); reframe channel's unfired roots fired (`g7`: the widening is the whole yield, 128× is the wall).

## IN FLIGHT ACROSS THIS BOUNDARY
Nothing.

## QUEUED IN DRIVE `prompts\` — not started, for the next instance (Matt: keep these, wipe nothing else)
- `LADDER_extend_0904.md` (wallpapers, commits): reframe ladder → drop 8×/12×, add 192×/256×; 20-min continuation `g8` over the 1,263 unfired roots; contact sheet of the new-end picks for Matt's eye (minibrot frames or filament frames?).
- `READ_stale_seat_files_0904.md` (wallpapers, read-only): 17 of 241 seats on `20260904T023748Z` whose stored file ≠ a re-render of its recipe (recorded 0.936 / re-rendered 0.24, 14 from `depth/`); first hypothesis `acted_unrecoverable` autolevel; population question = how many site seats cannot be regenerated from their row.

## NEXT CHECKPOINT GOAL
Matt's to set. Nothing is assumed or scheduled.

## OPEN (ordered) — Matt raises each
1. **Website: four figures carry the retired mode** (`gallery-floors` and `wallpapers-mine` show its NAME in the picture; `overview-pipeline` 1 of 3 front-page wallpapers and `gallery-output` 4 of 24 tiles stand on its panels). Matt: "later." Two panel re-picks; `wallpapers-mine` a re-bake; `gallery-floors` needs a solve record under the current roster — an augmented n=1000 record fills the gallery and is the natural re-base moment (also for the deferred `pipeline-growth` re-bake). The site-side vocabulary ban waits on this (`vocabulary.py` docstring names the blocker).
2. **Augment at n=2000**: `--augment-seconds` default 300 will bind; the prototype left 70 seats unknown (search not exhausted; depth ≥4 unsearched). A budget question when Matt wants n=2000.
3. **Modes page wallpaper-render column** is a ×64 proxy of the candidate mean; 169 renders finish it (rig `fractal-website/scratch/_modes_render_times.py`, `page-review.md`). The judge tier table dies on the next judge adoption (`page-review.md`).
4. Nested-verb / CLAUDE.md / exp_smoothing arcs: closed. `RETAIN_PER_PAIR` parked with a second number (→ parked.md).
Parked by Matt (medium refactors): `models/render_fit.py`, `models/bar.py`, `curation/leg.py`, flat `tests/`; `curate_commands.py` stays one module.

## STATUS / KNOWN REDS
None. Wallpapers fast lane 97.6 s / 3,573 (116 deselected; `.[dev,models]` install); slow lane 6:31 / 3,681 (`remode` commit, before augment); `cargo test` 216. Website `builder check` 18 green, nothing skipped; 47 JS tests. Box uptime under a week. Solve ~110 s at n=1000 with augment (51 s without).

## RULINGS THIS ERA
→ `preserve\settled_rulings.md §ckpt 106`.

## KEEP LIST
Drive `prompts\`: KEEP `LADDER_extend_0904.md`, `READ_stale_seat_files_0904.md`; wipe the rest. `reports\`: nothing to extract (this era's survivors are in the READMEs, `solver_design.md` and the docs) — wipe everything. Wallpapers `scratch/`: wipe `rare_cells_yield_0904/`, `exp_smoothing_0904/`, `exp_smoothing_resolve/`, `solve_bound_0904/`, `solve_speedups_0904/`, `augment_0904/`, `augment_ship/`, `reframe_unfired_0904/`; `probe_spiral/` is Matt's. Website `scratch/`: KEEP `_modes_render_times.py`.

## OWED
Nothing.

## SCRATCH/ARTIFACT FLAGS
Standing KEEP: `artifacts/curation/candidate_ledger/` (211,609 rows after the `remode` merge · clearing pool 18,628 rows / 9,286 places at the accepted roster) · the FIVE Durables · `neutral_embeddings.jsonl` (40,734 admitted) · `artifacts/curation/` HOT · live release rows · `artifacts/reframe_g1,g2,g4…g7` (g7 = latest, re-found 23.9%, chain unspent) · `artifacts/curation/tentative/<stamp>/` (the site stands on `20260902T161757Z`, `20260902T164622Z`, `20260904T023748Z` (capped); `20260904T080248Z` / `20260904T134242Z` are UNCAPPED — never mix the groups; all pre-augment) · `artifacts/curation/growth/20260902T150756Z/` · `data/coloring/texture_flat.jsonl` · `data/spiral/` · `models/spiral/` · `models/render/` weights-v6 beside v5 · `artifacts/render_folds/` · leg records: the four `rare_*`, the `remode` leg, `mine_diverse_0903`, `draw_cells_smoke`, `tentative_n1000_<stamp>`. ARCHIVED (RESTORE before reuse): `sheet_reframe_nuclei` · nine unreferenced legs/sheets · `mode_sheet` · `calibration` · `correction` · `palette_mass_sweep_calib`. Walk ledgers: seven hot, nine archive; no reframe leg archived.

## CLOSED (records wiped — verdicts in the docs and settled_rulings)
READ_rare_cells_yield_0904 · EVAL_exp_smoothing_0904 · DROP_exp_smoothing_0904 · MAKE_exp_smoothing_as_smooth_0904 · TIDY_nested_subparsers · READ_solve_bound_and_profile_0904 (+addendum1) · READ_augment_pass_0904 · BUILD_augment_solve_0904 · TIDY_claude_md_0904 · PLACE_rendering_modes_v2/v3_0904 · FIX_modes_page_wording_0904 · RUN_reframe_unfired_0904 · PRE_CLOSEOUT_0904.

## PARKED / SETTLED
→ `preserve\parked.md` (this era: `RETAIN_PER_PAIR` second number; augment at n=2000; the wallpaper-render column; the rung-frame overwrite; the wasm string; the twin-aware seed, superseded), `preserve\settled_rulings.md`, `preserve\sourcing_channel_laws.md`. `input_detail` PARKED on its ckpt-93 terms. The `mine` leg's autolevel stamp gap PARKED.
