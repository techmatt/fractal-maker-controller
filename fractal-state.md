# fractal-state — checkpoint 148 (2026-09-25: repo READMEs and the hosting audit; the ss cost test and the ss3 JPEG decision; CI across three platforms and CUDA made opt-in; the Rust-only renderer audit; the judges renamed for readers; Gallery curation cut to v2)

## Where we are
Three phases, each depending strictly on the one before (→ fractal-discovery). Matt iterates from pictures, not counts. Phase 3 is his eye on the final seating, and **every planned collection has a viewer at its official size.**

**★ MINING IS CLOSED (Matt, 2026-09-21) UNTIL HE REOPENS IT.**
- The pool as merged on 2026-09-21 is the population, and the `final139_*` solves (§RECORDS) are the semi-final galleries.
- On a reopen, read `preserve\mining_laws.md` whole, then wallpapers `curation/LEGS.md §Mining is CLOSED (2026-09-21) — reopen inventory`, which lists the open arms and prices, every line citing `MEASUREMENTS.md`. State carries none of it.
- Nothing is committed until Matt says "truly finalized". Nothing is published.

**★ EVERY COLLECTION HAS A TARGET, AND THE TARGETS LIVE IN `curation/targets.py` — NINETEEN COLLECTIONS: TWELVE FAMILIES, SEVEN MODES.**
- Reached by `curate solve run --collection NAME`; `--n` overrides; a collection with no target REFUSES. A change is a one-line edit there, never a number retyped into a prompt.
- **⚠ The GENERAL gallery's size is NOT a `targets.py` entry.** It is `tentative.RECORDED_SEATS` (1,000).
- There is no per-partition collection: every partition, d=6 included, enters the general gallery.
- Matt has said the sizes are essentially final.
- The website's `builder/seats.py` hand-lists the collections (→ website `builder/README.md`).

**★ ⚠ GALLERY SIZE IS MATT'S DECISION ALONE.**
- Never raise it, never queue it, never reason about shrinking `n`.
- "Final gallery quality" is his judgement, not a median.
- **Re-solving at a larger `n` reshuffles, and that is expected.**
- `final140_general2000` (n=2000) is offered on the site beside the n=1000 default. Its viewer is `artifacts/curation/viewer/general_n2000/index.html`; `viewer/index.html` stays the n=1000 page and `viewer/all.html` lists all 21.

**★ NOTHING IS PUBLISHED.**
- `tentative.PUBLISHED` is empty, so `tentative.latest()` refuses and every unstamped read names a stamp.
- Matt raises publishing himself; never ask, never list it.
- Viewers: `curate solve viewers STAMP…` → `artifacts/curation/viewer/<label>/index.html` and `viewer/all.html`. ⚠ The verb rebuilds `all.html` from only the stamps it is given: pass every kept stamp, or the index silently loses rows (a fix is queued in OPEN 13).

**★ PINNED SEATS.** `data/curation/pins.txt` → `curate pins resolve` → `pins.json`. Ten pins, seated before the seed and prune-proof; `--no-pins` for comparisons (→ `curation/GALLERY.md §Pinned seats`). `pins.query_of` writes gallery links; they are never hand-spelled.

**★ THE SUMMARY METRICS ARE SETTLED AT THIS HORIZON.** The 10,000-hour frame stays as the way to JUDGE a product choice (→ fractal-operating).

**★ THE BAR: `DEFAULT_FINE_BAR = 0.030242` ON THE FINE COLUMN**, under `fine_head = twelve_sheets_drop_high_asymmetric_auc_ge4_more_k3`, a k=3 seed ensemble averaged on the probability scale.
- **⚠ A bar is unreadable without its head.**
- **⚠ 0.50 is NOT the seating bar.** `solve.Q4_BAR = 0.50` is the RENDER judge's constant on `p_ge4`.
- **⚠ There are two quality columns.** `p_ge4` is the render judge's GATE reading. `p_fine` is the fine head's own column, where the bar lives, and it is THE quality reading. Its scale is compressed: read q1 and the fraction above a mark, not the bare median.
- **Reader names (ckpt 148):** on the site the render judge is **the wallpaper judge** and the fine head is **the gallery judge**; with the location and palette judges the site counts four (→ fractal-tutorial).
- ⚠ One seed of the fine head is not the mean. ⚠ `--fine-bar 0` still excludes unread rows. Provenance → `models/gallery_grade/README.md`.
- **★ `p_fine`, `p_coarse` and the bars are all operating well; every task that would alter them is CLOSED (Matt, 2026-09-12).**

**★ THE HUMAN VETO IS SHIPPED** (→ `curation/README.md`). The rejection pass is a labeling mode: Matt marks ONLY `1`s, and an unmarked tile is NOT a label.

**★ A THEMED PASS RELAXES THE BAR INSIDE ITS OWN CELL.** `solve.themed_fine_bar` = the lower of the shipped bar and the `p_fine` of the 4n-th best dominant row, floored at 0.01. Mining moves a family's bar. **⚠ `--themed CELL` names a codebook colour cell, not the family bar; the family pass is `--collection <family>`.**

**★ FAMILY PASSES FLOOR AT `mode_policy.seat_floors(n)`; A MODE PASS FLOORS AT 0.** `--flat-floor` is the door back. ⚠ The floor is NOT monotone. The recurring family holes are `itinerary`, `curvature` and `direct_trap_lines`, and they are supply, not rule.

**★ COLOUR:**
- ⚠ A hue family is NOT the union of its four cells (→ `palettes/README.md`).
- Curation constrains the 48 coloured cells only; the four neutrals of the 52-colour codebook get no ceiling or floor (`ceiling.py` `CELL_SHARE = 1/48`).
- The palette group cap is `0.075·n` themed and `0.025·n` general.
- ⚠ The colour allowance is proportional to `n`.
- K is Matt's; Claude never proposes reopening it.

**★ A GALLERY PAGE IS PRESENTED STRATIFIED** (`curation/page_order.py`).

**★ GUARD RULINGS: loosening only, and nothing was loosened.** The solver is not at its optimum, and Matt says that is not a concern. There is no honest score column over the seated population; Matt's eye is the only independent read. Every other standing fact of the solve → `curation/GALLERY.md`.

**★ `pool_scores.jsonl` IS ONE-SHOT: mine → merge → `gallery-grade score-pool` → solve.**

## MODES, PHASE, PALETTE
- **★ The targeted-gallery modes are seven.** Smooth is special and special-cased. `curvature` is `UNMINED`. A stored `smooth` score does not order a `tia` yield.
- **★ The explorer's render-mode roster is thirteen** (`listedModes()`), and the Walk's roster is that list. `gaussian_int`, `trap_circle`, `smooth_trap_circle` and `direct_trap_ring` are pipeline-only.
- **★ Texture weight is a drawn recipe parameter, [0.2, 0.9], on by default. Closed.**
- **★ Rotation and phase are CLOSED:** one random phase per candidate, `--phase-draw`, OFF by default (→ `curation/LEGS.md`, `preserve\rotation_phase_economics.md`).
- **★ Palette replication is PARKED (Matt, 2026-09-12).** `data/palettes/palettes_for_random_choice.csv` (232 maps) feeds the explorer's Random palette and the Walk's "All palettes".
- **★ The explorer's palette modes are EXPLORER-ONLY (ckpt 143).** `scale` (leveled | absolute), `lambda` and `period` are omitted at default, and the pipeline's key whitelist never emits them. Leveled stays the pipeline's default and the shallow view's (→ `engine/README.md`, `explorer/README.md`).
- ⚠ A seat's `mode` in `gallery.jsonl` is ROUTED; render at `recipe["mode"]` (→ fractal-tutorial). A seat recorded `smooth` whose recipe draws another mode is routing, not a record bug.

## FULL-RESOLUTION WALLPAPERS
- **★ The shipped setting is 2560×1440 at ss3 (a 3×3 grid per pixel), saved as JPEG q95 with 4:4:4 chroma (Matt, ckpt 148).** ss2 was nearly indistinguishable; ss3 costs about 2.2× ss2. WebP is out because Windows 10 does not open it natively. Every file carries its explorer link as metadata.
- **The population is 6,299 distinct recipes** across the 21 kept records. Measured on ten seats: ss4 costs 3.64× ss2, and the production pool buys only about 5% at this size. The ss3 run is projected at about 46 wall hours and roughly 13–14 GB.
- **`fulls_ss3_ckpt148` is QUEUED** (§QUEUED). It is resumable: the same prompt is the resume prompt, Matt may pause it by telling CC, and the whole CC instance may be killed and resumed. It first checks ss3 against the ss4 renders in `E:\FractalWallpapers\ss_test_ckpt148\` and warns (without stopping) if any picture is not closer to ss4 than ss2 was. Output: `E:\FractalWallpapers\full\`, with `membership.jsonl` for pack assembly.
- Until that prompt promotes it, the tree's phase-3 default is still ss4; fractal-tutorial's geometry line follows the code, not this decision.

## LAWS STATE STILL CARRIES
- **★ The degree-6 plane is never labelled** (`partitions.NEVER_LABELLED`).
- **★ Inside a minibrot copy is a named phenomenon** → `preserve\minibrot_copies.md`. It is a §Deep zoom source, with `preserve\deep_zoom_section.md` (OPEN 9).
- **★ Parabolic Julia sets are CLOSED (Matt, ckpt 147):** judged by eye on a sheet. The few that work sit just outside a root, at about ε = 1e-4; the rest fill with interior. They are reachable by hand in the explorer and are not included as a tool or in the pipeline. §13 points to Wikibooks and Chéritat.
- **★ Douady–Hubbard tuning in a Julia set is PARKED (Matt, ckpt 148)** (→ `preserve\parked.md`): the effect is real but the pictures are not artistic enough to earn a §14 figure.

## RETENTION
**★ The keep is five per `(place, mode)` plus one family allowance.** Forward-only and colour-blind (→ `curation/README.md`). Pinned rows and every kept record's seats are prune-proof via `tentative.kept()`.

## RECORDS — THE SEMI-FINAL SET
- **★ The store is exactly the twenty-one records on the keep list (`tentative.KEPT_UNPUBLISHED`):** the twenty `final139_*` (general n=1000 plus the nineteen collections, 9,000 seats) and `final140_general2000` (n=2000, same pool and config apart from `n`).
- **Every kept record carries its `recipes.jsonl`, and all are untracked.** ★ Tracking a recipe file IS publishing its stamp.
- **Check records are kept records:** `portable.GENERAL_CHECK` = `final139_general`, and `portable.REFERENCE` = `final139_green`. Nothing is re-cut while the pool is closed.
- **★ BACKUPS ARE MATT'S.** `storage export` runs only at his direction and is never proposed. He holds the copies off-box and deletes the local instance at once, so nothing expects one on disk. Restore → wallpapers `src/fractal_wallpapers/README.md §Continuing on a fresh box`.
- **★ ⚠ A record is discarded by default; preservation derives from the keep list alone.**
  - ⚠ A record is two directories.
  - `solve.write_record` refuses to overwrite. `record` never renders.
  - `git grep <stamp>` before calling any record stray.
  - `backfill.DEFAULT_RECORD` → `final139_general`.
  - The `final139_*` set is the PRE baseline until something merges.
- **★ A record carries its prose whole, and the source carries one copy** (`SCHEMA_NOTES`).

## THE REPO AS A CLONE SEES IT
- **★ A fresh box continues every stage from a `storage export` alone** (→ `preserve\fresh_box.md`).
- **★ CUDA is opt-in (Matt, ckpt 148): nothing heavy installs unless asked for.** The `models` extra is CPU torch on every platform; the conflicting `cuda` extra is cu124 on Windows and Linux x86_64 (→ wallpapers README §Install). ⚠ **This box syncs `--extra cuda`**; a plain `uv sync --extra models` here would swap its torch to CPU.
- **★ People should be able to run both repos on Windows, Linux and macOS (Matt, ckpt 148).** Wallpapers CI now runs one job on `ubuntu-latest`, `macos-latest` (arm64) and `windows-latest`; its first run comes on Matt's next git step. ⚠ The watch item is the exact-pixel digest checks on arm64 macOS: a red there is the first real platform difference, and the choice is per-platform digests or a tolerance, never a skip. Intel Macs get no `models` extra. The website's CI matrix waits on the video (OPEN 13).
- ⚠ `p_fine` rows are stamped with a weights sha, and a clone's rows differ by design.
- ⚠ Drive the makers through `.venv/Scripts/fractal-wallpapers.exe`.

## THE RUST-ONLY RENDERER (IN FLIGHT)
- **Goal (Matt):** Python is optional for anyone who only wants to render. `render_link_ckpt148` adds `fractal-engine render-link --link … --size WxH [--ss N] [--out FILE] [--data DIR]`, which finds `data/` in the checkout and replays the link's `level=` curve. Exact pixel parity with the pipeline is NOT a goal; a small tolerance is.
- Deep links are parsed and routed to a stub backend. For a later prompt, exact parity for a fresh-opened deep link needs three things: porting the arrival fit (or the link always carrying `scale`), a fresh reference orbit, and pinning `libm` in both builds.
- ⚠ **The levelling code now has two copies:** the engine's new `autolevel.rs` and the website's `explorer/engine-wasm/src/level.rs`, each naming the other. Switching engine-wasm to import the engine's copy is OPEN 13.
- The audit behind the design: wallpapers `scratch/cpu_default_and_rust_audit_ckpt148_findings.md` (KEEP until the follow-ups land).

## WEBSITE — THE EXPLORER STUDIO AND THE ARTICLE
**Nothing is live; the site never needs preserving or keeping in sync.** Every fact about the site is owned by the website repo, and state keeps no copy:

| Topic | Owner |
|---|---|
| Explorer: tabs, keys, Deep/Cancel/undo/recolour, Deep auto-render and its switch, palette modes, Fit (f) and the arrival refit, Hold look, the fade table, Find minibrots, zoom-out stop, screensaver, Walk, Phoenix, the two iteration ceilings, `panel=` and `collection=` links, measured timings | `explorer/README.md` |
| Deep kernel, oracle, calibration, closed verdicts (BLA included) | `explorer/perturb-wasm/README.md` |
| Atlas, and the live `atlas-live` figure with its miniatures | `atlas/README.md` |
| Builder, figures, the split rule, `seats.py`, the staged set, site size, the zoom-video tooling (`zoom.py`), the deep-figure maker (`builder deep`), automatic minibrot descents (`builder descent`), the `start-*` maker (`builder/start.py`), every `builder check` check, the site's icon | `builder/README.md` |
| Explorer links embedded in downloaded and released files | `stamp.js` · wallpapers `explorer_link`; the `stamps` check |
| The Deep tab's gallery: its register (`explorer/deep-gallery.jsonl`), maker (`builder/deep_gallery.py`) and method | `builder/README.md §How the first set was found` |
| Traps: native exe rebuild, perturb rebake, repo links, the no-`<video>` rule, the one script kind an article page may carry, the rail | `CLAUDE.md` |
| Style: no italics, no em-dashes, the Oxford comma, vocabulary | `prose\writing-guidance.md` · website `CLAUDE.md` |
| Per-page status | `docs/page-review.md` |

- **★ STAGING RULE (Matt):** no gallery-sized or library-sized commits until he says deploy.
- **Hosting:** the site already deploys to GitHub Pages at `techmatt.github.io/fractal-website` (`pages.yml`), about 156 MiB, every asset by relative path. Pages is its CDN; nothing else is needed for the site. The one open hosting decision is the wallpaper packs (OPEN 5).
- Shallow contract **v4** (an optional `n`, omitted at the width rule; ckpt 145); deep contract **v3**. `n` runs 50 to 2e6 in both.
- **★ No figure reuses a picture shown elsewhere on the site unless the reuse is intentional (Matt).** An intentional reuse carries a `reuse_reason` that names the figure it repeats.
- **★ The site reads as its final form (Matt, ckpt 147):** no "under construction" wording. Matt's own "yet"s are his to keep.
- **★ The Oxford comma everywhere (Matt, ckpt 148).**
- **★ The judges' reader names (Matt, ckpt 148):** the location judge, the wallpaper judge, the palette judge, and the gallery judge. "Render judge" no longer appears in reader-facing prose; code keeps its names.
- **★ Links (ckpt 148):** each thing a reader can go and use is linked once per page, at its first natural mention. `?panel=<tab>` opens a tab and `?panel=gallery&collection=<name>` opens one collection.
- **The article runs to fourteen sections plus Start here.**
  - Start here (`start-here.html`, master `Start here v2.md`) has h1 "Start here" and four h2 parts: Fractal wallpapers, Fractal explorer, Deep zoom rendering, Future work. The rail shows a START HERE group above CONTENTS.
  - §9 Gallery curation is v2 (`article/gallery-curation.html`, master `Gallery curation v2.md`), cut by the template below. Its figures are `gallery-top-scored` (the gallery judge's strict top 24), `gallery-twins` and `gallery-output`.
  - §12 is "Deep zoom rendering" (`article/deep-zoom.html`, master `Deep zoom v3.md`).
  - §14 is "Fractal math" (`article/fractal-math.html`, master `Fractal math v2.md`).
  - The front page carries hand-written intro and Contents blurbs, with no master and no ✓ marks.
  - `escape-families` has 18 panels: five planes (degree 2 to 6), each with two of Matt's Julia picks, then Phoenix.
- **★ The download page is "Wallpaper packs" (`wallpaper-packs/`),** distinct from the explorer's Gallery tab. The Gallery tab's staged images stay under `assets/images/galleries/`; where the packs' own images live is decided when packs exist.

**★ THE SECTION-CUT TEMPLATE (Matt, ckpt 148): Gallery curation v1 → v2. Apply it to Full pipeline next, then to other sections.**
- **The test for every passage:** would a reasonably intelligent CS undergrad think of this unprompted? If so, it collapses to a sentence or goes.
- **What stays:**
  - the non-obvious insight that motivates the section, shown with a figure. For Gallery curation: the judge's strict top 24 come out in clumps (one favourite palette on six of them, repeated places, near-twins) and score within 0.02 of each other, so past a point the rules choose the gallery, not the score;
  - Matt's own judgement calls, such as protecting the worst picture before the average;
  - facts invisible from outside, such as "same place" not showing in the coordinates, and twins being about colour rather than shape;
  - honest notes on what was considered and turned out unnecessary, such as family and plane balance, which Matt would have enforced but the solve produced on its own.
- **What collapses:** each rule becomes one bullet with its number in it, and the algorithm becomes two sentences plus links to the code files.
- **What goes:** mechanism detail (how a distance is computed, tier arithmetic, rounding, the swap loop); plumbing another section covers (rendering, autolevel); and figures that illustrate a mechanism rather than a result (the allowance chart, the release crop).
- **Shape:** the problem with its figure, then the fix in one paragraph, then the rules as a list, then the one judgement worth dwelling on, then the algorithm in brief, then the result figure, then a link onward.
- **Outcome:** about a third of the length, with three figures instead of five.
- **Process:** CC builds the review docx (as `review\gallery-curation.docx`); Matt marks it up and it is discussed; Claude writes the master (presented for Matt to place in `prose\`) and a placement prompt with a verify list at its foot.

**★ THE SITE IS RE-BASED ON `final139_*` + `final140_general2000` — DATA ONLY. Prose and captions wait for "ready for publishing".** ⚠ The `pipeline-growth` chart predates the gallery judge: it plots an older fitted rank, its alt says so, and its numbers change when it is re-baked for publishing.

**★ Figure recipes are never lost.** `article/figure-recipes.jsonl` is site-owned and tracked; a `spec` panel's recipe is its registry row. A panel whose run kept no tone curve may carry a re-measured one in an optional `tone` field (one row does: `4438b8c4`). ★ Every composite figure that can be split is split (Matt).

**★ THE EXPLORER'S BAR (Matt):**
- Complexity is a cost to the person using a tool; only clear wins are added (→ `preserve\rulings_website.md §2026-09-20`).
- Its text is for the artist, and every keyed button wears its key. "Render mode" is the term everywhere.
- Left panel changes the view; right panel manipulates this view.
- **The shallow view and the Deep tab are one tool at two depths (Matt, ckpt 144):** the same control grid, the same button in the same place wherever both have it, one Save, one Root (r), and Find minibrots in both. Details → `explorer/README.md`.
- **The Deep tab renders by itself, on by default and expected to stay on (Matt, ckpt 146),** with one per-viewer off switch that never enters a link.
- **★ Entering Deep switches to Absolute and fits (Matt, ckpt 147),** unless already Absolute or the link states `scale`. Leaving Deep keeps the scale. Fit (f) targets `PASSES = 7` (`explorer/fit.js`), which is Matt's to tune.
- It targets the desktop.
- Explorer-only fast paths are allowed only where the pixel difference from the pipeline is easy to bound. Wasm threads are out.
- ⚠ This box drifts ~30% between identical runs; alternate before/after.

**★ Deep (perturbation) is explorer-only; nothing deep enters the pipeline (Matt)** (→ fractal-engine §Deep render). The Inflection tab is paged out (`explorer/paged-inflection/`); §13 mentions it. **★ The Walk is a short demonstration of how the galleries were made.** Parked → `preserve\parked.md`.

## IN FLIGHT ACROSS THIS BOUNDARY
Matt left both running across the closeout; each reports at the start of the next checkpoint.
- **`double_descent_4k_ckpt148` (website, about 24 hours):** re-renders the favicon descent `double-descent_power_L0.38_a0.15_along-the-starry-way-25` at 3840×2160 60 fps, 1.27× faster along the same path, with a monotone, generous per-keyframe iteration cap checked by measured cap-hit fractions. It reports what supersampling the k26–k28 aliasing stretch would cost; that choice is Matt's. It commits its movie tooling by explicit path; output stays untracked under `artifacts/double-descent/`.
- **`render_link_ckpt148` (wallpapers):** the Rust-only renderer (§THE RUST-ONLY RENDERER), three phases, each committing. It proves no existing render moves (identity edges and timed anchors).

## QUEUED IN DRIVE `prompts\`
- **`fulls_ss3_ckpt148` (wallpapers):** launch only after both in-flight prompts have finished, so it runs on the settled engine and has the box to itself. Reboot the box first if its uptime is past a week.

## NEXT CHECKPOINT GOAL
Matt raises it at the top of the checkpoint. He has named the next writeup target: the section-cut template applied to Full pipeline.

## OPEN (ordered) — Matt raises each
Items 3, 6, 8, 10 and 11 are closed; the numbering is kept.
1. **Mining is CLOSED; he reopens it.** Read `preserve\mining_laws.md`, then the reopen inventory in wallpapers `curation/LEGS.md`. The `final139_*` set is the PRE baseline, and `gallery-grade score-pool` runs before any solve.
2. **"Truly finalized": the commits (Matt raises it).** What waits on it: the twenty-one kept records and their recipes (tracking = publishing), the staged website assets, and the pre-final history rewrite.
4. **Website: the section-by-section review pass** (Matt brings a section's review doc). Next: Full pipeline, by the section-cut template.
5. **Deploy preparation (preparing, not deploying).**
   - Done: the favicon (F08); explorer links embedded in every download and release render; the two repo READMEs open with a short paragraph and a link block funnelling each visitor (packs, explorer, article, the right repo).
   - **Left:**
     - **the wallpaper packs' host.** The site itself needs nothing beyond Pages. Options on record: GitHub Releases (2 GiB per file; JPEG packs fit per collection except general-2000, which would split), Matt's Google Drive (free, but a burst of traffic can lock a popular file for 24 hours), or Cloudflare R2 (no egress fees). The packs are built from `fulls_ss3`'s output and `membership.jsonl`;
     - a history rewrite before the final commit;
     - **cross-platform support is part of deployment:** both repos build and run on Linux and macOS as well as Windows, proven by a CI OS matrix (wallpapers done, first run pending; website waits);
     - the zoom videos' YouTube uploads and 4K masters (the double-descent 4K60 master is in flight), then final deployment. **★ A final video render raises the iteration cap on intermediate keyframes: Matt sees jumps where a keyframe's cap was too low.**
   - **After deployment:** post the site to fractalforums.org.
7. **The Deep tab's follow-ups.**
   - **The gallery (31 frames, Matt's picks).** Matt adds frames over time, including frames centred away from any minibrot. He sends links, and a one-line prompt appends each row and bakes its thumbnail (→ `builder/README.md`). Two Filigree tiles were re-baked at ckpt 148 once the frame width stopped being rounded.
9. **THE WRITEUP (Matt raises it; the session authors a prose master plus a placement prompt).**
   - **§Deep zoom rendering (`article/deep-zoom.html`, master `prose\Deep zoom v3.md`).**
     - **Placed figures:** `deep-f64-and-perturbation`; `deep-shallow-and-deep` (its two panels do NOT share a colouring, on purpose); `deep-descent-rungs` (Chalcedony, absolute, λ 0, period 0.5); `deep-descent-pairs` (seats `afdb47c0`, `9c6a3d87`, glowdon); `deep-misiurewicz-pairs`: three rows (a shallow degree-2 point, then tuned degree-3 and degree-4 points deep) by three columns (whole Julia set, Julia at c, parameter plane at c). Its per-row palettes are placeholders for Matt.
     - **Placeholders:** `deep-zoom-video` (first cut exists, paused on Matt's colour and ending; on the page a poster WebP linking out, never a `<video>` embed); `deep-final-colorings` (Matt's picks in the Deep tab); `deep-descent-video`; `deep-multibrots` (Matt writes the multibrots section).
     - **The double-descent movie** (the favicon seat, `smooth`, ending on M₂ at period 32,761, at its full 32 periods). Matt's baseline is `double-descent_power_L0.38_a0.15_along-the-starry-way-25`; its 4K60 re-render is in flight. Supersampled fields for the k26–k28 grain are Matt's call.
     - **When the figure round finishes,** delete `preserve\minibrot_copies.md` and `preserve\deep_zoom_section.md`.
   - **Start here:** `start-video` waits on Matt's new video. `start-pink-gallery` (six magenta, six rose) is a placeholder for his daughter's final picks. `start-modes` is two Mandelbrot rows Matt picked (ckpt 147). The other `start-*` figures are placeholders Matt adjusts. The "darker pink gallery" link opens `magenta`; `rose` is the other honest choice (Matt's call).
   - **Rendering modes (§4), after `fulls_ss3` reports:** finalize the mode table. The wallpaper-render column is a placeholder scaled from candidate time; fill it from real ss3 times (`E:\FractalWallpapers\full\progress.jsonl`), change the text's "supersampled 4×" to 3×, and drop the caption's "placeholder… pending a measurement". Also reword the sentence after the new lower-base-quality sentence: "That is the reason to try several modes…" now reads as pointing at the longer search.
12. **The section-cut pass** (§THE SECTION-CUT TEMPLATE): Full pipeline next, then other sections Matt names.
13. **Small follow-ups, each a short prompt:**
    - **Website, after the video finishes:** engine-wasm imports the engine's levelling code and deletes its own copy; the website CI and OS matrix; `article/prose.jsonl` gains the missing Start here row (the page currently reads as its own master).
    - **Wallpapers, after `render_link` commits:** `curate solve viewers` defaults to every kept record when no stamp is named.

Parked → `preserve\parked.md`.

## STATUS / KNOWN REDS
- ⚠ A website `builder check` beside a wallpapers merge can throw a transient "not in the candidate ledger" red; retry.
- ⚠ A report just copied to Drive `reports\` can read back EMPTY for minutes; re-read once, then ask Matt to paste it.
- `builder check` was all green at the end of ckpt 148.
- Reboot the box before `fulls_ss3` or the next overnight (per fractal-operating).

## RULINGS THIS ERA
ckpt 148 (2026-09-25). Reported prompts: `readme_funnel_wallpapers`, `readme_funnel_website`, `ss_cost_test` (with addendum1), `ci_crossplatform_wallpapers`, `tuning_julia_sheet`, `tuning_elephant_sheet`, `cpu_default_and_rust_audit`, `prose_micro_edits`, `wallpaper_judge`, `missing_links`, `gallery_judge`, `viewer_general2000`, `gallery_top24`, `escape_families`, `place_gallery_curation_v2`, `preclose_website` (all `_ckpt148`).

- **Full resolution (Matt):** ss3, JPEG q95 4:4:4; WebP ruled out for Windows 10 (→ §FULL-RESOLUTION WALLPAPERS).
- **Hosting:** Pages already serves the site; the CDN item is struck; the packs' host is the open question.
- **Platforms (Matt):** CUDA opt-in; three-platform CI; a Python-free renderer is the goal for render-only users, with exact pixel parity not required.
- **Cloud compute:** priced (tens of dollars for a 30-hour render) and not planned.
- **Article (Matt):** the Oxford comma; the wallpaper and gallery judges; nine front-page micro-edits; one link per target per page; `collection=` links; the families figure re-picked with degree 6 added (and a live mislabelling of its Phoenix row fixed); Gallery curation v2 by the section-cut template, opening on the strict top 24.
- **Parked (Matt):** tuning in a Julia set.
- **Closed:** the twins test red was a wrong test and is fixed.

## KEEP LIST
**Drive `prompts\`:** keep `double_descent_4k_ckpt148.md`, `render_link_ckpt148.md` and `fulls_ss3_ckpt148.md`; wipe everything else.

**Drive `reports\`:** wipe everything.

**Drive `prose\`:** unchanged by the closeout. The live masters include `Deep zoom v3.md`, `Fractal atlases v2.md`, `Start here v2.md`, `Other artistic techniques v1.md`, `Fractal math v2.md`, `Gallery curation v2.md`, `Escape-time fractals v1.md`, `Overview v2.md`, `Rendering modes v4.md` and `Full pipeline v3.md`.

The review docs' canonical copies are website `review\deep-zoom.docx` and `review\gallery-curation.docx`.

**Wallpapers `scratch/`:**
- KEEP `place_radius_sheet/`, `retired_tentative/`, `preclose_ckpt125/off_list_stamps.txt`, `tuning_test/`, `leg_numbers.py`, `mbc140/` (§Deep zoom's picking sheets) and `cpu_default_and_rust_audit_ckpt148_findings.md` (read by `render_link` and its follow-ups).
- WIPE everything else, including `ss_test_ckpt148/`.

**Website:**
- `scratch/`: wipe all except `deep_gallery_sheet/` (the 65-tile sheets, for further picks). This includes `tuning_julia_sheet/`, `tuning_elephant_sheet/` and `gallery_top24/`. The untracked staged set is NOT cleaned; it also holds `explorer/deep-gallery/` (31 thumbnails) and the atlas slot pictures.
- **KEEP `artifacts/deep-zoom/`** (fields, coloured keyframes, MP4s) and **`artifacts/double-descent/`** (the movie's fields, stills and cuts, the in-flight 4K60 render among them). Both are untracked.
- `artifacts/deep-gallery/` and `artifacts/cap-split/` are sweepable.

**`E:\FractalWallpapers\`:** KEEP `ss_test_ckpt148\` (the ss4 references `fulls_ss3`'s check compares against). `full\` is `fulls_ss3`'s output.

**`preserve\`:** `deep_zoom_section.md` and `minibrot_copies.md` stay until the figure round finishes. `art_techniques_links.md` stays until Matt rules.

**Outside both repos:** `C:\Tools\fraktaler-3\` stays until Matt removes it.

**Wallpapers records:** the twenty-one kept records are the whole store, and their `recipes.jsonl` stay.

**Hot artifacts:**
- Stay: `artifacts/discovery/minibrot_examples.jsonl`, `artifacts/tuned129x_*`, the d=6 harvest and depth directories, and every 2026-09-18/19/21 leg's directories.
- Sweepable when Matt sweeps: the parabolic pilot's legs, superseded `gallery_grade_head/pool_scores_*`, `curation_backup/`, `tiles/` manifests and `render_dose/*.pt`.

## OWED
Nothing beyond the two in-flight reports.

## SCRATCH/ARTIFACT FLAGS
- **★ The standing keep roster lives in the repo:** `src/fractal_wallpapers/README.md §The standing keep roster`.
- ⚠ `.leveled/` directories are sweepable (→ `preserve\leveled_identity.md`).
- `artifacts/atlas/<plane>/thumbs/` stays while the atlas may be re-ingested.
- ⚠ CRLF drift is real; check with `git ls-files --eol`.
- ARCHIVED (restore before reuse): unchanged from ckpt 106.

## PARKED / SETTLED
→ `preserve\INDEX.md`, which lists every file. Never re-list them here.
