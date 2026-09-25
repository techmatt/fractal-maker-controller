# fractal-state — checkpoint 149 (2026-09-25: Full pipeline cut to v5 and the Voice standard; a voice pass over every page; display math typeset from LaTeX; the Rust-only renderer shipped; the packs' host decided; two Deep gallery frames)

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
- Viewers: `curate solve viewers STAMP…` → `artifacts/curation/viewer/<label>/index.html` and `viewer/all.html`. ⚠ The verb rebuilds `all.html` from only the stamps it is given: pass every kept stamp, or the index silently loses rows (a fix is in OPEN 13, runnable now).

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
- **★ Pack hosting (Matt, ckpt 149):** GitHub Releases for the smaller packs; Matt's Google Drive for general-2000 and anything else too large. Most people will take the best 100–200.

## LAWS STATE STILL CARRIES
- **★ The degree-6 plane is never labelled** (`partitions.NEVER_LABELLED`).
- **★ Inside a minibrot copy is a named phenomenon** → `preserve\minibrot_copies.md`. It is a §Deep zoom source, with `preserve\deep_zoom_section.md` (OPEN 9).
- **★ Parabolic Julia sets are CLOSED (Matt, ckpt 147):** judged by eye on a sheet. The few that work sit just outside a root, at about ε = 1e-4; the rest fill with interior. They are reachable by hand in the explorer and are not included as a tool or in the pipeline. §13 points to Wikibooks and Chéritat.
- **★ Douady–Hubbard tuning in a Julia set is PARKED (Matt, ckpt 148)** (→ `preserve\parked.md`): the effect is real but the pictures are not artistic enough to earn a §14 figure.
- **★ BLA stays removed (ruling reaffirmed ckpt 149):** it ranged from about 20% slower to about 2.6× faster on frames with structure, and it moved escape counts at every tolerance tried. The site says so (Deep zoom); never re-argue it from the speedup alone.

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
- **★ People should be able to run both repos on Windows, Linux and macOS (Matt, ckpt 148).** Wallpapers CI runs one job on `ubuntu-latest`, `macos-latest` (arm64) and `windows-latest`; its first run comes on Matt's next git step. ⚠ The watch item is the exact-pixel digest checks on arm64 macOS: a red there is the first real platform difference, and the choice is per-platform digests or a tolerance, never a skip. Intel Macs get no `models` extra. The website's CI matrix waits on the video (OPEN 13).
- **★ The Rust-only renderer SHIPPED (ckpt 149):** `fractal-engine render-link` (→ fractal-engine). A render-only user needs no Python.
- ⚠ `p_fine` rows are stamped with a weights sha, and a clone's rows differ by design.
- ⚠ Drive the makers through `.venv/Scripts/fractal-wallpapers.exe`.

## WEBSITE — THE EXPLORER STUDIO AND THE ARTICLE
**Nothing is live; the site never needs preserving or keeping in sync.** Every fact about the site is owned by the website repo, and state keeps no copy:

| Topic | Owner |
|---|---|
| Explorer: tabs, keys, Deep/Cancel/undo/recolour, Deep auto-render and its switch, palette modes, Fit (f) and the arrival refit, Hold look, the fade table, Find minibrots, zoom-out stop, screensaver, Walk, Phoenix, the two iteration ceilings, `panel=` and `collection=` links, measured timings | `explorer/README.md` |
| Deep kernel, oracle, calibration, closed verdicts (BLA included) | `explorer/perturb-wasm/README.md` |
| Atlas, and the live `atlas-live` figure with its miniatures | `atlas/README.md` |
| Builder, figures, the split rule, `seats.py`, the staged set, site size, the zoom-video tooling (`zoom.py`), the deep-figure maker (`builder deep`), automatic minibrot descents (`builder descent`), the `start-*` maker (`builder/start.py`), display formulas (`builder formulas`), every `builder check` check, the site's icon | `builder/README.md` |
| Explorer links embedded in downloaded and released files | `stamp.js` · wallpapers `explorer_link`; the `stamps` check |
| The Deep tab's gallery: its register (`explorer/deep-gallery.jsonl`), maker (`builder/deep_gallery.py`) and method | `builder/README.md §How the first set was found` |
| Traps: native exe rebuild, perturb rebake, repo links, the no-`<video>` rule, the one script kind an article page may carry, the rail | `CLAUDE.md` |
| Style and voice: no italics, no em-dashes, the Oxford comma, vocabulary, §Voice | `prose\writing-guidance.md` · website `CLAUDE.md` |
| Per-page status | `docs/page-review.md` |

- **★ STAGING RULE (Matt):** no gallery-sized or library-sized commits until he says deploy.
- **Hosting:** the site deploys to GitHub Pages at `techmatt.github.io/fractal-website` (`pages.yml`), about 156 MiB, every asset by relative path. Pages is its CDN. The packs' host is decided (§FULL-RESOLUTION WALLPAPERS).
- Shallow contract **v4** (an optional `n`, omitted at the width rule; ckpt 145); deep contract **v3**. `n` runs 50 to 2e6 in both.
- **★ No figure reuses a picture shown elsewhere on the site unless the reuse is intentional (Matt).** An intentional reuse carries a `reuse_reason` that names the figure it repeats.
- **★ The site reads as its final form (Matt, ckpt 147):** no "under construction" wording. Matt's own "yet"s are his to keep.
- **★ The Oxford comma everywhere (Matt, ckpt 148).**
- **★ THE VOICE (Matt, ckpt 149; `prose\writing-guidance.md` §Voice):** first person, plain, conversational; what Matt did and why. No spec or essay register, no punchlines, no coined rules. **The article describes the design as intended: a rule that never had to bind (a floor or cap never hit) is written as existing, and is never flagged or "verified" as untrue.** A voice pass over every page applied 101 sentence swaps and 12 structural rewrites at ckpt 149. New prose is written to this standard; a green that paraphrases must keep every fact.
- **★ Display formulas are typeset (ckpt 149):** a master writes `$$ … $$` on its own line; the builder renders it to inline SVG with MathJax, fetched and never committed. Inline math stays HTML. The `formulas` check holds each SVG to a fresh typesetting.
- **★ The judges' reader names (Matt, ckpt 148):** the location judge, the wallpaper judge, the palette judge, and the gallery judge. "Render judge" no longer appears in reader-facing prose; code keeps its names.
- **★ Links (ckpt 148):** each thing a reader can go and use is linked once per page, at its first natural mention. `?panel=<tab>` opens a tab and `?panel=gallery&collection=<name>` opens one collection.
- **The article runs to fourteen sections plus Start here.**
  - Start here (`start-here.html`, master `Start here v2.md`) has h1 "Start here" and four h2 parts: Fractal wallpapers, Fractal explorer, Deep zoom rendering, Future work. The rail shows a START HERE group above CONTENTS.
  - §9 Gallery curation is v2 (`article/gallery-curation.html`, master `Gallery curation v2.md`). Its figures are `gallery-top-scored` (the gallery judge's strict top 24), `gallery-twins` and `gallery-output`.
  - Full pipeline is v5 (`Full pipeline v5.md`): about a third of v3, in Matt's voice, figures `pipeline-overview` and `pipeline-growth` only.
  - §12 is "Deep zoom rendering" (`article/deep-zoom.html`, master `Deep zoom v3.md`).
  - §14 is "Fractal math" (`article/fractal-math.html`, master `Fractal math v2.md`); its Pi section is two displayed limits.
  - The front page carries hand-written intro and Contents blurbs, with no master and no ✓ marks; the voice pass did not reach them.
  - `escape-families` has 18 panels: five planes (degree 2 to 6), each with two of Matt's Julia picks, then Phoenix.
- **★ The download page is "Wallpaper packs" (`wallpaper-packs/`),** distinct from the explorer's Gallery tab. The Gallery tab's staged images stay under `assets/images/galleries/`; where the packs' own images live is decided when packs exist.

**★ THE SECTION-CUT TEMPLATE (Matt, ckpt 148). Done: Gallery curation (v2), Full pipeline (v5). Next: other sections as Matt names them.**
- **The test for every passage:** would a reasonably intelligent CS undergrad think of this unprompted? If so, it collapses to a sentence or goes.
- **What stays:** the non-obvious insight that motivates the section, shown with a figure; Matt's own judgement calls; facts invisible from outside; honest notes on what was considered and turned out unnecessary.
- **What collapses:** each rule becomes one bullet with its number in it, and the algorithm becomes two sentences plus links to the code files.
- **What goes:** mechanism detail; plumbing another section covers; figures that illustrate a mechanism rather than a result.
- **Shape:** the problem with its figure, the fix in one paragraph, the rules as a list, the one judgement worth dwelling on, the algorithm in brief, the result figure, a link onward.
- **Process:** Matt may skip the review docx and ask Claude to cut directly (Full pipeline was cut that way). Claude writes the master in §Voice (presented for Matt to place in `prose\`) and a placement prompt with a verify list at its foot.
- **A sentence-level review uses a coloured docx:** numbered blocks of black context, red current text, green proposed text, and black context. Matt deletes the blocks he rejects and edits the greens; an apply prompt swaps by red text, found exactly once or skipped.

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
Matt left it running across the closeout; it reports at the start of the next checkpoint.
- **`double_descent_4k_ckpt148` (website, about 24 hours):** re-renders the favicon descent `double-descent_power_L0.38_a0.15_along-the-starry-way-25` at 3840×2160 60 fps, 1.27× faster along the same path, with a monotone, generous per-keyframe iteration cap checked by measured cap-hit fractions. It reports what supersampling the k26–k28 aliasing stretch would cost; that choice is Matt's. It commits its movie tooling by explicit path; output stays untracked under `artifacts/double-descent/`.

## QUEUED IN DRIVE `prompts\`
- **`fulls_ss3_ckpt148` (wallpapers):** launch after `double_descent_4k` has finished, so it has the box to itself. `render_link` has already committed, so the engine is settled. Reboot the box first if its uptime is past a week.

## NEXT CHECKPOINT GOAL
Matt raises it at the top of the checkpoint.

## OPEN (ordered) — Matt raises each
Items 3, 6, 8, 10 and 11 are closed; the numbering is kept.
1. **Mining is CLOSED; he reopens it.** Read `preserve\mining_laws.md`, then the reopen inventory in wallpapers `curation/LEGS.md`. The `final139_*` set is the PRE baseline, and `gallery-grade score-pool` runs before any solve.
2. **"Truly finalized": the commits (Matt raises it).** What waits on it: the twenty-one kept records and their recipes (tracking = publishing), the staged website assets, and the pre-final history rewrite.
4. **Website: the section-by-section review pass** (Matt brings a section's review doc, or asks for a direct cut).
5. **Deploy preparation (preparing, not deploying).**
   - Done: the favicon (F08); explorer links embedded in every download and release render; the two repo READMEs' funnels; the packs' host decided.
   - **Left:**
     - building the packs from `fulls_ss3`'s output and `membership.jsonl`, and uploading them (Releases for the smaller packs, Drive for the large);
     - a history rewrite before the final commit;
     - **cross-platform support:** both repos build and run on Linux and macOS as well as Windows, proven by a CI OS matrix (wallpapers done, first run pending; website waits);
     - the zoom videos' YouTube uploads and 4K masters (the double-descent 4K60 master is in flight), then final deployment. **★ A final video render raises the iteration cap on intermediate keyframes: Matt sees jumps where a keyframe's cap was too low.**
   - **After deployment:** post the site to fractalforums.org.
7. **The Deep tab's follow-ups.**
   - **The gallery (33 frames, Matt's picks).** Matt adds frames over time, including frames centred away from any minibrot. He sends links, and a one-line prompt appends each row, pins `n` from the width rule, and bakes its thumbnail (→ `builder/README.md`). Julia frames are supported. One Filigree place now appears twice, in two colourings, as asked.
9. **THE WRITEUP (Matt raises it; the session authors a prose master plus a placement prompt).**
   - **§Deep zoom rendering (`article/deep-zoom.html`, master `prose\Deep zoom v3.md`).**
     - **Placed figures:** `deep-f64-and-perturbation`; `deep-shallow-and-deep` (its two panels do NOT share a colouring, on purpose); `deep-descent-rungs` (Chalcedony, absolute, λ 0, period 0.5); `deep-descent-pairs` (seats `afdb47c0`, `9c6a3d87`, glowdon); `deep-misiurewicz-pairs`: three rows (a shallow degree-2 point, then tuned degree-3 and degree-4 points deep) by three columns (whole Julia set, Julia at c, parameter plane at c). Its per-row palettes are placeholders for Matt.
     - **Placeholders:** `deep-zoom-video` (first cut exists, paused on Matt's colour and ending; on the page a poster WebP linking out, never a `<video>` embed); `deep-final-colorings` (Matt's picks in the Deep tab); `deep-descent-video`; `deep-multibrots` (Matt writes the multibrots section).
     - **The double-descent movie** (the favicon seat, `smooth`, ending on M₂ at period 32,761, at its full 32 periods). Matt's baseline is `double-descent_power_L0.38_a0.15_along-the-starry-way-25`; its 4K60 re-render is in flight. Supersampled fields for the k26–k28 grain are Matt's call.
     - **When the figure round finishes,** delete `preserve\minibrot_copies.md` and `preserve\deep_zoom_section.md`.
   - **Start here:** `start-video` waits on Matt's new video. `start-pink-gallery` (six magenta, six rose) is a placeholder for his daughter's final picks. `start-modes` is two Mandelbrot rows Matt picked (ckpt 147). The other `start-*` figures are placeholders Matt adjusts. The "darker pink gallery" link opens `magenta`; `rose` is the other honest choice (Matt's call).
   - **After `fulls_ss3` reports:** finalize §4's mode table. The wallpaper-render column is a placeholder scaled from candidate time; fill it from real ss3 times (`E:\FractalWallpapers\full\progress.jsonl`), change the text's "supersampled 4×" to 3×, and drop the caption's "placeholder… pending a measurement". Reword the sentence after the lower-base-quality sentence, which now reads as pointing at the longer search. **Rendering fundamentals' "The production setting is s = 4, so sixteen orbits" becomes s = 3 and nine, in the same prompt.**
   - **Voice-pass leftovers (one short prompt when Matt wants it):** Overview's "outside its scope" → "outside this project's scope"; Rendering fundamentals' "it is not a per-pixel average" (a not-X construction the pass left). Training judges' Evaluating paragraph could name which sets were actually held out, but only from Matt's facts.
12. **The section-cut pass:** other sections as Matt names them.
13. **Small follow-ups, each a short prompt:**
    - **Website, after the video finishes:** engine-wasm imports `fractal_engine::{autolevel, derive, mode::tune}`, deletes its own copies, and repoints `level-cases.json` / `level-derive-cases.json` (the engine's tests already read them in place); the `stamps` check may add render-link as a third embedder; the website CI and OS matrix; `article/prose.jsonl` gains the missing Start here row.
    - **Wallpapers, runnable now:** `curate solve viewers` defaults to every kept record when no stamp is named.

Parked → `preserve\parked.md`.

## STATUS / KNOWN REDS
- ⚠ A website `builder check` beside a wallpapers merge can throw a transient "not in the candidate ledger" red; retry.
- ⚠ A report just copied to Drive `reports\` can read back EMPTY for minutes; re-read once, then ask Matt to paste it.
- `builder check` was all green at the end of ckpt 149 (23 checks; `formulas` is the new one, and its render half is a named skip on a bare clone).
- Reboot the box before `fulls_ss3` or the next overnight (per fractal-operating).

## RULINGS THIS ERA
ckpt 149 (2026-09-25). Reported prompts: `render_link_ckpt148`, and `gallery_curation_edits`, `place_full_pipeline_v4`, `deep_gallery_add2`, `display_math`, `place_full_pipeline_v5`, `voice_pass_apply` (all `_ckpt149`).

- **Voice (Matt):** the article is in Matt's plain first-person voice, and describes the design as intended (→ §WEBSITE, `writing-guidance.md` §Voice).
- **Full pipeline (Matt):** cut directly to v4, then rewritten to v5 in his voice; the loop paragraph is his.
- **Gallery curation (Matt):** every mode has a floor and a ceiling; family and plane balance is the solve's own; the twins caption rewritten; `gallery-output`'s top-left panel recoloured.
- **Display math:** every display formula is typeset SVG from LaTeX; the Pi section is two displayed limits.
- **The packs' host (Matt):** Releases for the smaller packs, Drive for the large.
- **BLA (Matt):** the ruling stands; the page states the real reason.
- **The Rust-only renderer shipped:** pixel-identical to the pipeline on ten seats, with no existing render moved.

## KEEP LIST
**Drive `prompts\`:** keep `double_descent_4k_ckpt148.md` and `fulls_ss3_ckpt148.md`; wipe everything else.

**Drive `reports\`:** wipe everything.

**Drive `prose\`:** unchanged by the closeout. The live masters are `Start here v2.md`, `Overview v2.md`, `Escape-time fractals v1.md`, `Rendering fundamentals v1.md`, `Color palettes v6.md`, `Make your own palettes v4.md`, `Rendering modes v4.md`, `Training judges v6.md`, `Finding good locations v7.md`, `Finding good wallpapers v3.md`, `Gallery curation v2.md`, `Full pipeline v5.md`, `Fractal atlases v2.md`, `Deep zoom v3.md`, `Other artistic techniques v1.md` and `Fractal math v2.md`, plus `writing-guidance.md`.

The review docs' canonical copies are website `review\deep-zoom.docx` and `review\gallery-curation.docx`; the applied voice pass is archived in Drive `review\applied\voice-pass-2026-09-25.docx`.

**Wallpapers `scratch/`:**
- KEEP `place_radius_sheet/`, `retired_tentative/`, `preclose_ckpt125/off_list_stamps.txt`, `tuning_test/`, `leg_numbers.py`, `mbc140/` (§Deep zoom's picking sheets) and `cpu_default_and_rust_audit_ckpt148_findings.md` (until the engine-wasm switch in OPEN 13 lands).
- WIPE everything else.

**Website:**
- `scratch/`: wipe all except `deep_gallery_sheet/` (the 65-tile sheets, for further picks). The untracked staged set is NOT cleaned; it also holds `explorer/deep-gallery/` (33 thumbnails) and the atlas slot pictures.
- **KEEP `artifacts/deep-zoom/`** (fields, coloured keyframes, MP4s), **`artifacts/double-descent/`** (the movie's fields, stills and cuts, the in-flight 4K60 render among them) and **`artifacts/mathjax/`** (the fetched typesetter). All are untracked.
- `artifacts/deep-gallery/` and `artifacts/cap-split/` are sweepable.

**`E:\FractalWallpapers\`:** KEEP `ss_test_ckpt148\` (the ss4 references `fulls_ss3`'s check compares against). `full\` is `fulls_ss3`'s output.

**`preserve\`:** `deep_zoom_section.md` and `minibrot_copies.md` stay until the figure round finishes. `art_techniques_links.md` stays until Matt rules.

**Outside both repos:** `C:\Tools\fraktaler-3\` stays until Matt removes it.

**Wallpapers records:** the twenty-one kept records are the whole store, and their `recipes.jsonl` stay.

**Hot artifacts:**
- Stay: `artifacts/discovery/minibrot_examples.jsonl`, `artifacts/tuned129x_*`, the d=6 harvest and depth directories, and every 2026-09-18/19/21 leg's directories.
- Sweepable when Matt sweeps: the parabolic pilot's legs, superseded `gallery_grade_head/pool_scores_*`, `curation_backup/`, `tiles/` manifests and `render_dose/*.pt`.

## OWED
Nothing beyond the `double_descent_4k` report.

## SCRATCH/ARTIFACT FLAGS
- **★ The standing keep roster lives in the repo:** `src/fractal_wallpapers/README.md §The standing keep roster`.
- ⚠ `.leveled/` directories are sweepable (→ `preserve\leveled_identity.md`).
- `artifacts/atlas/<plane>/thumbs/` stays while the atlas may be re-ingested.
- ⚠ CRLF drift is real; check with `git ls-files --eol`.
- ARCHIVED (restore before reuse): unchanged from ckpt 106.

## PARKED / SETTLED
→ `preserve\INDEX.md`, which lists every file. Never re-list them here.
