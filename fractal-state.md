# fractal-state — checkpoint 153 (2026-09-26: the pack tool and the Wallpaper packs page; Browse and "General gallery · all" in the explorer; README thumbnail strips in both repos; explorer render seams and four hunt findings fixed; the Dive block decided; `fulls_ss3` still in flight)

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

**★ ⚠ GALLERY SIZE IS MATT'S DECISION ALONE.** Never raise it, queue it, or reason about shrinking `n`. "Final gallery quality" is his judgement, not a median. Re-solving at a larger `n` reshuffles, as expected. `final140_general2000` (n=2000) is offered on the site beside the n=1000 default.

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

## FULL-RESOLUTION WALLPAPERS AND PACKS
- **★ The shipped setting is 2560×1440 at ss3, JPEG q95 with 4:4:4 chroma (Matt, ckpt 148).** Every file carries its explorer link as metadata. The ss3 check passed (ckpt 152).
- **`fulls_ss3_ckpt148` is IN FLIGHT** (§IN FLIGHT): 6,299 pictures into `E:\FractalWallpapers\full\`. The general thousand renders first; the whole run is projected to end Monday (about 105–146 pictures an hour). Mean file is about 2.85 MB.
- **★ THE PACK TOOL IS BUILT (ckpt 153):** `curate packs status|build` (`curation/packs.py`; operation → `curation/README.md §Wallpaper packs`). It reads only the full set and `membership.jsonl`, and uploads nothing.
- **★ THE PACKS (Matt):**
  - n=1000 in three parts (334, 333, 333), in rank order; part 2 opens at `0335`;
  - best 30, 100 and 200, the first K of the same order, so nested in part 1;
  - the twelve colour collections, one zip each.
  - **Not shipped:** n=2000 and the mode collections.
- **Rank order:** a seeded permutation (`packs.SEED = 20260926`) until friends' votes arrive through `--order FILE` (one recipe key per line, exactly the thousand).
- **Inside a zip:**
  - file names `<rank> <palette display name> <fractal type>.jpg`, with palette names from the explorer's `palette-names.json` and fractal names such as Cubic Multibrot or Quartic Julia;
  - store mode;
  - a `README.txt` with the site link and the licence line.
- **★ The wallpapers are licensed CC BY 4.0, credit Matt Fisher (Matt, ckpt 153).** Both repos' code stays MIT.
- **★ Hosting: every pack goes on one GitHub Release on `techmatt/fractals` (Matt, ckpt 153).** This supersedes ckpt 149's Drive split. The per-file limit is 2 GiB (verified), and Matt accepted colour zips of about 1.05–1.26 GB rather than splitting them.
- **After the build:** Matt uploads the zips, then the website's `builder packs --import` and a build fill the sizes onto the packs page.
- **Friend votes (Matt, ckpt 153):** no vote kit. Friends pick favourites on the site (Saved, or Browse's save marks) and send Saved's Copy links. **An ingest is unbuilt:** paste the lists, match each line to a seat by exact link, count likes per seat, and write the `--order` file. Only exact matches count, and the rest are reported.

## LAWS STATE STILL CARRIES
- **★ The degree-6 plane is never labelled** (`partitions.NEVER_LABELLED`).
- **★ Inside a minibrot copy is a named phenomenon** → `preserve\minibrot_copies.md`, a §Deep zoom source with `preserve\deep_zoom_section.md`.
- **★ Parabolic Julia sets are CLOSED (ckpt 147); Douady–Hubbard tuning is PARKED (ckpt 148); BLA stays removed (ckpt 149).**

## RETENTION
**★ The keep is five per `(place, mode)` plus one family allowance** (→ `curation/README.md`). Pinned rows and every kept record's seats are prune-proof via `tentative.kept()`.

## RECORDS: THE SEMI-FINAL SET
- **★ The store is exactly the twenty-one records on `tentative.KEPT_UNPUBLISHED`:** the twenty `final139_*` and `final140_general2000`. Every one carries an untracked `recipes.jsonl`. ★ Tracking a recipe file IS publishing its stamp.
- `portable.GENERAL_CHECK` = `final139_general`; `portable.REFERENCE` = `final139_green`. Nothing is re-cut while the pool is closed.
- **★ BACKUPS ARE MATT'S.** `storage export` runs only at his direction and is never proposed.
- **★ ⚠ A record is discarded by default; preservation derives from the keep list alone.** A record is two directories. `git grep <stamp>` before calling any record stray.
- **★ A record carries its prose whole** (`SCHEMA_NOTES`).

## THE REPO AS A CLONE SEES IT
- **★ A fresh box continues every stage from a `storage export` alone** (→ `preserve\fresh_box.md`).
- **★ CUDA is opt-in.** ⚠ This box syncs `--extra cuda`.
- **★ Both repos build and run on Windows, Linux and macOS, and CI proves it (ckpt 152).** ⚠ `engine.wasm` embeds absolute paths, so CI reports hashes without asserting them (→ OPEN 13).
- **★ The Rust-only renderer `fractal-engine render-link` shipped (ckpt 149).** The website's `stamps` check now also exercises it with the existing binary, building nothing.
- ⚠ Drive the makers through `.venv/Scripts/fractal-wallpapers.exe`. Concurrent prompts in one checkout commit with a pathspec. `gh` is logged in as techmatt.
- **★ README thumbnail strips (ckpt 153):** both repos' root READMEs open with four thumbnails in `examples/`, each linking to its live explorer view. The website's four are Matt's picks.

## WEBSITE: THE EXPLORER STUDIO AND THE ARTICLE
**★ The site is LIVE BUT UNADVERTISED** at `techmatt.github.io/fractals/` (repo `techmatt/fractals`; the local folder stays `C:\Code\fractal-website`). Until Matt advertises it, it never needs preserving or keeping in sync. Every fact about the site is owned by the website repo:

| Topic | Owner |
|---|---|
| Explorer: tabs, keys, Deep, palette modes, Fit, Find minibrots, screensaver, Walk, Phoenix, the ceilings, `panel=` and `collection=` links, undo, **Browse** (`explorer/browse.js`), the render-seam behaviours, measured timings, the WASM toolchain pin | `explorer/README.md` |
| Deep kernel, oracle, calibration, closed verdicts | `explorer/perturb-wasm/README.md` |
| Atlas | `atlas/README.md` |
| Builder, figures, `seats.py` (including the `all` union), the **packs page** (`builder/packs.py`, `wallpaper-packs/packs.jsonl`, `builder packs --import`), `zoom.py`, `builder deep`, `builder descent`, `start.py`, formulas, the pool study, `go/`, every `builder check` check, and **the Deep gallery's method** (`§How the first set was found`) | `builder/README.md` |
| The hunt harness `explorer/bench/hunt/` (u1–u10) | its `lib.mjs` header, `explorer/README.md` |
| Traps: native exe rebuild, perturb rebake, the one video form, pathspec commits, CI, the checks a bare clone skips | `CLAUDE.md` |
| Style and voice | `prose\writing-guidance.md` · website `CLAUDE.md` |
| Per-page status | `docs/page-review.md` |

- **Browse (ckpt 153)** is the Gallery tab at full width:
  - Matt's name for it, with no hotkey;
  - one header row: tabs, collection, Screensaver, and "Back to explorer (Esc)";
  - five chip rows, where fractal family, centered on a minibrot, and spiral exist in Browse only;
  - tiles with save marks;
  - a preview fit within 85% of the layer, backed by a canvas capped at 2560, rendered in the three-stage path, with Save, Open in explorer, ← → and Esc.

  The narrow Gallery panel stays uncluttered (Matt). Copy link copies what is on screen. Browse enters no link.
- **"General gallery · all" (`collection=all`)** is the union of every collection: 6,299 pictures, with its own page order and no new images. A `seats --records-only` re-stage takes about 5.5 minutes.
- **★ The site never tells a reader a view is "not exact" (Matt, ckpt 153).** The view is the view. All such wording is gone; `gap` survives only in Copy view's JSON.
- **★ Every video we launch gets "Midway" and "Final frame" picture links under its player, through its own `go/` redirects (Matt, ckpt 153).**
- **The staging rule is retired (ckpt 152):** every served asset is tracked, about 166 MB.
- Shallow contract **v4**, deep contract **v3**. **★ A LINK IS A PICTURE.**
- **★ No figure reuses a picture unless the reuse is intentional.** The Wallpaper packs page has one blanket exception (Matt).
- **★ Figures are never changed because they drifted from the records (ckpt 152).**
- **★ The site reads as its final form; the Oxford comma; American spelling; THE VOICE** (`prose\writing-guidance.md` §Voice). The article describes the design as intended.
- **★ Display formulas are typeset; the judges' reader names; each usable thing is linked once per page** (ckpt 148–149).
- **The article runs to fourteen sections plus Start here and the Wallpaper packs page.**
  - Start here (`Start here v2.md`): `start-video` is the Double Descent embed with Midway and Final frame links. Its caption is now "A deep zoom into the degree-3 Mandelbrot set, rendered with the same perturbation code as the explorer's Deep tab." ⚠ `start-here.html` has no `prose.jsonl` row (`builder prose` treats it as its own master).
  - **Wallpaper packs (`wallpaper-packs/`, master `Wallpaper packs v1.md`, generated from `builder/packs.py` `PROSE`):**
    - `packs-hero`, one intro paragraph (CC BY 4.0, "found and rendered with the methods this site describes"), then sixteen pack blocks;
    - each block has five tiles and centered download buttons pointing at `releases/latest/download/<file>` (404 until upload);
    - General and the colours also get a dim "View this gallery in the explorer";
    - 15 of the 80 tiles are unlinked because their seat links are inexact.
  - §12 Deep zoom (`Deep zoom v3.md`): `deep-descent-video` is DROPPED (Matt, ckpt 153); `deep-zoom-video` remains a placeholder.
  - Gallery curation v2, Full pipeline v6, Finding good locations v8, Training judges v7, Color palettes v7, Rendering modes v5, Fractal math v2.

**★ THE SECTION-CUT TEMPLATE (Matt, ckpt 148). Done:** Gallery curation, Full pipeline, Finding good locations, Training judges, Color palettes, Rendering modes. The test, what stays, what collapses, what goes, and the process (a prose master in `prose\`, a placement prompt with a verify list, a coloured docx for sentence review, and an HTML sheet in `scratch/` for figure review) are unchanged from ckpt 152.

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
- **`fulls_ss3_ckpt148` (wallpapers), running until about Monday.** Phase 3 renders into `E:\FractalWallpapers\full\`.
  - **To resume after any stop:** paste the same prompt into a fresh session, or say "resume fulls_ss3 phase 3".
  - **To pause:** `fractal-wallpapers curate full-set pause --out E:\FractalWallpapers\full` (or `--now`). `curate full-set status` reads progress.
  - **While it runs, no prompt may:**
    - touch the render path (`colorize`, `release`, `explorer_link`, `embed_link`, `full_set`, `engine/`);
    - run `cargo build --release` in wallpapers;
    - run the wallpapers fast lane.
  - Other wallpapers edits commit with a pathspec.
  - Its final report, and the README promotion of ss3 as the phase-3 default, come at its end.

## QUEUED IN DRIVE `prompts\`
- **`wallpapers_readme_links_fix_ckpt153.md` (wallpapers), unless it already ran.** Check wallpapers `git log` for a commit rewriting the README seat links with `explorer_link`. It fixes the wallpapers README's three seat links, which came from `pins.query_of`: that dropped `mirror`, so `mandelbrot_stripe` opens in the wrong colouring.

## NEXT CHECKPOINT GOAL (Matt, ckpt 153)
1. Revisit the Deep tab's palette scroll range.
2. The deep minibrot figure.
3. Then the Dive block and New coloring build prompt (OPEN 14).

## OPEN (ordered): Matt raises each
Items 3, 6, 8, 10 and 11 are closed; the numbering is kept.
1. **Mining is CLOSED; he reopens it.** Read `preserve\mining_laws.md`, then the reopen inventory in wallpapers `curation/LEGS.md`.
2. **"Truly finalized": the commits (Matt raises it).** What waits on it: the twenty-one kept records and their recipes, and the pre-final history rewrite.
4. **The section-by-section review pass** (→ OPEN 12).
5. **Deploy preparation (preparing, not deploying).** Left:
   - friends' votes, then the vote ingest, then the `--order` file;
   - `curate packs build` when `fulls_ss3` ends, then the upload, then `builder packs --import` and a build;
   - `deep-zoom-video`: Matt's colour and ending, render, YouTube, and the Midway and Final frame links;
   - the history rewrite before the final commit;
   - flip the videos public, advertise the site, then post to fractalforums.org.
7. **The Deep tab gallery (33 frames, Matt's picks).** He sends links; a one-line prompt appends each row and bakes its thumbnail.
9. **THE WRITEUP (Matt raises it; the session authors a prose master plus a placement prompt).**
   - **§Deep zoom:** placed figures as at ckpt 152. `deep-zoom-video` is a placeholder. When the figure round finishes, delete `preserve\minibrot_copies.md` and `preserve\deep_zoom_section.md`.
   - **Start here:** `start-pink-gallery` awaits his daughter's picks; the other `start-*` placeholders are Matt's to adjust.
   - **★ PENDING EDIT, Wallpaper packs:** after the licence sentence, add "If you want a different size, open any picture in the explorer and download it at the resolution you need, or render it yourself with the code in fractal-wallpapers." (Matt: pending). **It rides the next website prompt that touches the page, or the next pre-closeout prompt.**
   - **"Ready for publishing" (waiting on `fulls_ss3` or an idle box):**
     - Rendering fundamentals: s = 4 and sixteen become s = 3 and nine, and `render-supersample` moves to ss3.
     - Rendering modes: 4× becomes 3×; fill the wallpaper-render column from real ss3 times (`progress.jsonl`); recompute the candidate counts and shares.
     - Deep zoom's speed sentence is remeasured.
     - The download promises become true when the packs ship.
12. **The section-cut pass:** not yet cut are Overview, Escape-time fractals, Rendering fundamentals, Make your own palettes, Finding good wallpapers, Fractal atlases, Deep zoom rendering, Other artistic techniques, Fractal math, and Start here.
13. **Small follow-ups:** optional `--remap-path-prefix` for byte-reproducible `engine.wasm` (a rebake; after `fulls_ss3`). Optional: a loading state while a large collection's record arrives. The containment CSS for a fresh `collection=all` load was probed and not taken.
14. **★ THE DIVE BLOCK AND NEW COLORING (decided by Matt at ckpt 153; the first build prompt after goals 1–2).**
    - **The method it formalises** → website `builder/README.md §How the first set was found`:
      - rung descents by `nuclei::search`, largest first, each under an eighth of the last body, up to 12 rungs;
      - copy-mapped points `c = nucleus + C/σ` (σ = `d·l^{1/(D−1)}`, native fixed point) and the embedded Julia frames;
      - the colouring rule;
      - the ceiling trap: a mapped point escapes after about period × its shallow count.
    - **The Dive block:** a section at the top of the Deep tab's left panel with buttons, a status line, one progress bar (search, then render), Cancel covering both, and a small options row. It works on Mandelbrot and Multibrot 3–6 only; elsewhere the buttons are disabled with a reason.
    - **The five buttons.** A is where the minibrot is found and B is the picture found inside it; each is the screen or a random same-plane seat from `all`:
      - Dive: descend into a nearby minibrot, with a "halfway" option for the symmetry stage;
      - A = screen, B = screen;
      - A = screen, B = random;
      - A = random, B = screen;
      - Double random.
      
      Working names are Dive, Echo here, Wallpaper here, Echo elsewhere and Double random; **Matt wants them renamed**, so settle the names in the prompt.
    - **The iteration budget:** B is eligible only if the copy's period × B's count fits the 2M explicit ceiling. Retry a few draws, then say so in the status line. The "this view" buttons are often disabled on deep screens.
    - **Results:** ordinary deep links (v3) with `n` pinned by the cap rule; one undo step per press; the status line states provenance, which enters no link.
    - **Palette:** kept on every jump except Double random, which applies New coloring.
    - **New coloring (Deep and shallow):**
      - draw a palette from the approved-for-random list (the 232);
      - run the λ smoothness test from {0, 0.15, 0.3, 0.5, 0.75, 1};
      - set the period from the field's 3rd–97th-percentile range of g divided by a random cycle count (1.5–6);
      - draw a random phase.
      
      It is an Absolute-mode rule, so in the shallow view it presumably switches to Absolute. Settle that in the prompt.
    - **★ The mirror policy (Matt):** in Deep, choosing a non-cyclic palette turns Mirror on by default.
    - **Build:** σ, the dive policy and the colour rule go into `perturb-wasm` (a perturb rebake, website only; it does not lock wallpapers).

Parked → `preserve\parked.md`.

## STATUS / KNOWN REDS
- `builder check`: 25 checks green at the end of ckpt 153. The hunt units u1–u10 are clean, including the undo-across-Deep fix and two Deep/Walk leave-redraw fixes.
- ⚠ A website `builder check` beside a wallpapers merge can throw a transient ledger red; retry.
- ⚠ A report just copied to Drive `reports\` can read back empty for minutes; retry once, then ask Matt to paste it.

## RULINGS THIS ERA
ckpt 153 (2026-09-26). Reported prompts:
- `readme_examples_ckpt153`, `wallpapers_readme_links_ckpt153`;
- `packs_assemble_ckpt153`, `drop_descent_video_ckpt153`, `packs_page_ckpt153`, `packs_page_edits_ckpt153`;
- `explorer_browse_ckpt153`, `browse_chrome_ckpt153` (and addendum 1), `browse_preview_size_ckpt153`, `browse_header_ckpt153`;
- `gallery_all_ckpt153`, `explorer_render_seams_ckpt153`, `preclose_website_ckpt153`.

- **Packs:** n=1000 in three parts, best 30, 100 and 200, and the twelve colours. No n=2000 and no mode packs. All on one GitHub Release. CC BY 4.0.
- **Friend votes come from the site's Saved lists, not a kit.**
- **Browse, the "all" gallery, one header row, save marks, and bigger previews (Matt).**
- **No "not exact" wording anywhere (Matt).**
- **Every launched video gets Midway and Final frame links (Matt).**
- **The descent video is dropped from Deep zoom (Matt).**
- **The Dive block, New coloring and the mirror policy are decided** (OPEN 14).

## KEEP LIST
**Drive `prompts\`:** keep `fulls_ss3_ckpt148.md` (in flight) and `wallpapers_readme_links_fix_ckpt153.md` (queued, unless it already ran). Matt wipes the rest himself.

**Drive `reports\`:** wipe everything. The final `fulls_ss3_ckpt148` report arrives in the next era.

**Drive `prose\`:** the live masters are:
- `Start here v2.md` and `Deep zoom v3.md` (both edited in place at ckpt 153);
- `Overview v2.md`, `Escape-time fractals v1.md`, `Rendering fundamentals v1.md`;
- `Color palettes v7.md`, `Make your own palettes v4.md`, `Rendering modes v5.md`;
- `Training judges v7.md`, `Finding good locations v8.md`, `Finding good wallpapers v3.md`;
- `Gallery curation v2.md`, `Full pipeline v6.md`, `Fractal atlases v2.md`;
- `Other artistic techniques v1.md`, `Fractal math v2.md`;
- **`Wallpaper packs v1.md` (new)**;
- `writing-guidance.md`.

**Wallpapers `scratch/`:** KEEP `fulls_ss3_ckpt148/`, `place_radius_sheet/`, `retired_tentative/`, `preclose_ckpt125/off_list_stamps.txt`, `tuning_test/`, `leg_numbers.py` and `mbc140/`. WIPE everything else.

**Website:**
- `scratch/`: wipe all except `deep_gallery_sheet/`.
- KEEP `artifacts/deep-zoom/`, `artifacts/double-descent/`, `artifacts/mathjax/` and `artifacts/pool-study/`. `artifacts/deep-gallery/` and `artifacts/cap-split/` are sweepable.

**`E:\FractalWallpapers\`:** KEEP `ss_test_ckpt148\` and `full\`. `packs\` does not exist yet; the trial zips were deleted.

**`preserve\`:** `deep_zoom_section.md` and `minibrot_copies.md` stay until the figure round finishes. `art_techniques_links.md` stays until Matt rules.

**Outside both repos:** `C:\Tools\fraktaler-3\` stays until Matt removes it. The rustc 1.96.0 toolchain stays.

**Wallpapers records:** the twenty-one kept records are the whole store. **Hot artifacts:** unchanged from ckpt 152.

## OWED
Nothing.

## SCRATCH/ARTIFACT FLAGS
- **★ The standing keep roster lives in the repo:** `src/fractal_wallpapers/README.md §The standing keep roster`.
- ⚠ `.leveled/` directories are sweepable. ⚠ CRLF drift is real; check with `git ls-files --eol`.

## PARKED / SETTLED
→ `preserve\INDEX.md`, which lists every file. Never re-list them here.
