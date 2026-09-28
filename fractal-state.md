# fractal-state — checkpoint 154 (2026-09-28: gallery tone gaps closed; the Dive block rebuilt as slots with a generator-matched mixture, true-copy landings and Dive results; friend-vote ingest built; Deep zoom figure round closed; README and duplicate-key link fixes; `fulls_ss3` still in flight)

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
- ⚠ A seat's `mode` in `gallery.jsonl` is ROUTED; render at `recipe["mode"]`.

## TONE CURVES (ckpt 154)
- **★ Every gallery seat's tone curve is recorded.** A `--record all` backfill re-derived the 1,527 missing curves into wallpapers' `artifacts/curation/autolevel_backfill.jsonl` (553 agreed with a shipped ramp, 0 differed). Every one of the 6,299 gallery links carries its curve or is in band. The site's readers prefer a run's recorded stamp over a `rederived` one.
- The full set inherits the candidate's curve from the sidecar (`stamps.for_release`). The 22 fulls drawn with another tone were deleted and redrawn.
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
- **★ FRIEND VOTES ARE INGESTED (ckpt 154):** friends send Saved links; Matt says "ingest NAME <links>" to CC in fractal-website, which runs `builder votes ingest`.
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
- **★ README thumbnail strips:** both root READMEs open with four thumbnails in `examples/`, each linking to its view. **Every README link is the full writer's link, and `builder check`'s `readmes` holds both READMEs to it (ckpt 154).**
- ⚠ `perturb.wasm` builds on rustc 1.96.0 (`RUSTUP_TOOLCHAIN=1.96.0`); the box default is 1.98.1. A committed module once lagged its own source by a prompt; a rebake brings it back in line.

## WEBSITE: THE EXPLORER STUDIO AND THE ARTICLE
**★ The site is LIVE BUT UNADVERTISED** at `techmatt.github.io/fractals/` (repo `techmatt/fractals`; the local folder stays `C:\Code\fractal-website`). Until Matt advertises it, it never needs preserving or keeping in sync. Every fact about the site is owned by the website repo:

| Topic | Owner |
|---|---|
| Explorer: tabs, keys, Deep, **the Dive block and Dive results**, palette modes, New coloring and its aliasing guard, Fit, Find minibrots, screensaver, Walk, Phoenix, the ceilings, `panel=` and `collection=` links, link parsing and reader messages, undo, Browse, measured timings, the WASM toolchain pin | `explorer/README.md` |
| Deep kernel, oracle, calibration, `nuclei::classify`, `dive::`, the twin, closed verdicts | `explorer/perturb-wasm/README.md` |
| Atlas | `atlas/README.md` |
| Builder, figures, `seats.py`, the packs page, **`votes`**, **`dive-candidates`**, **`screenshot`**, `zoom.py`, `builder deep`, `builder descent`, `start.py`, `go/`, every `builder check` check (27, incl. `readmes` and `repeats`), the Deep gallery's method | `builder/README.md` |
| The hunt harness `explorer/bench/hunt/` (u1–u10) | its `lib.mjs` header, `explorer/README.md` |
| Traps: native exe rebuild, perturb rebake, the one video form, pathspec commits, CI, the checks a bare clone skips, the "ingest NAME" rule | `CLAUDE.md` |
| Style and voice | `prose\writing-guidance.md` · website `CLAUDE.md` |
| Per-page status | `docs/page-review.md` |

- **★ THE DIVE BLOCK (ckpt 154, Matt's design):**
  - *Search for minibrots near [A] then [dive into | zoom out to symmetry point | save those minibrots] [B] Go*. Go has no key.
  - A is Here (live by default), Paste or Random. B is None, Here, Paste or Random.
  - Defaults: A Random, B Random, with New coloring on arrival and Keep diving ticked.
  - B = Random draws the candidate generator's mixture: carry 70% (30% of carries are A itself), center 15%, halfway 15%, 60% of those two first descending 1–8 rungs.
  - Results go to the Deep tab's **Gallery | Dive results** switch: newest first, Clear, gone on reload.
  - Keep diving stops only on Stop or on leaving the Deep tab.
  - Only true copies are landed on (`nuclei::classify`).
  - **The reference look** is `artifacts/dive-reference/` (the 3-hour candidate sheet plus the mixture sheet).
- **★ The site never tells a reader a view is "not exact."** Reader-facing link refusals are plain sentences (ckpt 154). Paste and Saved import read only the first link in pasted text.
- **★ Every video we launch gets "Midway" and "Final frame" picture links under its player, through its own `go/` redirects.**
- Every served asset is tracked. Shallow contract **v4**, deep contract **v3**. **★ A LINK IS A PICTURE.**
- **★ No figure reuses a picture unless the reuse is intentional.** The Wallpaper packs page has one blanket exception (Matt).
- **★ Figures are never changed because they drifted from the records.**
- **★ The site reads as its final form; the Oxford comma; American spelling; THE VOICE** (`prose\writing-guidance.md` §Voice). The article describes the design as intended.
- **★ Display formulas are typeset; the judges' reader names; each usable thing is linked once per page.**
- **The article runs to fourteen sections plus Start here and the Wallpaper packs page.**
  - Start here (`Start here v2.md`): `start-video` is the Double Descent embed with Midway and Final frame links. ⚠ `start-here.html` has no `prose.jsonl` row.
  - Wallpaper packs (`Wallpaper packs v1.md`, generated from `builder/packs.py` `PROSE`): the different-size sentence is placed; 11 of the old 15 unlinked tiles gained links, and the 4 left are cap gaps.
  - **§12 Deep zoom (`Deep zoom v4.md`): the figure round is CLOSED.** `deep-multibrots` has five parameter/Julia pairs with the Misiurewicz-contrast caption. `deep-final-colorings` is Leveled, Higher period, Palette switch and Another palette. `deep-dive-block` is a tracked screenshot (`builder screenshot`). **`deep-zoom-video` is a "Video pending" well** with Midway and Final frame links (`go/seahorse-mid`, `go/seahorse-end`); adding its YouTube id swaps in the player.
  - Rendering fundamentals v1 and Rendering modes v5 now state ss3 and real wallpaper times.
  - Gallery curation v2, Full pipeline v6, Finding good locations v8, Training judges v7, Color palettes v7, Fractal math v2.

**★ THE SECTION-CUT TEMPLATE (Matt, ckpt 148). Done:** Gallery curation, Full pipeline, Finding good locations, Training judges, Color palettes, Rendering modes. The process is unchanged: a prose master in `prose\`, a placement prompt with a verify list, a coloured docx for sentence review, and an HTML sheet in `scratch/` for figure review.

**★ Figure recipes are never lost** (`article/figure-recipes.jsonl`, tracked).

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
Items 3, 6, 8, 10, 11 and 14 are closed; the numbering is kept.
1. **Mining is CLOSED; he reopens it.** Read `preserve\mining_laws.md`, then the reopen inventory in wallpapers `curation/LEGS.md`.
2. **"Truly finalized": the commits (Matt raises it).** What waits on it: the twenty-one kept records and their recipes, and the pre-final history rewrite.
4. **The section-by-section review pass** (→ OPEN 12).
5. **Deploy preparation (preparing, not deploying).** Left:
   - collect friends' votes → `ingest` → `votes export-order`;
   - `curate packs build` when `fulls_ss3` ends, then the upload, then `builder packs --import` and a build;
   - `deep-zoom-video`: Matt's colour and ending, render, YouTube, then its id into the pending row;
   - the history rewrite before the final commit;
   - flip the videos public, hook the site up to Matt's personal website, advertise it, then post to fractalforums.org and other fractal forums.
7. **The Deep tab gallery (48 frames, Matt's picks).** He sends links; a one-line prompt appends each row and bakes its thumbnail.
9. **THE WRITEUP (Matt raises it; the session authors a prose master plus a placement prompt).**
   - **Start here:** `start-pink-gallery` awaits his daughter's picks; the other `start-*` placeholders are Matt's to adjust.
   - **"Ready for publishing":** only Deep zoom's speed sentence (remeasure) is left. The download promises become true when the packs ship.
12. **The section-cut pass:** not yet cut are Overview, Escape-time fractals, Rendering fundamentals, Make your own palettes, Finding good wallpapers, Fractal atlases, Deep zoom rendering, Other artistic techniques, Fractal math, and Start here.
13. **Small follow-ups (all optional):**
    - `--remap-path-prefix` for a byte-reproducible `engine.wasm` (a rebake; after `fulls_ss3`);
    - a loading state while a large collection's record arrives;
    - the atlas rebuild for the nine replayable tone dots;
    - `nuclei::classify` is slow at degree 6 and at large periods; perturbation from the nucleus orbit is the untried fix;
    - `perturb-wasm/README.md` §11's twin-mapping numbers may have been measured on the period-15 non-nucleus.
15. **The Deep tab's palette scroll range** (Matt's ckpt 153 goal 1, not yet done).

Parked → `preserve\parked.md`.

## STATUS / KNOWN REDS
- `builder check`: 27 checks green at the end of ckpt 154.
- ⚠ A website `builder check` beside a wallpapers merge can throw a transient ledger red; retry.
- ⚠ A report just copied to Drive `reports\` can read back empty for minutes; retry once, then ask Matt to paste it.

## RULINGS THIS ERA
ckpt 154 (2026-09-26 to 09-28). Reported prompts:
- tone: `gallery_tone_backfill` (and addendum 1);
- explorer: `screensaver_first_frame`, `deep_dive_block`, `keep_diving`, `keep_diving_anchor`, `dive_slots`, `dive_primitive_only`, `dive_mixture`, `dive_defaults` (and addendum 1), `duplicate_key_links`;
- votes: `friend_votes_ingest`;
- Deep zoom: `deep_multibrots_gallery`, `deep_zoom_v4_place`, `deep_multibrots_pairs`, `deep_multibrots_final_rows` (and addendum 1), `publish_prep`;
- READMEs: `readme_links_complete` (superseding `wallpapers_readme_links_fix_ckpt153`);
- housekeeping: `dive_reference_keep`.

Matt's rulings:
- **The Dive block is slots, not buttons.** Random draws always come from `all`, ignoring the Gallery selection. Results are their own Dive results, not a gallery collection. The defaults are Random / Random with New coloring and Keep diving on, and its loop should roughly match the candidate sheet.
- **Only true copies are dive landings.**
- **Keep diving is stopped only by Stop or by leaving the Deep tab.**
- **`deep-multibrots` pairs a multibrot location with a view of the Julia set for its c.** It uses "zoomed in close", not the point itself, and its caption contrasts the pairs with Misiurewicz points.
- **Everything drawn without its tone curve is redrawn.**
- **Small parked edits ride the very next prompt to that repo.**

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
- `scratch/`: wipe all except `deep_gallery_sheet/`.
- KEEP `artifacts/deep-zoom/`, `artifacts/double-descent/`, `artifacts/mathjax/`, `artifacts/pool-study/` and **`artifacts/dive-reference/`**. `artifacts/deep-gallery/`, `artifacts/cap-split/` and `artifacts/dive-candidates/` are sweepable. `artifacts/votes/` regenerates.

**`E:\FractalWallpapers\`:** KEEP `ss_test_ckpt148\` and `full\`.

**`preserve\`:** `art_techniques_links.md` stays until Matt rules. (`minibrot_copies.md` and `deep_zoom_section.md` were deleted at ckpt 154.)

**Outside both repos:** `C:\Tools\fraktaler-3\` stays until Matt removes it. The rustc 1.96.0 toolchain stays.

**Wallpapers records:** the twenty-one kept records are the whole store. **Hot artifacts:** unchanged, plus `autolevel_backfill.jsonl` (now covering every gallery seat).

## OWED
Nothing.

## SCRATCH/ARTIFACT FLAGS
- **★ The standing keep roster lives in the repo:** `src/fractal_wallpapers/README.md §The standing keep roster`.
- ⚠ `.leveled/` directories are sweepable. ⚠ CRLF drift is real; check with `git ls-files --eol`.

## PARKED / SETTLED
→ `preserve\INDEX.md`, which lists every file. Never re-list them here.
