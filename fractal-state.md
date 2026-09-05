# fractal-state — checkpoint 107 (2026-09-05)

## Where we are
THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE: (1) the LOCATION hunt · (2) the WALLPAPER hunt · (3) the final curation SOLVE + release render. `MODE_POLICY` is the one place a mode carries a standing; Matt iterates from pictures, not counts. Phase 3 is Matt's eye on the final seating — no label-feedback loop, not tracked.

**STANDING DIRECTION (Matt): THE SIMPLE LOOP, mining RESUMED (2026-09-05).** Mine until the pool is healthy across palettes, modes, locations and families → solve at whatever n → if a gallery comes up short, mine longer until it looks good to Matt's eye. This era set three mining goals at once — the rare vivid palettes (themed n=200 galleries), the general n=1000 gallery, and more `smooth_angle_min` / `smooth_mean_angle` pictures — with the split "distribution, not cleverness": levels are watched on the balance census and CEILINGS (the spiral cap's shape) are Matt's instrument if one runs away. **Busy-over-sparse in the seating is INTENTIONAL** (the rank key reads flatness). K stands; spiral cap 10% default; τ = 0.034281 (0.90×) since this checkpoint, Matt judges by eye as galleries land.

**Records.** The augmented solve fills n=1000 exhaustively; a tentative record is PUBLISHED only when Matt names it (→ tutorial). PUBLISHED: `20260904T233233Z` (augmented n=1000, OLD τ — the site's figures and the friends' n40/n250 kits stand on it) + the three pre-augment stamps the site stands on. Publication and the site re-base wait until nearer finalizing (Matt). UNPUBLISHED in the store (all prune-protected, none durable): `20260905T023657Z` (n=1000 at the new τ, pre-1h pool — the "before both mines" general point) · two n=2000 augment reads (300 s / 1,800 s, `20260904T2337…`-era) · four τ counterfactuals (`20260905T0214…`) · six themed n=200 baselines and six post-1h themed records (`themed_<cell>_n200…`) · the pre-8h and post-8h records the overnight writes.

This era (ckpt 106→107, one day): fourteen prompts reported and absorbed. Stale-seat finding overturned (routed-mode reader trap); reframe ladder extended to 16–256× and closed; FGL page pass 2; augmented n=1000 record + n=2000 budget read; the record-publication ruling; the balance census; the twin boundary sitting → τ 0.90×; friends' votes viewer built (v2.0) and priced; themed n=200 baselines; the 1 h thin-cell mine (recolour proven places is the cheapest q4); website `RUN_RECORDS` gap closed with a reachability guard.

## IN FLIGHT ACROSS THIS BOUNDARY
**`MINE_overnight_8h_0905` (+ `_ADDENDUM1`)** — wallpapers, unattended, 8 h of leg time: arm 1 general breadth + near band (3 h, opener sized with room under `RETAIN_PER_PAIR`) · arm 2 recolour proven places into the fifteen thin cells (2.5 h; `smooth`/`stripe`/`tia`) · arm 3 angle-mode dump (1.5 h) · arm 4 full-render modes unaimed (1 h). Readout = three tables: themes vs `baseline.json` AND post-1h; n=1000 vs the pre-8h record (addendum) / `20260905T023657Z` / published; the balance census with the angle modes and `threads` called out; plus a same-recipe-duplicates READ (what the key collapses, what can still vary inside a (location, mode, palette) triple, whether the retained three can be one palette). Sheets per arm in `scratch/overnight_8h_0905/`. **The next instance reads its report first**; three decisions hang on it (OPEN 1–3).

## QUEUED IN DRIVE `prompts\` — none. The two in-flight files stay there for reference.

## NEXT CHECKPOINT GOAL
Matt's to set. Nothing is assumed or scheduled.

## OPEN (ordered) — Matt raises each
1. **From the 8 h report: ceilings.** Per-mode ceilings (spiral-cap shape) if a level ran away — `threads` (20% of seats from 3% of pool) first candidate; composites 44%, centered 34%. Decided from the census table, by eye on the pictures.
2. **From the 8 h report: the duplicate-recipe rule.** Matt's concern: over 10k hours the ledger converges on three near-copies of one palette per pair. Ruling after the read; expected shape "one row per (location, mode, palette); the retained three are three palettes."
3. **From the 8 h report: next-night sizing** — seconds per kept q4 clear per arm.
4. **`release.parity` drops `mode_params`** (`release.py:578`) — a parity run over a varied plan compares two bare renders and passes. Small wallpapers fix, owed.
5. **Consumed-roots record for reframe continuations** — barren re-offers cost 46% of `g8`; Matt: discuss at this checkpoint.
6. **Full friends' kit**: which record, when. Ruled: ss2 with `smooth_mean_angle` at ss4 for the friends' round (≈5.1 h + the ss4 seats), ss4 for the true final; q85 4:2:0; zip size not a concern yet. Ingest of `<name>_labels.json` UNBUILT; how the votes are used is Matt's to dictate.
7. **Augment at n=2000** — a search-cost question (chain search dominates there); only when Matt wants n=2000.
8. **Website**: four figures on the retired mode / re-base / publication — nearer finalizing (Matt). Modes page wallpaper-render column is a ×64 proxy (169 renders finish it; rig `fractal-website/scratch/_modes_render_times.py`).
9. **Before the first FINAL n=2000 record**: `index.html` crosses 1 MiB at ~1,600 seats — untrack it (regenerate from `gallery.jsonl`) or `LARGE_TEXT_ALLOWLIST`; a decision.
Parked by Matt (medium refactors): `models/render_fit.py`, `models/bar.py`, `curation/leg.py`, flat `tests/`; `curate_commands.py` stays one module.

## STATUS / KNOWN REDS
None known. Wallpapers fast lane green at the last commit (`SOLVE_themed…`/`BUILD_v2`; counts in those reports); slow lane last run at `SET_tau`; `cargo test` unchanged. The nested-verb `SURFACE` table pins every flag list — a new flag is a red until listed (expected). Website `builder check` 18 green, nothing skipped; 47 JS tests. Solve ~117 s at n=1000 with augment.

## RULINGS THIS ERA
→ `preserve\settled_rulings.md §ckpt 107`.

## KEEP LIST
Drive `prompts\`: KEEP `MINE_overnight_8h_0905.md`, `MINE_overnight_8h_0905_ADDENDUM1.md` (in flight); wipe the rest. `reports\`: wipe everything present at closeout (survivors are in the docs and READMEs); the overnight report lands after. Wallpapers `scratch/`: KEEP `n1000_census_0905/` (balance rig), `themed_baselines_0905/` (rig + `baseline.json`), `thin_cells_1h_0905/` and `overnight_8h_0905/` (sizing evidence until the next night is planned), `twin_boundary_0905/` (verdicts also in `labels/twin_verdicts.json`); WIPE `votes_pilot/`, `twin_tau_candidates_0905/`, `ladder_0904/`, `stale_seats_0904/`; `probe_spiral/` is Matt's. Website `scratch/`: KEEP `_modes_render_times.py`.

## OWED
`release.parity` fix (OPEN 4). Nothing else.

## SCRATCH/ARTIFACT FLAGS
Standing KEEP: `artifacts/curation/candidate_ledger/` (post-1h pool stamp `644d466b2e25`; the overnight re-stamps) · the FIVE Durables · `neutral_embeddings.jsonl` · `artifacts/curation/` HOT · live release rows · `artifacts/reframe_g1,g2,g4…g8` (g8 = latest, re-found 57.5%) · `artifacts/curation/tentative/<stamp>/` — the published four + every unpublished record above (prune-protected; delete a record to release its seats) · `artifacts/votes/` kits (`20260904T233233Z_n40_ss2_angle4`, `…_n250_ss1_v2`; finished bulk) · `artifacts/curation/growth/20260902T150756Z/` · `data/coloring/texture_flat.jsonl` · `data/spiral/` · `models/spiral/` · `models/render/` weights-v6 beside v5 · `artifacts/render_folds/` · leg records: `thin_a/b1/b1b/b2/c` (the 1 h), the overnight's four, `mine_diverse_0903`, the four `rare_*`, the `remode` leg. ARCHIVED (RESTORE before reuse): unchanged from ckpt 106. Walk ledgers: seven hot, nine archive; no reframe leg archived.

## CLOSED (records wiped — verdicts in the docs and settled_rulings)
READ_stale_seat_files_0904 · LADDER_extend_0904 · FIX_finding_good_locations_pass2_0904 · RECORD_augmented_n1000_and_n2000_0904 · BUILD_votes_viewer_and_pilot_0904 · READ_n1000_balance_census_0905 · SHEET_twin_boundary_0905 · READ_twin_verdicts_and_tau_candidates_0905 · SET_tau_0p90_and_votes_keys_0905 · SOLVE_themed_baselines_n200_0905 · MINE_thin_cells_1h_0905 · BUILD_votes_viewer_v2_debug_0905 · PRE_CLOSEOUT_website_0905.

## PARKED / SETTLED
→ `preserve\parked.md` (this era: `index.html` tracking / 1 MiB; the rung-frame overwrite stands), `preserve\settled_rulings.md`, `preserve\sourcing_channel_laws.md`. `input_detail` PARKED on its ckpt-93 terms. The `mine` leg's autolevel stamp gap PARKED. `RETAIN_PER_PAIR` second number PARKED.
