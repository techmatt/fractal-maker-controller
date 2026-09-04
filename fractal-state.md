# fractal-state — checkpoint 105 (2026-09-04)

## Where we are
THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE: (1) the LOCATION hunt · (2) the WALLPAPER hunt · (3) the final curation SOLVE + release render. `MODE_POLICY` is the one place a mode carries a standing; Matt iterates from pictures, not counts. **Phase 3 is Matt's eye on the final seating — no label-feedback loop, not tracked (ruled ckpt 104).**

**STANDING DIRECTION (Matt): THE SIMPLE LOOP.** Mine until the pool is healthy across palettes, modes, locations and families → solve at whatever n → if a gallery comes up short, mine longer until it looks good to Matt's eye. General mining = breadth to OPEN places (full roster; a cheap field share is permission, not a target — breadth has no per-mode weight), the near band ONCE to make fresh places pay (`--near-places` since ckpt 105), the dear kinds on the floor draw (→ discovery §Mining economics); the phoenix planes at SECONDS shares (`phoenix:classic` 3%, `phoenix` 15% — **acting only since the ckpt-105 fix; every leg before it drew both at 0.25 turns**); the palette draw narrowed by `--draw-cells` when composition is the goal. **K stands; the spiral cap is 10%; no walk downweight for spirals (ruled); pool quality is Matt's read.** The rare-cell instrument WORKS (listed cells +6 net at n=1000, thinnest cells moved most) — it has never run at the corrected phoenix mix.

This era (ckpt 104→105, one day): sixteen prompts, all reported and absorbed. Codebase census follow-ups → four structural moves (ledger package, `cli/` package, cycle/layering tidy, `curation/README.md` four-way split) and their tidy; the Rendering Modes page rebuilt around thirteen per-mode 2×2 figures from the capped record; the rare-cell mine (`MINE_rare_cells_0904`) and the seconds-share fix it exposed; line-ending drift found (20 files) and closed machine-wide. Largest import cycle 70 → 44.

## IN FLIGHT ACROSS THIS BOUNDARY
Nothing (FIX_website_line_endings_0904 assumed closed clean — if its report says otherwise, its findings go on OPEN 1's list).

## NEXT CHECKPOINT GOAL
Matt's to set. Nothing is assumed or scheduled.

## OPEN (ordered) — Matt raises each
1. **Rendering Modes prose pass.** Figures are placed; the master waits on two of Matt's reads from the site: `exp_smoothing` (nearly no change vs `smooth` at both locations — re-pick or soften) and `modes-itinerary` row 1's hard edges vs the wedge-seam paragraph. Then a wholesale master → `prose\` → PLACE. The BUILD report's six contradictions (direct-traps ¶2 claims a same-geometry comparison no figure shows; blending ¶1 names four composites for five figures; fields wants the "one location twice" sentence; `exp_smoothing` claim; itinerary ¶3; `modes-gallery` scoreboard says fourteen — correct) are the whole delta.
2. **`exp_smoothing` — drop candidate.** Evaluate across the whole 1000 gallery: the field dump makes it cheap — recolour every seat location `smooth` vs `exp_smoothing`, per-seat pixel and judge delta, sorted, so the difference is seen before the mode is dropped (weight 0 is the drop mechanism).
3. **Nested-verb spelling → real subparsers (ruled ckpt 105, unscheduled).** Typed commands are unchanged either way; one mechanical prompt with a `--help` diff when there is nothing better to run.
4. **`RETAIN_PER_PAIR`** — now with a number: the near band is 7.2× breadth per engine second and discards 5 of 8 by construction (3 vs width 8; 12.6% survive, third reading). Parked with the number.
5. **Rare-cell instrument at the corrected phoenix mix** — a rerun is a new budget question. **1,518 of 2,153 proven roots unfired** (reframe channel); nucleus yield unread.
6. **Website**: NOTHING IS LIVE; gallery page waits for Matt; `pipeline-growth` re-bake at the final pool, if ever. `docs/page-review.md` owns the pile.
Parked by Matt (medium refactors, not low-hanging): `models/render_fit.py` (then `render_grade`/`render_dose` cullable), `models/bar.py` across the five acceptance modules, `curation/leg.py` under the four legs; the flat `tests/` dir; `curate_commands.py` stays one module (registration order is `--help` surface).

## STATUS / KNOWN REDS
None. Wallpapers fast lane 119.9 s / 3,458 (comparable only across a `.[dev,models]` install — a torch-less interpreter collects 57 fewer, now reported not silent); slow lane 6:54 / 3,574 (clean, `8c753b4`); `cargo test` 216. Website `builder check` green (16 named + the line-endings guard if it landed as a check). Largest SCC 44. Box uptime under a week (reboot at ckpt 103); 20 CRLF worktree files normalised zero-diff; `~/.claude/` hook + `CLAUDE.md` override in place (box facts → fractal-operating).

## RULINGS THIS ERA
→ `preserve\settled_rulings.md §ckpt 105`: no walk downweight for spirals · modes page = two examples per mode, 2×2 smooth-left, unique locations, no `smooth` figure, no dtm variants shown · `curate gallery` → `curate solve record` · `curate_commands` stays one module · nested verbs → real subparsers · a line number is not an anchor · "half is fine" = permission · a test count is comparable only across the same install · `phoenix:classic` above its 3% is the one-place-per-draw floor, by design · eager re-export is banned (one binding per name) · `exp_smoothing` under evaluation, not yet dropped.

## KEEP LIST
Drive `prompts\`: nothing in flight — wipe everything (dead: `RUN_slow_lane_0904`, superseded by the CRLF commit's clean run). `reports\`: **EXTRACT `line-ending-drift-playbook.md` → `preserve\line_ending_playbook.md`** (the apply prompt does it); then wipe everything. Wallpapers `scratch/`: wipe `modes_carry/`, `modes_seats/` (figures placed), `rare_cells_0904/` (absorbed; bars derive at read time); `probe_spiral/` is Matt's (the 1e-8 drift is nothing). Website `scratch/`: nothing.

## OWED
Nothing.

## SCRATCH/ARTIFACT FLAGS
Standing KEEP: `artifacts/curation/candidate_ledger/` (210,845 rows · 24,191 locations · clearing pool 22,275) · the FIVE Durables (manifest hashes guarded per test session) · `neutral_embeddings.jsonl` (ADMITTED, 40,734) · `artifacts/curation/` HOT · live release rows · `artifacts/reframe_g1,g2,g4…g6` · `artifacts/curation/tentative/<stamp>/` (tracked; the site stands on `20260902T161757Z`, `20260902T164622Z` and `20260904T023748Z`; Matt's pair `20260903T234205Z`/`20260904T023748Z`; the rare-cell pair `20260904T080248Z` (941) / `20260904T134242Z` (947, spiral 25.8%)) · `artifacts/curation/growth/20260902T150756Z/` · `data/coloring/texture_flat.jsonl` · `data/spiral/` · `models/spiral/` · `models/render/` weights-v6 beside v5 (`RUNS.md` maps the 25 run dirs) · `artifacts/render_folds/` · solve records `v6_flip_n2000` · `mine_diverse_0903` · `draw_cells_smoke` · `tentative_n1000_<stamp>` · the four `rare_*` leg records (realised shares read from them). ARCHIVED (RESTORE before reuse): `sheet_reframe_nuclei` · nine unreferenced legs/sheets · `mode_sheet` · `calibration` · `correction` · `palette_mass_sweep_calib`. Walk ledgers: seven hot, nine archive; no reframe leg is archived.

## CLOSED (records wiped — verdicts in the docs and settled_rulings)
TIDY_census_followups_0904 · SPLIT_candidate_ledger_0904 · SHEET_modes_carry_0904 · SPLIT_cli_0904 · TIDY_cycle_and_guards_0904 · SPLIT_curation_readme_0904 · POLISH_help_groups_0904 · FIX_website_solve_record_0904 · SHEET_modes_seats_0904 · TIDY_wrapup_0904 (+addendum1) · BUILD_modes_page_figures_0904 (+addendum1) · FIX_handoff_pointers_0904 (+_b) · MINE_rare_cells_0904 · FIX_seconds_share_0904 · the CRLF drift work (`8c753b4`) · FIX_website_line_endings_0904.

## PARKED / SETTLED
→ `preserve\parked.md` (this era: `RETAIN_PER_PAIR` with its number; ~1,470 leaked process objects still unexplained), `preserve\settled_rulings.md`, `preserve\sourcing_channel_laws.md`. `input_detail` PARKED on its ckpt-93 terms. The `mine` leg's autolevel stamp gap PARKED (52.8% of depth rows unreplayable; five modes-page right panels are copied seat JPEGs for that reason).
