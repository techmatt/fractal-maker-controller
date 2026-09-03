# fractal-state — checkpoint 103 (2026-09-03)

## Where we are
THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE: (1) the LOCATION hunt · (2) the WALLPAPER hunt · (3) the final curation SOLVE + release render. `MODE_POLICY` is the one place a mode carries a standing; Matt iterates from pictures, not counts.

**STANDING DIRECTION (Matt): THE SIMPLE LOOP.** Mine until the pool is healthy across palettes, modes, locations and families → solve at whatever n → if a gallery comes up short, mine longer until it looks good to Matt's eye. General mining = breadth to OPEN places (full roster, a large cheap smooth/field share — ≥50% is fine), the near band to make them pay, the dear kinds on the floor draw (→ discovery §Mining economics); the phoenix planes at 0.25 weight in breadth (kept for now, ruled ckpt 103); the palette draw filtered away from the full colour cells when composition is the goal. **K stands and pool quality is Matt's read.** **At n=2000 the constraints choose the gallery, not the judge** (→ discovery §What binds) — the top end is bought by labels on seats, if and when Matt raises it.

This era (ckpt 102→103, one day): twelve prompts, all reported and absorbed.
- **Render judge v6 SHIPPED** on v5's recipe over 722 new rows (four sittings ingested: dtm 188, phoenix band 200, judge band 300, classic 34); adoption unconditional, no eval instrument, Matt is the instrument (→ corpus §Judge method; `preserve\judge_training.md §v6`). Flip at n=2000: 1,578 → 1,635 seats with three quarters of the seats turned over; Matt's eye: fine.
- **The judge has no order inside its own top, on any kind** — every sitting this era said so (→ corpus).
- **Roots law widened:** a finished-render q3+ verdict is a proven root (→ discovery).
- **The near band is 24× cheaper per clear than breadth** — MINE_diverse_0903: 18,940 candidates, seats 1,635 → 1,669, the whole gain in OPEN cells; the palette filter is a composition instrument (→ discovery).
- Phoenix downweight in code (`draw_weights.py`); candidate rows stamped at intake; `depth` records keep the whole autolevel stamp; `--draw-maps`, `--explain-seats-of`, by-(mode, settings) records (→ tutorial, engine).
- **The box leaks commit charge** — reboot cadence is the rule (→ operating). Matt rebooted at this boundary.

## IN FLIGHT ACROSS THIS BOUNDARY
Nothing.

## NEXT CHECKPOINT GOAL
Matt's to set. Nothing is assumed or scheduled.

## OPEN (ordered)
1. **The empty-cell leg (Matt's TODO, not scheduled).** Design, Matt's: the draw takes a sparse list of the 48 chromatic cells (default all = today's behaviour); maps whose carrier/`color_mass` probability for a listed cell clears a cutoff form the palette neighbourhood; mode-conditional mass where it exists, the carrier prior where not; run it through the near band so a recolour costs a colour pass. First read wanted: per empty cell (light/dark lime, yellow, magenta ~24–30 seats), carriers in the library, clearing rows in the pool, seats — if lime has three carriers the ceiling is the library, not the draw.
2. **`phoenix:classic` at 0.25 weight** while it clears 15.3% in a breadth arm (best partition by 2×) — Matt keeps 0.25 for now.
3. **dtm under v6 — Matt's read of the sheets** (`scratch/retrain_v6/c_…`, `scratch/mine_diverse_0903/d_…`): the four variants clear at half their v5 rate, bare rose; the leg's 16 clears were flat across settings (n tiny). Expected the opposite. His eye decides whether v6 learned the sitting.
4. **`models/render/README.md` says "no leak to chase, only a baseline to live under"** — wrong (the baseline IS the leak); one-line fix rides the next wallpapers prompt.
5. **`texture_flat` register has no entry at label geometry (1280×720 ss2)** — flat-texture modulates at label geometry route strange while being smooth material by rule; fired twice (9 of 300, then 4 of 6 `itinerary` cards). Ruling wanted: extend the register or accept.
6. **Phase 3 — Matt-curation of seats** (design question, his): 19.8% of seats sit at labelled PLACES, zero seated PICTURES carry a label; the judge does not order inside its top, so the top end is bought by labels on seats — seat, label the seats, demote non-fours, re-seat, repeat.
7. **Website review pile** (→ `docs/page-review.md`): unchanged from ckpt 102 (two false Gallery-curation claims; `palette-moods` caption; `judges`/`render-maxiter` repetition; `pool.py`'s two prose claims; the 16:46 standardization). The site stands on two v5 seatings — NOTHING IS LIVE; not a concern until Matt raises it.
8. `pipeline-growth` re-bake over 700/1000/2000 when the pool seats 2000.
9. Website consistency pass — DEFERRED until Matt raises it.

WATCH (no action owed): the next reframe leg MUST `--reprobe` · growth rerun wants a "freeze bars at the full pool" option · `Twins.hold` is lazy · **the fast lane never runs beside a leg** (commit, not time — CLAUDE.md) · ~1,470 leaked process objects on the box (separate from the commit leak, unexplained) · Drive Desktop lagged `reports\` by ~2 h once · `renders/` was restored HOT for the retrain (re-archive is Matt's).

## STATUS / KNOWN REDS
None. Wallpapers fast lane 157 s / 3,345 tests run alone after the leg; `cargo test` 216; slow lane 6:27 stands, not re-run. Website `builder check` 16/16 (untouched this era).

## RULINGS THIS ERA
→ `preserve\settled_rulings.md §ckpt 103`: v6 adopted unconditionally, Matt is the instrument, no eval bar · K stands · phoenix planes 0.25 for now · finished-store q3+ verdicts are proven roots, repo-wide · dtm roster = four entries, both-knobs excluded · boundary sittings are ±k around the crossing · "far-draw arm" deleted (no referent) · the unexported smooth card is forgotten · empty-cell leg on the TODO, unscheduled.

## KEEP LIST
Drive `prompts\`: nothing in flight — Matt wipes everything (dead: `READ_n2000_gallery_shortfall`, `SHEET_judge_band_300_addendum1`, `MINE_open_cells_overnight`). `reports\`: everything absorbed — wipe everything. Wallpapers `scratch/`: **KEEP `retrain_v6/` and `mine_diverse_0903/`** until Matt has looked at the dtm sheets (OPEN 3); wipe `dtm_variants/`, `phoenix_q3q4/`, `judge_band/`, `phoenix_classic_20m/`. Website `scratch/`: nothing new.

## OWED
Nothing. The README one-liner (OPEN 4) rides the next wallpapers prompt.

## SCRATCH/ARTIFACT FLAGS
Standing KEEP: `artifacts/curation/candidate_ledger/` (201,174 recipes) · the FIVE Durables · `neutral_embeddings.jsonl` · `artifacts/curation/` HOT · live release rows · `artifacts/reframe_g1,g2,g4…g6` · `artifacts/curation/tentative/<stamp>/` (tracked; the site stands on `20260902T161757Z` AND `20260902T164622Z`, both v5 seatings) · `artifacts/curation/growth/20260902T150756Z/` · `data/coloring/texture_flat.jsonl` · this era's `curation/depth/` run records · **`models/render/` weights-v6 (`481fe058…`) beside v5 (`deploy_seed1` = revert)** · solve records `v5_control_n2000` · `v6_flip_n2000` · `mine_diverse_0903` (the n=2000 baselines `empty_modes_n2000` and the `_2026-09-01` siblings are v5-era, superseded). ARCHIVED (RESTORE before reuse): `renders/` is HOT this boundary (see WATCH) · `sheet_reframe_nuclei` · nine unreferenced legs/sheets · `mode_sheet` · `calibration` · `correction` · `palette_mass_sweep_calib`. Walk ledgers: seven hot, nine archive.

## CLOSED (records wiped — verdicts in the docs and settled_rulings)
INGEST_dtm_variants_labels · FIX_phoenix_downweight_and_STAMP_candidate_provenance · SHEET_phoenix_q3q4_breadth · INGEST_phoenix_q3q4_labels · SHEET_judge_band_300 · INGEST_judge_band_labels · MINE_phoenix_classic_20m (+addendum1) · INGEST_phoenix_classic_labels · RETRAIN_render_v6 · READ_box_commit_charge · MINE_diverse_0903 · TIDY addendum1 (18 seats = flat-texture routing, closed).

## PARKED / SETTLED
→ `preserve\parked.md`, `preserve\settled_rulings.md`, `preserve\sourcing_channel_laws.md`. `input_detail` PARKED on its ckpt-93 terms (→ `preserve\judge_training.md`). The `mine` leg's autolevel stamp gap (`profile.jsonl` boolean; `mine.make` returns the stamp) PARKED.
