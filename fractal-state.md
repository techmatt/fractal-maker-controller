# fractal-state — checkpoint 147 (2026-09-24: interior seam extended to the orbit modes; Absolute Fit in the explorer; parabolic Julia sets closed; Start here v2, Fractal math, Wallpaper packs, Contents blurbs, the site audit)

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
- `final140_general2000` (n=2000) is offered on the site beside the n=1000 default.

**★ NOTHING IS PUBLISHED.**
- `tentative.PUBLISHED` is empty, so `tentative.latest()` refuses and every unstamped read names a stamp.
- Matt raises publishing himself; never ask, never list it.
- Viewers: `curate solve viewers STAMP…` → `artifacts/curation/viewer/<label>/index.html` and `viewer/all.html`.

**★ PINNED SEATS.** `data/curation/pins.txt` → `curate pins resolve` → `pins.json`. Ten pins, seated before the seed and prune-proof; `--no-pins` for comparisons (→ `curation/GALLERY.md §Pinned seats`). `pins.query_of` writes gallery links; they are never hand-spelled.

**★ THE SUMMARY METRICS ARE SETTLED AT THIS HORIZON.** The 10,000-hour frame stays as the way to JUDGE a product choice (→ fractal-operating).

**★ THE BAR: `DEFAULT_FINE_BAR = 0.030242` ON THE FINE COLUMN**, under `fine_head = twelve_sheets_drop_high_asymmetric_auc_ge4_more_k3`, a k=3 seed ensemble averaged on the probability scale.
- **⚠ A bar is unreadable without its head.**
- **⚠ 0.50 is NOT the seating bar.** `solve.Q4_BAR = 0.50` is the RENDER judge's constant on `p_ge4`.
- **⚠ There are two quality columns.** `p_ge4` is the render judge's GATE reading. `p_fine` is the fine head's own column, where the bar lives, and it is THE quality reading. Its scale is compressed: read q1 and the fraction above a mark, not the bare median.
- ⚠ One seed of the fine head is not the mean. ⚠ `--fine-bar 0` still excludes unread rows. Provenance → `models/gallery_grade/README.md`.
- **★ `p_fine`, `p_coarse` and the bars are all operating well; every task that would alter them is CLOSED (Matt, 2026-09-12).**

**★ THE HUMAN VETO IS SHIPPED** (→ `curation/README.md`). The rejection pass is a labeling mode: Matt marks ONLY `1`s, and an unmarked tile is NOT a label.

**★ A THEMED PASS RELAXES THE BAR INSIDE ITS OWN CELL.** `solve.themed_fine_bar` = the lower of the shipped bar and the `p_fine` of the 4n-th best dominant row, floored at 0.01. Mining moves a family's bar. **⚠ `--themed CELL` names a codebook colour cell, not the family bar; the family pass is `--collection <family>`.**

**★ FAMILY PASSES FLOOR AT `mode_policy.seat_floors(n)`; A MODE PASS FLOORS AT 0.** `--flat-floor` is the door back. ⚠ The floor is NOT monotone. The recurring family holes are `itinerary`, `curvature` and `direct_trap_lines`, and they are supply, not rule.

**★ COLOUR:**
- ⚠ A hue family is NOT the union of its four cells (→ `palettes/README.md`).
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

## LAWS STATE STILL CARRIES
- **★ The degree-6 plane is never labelled** (`partitions.NEVER_LABELLED`).
- **★ Inside a minibrot copy is a named phenomenon** → `preserve\minibrot_copies.md`. It is a §Deep zoom source, with `preserve\deep_zoom_section.md` (OPEN 9).
- **★ Parabolic Julia sets are CLOSED (Matt, ckpt 147):** judged by eye on a sheet. The few that work sit just outside a root, at about ε = 1e-4; the rest fill with interior. They are reachable by hand in the explorer and are not included as a tool or in the pipeline. §13 points to Wikibooks and Chéritat.

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
- The install is `uv sync` naming all three extras.
- ⚠ `p_fine` rows are stamped with a weights sha, and a clone's rows differ by design.
- ⚠ Drive the makers through `.venv/Scripts/fractal-wallpapers.exe`.

## WEBSITE — THE EXPLORER STUDIO AND THE ARTICLE
**Nothing is live; the site never needs preserving or keeping in sync.** Every fact about the site is owned by the website repo, and state keeps no copy:

| Topic | Owner |
|---|---|
| Explorer: tabs, keys, Deep/Cancel/undo/recolour, Deep auto-render and its switch, palette modes, Fit (f) and the arrival refit, Hold look, the fade table, Find minibrots, zoom-out stop, screensaver, Walk, Phoenix, the two iteration ceilings, measured timings | `explorer/README.md` |
| Deep kernel, oracle, calibration, closed verdicts (BLA included) | `explorer/perturb-wasm/README.md` |
| Atlas, and the live `atlas-live` figure with its miniatures | `atlas/README.md` |
| Builder, figures, the split rule, `seats.py`, the staged set, site size, the zoom-video tooling (`zoom.py`), the deep-figure maker (`builder deep`), automatic minibrot descents (`builder descent`), the `start-*` maker (`builder/start.py`), every `builder check` check, the site's icon | `builder/README.md` |
| Explorer links embedded in downloaded and released files | `stamp.js` · wallpapers `explorer_link`; the `stamps` check |
| The Deep tab's gallery: its register (`explorer/deep-gallery.jsonl`), maker (`builder/deep_gallery.py`) and method | `builder/README.md §How the first set was found` |
| Traps: native exe rebuild, perturb rebake, repo links, the no-`<video>` rule, the one script kind an article page may carry, the rail | `CLAUDE.md` |
| Style: no italics, no em-dashes, vocabulary | `prose\writing-guidance.md` · website `CLAUDE.md` |
| Per-page status | `docs/page-review.md` |

- **★ STAGING RULE (Matt):** no gallery-sized or library-sized commits until he says deploy.
- Shallow contract **v4** (an optional `n`, omitted at the width rule; ckpt 145); deep contract **v3**. `n` runs 50 to 2e6 in both.
- **★ No figure reuses a picture shown elsewhere on the site unless the reuse is intentional (Matt).** The collection's diversity is the point; an intentional reuse carries a `reuse_reason`.
- **★ The site reads as its final form (Matt, ckpt 147):** no "under construction" wording. Matt's own "yet"s are his to keep.
- **The article runs to fourteen sections plus Start here.**
  - Start here (`start-here.html`, master `Start here v2.md`) has h1 "Start here" and four h2 parts: Fractal wallpapers, Fractal explorer, Deep zoom rendering, Future work. The rail shows a START HERE group above CONTENTS.
  - §12 is "Deep zoom rendering" (`article/deep-zoom.html`, master `Deep zoom v3.md`).
  - §14 is "Fractal math" (`article/fractal-math.html`, master `Fractal math v2.md`).
  - The front page carries hand-written intro and Contents blurbs, with no master and no ✓ marks.
- **★ The download page is "Wallpaper packs" (`wallpaper-packs/`),** distinct from the explorer's Gallery tab. The Gallery tab's staged images stay under `assets/images/galleries/`; where the packs' own images live is decided when packs exist.

**★ THE SITE IS RE-BASED ON `final139_*` + `final140_general2000` — DATA ONLY. Prose and captions wait for "ready for publishing".** Held until then: the `gallery-pool` chart. Its maker reads `places_refused`, a stage `fold: pool` records do not write, so decide then whether the chart still belongs.

**★ Figure recipes are never lost.** `article/figure-recipes.jsonl` is site-owned and tracked; a `spec` panel's recipe is its registry row. ★ Every composite figure that can be split is split (Matt).

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
Nothing.

## QUEUED IN DRIVE `prompts\`
Nothing.

## NEXT CHECKPOINT GOAL
Matt raises it at the top of the checkpoint.

## OPEN (ordered) — Matt raises each
Items 3, 6, 8, 10 and 11 are closed; the numbering is kept.
1. **Mining is CLOSED; he reopens it.** Read `preserve\mining_laws.md`, then the reopen inventory in wallpapers `curation/LEGS.md`. The `final139_*` set is the PRE baseline, and `gallery-grade score-pool` runs before any solve.
2. **"Truly finalized": the commits (Matt raises it).** What waits on it: the twenty-one kept records and their recipes (tracking = publishing), the staged website assets, and the pre-final history rewrite and CDN question.
4. **Website: the section-by-section review pass** (Matt brings a section's review doc).
5. **Deploy preparation (preparing, not deploying).**
   - Done: the favicon (F08, → `builder/README.md §The site's icon`); explorer links embedded in every download and release render as invisible metadata (no backfill of release files already on disk).
   - **Left:**
     - a CDN in front of the big fetches;
     - a history rewrite before the final commit;
     - **the two repo READMEs open by linking each other and the live site, and funnel each visitor to where they want to go** (wallpapers → the wallpaper packs; exploring → the explorer; how it works → the article; code → the right repo) (Matt, ckpt 147);
     - the zoom videos' YouTube uploads and 4K masters, which wait until the ideal fractal is settled, then final deployment. **★ A final video render raises the iteration cap on intermediate keyframes: Matt sees jumps where a keyframe's cap was too low.**
   - **After deployment:** post the site to fractalforums.org.
7. **The Deep tab's follow-ups.**
   - **The gallery (31 frames, Matt's picks).** Matt adds frames over time, including frames centred away from any minibrot. He sends links, and a one-line prompt appends each row and bakes its thumbnail (→ `builder/README.md`).
9. **THE WRITEUP (Matt raises it; the session authors a prose master plus a placement prompt).**
   - **§Deep zoom rendering (`article/deep-zoom.html`, master `prose\Deep zoom v3.md`).**
     - **Placed figures:** `deep-f64-and-perturbation`; `deep-shallow-and-deep` (its two panels do NOT share a colouring, on purpose); `deep-descent-rungs` (Chalcedony, absolute, λ 0, period 0.5); `deep-descent-pairs` (seats `afdb47c0`, `9c6a3d87`, glowdon); `deep-misiurewicz-pairs`: three rows (a shallow degree-2 point, then tuned degree-3 and degree-4 points deep) by three columns (whole Julia set, Julia at c, parameter plane at c). Its per-row palettes are placeholders for Matt.
     - **Placeholders:** `deep-zoom-video` (first cut exists, paused on Matt's colour and ending; on the page a poster WebP linking out, never a `<video>` embed); `deep-final-colorings` (Matt's picks in the Deep tab); `deep-descent-video`; `deep-multibrots` (Matt writes the multibrots section).
     - **The double-descent movie** (the favicon seat, `smooth`, ending on M₂ at period 32,761, at its full 32 periods). Matt's baseline is `double-descent_power_L0.38_a0.15_along-the-starry-way-25`, and he is still experimenting. The record defaults to the power mapping (α 0.15, L 0.38). The grain at k26–k28 is sub-pixel aliasing; supersampled fields (about 4× field time) are Matt's call.
     - **When the figure round finishes,** delete `preserve\minibrot_copies.md` and `preserve\deep_zoom_section.md`.
   - **Start here:** `start-video` waits on Matt's new video. `start-pink-gallery` (six magenta, six rose) is a placeholder for his daughter's final picks. `start-modes` is two Mandelbrot rows Matt picked (ckpt 147). The other `start-*` figures are placeholders Matt adjusts.

Parked → `preserve\parked.md`.

## STATUS / KNOWN REDS
- ⚠ Wallpapers fast lane: `tests/test_twins.py::test_the_channel_only_ever_hands_over_what_nobody_has_walked` is red at HEAD and predates ckpt 146. It sits in the twins supply channel, which matters only if mining reopens.
- ⚠ A website `builder check` beside a wallpapers merge can throw a transient "not in the candidate ledger" red; retry.
- ⚠ A report just copied to Drive `reports\` can read back EMPTY for minutes; re-read once, then ask Matt to paste it.
- Reboot the box before the next overnight (per fractal-operating).

## RULINGS THIS ERA
ckpt 147 (2026-09-24). Reported prompts: `gallery_curation_cut_ckpt146`, `interior_seam_orbit_modes`, `parabolic_eye_sheet`, `start_here_v2`, `no_italics`, `small_fixes`, `start_here_heading`, `start_modes_sheet`, `start_modes_rebuild`, `fractal_math`, `front_and_start`, `absolute_fit`, `contents_blurbs`, `fit_busier`, `wallpaper_packs`, `site_audit`, `final_fixes` (all `_ckpt147`).

- **Engine (→ fractal-engine):** an exact repeat now also stops the orbit-extreme modes, with byte-identical pictures. `itinerary` on the Mandelbrot anchor went from 11.0 s to 1.2 s. OPEN 11 is closed.
- **Parabolic Julia sets (Matt):** closed and not included (→ §LAWS).
- **Explorer (Matt):** Absolute Fit (f) at 7 passes; Deep enters on Absolute and refits once when the finished frame lands; Leaving Deep keeps the scale.
- **Article (Matt):**
  - No italics for emphasis anywhere (84 removed; the rule lives in writing guidance and `CLAUDE.md`).
  - No ✓ status marks.
  - No "under construction" wording (the site audit made 16 edits).
  - Start here v2 and its four-part structure; §12 "Deep zoom rendering"; §14 "Fractal math" (renamed file, reordered, and "Which Julia sets are connected" and "Minibrots everywhere" retitled).
  - The Contents blurbs are rewritten in Matt's tone ("Here, we show…").
  - "Wallpaper packs" is the download page's name.
  - §13 carries the parabolic paragraph.
  - The atlas page links the Phoenix tab and the seahorse valley.
  - Gallery curation §What comes up short is deleted.
  - `start-modes` is re-picked.

## KEEP LIST
**Drive `prompts\`:** wipe everything.

**Drive `reports\`:** wipe everything.

**Drive `prose\`:** unchanged by the closeout. The live masters include `Deep zoom v3.md`, `Fractal atlases v2.md`, `Start here v2.md`, `Other artistic techniques v1.md`, `Fractal math v2.md`, `Gallery curation v1.md`, `Escape-time fractals v1.md` and `Overview v2.md`.

The review doc's canonical copy is website `review\deep-zoom.docx`.

**Wallpapers `scratch/`:**
- KEEP `place_radius_sheet/`, `retired_tentative/`, `preclose_ckpt125/off_list_stamps.txt`, `tuning_test/`, `leg_numbers.py` and `mbc140/` (§Deep zoom's picking sheets).
- WIPE everything else, including `parabolic_c_pilot_ckpt139/` and `parabolic_eye_ckpt147/`.

**Website:**
- `scratch/`: wipe all except `deep_gallery_sheet/` (the 65-tile sheets, for further picks). The untracked staged set is NOT cleaned; it also holds `explorer/deep-gallery/` (31 thumbnails) and the atlas slot pictures.
- **KEEP `artifacts/deep-zoom/`** (fields, coloured keyframes, MP4s) and **`artifacts/double-descent/`** (the movie's fields, stills and cuts, Matt's baseline among them). Both are untracked.
- `artifacts/deep-gallery/` and `artifacts/cap-split/` are sweepable.

**`preserve\`:** `deep_zoom_section.md` and `minibrot_copies.md` stay until the figure round finishes. `art_techniques_links.md` lost its OPEN 8 role; it stays until Matt rules.

**Outside both repos:** `C:\Tools\fraktaler-3\` stays until Matt removes it.

**Wallpapers records:** the twenty-one kept records are the whole store, and their `recipes.jsonl` stay.

**Hot artifacts:**
- Stay: `artifacts/discovery/minibrot_examples.jsonl`, `artifacts/tuned129x_*`, the d=6 harvest and depth directories, and every 2026-09-18/19/21 leg's directories.
- Sweepable when Matt sweeps: the parabolic pilot's legs, superseded `gallery_grade_head/pool_scores_*`, `curation_backup/`, `tiles/` manifests and `render_dose/*.pt`.

## OWED
Nothing.

## SCRATCH/ARTIFACT FLAGS
- **★ The standing keep roster lives in the repo:** `src/fractal_wallpapers/README.md §The standing keep roster`.
- ⚠ `.leveled/` directories are sweepable (→ `preserve\leveled_identity.md`).
- `artifacts/atlas/<plane>/thumbs/` stays while the atlas may be re-ingested.
- ⚠ CRLF drift is real; check with `git ls-files --eol`.
- ARCHIVED (restore before reuse): unchanged from ckpt 106.

## PARKED / SETTLED
→ `preserve\INDEX.md`, which lists every file. Never re-list them here.
