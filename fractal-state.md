# fractal-state — checkpoint 155 (2026-09-28: the Period slider moves in cycles across the frame; `nuclei::classify` 5–8× faster at degree 6; Random dives (1,000) shipped; the final prose pass placed and prose CLOSED; the pink picks list; seat links carry `n`; `fulls_ss3` still in flight)

## Where we are
Three phases, each depending strictly on the one before (→ fractal-discovery). Matt iterates from pictures, not counts. Phase 3 is his eye on the final seating, and **every planned collection has a viewer at its official size.**

**★ MINING IS CLOSED (Matt, 2026-09-21) UNTIL HE REOPENS IT.**
- The pool as merged on 2026-09-21 is the population, and the `final139_*` solves (§RECORDS) are the semi-final galleries.
- On a reopen, read `preserve\mining_laws.md` whole, then wallpapers `curation/LEGS.md §Mining is CLOSED (2026-09-21) — reopen inventory`. State carries none of it.
- ⚠ Before 2026-09-26, `headroom.population` never passed spiral scores to the solve, so every `curate headroom` census and `pool_draw` reading taken before then counted spiral places as uncapped. Production solves were never affected. Retake any such census before relying on it.
- Nothing in wallpapers is committed as publishing until Matt says "truly finalized". Nothing is published.

**★ EVERY COLLECTION HAS A TARGET, IN `curation/targets.py`: NINETEEN COLLECTIONS, TWELVE FAMILIES AND SEVEN MODES.**
- Reached by `curate solve run --collection NAME`; `--n` overrides; a collection with no target REFUSES. A change is a one-line edit there.
- ⚠ The general gallery's size is `tentative.RECORDED_SEATS` (1,000), not a `targets.py` entry.
- Matt has said the sizes are essentially final. The website's `builder/seats.py` hand-lists the collections.

**★ ⚠ GALLERY SIZE IS MATT'S DECISION ALONE.** Never raise it, queue it, or reason about shrinking `n`. "Final gallery quality" is his judgement, not a median. `final140_general2000` (n=2000) is offered on the site beside the n=1000 default.

**★ NOTHING IS PUBLISHED.** `tentative.PUBLISHED` is empty. Matt raises publishing himself; never ask, never list it. `curate solve viewers` with no stamp builds every kept record and `viewer/all.html`.

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
- **★ Exponential smoothing reads as "smooth" on the site (Matt, ckpt 152)**; recipes keep `exp_smoothing`.
- **★ Texture weight, rotation and phase are CLOSED; palette replication is PARKED.** `data/palettes/palettes_for_random_choice.csv` (232 maps) is the approved-for-random list.
- **★ The explorer's palette modes are EXPLORER-ONLY** (`scale`, `lambda`, `period`; → `engine/README.md`, `explorer/README.md`).
- **★ THE PERIOD SLIDER MOVES IN CYCLES ACROSS THE FRAME (Matt, ckpt 155)** (→ `explorer/README.md`, `explorer/period-range.js`). `period` stays stored in absolute units. The log range is anchored per frame (navigation, arrival, Fit, dive), never while dragging. Its dense end is on the right, at a tenth of a turn per pixel. Moving Lambda rescales `period` to hold the look. Only the slider clamps; the text box takes any value. Phase is unchanged.
- ⚠ A seat's `mode` in `gallery.jsonl` is ROUTED; render at `recipe["mode"]`.

## TONE CURVES
- **★ Every gallery seat's tone curve is recorded** (`artifacts/curation/autolevel_backfill.jsonl` in wallpapers). Every gallery link carries its curve or is in band. The site's readers prefer a run's recorded stamp over a `rederived` one.
- The full set inherits the candidate's curve from the sidecar (`stamps.for_release`).
- Nine atlas `lost` dots are replayable after a `curate atlas --plane` rebuild (optional; 4 have no curve anywhere).

## FULL-RESOLUTION WALLPAPERS AND PACKS
- **★ The shipped setting is 2560×1440 at ss3, JPEG q95 with 4:4:4 chroma (Matt, ckpt 148)** (`curation/full_set.REGIME`). Every file carries its explorer link as metadata. ⚠ `curation.run.RELEASE_SUPERSAMPLE` still reads 4 and is not what ships; settle it at `fulls_ss3`'s README promotion.
- **`fulls_ss3_ckpt148` is RUNNING** (§IN FLIGHT): 6,299 pictures into `E:\FractalWallpapers\full\`, general thousand first.
- **★ THE PACK TOOL IS BUILT:** `curate packs status|build` (`curation/packs.py`; → `curation/README.md §Wallpaper packs`). It reads only the full set and `membership.jsonl`, and uploads nothing.
- **★ THE PACKS (Matt):** n=1000 in three parts (334, 333, 333), in rank order; best 30, 100 and 200, nested in part 1; the twelve colour collections, one zip each. **Not shipped:** n=2000 and the mode collections.
- **Rank order:** a seeded permutation (`packs.SEED = 20260926`) until votes arrive through `--order FILE`.
- **Inside a zip:** `<rank> <palette display name> <fractal type>.jpg`, store mode, and a `README.txt` with the site link and the licence line.
- **★ The wallpapers are licensed CC BY 4.0, credit Matt Fisher.** Both repos' code stays MIT.
- **★ Hosting: every pack goes on one GitHub Release on `techmatt/fractals`.**
- **After the build:** Matt uploads the zips, then the website's `builder packs --import` and a build fill the sizes onto the packs page.
- **★ FRIEND VOTES:** friends send Saved links; Matt says "ingest NAME <links>" to CC in fractal-website, which runs `builder votes ingest`.
  - The store is `C:\Code\fractal-drive-sync\votes\events.jsonl`: append-only, never in a repo, and losing it is a major failure. It is created on the first real ingest.
  - Matching ignores `level`. `votes export-order` writes the packs `--order` file (all thousand, likes first, ties in seeded order).
  - The local viewer is `artifacts/votes/index.html` under `builder serve`.

## LAWS STATE STILL CARRIES
- **★ The degree-6 plane is never labelled** (`partitions.NEVER_LABELLED`).
- **★ Parabolic Julia sets are CLOSED (ckpt 147); Douady–Hubbard tuning is PARKED (ckpt 148); BLA stays removed (ckpt 149).**

## RETENTION
**★ The keep is five per `(place, mode)` plus one family allowance** (→ `curation/README.md`). Pinned rows and every kept record's seats are prune-proof via `tentative.kept()`.

## RECORDS: THE SEMI-FINAL SET
- **★ The store is exactly the twenty-one records on `tentative.KEPT_UNPUBLISHED`:** the twenty `final139_*` and `final140_general2000`. Every one carries an untracked `recipes.jsonl`. ★ Tracking a recipe file IS publishing its stamp.
- `portable.GENERAL_CHECK` = `final139_general`; `portable.REFERENCE` = `final139_green`. Nothing is re-cut while the pool is closed.
- **★ BACKUPS ARE MATT'S.** `storage export` runs only at his direction and is never proposed.
- **★ ⚠ A record is discarded by default; preservation derives from the keep list alone.** `git grep <stamp>` before calling any record stray.
- **★ A record carries its prose whole** (`SCHEMA_NOTES`).

## THE REPO AS A CLONE SEES IT
- **★ A fresh box continues every stage from a `storage export` alone** (→ `preserve\fresh_box.md`).
- **★ CUDA is opt-in.** ⚠ This box syncs `--extra cuda`.
- **★ Both repos build and run on Windows, Linux and macOS, and CI proves it.** ⚠ `engine.wasm` embeds absolute paths, so CI reports hashes without asserting them (→ OPEN 13).
- **★ `fractal-engine render-link` is the Rust-only renderer.**
- ⚠ Drive the makers through `.venv/Scripts/fractal-wallpapers.exe`. Concurrent prompts in one checkout commit with a pathspec. `gh` is logged in as techmatt.
- **★ README thumbnail strips:** both root READMEs open with four thumbnails in `examples/`, each linking to its view. Every README link is the full writer's link, and `builder check`'s `readmes` holds both READMEs to it.
- ⚠ `perturb.wasm` builds on rustc 1.96.0 (`RUSTUP_TOOLCHAIN=1.96.0`); the box default is 1.98.1. A build on the wrong toolchain once shipped and was caught a prompt later; a rebake brings it back in line.

## WEBSITE: THE EXPLORER STUDIO AND THE ARTICLE
**★ The site is LIVE BUT UNADVERTISED** at `techmatt.github.io/fractals/` (repo `techmatt/fractals`; the local folder stays `C:\Code\fractal-website`). Until Matt advertises it, it never needs preserving or keeping in sync. **Matt's homepage (`techmatt.github.io`, repo `C:\Code\techmatt.github.io`) has a Fractals button to `/fractals/` (ckpt 155);** the fractal site's header links back. A prompt there changes only what it asks and adds no files. Every fact about the site is owned by the website repo:

| Topic | Owner |
|---|---|
| Explorer: tabs, keys, Deep, the Dive block, **Dive results and Random dives**, palette modes, **the Period slider**, New coloring and its aliasing guard, Fit, Find minibrots, screensaver, Walk, Phoenix, the ceilings, `panel=` and `collection=` links, link parsing and reader messages, undo, Browse, measured timings, the WASM toolchain pin | `explorer/README.md` |
| Deep kernel, oracle, calibration, `nuclei::classify` (perturbed root solve, ckpt 155), `dive::`, the twin, closed verdicts | `explorer/perturb-wasm/README.md` |
| Atlas | `atlas/README.md` |
| Builder, figures, `seats.py`, the packs page, `votes`, `dive-candidates`, **the Random dives generator**, `screenshot`, `zoom.py`, `builder deep`, `builder descent`, `start.py` and the pink picks list, `go/`, every `builder check` check (28, incl. `readmes`, `repeats` and `deep`), the Deep gallery's method | `builder/README.md` |
| The hunt harness `explorer/bench/hunt/` (u1–u10) | its `lib.mjs` header, `explorer/README.md` |
| Traps: native exe rebuild, perturb rebake, the one video form, pathspec commits, CI, the checks a bare clone skips, the "ingest NAME" rule, the `link` panel field | `CLAUDE.md` |
| Style and voice | `prose\writing-guidance.md` · website `CLAUDE.md` |
| Per-page status | `docs/page-review.md` |

- **★ THE DIVE BLOCK (Matt's design):**
  - *Search for minibrots near [A] then [dive into | zoom out to symmetry point | save those minibrots] [B] Go*. Go has no key.
  - A is Here (live by default), Paste or Random. B is None, Here, Paste or Random. **A Random slot shows its plane's atlas plate**, unfaded and never recoloured.
  - Defaults: A Random, B Random, with New coloring on arrival and Keep diving ticked.
  - B = Random draws the candidate generator's mixture: carry 70% (30% of carries are A itself), center 15%, halfway 15%, 60% of those two first descending 1–8 rungs.
  - The Deep tab's switch is **Gallery | Dive results | Random dives**. Dive results are newest first, with Clear, and are gone on reload.
  - Keep diving stops only on Stop or on leaving the Deep tab. Only true copies are landed on (`nuclei::classify`).
  - **`artifacts/dive-reference/` is the reference LOOK, not a replay:** compare by eye, never unit by unit.
- **★ RANDOM DIVES (Matt, ckpt 155):** 1,000 pre-computed dives in `explorer/random-dives.jsonl` (links only, no place twice), with Gallery-size tiles tracked beside it. They are shown all at once, lazily loaded, and shuffled on each page load. No full-size renders are stored. `artifacts/random-dives/` is ignored provenance.
- **★ Seat links carry `n` (ckpt 155):** collection link gaps went from 423 to 8. The 8 left are mode-curve gaps that no link can express.
- **★ The site never tells a reader a view is "not exact."** Reader-facing link refusals are plain sentences. Paste and Saved import read only the first link in pasted text.
- **★ Every video we launch gets "Midway" and "Final frame" picture links under its player, through its own `go/` redirects.**
- Every served asset is tracked. Shallow contract **v4**, deep contract **v3**. **★ A LINK IS A PICTURE.**
- **★ No figure reuses a picture unless the reuse is intentional.** The Wallpaper packs page has one blanket exception (Matt).
- **★ Figures are never changed because they drifted from the records.**
- **★ The site reads as its final form; the Oxford comma; American spelling; THE VOICE** (`prose\writing-guidance.md` §Voice). The article describes the design as intended.
- **★ Display formulas are typeset; the judges' reader names; each usable thing is linked once per page.**

**★ PROSE IS CLOSED (Matt, ckpt 155) UNTIL HE REOPENS IT. FIGURES ARE NOT.** The final read-through's 13 items were placed at ckpt 155, into the site and into the masters in place. The download sentences already read as available. The one prose item still open is Deep zoom's speed sentence (→ OPEN 9).
- **The article runs to fourteen sections plus Start here and the Wallpaper packs page.** The contents page (`index.html`, no master) leads with "New here? Start here…". Start here ends with a hand-off to the explorer, the Gallery tab and the packs.
- **★ Start here's pink figure is Matt's daughter's PICKS, not a gallery** (`article/pink-gallery.jsonl`: 10 picks, then 2 placeholders). To add a pick, append a row and run `builder start start-pink-gallery --replace`; it takes the first remaining placeholder's cell. The phrase reads "final darker pink picks", unlinked.
- `deep-zoom-video` is a "Video pending" well with Midway and Final frame links (`go/seahorse-mid`, `go/seahorse-end`); adding its YouTube id swaps in the player. `deep-dive-block` was retaken at ckpt 155.

**★ Figure recipes are never lost** (`article/figure-recipes.jsonl`, tracked; a `kind: "link"` row carries a link verbatim). Landing a figure writes its links before the page, so no heal pass is needed.

**★ THE EXPLORER'S BAR (Matt):**
- Complexity is a cost to the person using a tool; only clear wins are added.
- Text is for the artist, and every keyed button wears its key.
- Left panel changes the view; right panel manipulates it.
- The shallow view and Deep are one tool at two depths.
- Deep auto-renders; entering Deep switches to Absolute and fits.
- It targets the desktop. Wasm threads are out.
- ⚠ This box drifts about 30% between identical runs.

**★ Deep (perturbation) is explorer-only; nothing deep enters the pipeline.** **★ ZOOM VIDEOS:** the double-descent 4K60 settings are the baseline (→ `builder/README.md`). Videos are YouTube embeds, never self-hosted. Double Descent is uploaded UNLISTED at `youtu.be/MgmOF7Q-YIA`; Matt flips it public at deployment.

## IN FLIGHT ACROSS THIS BOUNDARY
- **`fulls_ss3_ckpt148` (wallpapers), RUNNING.** Phase 3 renders into `E:\FractalWallpapers\full\`.
  - **To resume after any stop:** paste the same prompt into a fresh session, or say "resume fulls_ss3 phase 3". A deleted `<key>.jpg` is redrawn on resume.
  - **To pause:** `fractal-wallpapers curate full-set pause --out E:\FractalWallpapers\full` (or `--now`). `curate full-set status` reads progress.
  - **While it runs, no prompt may:** touch the render path (`colorize`, `release`, `explorer_link`, `embed_link`, `full_set`, `engine/`), run `cargo build --release` in wallpapers, or run the wallpapers fast lane. Other wallpapers edits commit with a pathspec.
  - At its end: its final report, and the README promotion of ss3 as the phase-3 default (retiring `RELEASE_SUPERSAMPLE = 4`).

## QUEUED IN DRIVE `prompts\`
Nothing.

## OPEN (ordered): Matt raises each
Items 3, 6, 7, 8, 10, 11, 12, 14 and 15 are closed; the numbering is kept.
1. **Mining is CLOSED; he reopens it.** Read `preserve\mining_laws.md`, then the reopen inventory in wallpapers `curation/LEGS.md`.
2. **"Truly finalized": the commits (Matt raises it).** What waits on it: the twenty-one kept records and their recipes, and the pre-final history rewrite.
4. **Prose is CLOSED until Matt reopens it.** The review pass and the section cuts wait on that. Not yet cut: Overview, Escape-time fractals, Rendering fundamentals, Make your own palettes, Finding good wallpapers, Fractal atlases, Deep zoom rendering, Other artistic techniques, Fractal math, and Start here.
5. **Deploy preparation (preparing, not deploying).** Left:
   - collect friends' votes → `ingest` → `votes export-order`;
   - `curate packs build` when `fulls_ss3` ends, then the upload, then `builder packs --import` and a build;
   - `deep-zoom-video`: Matt's colour and ending, render, YouTube, then its id into the pending row;
   - the history rewrite before the final commit;
   - flip the videos public, advertise the site, then post to fractalforums.org and other fractal forums.
9. **Figures and the one prose sentence (Matt raises each):**
   - Start here's other `start-*` placeholders are Matt's to finalize. The pink picks' 2 placeholders fill as his daughter picks.
   - Deep zoom's speed sentence: remeasure after `fulls_ss3` ends, when the box is quiet.
13. **Small follow-ups (all optional):**
    - `--remap-path-prefix` for a byte-reproducible `engine.wasm` (a rebake; after `fulls_ss3`);
    - the atlas rebuild for the nine replayable tone dots (after `fulls_ss3`);
    - a figure panel addressed by seat still builds its link without the cap (`links._panel_links`); no link moved, and it is unsurveyed;
    - the Period slider's one-decade minimum travel may leave deep frames' left end near a flat colour. Matt looks first; if so, it is one constant.

Parked → `preserve\parked.md`.

## STATUS / KNOWN REDS
- `builder check`: 28 checks green at the end of ckpt 155.
- ⚠ A website `builder check` beside a wallpapers merge can throw a transient ledger red; retry.
- ⚠ A report just copied to Drive `reports\` can read back empty for minutes; retry once, then ask Matt to paste it.

## RULINGS THIS ERA
ckpt 155 (2026-09-28). Reported prompts:
- explorer: `period_slider`, `classify_speed` (and addendum 1), `random_dives` (and addendum 1);
- prose: `final_pass_review`, `final_pass_place`;
- figures: `start_pink_gallery` (and addenda 1–2), `preclose_website`;
- homepage: `homepage_fractals_link`. `start_here_pink_wording` is a micro-task, assumed handled.

Matt's rulings:
- **Period slider:** it moves in cycles across the frame; Lambda rescales `period` to hold the look; only the slider clamps; Phase is unchanged.
- **The Deep tab gallery (the old OPEN 7) is closed;** it was never meant to be comprehensive.
- **Random dives:** 1,000, Gallery-size tiles only, all shown in one grid, shuffled per page load.
- **A Random slot shows the atlas plate,** never the palette.
- **Prose is CLOSED until he reopens it; figures are not.**
- **The homepage links straight to `/fractals/`; `index.html` stays the contents page, led by a Start here line.**
- **Micro-tasks are assumed handled** once delivered; no report is tracked.
- **Start here's pink figure is picks, not a gallery,** and is unlinked.

## KEEP LIST
**Drive `prompts\`:** keep `fulls_ss3_ckpt148.md` (in flight). Matt wipes the rest himself.

**Drive `reports\`:** wipe everything. The final `fulls_ss3_ckpt148` report arrives in the next era.

**Drive `votes\`: DURABLE, never wiped** (friends' picks, append-only).

**Drive `prose\`:** the live masters are:
- `Start here v2.md`, `Deep zoom v4.md`, `Wallpaper packs v1.md`;
- `Overview v2.md`, `Escape-time fractals v1.md`, `Rendering fundamentals v1.md`;
- `Color palettes v7.md`, `Make your own palettes v4.md`, `Rendering modes v5.md`;
- `Training judges v7.md`, `Finding good locations v8.md`, `Finding good wallpapers v3.md`;
- `Gallery curation v2.md`, `Full pipeline v6.md`, `Fractal atlases v2.md`;
- `Other artistic techniques v1.md`, `Fractal math v2.md`;
- `writing-guidance.md`.

**Wallpapers `scratch/`:** KEEP `fulls_ss3_ckpt148/`, `place_radius_sheet/`, `retired_tentative/`, `preclose_ckpt125/off_list_stamps.txt`, `tuning_test/`, `leg_numbers.py` and `mbc140/`. WIPE everything else.

**Website:**
- `scratch/`: wipe all except `deep_gallery_sheet/` and `deep_minibrot_candidates/`.
- KEEP `artifacts/deep-zoom/`, `artifacts/double-descent/`, `artifacts/mathjax/`, `artifacts/pool-study/` and `artifacts/dive-reference/`. `artifacts/deep-gallery/`, `artifacts/cap-split/`, `artifacts/dive-candidates/` and `artifacts/random-dives/` are sweepable. `artifacts/votes/` regenerates.
- `temp-pics/` is Matt's (untracked); leave it.

**`E:\FractalWallpapers\`:** KEEP `ss_test_ckpt148\` and `full\`.

**`preserve\`:** `art_techniques_links.md` stays until Matt rules.

**Outside both repos:** `C:\Tools\fraktaler-3\` stays until Matt removes it. The rustc 1.96.0 toolchain stays.

**Wallpapers records:** the twenty-one kept records are the whole store. **Hot artifacts:** unchanged.

## OWED
Nothing.

## SCRATCH/ARTIFACT FLAGS
- **★ The standing keep roster lives in the repo:** `src/fractal_wallpapers/README.md §The standing keep roster`.
- ⚠ `.leveled/` directories are sweepable. ⚠ CRLF drift is real; check with `git ls-files --eol`.

## PARKED / SETTLED
→ `preserve\INDEX.md`, which lists every file. Never re-list them here.
