# fractal-state — checkpoint 109 (2026-09-06)

## Where we are
THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE: (1) the LOCATION hunt · (2) the WALLPAPER hunt · (3) the final curation SOLVE + release render. `MODE_POLICY` is the one place a mode carries a standing; Matt iterates from pictures, not counts. Phase 3 is Matt's eye on the final seating — no label-feedback loop, not tracked. **NO PUBLISHING OF ANY KIND until Matt raises it — never ask, never list it.**

**STANDING DIRECTION (Matt): THE SIMPLE LOOP.** Mine until the pool is healthy across palettes, modes, locations and families → solve at whatever n → if a gallery comes up short, mine longer until it looks good to Matt's eye. "Distribution, not cleverness": levels are watched on the balance census and CEILINGS are Matt's instrument if one runs away. Busy-over-sparse in the seating is INTENTIONAL. K stands; τ 0.90× stands. The angle modes are OFF the mining goals (over-seated already); `curvature` is UNMINED since this checkpoint. **ACTIVE GOAL: push the thin themes' quality** (green, yellow; lime/cyan/teal) — recolour-into-cell is the lever. The ckpt-109 sheet answered the open read: the judge-disliked-hue tail is the JUDGE's, not the pictures' (→ fractal-corpus), and no retrain was taken on it.

**This era (ckpt 108→109, one day): the 120-palette drop, end to end.** Ingest (`classic-pairs-2026-09`, all cyclic, zero name collisions) → a 580-row sitting (480 correction rows over the drop's best four pictures each, plus the 100-row `blind_palettes` instrument) → a 1 h aimed mine → a fresh solve. The drop seats: **54 new-map pictures in the general n=1000 against the baseline's 25, from 44 distinct maps, and 74 of the 120 seat somewhere.** Worst seat rose 0.152 → 0.216 with the sum up 1.80. Yellow answered (its cell 68 → 78, deepest reach of any theme); green did not (one new-map seat in the general). Website: `finding-good-locations` placed at v6 and swept of em-dashes, `wallpapers-three-bands` and a re-picked `modes-gallery` built off committed records only.

**Records.** Published, and the four the site stands on: `20260902T161757Z` · `20260902T164622Z` · `20260904T023748Z` · `20260904T233233Z`. New this era, unpublished, prune-protected: the **pre-mine baselines** at pool `2f8f271028e5` / commit `7eaf9b4` (general `20260905T233439Z` + six themed `20260905T2336–2340Z`) and the **post-mine set** at pool `6d74bf49abeb` / commit `1308300` (general `20260906T022930Z` + six themed `20260906T0231–0236Z`). The two sets differ ONLY by the mine's 10,121 rows and were solved under identical config — they are the one clean before/after in the store. Older ckpt-108 records remain; deleting a record releases its seats. Pool stamp `6d74bf49abeb`; ledger 261,616 rows, 214,059 candidates, 26,406 reachable locations.

## IN FLIGHT ACROSS THIS BOUNDARY — none.

## QUEUED IN DRIVE `prompts\` — none.

## NEXT CHECKPOINT GOAL
Matt names it at the top of the next checkpoint. Nothing is assumed or scheduled here.

## OPEN (ordered) — Matt raises each
1. **Full friends' kit — ACTIVE.** Which record, when. Ruled: ss2 with `smooth_mean_angle` at ss4 for the friends' round, ss4 for the true final; q85 4:2:0; zip size not a concern yet. Ingest of `<name>_labels.json` UNBUILT (the schema is the contract); how votes are used is Matt's.
2. **Website** (Matt's pace). The **em-dash sweep**: the rule is standing in `writing-guidance.md`, `finding-good-locations` is swept, ten pages are not — body+caption counts are rendering modes 31+9, full pipeline 26+0, rendering fundamentals 25+2, training judges 25+0, escape-time fractals 22+6, color palettes 19+0, overview 18+2, gallery curation 17+0, finding good wallpapers 9+0, make-your-own 3+0; captions exist only on the four earliest pages. Method: Claude authors sentence-level hunks, applied to page and master together, page by page. **Two decisions owed:** whether the rule extends to ALT TEXT (8 occurrences, outside the rule as written), and how `fractal-atlases` is handled — its two sit in an intro section no counter reads, so it will report clean while carrying them. Also still open: re-base onto a newer record; the modes-page wallpaper-render column (a ×64 proxy, 169 renders, rig `fractal-website/scratch/_modes_render_times.py`). Stale figures and prose are NOT tracked or refreshed until "ready for publishing"; holds live in `docs/page-review.md`.
3. **`color_mass` — TODO (Matt queued it).** The drop's 120 maps have no row and are read through the carrier prior, so cell aiming mostly cannot see them (20 of 120 survive a four-thin-cell cut). Nothing in the solve reads it. Cost, keying and what a close would take → `palettes/README.md`.
4. **`groups.jsonl` re-cut — computed, NOT applied; blocked behind item 3.** Purely additive and no existing group changes membership, but a re-cut renumbers group ids and `color_mass` is keyed on them. Numbers and the four-step recipe → `palettes/README.md`.
5. **`carriers.jsonl` size guard** — reached by the drop AFTER next, not the next one. Reading and relief options → `palettes/README.md`.

Parked → `preserve\parked.md`: augment at n=2000; the rung-frame overwrite; the `mine` leg's autolevel stamp gap; medium refactors (`models/render_fit.py`, `models/bar.py`, `curation/leg.py`, flat `tests/`; `curate_commands.py` stays one module).

## STATUS / KNOWN REDS
None known. Wallpapers fast lane green at PRE_CLOSEOUT, with five new guards in `tests/test_mode_policy.py`; `cargo test` unchanged. Website `builder check` 17 green, nothing skipped; 47 JS tests; `ruff` clean. Solve ~105 s at n=1000 with augment.

## RULINGS THIS ERA
→ `preserve\settled_rulings.md §ckpt 109`.

## KEEP LIST
Drive `prompts\`: wipe everything (nothing in flight, nothing queued). `reports\`: wipe everything. Wallpapers `scratch/`: KEEP `overnight_8h_0905/census/` (the balance-census rig the ceilings are read from) and `probe_spiral/` (Matt's); WIPE everything else, including this era's leg and headroom scratch. Website `scratch/`: KEEP `_modes_render_times.py`, the walk-descent figure rig, and `three_bands/pick_seats.py` (the seeded seat picker both figure draw rigs now carry).

## OWED
Nothing.

## SCRATCH/ARTIFACT FLAGS
Standing KEEP: `artifacts/curation/candidate_ledger/` (pool stamp `6d74bf49abeb`) · the FIVE Durables · `neutral_embeddings.jsonl` · `artifacts/curation/` HOT · live release rows · `artifacts/reframe_g1…g8` · `artifacts/curation/tentative/<stamp>/` — every record above (prune-protected) · `artifacts/votes/` kits · `artifacts/curation/growth/20260902T150756Z/` · `data/coloring/texture_flat.jsonl` · `data/spiral/` · `models/spiral/` · `models/render/` weights-v6 beside v5 · `artifacts/render_folds/` · leg records: `sheet_pilot`, `sheet_leg_0905`, `maps_smooth_0905`, `maps_tia_0905`, `maps_stripe_0905`, `maps_curvature_0905`, `night_a1/a2/a3/b/c/d`, `thin_a/b1/b1b/b2/c`, `mine_diverse_0903`, the four `rare_*`, the `remode` leg. WIPE: `artifacts/curation/headroom/pre_closeout_0906/` (re-runnable). ARCHIVED (RESTORE before reuse): unchanged from ckpt 106. Walk ledgers: seven hot, nine archive; no reframe leg archived.

## CLOSED (records wiped — verdicts in the docs and settled_rulings)
INGEST_new_palettes_0905 · SHEET_new_palettes_0905 · INGEST_new_maps_labels_0905 · CHECK_dud_maps_0905 · MINE_new_maps_1h_0905 · SOLVE_after_new_maps_0905 · EDIT_locations_page_figures_0905 · PLACE_locations_v6_0905 · EDIT_website_figures_and_captions_0905 · PRE_CLOSEOUT_wallpapers_0906 · PRE_CLOSEOUT_website_0906.

## PARKED / SETTLED
→ `preserve\parked.md`, `preserve\settled_rulings.md`, `preserve\sourcing_channel_laws.md`.
