# fractal-state — checkpoint 156 (2026-09-29: the full set and the packs shipped (release `wallpapers-2026-09-29`); the twenty-one records published; Tools and data and Deep zoom videos pages; the link `curve` key; the judges-at-depth fold; README overhauls; `build` owns the site header; `deep_zoom_video_ckpt156` still rendering)

## Where we are
Three phases, each depending strictly on the one before (→ fractal-discovery). Matt iterates from pictures, not counts. Phase 3 is his eye on the final seating, and **every planned collection has a viewer at its official size.**

**★ MINING IS CLOSED (Matt, 2026-09-21) UNTIL HE REOPENS IT.**
- The pool as merged on 2026-09-21 is the population, and the `final139_*` solves (§RECORDS) are the published galleries.
- On a reopen, read `preserve\mining_laws.md` whole, then wallpapers `curation/LEGS.md §Mining is CLOSED (2026-09-21) — reopen inventory`. State carries none of it.
- ⚠ Before 2026-09-26, `headroom.population` never passed spiral scores to the solve, so every `curate headroom` census and `pool_draw` reading taken before then counted spiral places as uncapped. Production solves were never affected. Retake any such census before relying on it.

**★ EVERY COLLECTION HAS A TARGET, IN `curation/targets.py`: NINETEEN COLLECTIONS, TWELVE FAMILIES AND SEVEN MODES.**
- Reached by `curate solve run --collection NAME`; `--n` overrides; a collection with no target REFUSES. A change is a one-line edit there.
- ⚠ The general gallery's size is `tentative.RECORDED_SEATS` (1,000), not a `targets.py` entry.
- Matt has said the sizes are essentially final. The website's `builder/seats.py` hand-lists the collections.

**★ ⚠ GALLERY SIZE IS MATT'S DECISION ALONE.** Never raise it, queue it, or reason about shrinking `n`. "Final gallery quality" is his judgement, not a median. `final140_general2000` (n=2000) is offered on the site beside the n=1000 default.

**★ THE SAVED SET IS PUBLISHED (Matt, ckpt 156: "truly finalized").**
- `tentative.PUBLISHED` holds all twenty-one stamps; `KEPT_UNPUBLISHED` is empty. `tentative.DEFAULT = final139_general`, and `latest()` returns it first.
- All twenty-one are tracked whole, with their `recipes.jsonl` (63 files, 15.71 MiB). The per-file cap is `MAX_TRACKED_BYTES` = 2 MiB (`tests/test_history_purity.py`, raised from 1 MiB at ckpt 156).
- The website's seated-candidates header reads `"published": true`. The 6,299 gallery recipes are also published on Tools and data (`gallery-locations.jsonl`).
- **What remains of "truly finalized": the history rewrite** (OPEN 2). Any further publishing is Matt's to raise.

**★ PINNED SEATS.** `data/curation/pins.txt` → `curate pins resolve` → `pins.json`: ten pins, seated before the seed and prune-proof (→ `curation/GALLERY.md §Pinned seats`).

**★ THE BAR: `DEFAULT_FINE_BAR = 0.030242` ON THE FINE COLUMN**, under `fine_head = twelve_sheets_drop_high_asymmetric_auc_ge4_more_k3`.
- ⚠ A bar is unreadable without its head.
- ⚠ 0.50 is NOT the seating bar: `solve.Q4_BAR = 0.50` is the render judge's constant on `p_ge4`.
- `p_ge4` is the render judge's gate reading. `p_fine` is the fine head's column, where the bar lives: THE quality reading. Read q1 and the fraction above a mark, not the bare median.
- On the site: the location, wallpaper, palette and gallery judges.
- **`p_fine`, `p_coarse` and the bars are closed (Matt, 2026-09-12).** Provenance → `models/gallery_grade/README.md`.

**★ THE HUMAN VETO IS SHIPPED** (→ `curation/README.md`): Matt marks ONLY `1`s; an unmarked tile is not a label.

**★ A THEMED PASS RELAXES THE BAR INSIDE ITS OWN CELL** (`solve.themed_fine_bar`). ⚠ `--themed CELL` names a codebook cell; the family pass is `--collection <family>`.

**★ FAMILY PASSES FLOOR AT `mode_policy.seat_floors(n)`; A MODE PASS FLOORS AT 0.** ⚠ The floor is not monotone. The recurring family holes (`itinerary`, `curvature`, `direct_trap_lines`) are supply, not rule.

**★ COLOUR:** a hue family is not the union of its four cells (→ `palettes/README.md`). Curation constrains the 48 coloured cells only. The palette group cap is `0.075·n` themed and `0.025·n` general. K is Matt's; Claude never proposes reopening K.

**★ A GALLERY PAGE IS PRESENTED STRATIFIED** (`curation/page_order.py`). **★ GUARD RULINGS: loosening only, nothing loosened.** The solver is not at its optimum; Matt says that is not a concern. Other standing facts → `curation/GALLERY.md`. **★ `pool_scores.jsonl` IS ONE-SHOT: mine → merge → `gallery-grade score-pool` → solve.**

## MODES, PHASE, PALETTE
- **★ Seven targeted-gallery modes.** `curvature` is `UNMINED`.
- **★ The explorer's render-mode roster is thirteen** (`listedModes()`).
- **★ THE EXPLORER SHOWS ENGINE NAMES for modes and families (Matt, ckpt 156; a display-name pass was reverted).** The article teaches the same names.
- **★ Exponential smoothing reads as "smooth" on the site (Matt, ckpt 152)**; recipes keep `exp_smoothing`.
- **★ Texture weight, rotation and phase are CLOSED; palette replication is PARKED.** `data/palettes/palettes_for_random_choice.csv` (232 maps) is the approved-for-random list.
- **★ The explorer's palette modes are EXPLORER-ONLY** (`scale`, `lambda`, `period`; → `engine/README.md`, `explorer/README.md`).
- **★ THE PERIOD SLIDER MOVES IN CYCLES ACROSS THE FRAME (Matt, ckpt 155)** (→ `explorer/README.md`, `explorer/period-range.js`).
- ⚠ A seat's `mode` in `gallery.jsonl` is ROUTED; render at `recipe["mode"]`.

## TONE CURVES AND LINKS
- **★ Every gallery seat's tone curve is recorded** (`artifacts/curation/autolevel_backfill.jsonl` in wallpapers). The site's readers prefer a run's recorded stamp over a `rederived` one.
- **★ THE LINK CONTRACT SPELLS `curve` (ckpt 156):** `linear|sqrt|log|scurve`, omitted when it is the catalog's own. Owner: website `explorer/README.md`. Wallpapers `explorer_link.query_of` writes it byte for byte like the site (verified over 11,000 seats). **Every gallery seat's link now draws its picture; no seat has a `gap`.**
- Nine atlas `lost` dots are replayable after a `curate atlas --plane` rebuild (optional; 4 have no curve anywhere).

## FULL-RESOLUTION WALLPAPERS AND PACKS
- **★ THE FULL SET IS DONE:** 6,299 pictures at 2560×1440 ss3, JPEG q95 4:4:4, in `E:\FractalWallpapers\full\` with `membership.jsonl`. `curation/full_set.REGIME` is the one spelling; the `RELEASE_*` constants are retired, and `release.FORMER_RELEASE_REGIME` (ss4) reads history. Every file carries its explorer link; the eight that lacked one were re-stamped at ckpt 156.
- **★ THE PACKS ARE BUILT AND RELEASED:** 18 zips (15.1 GB) in `E:\FractalWallpapers\packs\`, uploaded as the release **`wallpapers-2026-09-29`** (latest) on `techmatt/fractals`. The site downloads through `releases/latest/download/<file>`, and the packs page shows sizes (`builder packs --import`).
  - ⚠ Four of the eight re-stamped pictures ship linkless inside the zips until the next pack rebuild.
  - **A rebuild** (votes via `--order`) goes to a NEW dated release with the same file names, marked latest; the site follows with no change.
- **★ THE PACKS (Matt):** n=1000 in three parts, in rank order; best 30, 100 and 200, nested in part 1; the twelve colour collections. Not shipped: n=2000 and the mode collections. Rank order is the seeded permutation (`packs.SEED = 20260926`) until votes arrive.
- **★ The wallpapers are licensed CC BY 4.0, credit Matt Fisher (linked to `techmatt.github.io`).** Both repos' code stays MIT.
- **★ FRIEND VOTES:** friends send Saved links; Matt says "ingest NAME <links>" to CC in fractal-website, which runs `builder votes ingest`. The store is `C:\Code\fractal-drive-sync\votes\events.jsonl`: append-only, never in a repo; losing it is a major failure. `votes export-order` writes the packs `--order` file.

## LAWS STATE STILL CARRIES
- **★ The degree-6 plane is never labelled** (`partitions.NEVER_LABELLED`).
- **★ Parabolic Julia sets are CLOSED (ckpt 147); Douady–Hubbard tuning is PARKED (ckpt 148); BLA stays removed (ckpt 149).**

## RETENTION
**★ The keep is five per `(place, mode)` plus one family allowance** (→ `curation/README.md`). Pinned rows and every published record's seats are prune-proof via `tentative.kept()`.

## RECORDS: THE PUBLISHED SET
- **★ The store is exactly the twenty-one published records:** the twenty `final139_*` and `final140_general2000`, tracked whole.
- `portable.GENERAL_CHECK` = `final139_general`; `portable.REFERENCE` = `final139_green`. Nothing is re-cut while the pool is closed.
- **★ BACKUPS ARE MATT'S.** `storage export` runs only at his direction and is never proposed.
- **★ `git grep <stamp>` before calling any record stray.** **★ A record carries its prose whole** (`SCHEMA_NOTES`).

## THE REPO AS A CLONE SEES IT
- **★ A fresh box continues every stage from a `storage export` alone** (→ `preserve\fresh_box.md`). A clone now holds all twenty-one records whole.
- **★ Both root READMEs were rewritten for GitHub visitors (ckpt 156):** a map, run commands, how the two repos relate, and the licences. Machine-specific detail moved to the sub-READMEs. Both `CLAUDE.md` files are rules only.
- **★ CUDA is opt-in.** ⚠ This box syncs `--extra cuda`.
- **★ Both repos build and run on Windows, Linux and macOS, and CI proves it.** ⚠ `engine.wasm` embeds absolute paths, so CI reports hashes without asserting them (→ OPEN 13).
- ⚠ Drive the makers through `.venv/Scripts/fractal-wallpapers.exe`. Concurrent prompts in one checkout commit by pathspec, **and stage by hunk when a file holds another prompt's edits** (a pathspec commit takes the whole working-tree file). `gh` is logged in as techmatt.
- ⚠ `perturb.wasm` builds on rustc 1.96.0 (`RUSTUP_TOOLCHAIN=1.96.0`); the box default is 1.98.1.

## WEBSITE
**★ The site is LIVE BUT UNADVERTISED** at `techmatt.github.io/fractals/` (repo `techmatt/fractals`; the local folder stays `C:\Code\fractal-website`). Until Matt advertises it, it never needs preserving or keeping in sync. Matt's homepage links to `/fractals/`. Every fact about the site is owned by the website repo:

| Topic | Owner |
|---|---|
| Explorer: tabs, Deep, the Dive block, Dive results, Random dives, palette modes, the Period slider, the link contract (incl. `curve`), Browse, measured timings, the WASM toolchain pin | `explorer/README.md` |
| Deep kernel, `nuclei::classify`, `dive::`, the twin, closed verdicts | `explorer/perturb-wasm/README.md` |
| Atlas | `atlas/README.md` |
| Builder: figures (bands, band groups, folds), `seats.py`, packs, `votes`, `dive-candidates`, `random-dives`, `tools-and-data`, `tools`, `deep_judges.py`, the rail and the site header (`pages.topbar`), zoom videos, every `builder check` check (29, incl. `bar`) | `builder/README.md` |
| Traps, the rail rule, the header rule, pathspec and hunk staging | `CLAUDE.md` |
| Style and voice | `prose\writing-guidance.md` · website `CLAUDE.md` |
| Per-page status | `docs/page-review.md` |

- **★ NAVIGATION:** the rail's top group is Start here, Wallpaper packs, Tools and data, Deep zoom videos, then Contents. The site header carries the same links, written by `build` and held by `check`'s `bar`. The explorer's studio bar carries no videos link (no room at phone width).
- **★ TOOLS AND DATA** (`tools-and-data/index.html`, master `Tools and data v1.md`):
  - `gallery-locations.jsonl`: 6,299 recipes, CC BY 4.0;
  - `hand-made-palettes.json`: the 495 authored palettes, CC0. Converted and extracted maps are never shipped;
  - the judges link to `weights-2026-09-14`; the hand labels link to wallpapers `data/`.
  - Figures: `tools-atlas`, `tools-palettes`, `tools-judges` (P(=k) examples; palette row = one place in five palettes), `tools-labels` (three bands of rating groups). Maker: `python -m builder tools`; data: `builder tools-and-data`.
- **★ DEEP ZOOM VIDEOS** (`deep-zoom/videos.html`, master `Deep zoom videos v1.md`): double descent, the seahorse video (pending) and `julia3-descent` (pending; Final frame `go/julia3-end`, Midway blank). Linked from Deep zoom, Start here and the rail.
- **★ DEEP ZOOM PAGE (ckpt 156):** "Julia sets inside the Mandelbrot set" moved to Fractal math's Tan Lei section (`math-misiurewicz-pairs`). §Random dives replaced "The deep gallery", with `deep-random-dives` (Matt's 15 picks) and the judges fold (`deep-judges-top15`, collapsed; `[FOLD: …] … [/FOLD]` in a master). The Deep gallery holds 105 frames.
- **★ The palette library page shows explorer names only** and links to the CC0 download.
- **★ THE DIVE BLOCK and RANDOM DIVES** are as ckpt 155 left them (→ `explorer/README.md`). The Deep tab names a carried wallpaper by collection and rank.
- **★ A LINK IS A PICTURE.** **★ The site never tells a reader a view is "not exact."** **★ No figure reuses a picture unless the reuse is intentional** (`reuse_reason`).
- **★ Figures are never changed because they drifted from the records.** **★ Figure recipes are never lost** (`article/figure-recipes.jsonl`).
- **★ The site reads as its final form; the Oxford comma; American spelling; THE VOICE** (`prose\writing-guidance.md` §Voice).

**★ PROSE: MATT REOPENS IT PIECEMEAL, ONE PASSAGE AT A TIME.** This era he placed passages in Deep zoom, Fractal math, Full pipeline (the reward-hacking sentence), Start here, Overview and the packs page, all edited in their masters in place, plus the two new masters. Everything else stays closed. Deep zoom's speed sentence was remeasured and holds (the GPU's "under 3 seconds" is now 2.98 s).

**★ THE EXPLORER'S BAR (Matt):** complexity is a cost; text is for the artist; the left panel changes the view, the right manipulates it; the shallow view and Deep are one tool; Deep auto-renders. **Phones should be as reasonable as possible (Matt, ckpt 156)**: phone-specific refactors are welcome, without going overboard (OPEN 16). Wasm threads are out. ⚠ This box drifts about 30% between identical runs.

**★ ZOOM VIDEOS:** the double-descent 4K60 settings are the baseline (→ `builder/README.md`). Videos are YouTube embeds. Double Descent is UNLISTED at `youtu.be/MgmOF7Q-YIA`; Matt flips it public at deployment. **Every video gets Midway and Final frame links through its own `go/` redirects.** New videos are prototyped on the `preview` variant (960×540) before the 4K render.

## IN FLIGHT ACROSS THIS BOUNDARY
- **`deep_zoom_video_ckpt156` (+ addendum 1; addendum 2 was never used), website, RUNNING.** The seahorse descent is re-rendered at 4K60: glowdon's recipe, 1.25× faster, a 7 s tail hold, caps by the measured rule.
  - Committed so far: the recipe as the `4k60` variant of `deep-zoom-descent.keyframes.json`, and the addendum's doc edits.
  - At the interim report (09-29 21:20) fields k00–k21 of 52 were drawn; fields were expected to finish 09-30 02:00–03:00, then colour and encode (~45 min).
  - Output: `E:\FractalStorage\fractal-website\deep-zoom-4k60\video\deep-zoom-video_ckpt156.mp4` (`artifacts/deep-zoom/4k60` is a junction to it).
  - Its final report closes the go-link check: `go/seahorse-mid` has no written definition of "midway", and this render passes glowdon's midway depth at 29.6 s, not 36.8 s.

## QUEUED IN DRIVE `prompts\`
Nothing.

## OPEN (ordered): Matt raises each
Items 3, 6, 7, 8, 10, 11, 12, 14 and 15 are closed; the numbering is kept.
1. **Mining is CLOSED; he reopens it.** Read `preserve\mining_laws.md`, then the reopen inventory in wallpapers `curation/LEGS.md`.
2. **The history rewrite** (the last piece of "truly finalized"; Matt wants it soon). It is git surgery; who runs it, and how, is his call.
4. **Prose reopens piecemeal (Matt).** Not yet cut: Overview, Escape-time fractals, Rendering fundamentals, Make your own palettes, Finding good wallpapers, Fractal atlases, Deep zoom rendering, Other artistic techniques, Fractal math, and Start here.
5. **Deploy preparation (preparing, not deploying).** Left:
   - collect friends' votes → `ingest` → `votes export-order` → rebuild the packs with `--order` → a new dated release;
   - `deep-zoom-video`: the render in flight, then YouTube, then its id into the pending row (on both Deep zoom and the videos page);
   - `julia3-descent`: its mapping and period (the final frame's `period=1870` suits only the deep end), tried on cheap `preview` renders first. ⚠ Unverified: whether the zoom tools' keyframe record takes a Julia `c`;
   - more deep zoom videos for the videos page, each with Midway and Final frame links;
   - flip the videos public, advertise the site, then post to fractalforums.org and other fractal forums.
9. **Figures:** Start here's other `start-*` placeholders are Matt's to finalize; the pink picks' 2 placeholders fill as his daughter picks.
13. **Small follow-ups (all optional):**
    - `--remap-path-prefix` for a byte-reproducible `engine.wasm` (a rebake);
    - the atlas rebuild for the nine replayable tone dots;
    - a figure panel addressed by seat still builds its link without the cap (`links._panel_links`); unsurveyed;
    - the Period slider's one-decade minimum travel may leave deep frames' left end near a flat colour; Matt looks first;
    - `docs/page-review.md`'s atlas-places paragraph describes a figure that no longer exists.
16. **PHONE SUPPORT (next checkpoint, Matt).** Reasonable, not overboard:
    - every page lays out cleanly at 375 px;
    - the explorer's studio bar wraps or collapses rather than overlapping (it overlaps today);
    - its panels stack under the canvas in portrait;
    - touch pan and pinch only if cheap.
    - **Investigate first: on a phone, panning does not always trigger a re-render at the new location.**

Parked → `preserve\parked.md`.

## STATUS / KNOWN REDS
- `builder check`: 29 checks green at the end of ckpt 156.
- ⚠ A website `builder check` beside a wallpapers merge can throw a transient ledger red; retry.
- ⚠ A report just copied to Drive `reports\` can read back empty for minutes; retry once, then ask Matt to paste it.

## RULINGS THIS ERA
ckpt 156 (2026-09-28/29). Reported prompts:
- wallpapers: `fulls_ss3_ckpt148` (done), `readme_overhaul_wallpapers`, `wallpapers_followups` (packs build, ss3 promotion), `preclose_wallpapers` (`curve`, the re-stamp), `finalize_records`, `final_wallpapers`;
- website: `deep_picks_prose`, `deep_micro`, `readme_overhaul_website`, `packs_import`, `judge_deep` (+ addendum 1), `tools_and_data`, `tools_figures`, `deep_videos_page`, `deep_judges_fold`, `tools_bands`, `deep_fold_micro`, `tools_labels_groups`, `videos_nav`, `preclose_website`, `revert_names`, `final_website`.

Matt's rulings:
- **Truly finalized:** the twenty-one records are committed and published; the history rewrite follows.
- **The tracked-file cap is 2 MiB;** nothing depended on 1 MiB.
- **Gallery locations are published** (CC BY 4.0). **Palettes ship only hand-made, CC0.**
- **The explorer keeps engine names** for modes and families.
- **Deep zoom videos is a page hanging off Deep zoom, in the rail's top group**, not a fifteenth section.
- **The judges-at-depth result lives in a collapsed fold** in Deep zoom §Random dives.
- **Figures don't repeat Matt's 15 picks for comparison;** they star them and point back.
- **Phones: reasonable support, phone-specific refactors welcome, not overboard.**
- **Prose reopens piecemeal** when Matt brings a passage.

## KEEP LIST
**Drive `prompts\`:** keep `deep_zoom_video_ckpt156.md` and `deep_zoom_video_ckpt156_addendum1.md` (in flight). Matt wipes the rest himself.

**Drive `reports\`:** wipe everything. The video's final report arrives in the next era.

**Drive `votes\`: DURABLE, never wiped.**

**Drive `prose\`:** the live masters are:
- `Start here v2.md`, `Deep zoom v4.md`, `Wallpaper packs v1.md`, `Tools and data v1.md`, `Deep zoom videos v1.md`;
- `Overview v2.md`, `Escape-time fractals v1.md`, `Rendering fundamentals v1.md`;
- `Color palettes v7.md`, `Make your own palettes v4.md`, `Rendering modes v5.md`;
- `Training judges v7.md`, `Finding good locations v8.md`, `Finding good wallpapers v3.md`;
- `Gallery curation v2.md`, `Full pipeline v6.md`, `Fractal atlases v2.md`;
- `Other artistic techniques v1.md`, `Fractal math v2.md`;
- `writing-guidance.md`.

**Wallpapers `scratch/`:** KEEP `place_radius_sheet/`, `retired_tentative/`, `preclose_ckpt125/off_list_stamps.txt`, `tuning_test/`, `leg_numbers.py` and `mbc140/`. WIPE everything else (including `fulls_ss3_ckpt148/`).

**Website:**
- `scratch/`: wipe all except `deep_gallery_sheet/` and `deep_minibrot_candidates/` (`judge_deep_ckpt156/` and `deep_picks_ckpt156/` go; the judges' scores are tracked in `builder/data/deep-judges-scores.jsonl`).
- KEEP `artifacts/deep-zoom/` (with its `4k60` junction), `artifacts/double-descent/`, `artifacts/mathjax/`, `artifacts/pool-study/` and `artifacts/dive-reference/`. `artifacts/deep-gallery/`, `artifacts/cap-split/`, `artifacts/dive-candidates/` and `artifacts/random-dives/` are sweepable. `artifacts/votes/` regenerates.
- `temp-pics/` is Matt's (untracked); leave it.

**`E:\`:** KEEP `E:\FractalWallpapers\ss_test_ckpt148\`, `full\` and `packs\`, and `E:\FractalStorage\fractal-website\` (both 4K60 video trees).

**`preserve\`:** `art_techniques_links.md` stays until Matt rules.

**Outside both repos:** `C:\Tools\fraktaler-3\` stays until Matt removes it. The rustc 1.96.0 toolchain stays.

## OWED
Nothing.

## SCRATCH/ARTIFACT FLAGS
- **★ The standing keep roster lives in the repo:** `src/fractal_wallpapers/README.md §The standing keep roster`.
- ⚠ `.leveled/` directories are sweepable. ⚠ CRLF drift is real; check with `git ls-files --eol`.

## PARKED / SETTLED
→ `preserve\INDEX.md`, which lists every file. Never re-list them here.
