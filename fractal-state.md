# fractal-state — checkpoint 145 (2026-09-24: §Deep zoom placed as v3; the deep-figure maker and automatic minibrot descents; shallow link v4 with `n`; Find minibrots copies-first at 32 periods; Hold look; favicon; embedded links)

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
- **★ The explorer's palette modes are EXPLORER-ONLY (ckpt 143).** `scale` (leveled | absolute), `lambda` and `period` are omitted at default, and the pipeline's key whitelist never emits them. Leveled stays the default everywhere (→ `engine/README.md`, `explorer/README.md`).

## LAWS STATE STILL CARRIES
- **★ The degree-6 plane is never labelled** (`partitions.NEVER_LABELLED`).
- **★ Inside a minibrot copy is a named phenomenon** → `preserve\minibrot_copies.md`. It is a §Deep zoom source, with `preserve\deep_zoom_section.md` (OPEN 9).
- **★ Parabolic aiming is answered above ε ≈ 3e-3: dead.** Below that ε it is untested (OPEN 8, fractal-engine).

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
| Explorer: tabs, keys, Deep/Cancel/undo/recolour, palette modes and Hold look, the fade table, Find minibrots (copies before bulbs, 32 periods, measured framing), zoom-out stop, screensaver, Walk, Phoenix | `explorer/README.md` |
| Deep kernel, oracle, calibration, closed verdicts (BLA included) | `explorer/perturb-wasm/README.md` |
| Atlas | `atlas/README.md` |
| Builder, figures, the split rule, `seats.py`, the staged set, site size, the zoom-video tooling (`zoom.py`), the deep-figure maker (`builder deep`), automatic minibrot descents (`builder descent`), the site's icon | `builder/README.md` |
| Explorer links embedded in downloaded and released files | `stamp.js` · wallpapers `explorer_link`; the `stamps` check |
| The Deep tab's gallery: its register (`explorer/deep-gallery.jsonl`), maker (`builder/deep_gallery.py`) and method | `builder/README.md §How the first set was found` |
| Traps: native exe rebuild, perturb rebake, repo links, the no-`<video>` rule | `CLAUDE.md` |
| Per-page status | `docs/page-review.md` |

- **★ STAGING RULE (Matt):** no gallery-sized or library-sized commits until he says deploy.
- Shallow contract **v4** (an optional `n`, omitted at the width rule; ckpt 145); deep contract **v3**.

**★ THE SITE IS RE-BASED ON `final139_*` + `final140_general2000` — DATA ONLY. Prose and captions wait for "ready for publishing".** Held until then:
- `gallery-curation.html`'s prose, which describes a mode-floor shortfall the current record lacks.
- Its `gallery-pool` chart. Its maker reads `places_refused`, a stage `fold: pool` records do not write, so decide then whether the chart still belongs.

**★ Figure recipes are never lost.** `article/figure-recipes.jsonl` is site-owned and tracked; a `spec` panel's recipe is its registry row. ★ Every composite figure that can be split is split (Matt).

**★ THE EXPLORER'S BAR (Matt):**
- Complexity is a cost to the person using a tool; only clear wins are added (→ `preserve\rulings_website.md §2026-09-20`).
- Its text is for the artist, and every keyed button wears its key. "Render mode" is the term everywhere.
- Left panel changes the view; right panel manipulates this view.
- **The shallow view and the Deep tab are one tool at two depths (Matt, ckpt 144):** the same control grid (Render | Navigation over the view's draw control | Download), the same button in the same place wherever both have it, one Save, one Root (r), and Find minibrots in both. Details → `explorer/README.md`.
- It targets the desktop.
- Explorer-only fast paths are allowed only where the pixel difference from the pipeline is easy to bound. Wasm threads are out.
- ⚠ This box drifts ~30% between identical runs; alternate before/after.

**★ Deep (perturbation) is explorer-only; nothing deep enters the pipeline (Matt)** (→ fractal-engine §Deep render). The Inflection tab is paged out (`explorer/paged-inflection/`), and gets an article mention only (OPEN 9). **★ The Walk is a short demonstration of how the galleries were made.** Parked → `preserve\parked.md`.

## IN FLIGHT ACROSS THIS BOUNDARY
- **`double_descent_ckpt145` + addendum 1 (website).** Its interim report is read and carried here. The favicon-seat movie's fields were still rendering at the boundary (a 960×540 cut, then colour and encode). Its final report may arrive after this closeout; read it for the movie and whatever changed since.

## QUEUED IN DRIVE `prompts\`
Both run after `double_descent` commits, in either order (Matt's):
- **`cap_split_ckpt145` (website; may lock both).** Two ceilings, separately named: automatic 1e6 (the depth rule and the probe; the `cap::CEILING` ruling) and explicit 2e6 (a typed or linked `n`, Halve/Double, Find minibrots' `32·p`, descent pins). The `n` range widens to 2e6 in both contracts. It also measures orbit memory per worker and renders the movie's M₂ at its full 32 periods.
- **`deep_zoom_slots_ckpt145` + addendum 1 (website).**
  - The BLA line becomes "about 20% slower … to about 2.6 times faster".
  - Placeholders `deep-descent-video` and §The multibrots (`deep-multibrots`) are added.
  - Two corrections go into §Automatic minibrot descents.

## NEXT CHECKPOINT GOAL
Matt raises it at the top of the checkpoint.

## OPEN (ordered) — Matt raises each
Items 3, 6 and 11 were closed at ckpt 145; the numbering is kept.
1. **Mining is CLOSED; he reopens it.** Read `preserve\mining_laws.md`, then the reopen inventory in wallpapers `curation/LEGS.md`. The `final139_*` set is the PRE baseline, and `gallery-grade score-pool` runs before any solve.
2. **"Truly finalized": the commits (Matt raises it).** What waits on it: the twenty-one kept records and their recipes (tracking = publishing), the staged website assets, and the pre-final history rewrite and CDN question.
4. **Website: the section-by-section review pass** (Matt brings a section's review doc).
5. **Deploy preparation (preparing, not deploying).**
   - **Done at ckpt 145:**
     - **The favicon** is F08, cropped from seat `dff7e280effc3aa3` (→ `builder/README.md §The site's icon`). The Galleries page opens on its source picture.
     - **Embedded links.** Every explorer download and every release render carries its explorer link as invisible metadata: PNG `iTXt`, and JPG XMP `dc:source` plus EXIF. The base URL is one constant per repo, held to `pages.SITE_URL`. Release files already on disk are unstamped; there is no backfill.
   - **Left:**
     - a CDN in front of the big fetches;
     - a history rewrite before the final commit;
     - the deep zoom video's YouTube upload and 4K master, which wait until the ideal fractal is settled, then final deployment.
   - **After deployment:** post the site to fractalforums.org.
7. **The Deep tab's follow-ups.**
   - **The gallery (31 frames, Matt's picks).** Matt adds frames over time, including frames centred away from any minibrot. He sends links, and a one-line prompt appends each row and bakes its thumbnail (→ `builder/README.md`).
   - **Resolved at ckpt 145:**
     - Find minibrots opens a copy at 32 periods, lists copies before bulbs (bulbs only when the view holds no copy), and frames by the measured body.
     - Halve and Double stay live mid-pass.
   - **Closed:** the Newton early-stop at symmetry stages. Smaller framing lets the user zoom out to the stages.
8. **LONG-TERM: rich SHALLOW Julia pictures at `c` near a parabolic point.** The explorer half exists (the Julia preview under the pointer). The pipeline residue: the sub-floor regime needs a cap field on `expand.rs`'s `Node` and the route from the seed row. After that, ungated spot renders per stratum are the primary read, and the walk comes second (sheets in wallpapers `scratch/parabolic_c_pilot_ckpt139/`). The source list is `preserve\art_techniques_links.md`.
9. **THE WRITEUP (Matt raises it; the session authors a prose master plus a placement prompt).**
   - (a) **§Deep zoom (`article/deep-zoom.html`) is placed as v3** (master `prose\Deep zoom v3.md`).
     - **Placed figures:**
       - `deep-f64-and-perturbation`;
       - `deep-shallow-and-deep` (its two panels do NOT share a colouring, on purpose);
       - `deep-descent-rungs` (six, 2×3);
       - `deep-misiurewicz-pairs`;
       - `deep-descent-pairs`.
     - **Placeholders:**
       - `deep-zoom-video`: the first cut exists (`builder/zoom.py`, three MP4s in `artifacts/deep-zoom/video/`). It is paused on Matt's colour and ending. On the page it is a poster WebP linking out, never a `<video>` embed.
       - `deep-final-colorings`: Matt's picks in the Deep tab.
       - Once `deep_zoom_slots` lands, `deep-descent-video` and `deep-multibrots`. Matt writes the multibrots section.
     - **The double-descent movie** is the favicon seat, rendered `smooth`, chain [A, A], ending on M₂ at period 32,761. It is rendering under `double_descent`, and its full 32 periods need `cap_split`'s explicit ceiling.
     - **When the figure round finishes,** delete `preserve\minibrot_copies.md` and `preserve\deep_zoom_section.md`.
   - (b) A ***Future work / Other artistic techniques*** section, with inflection first ("not worth integrating in Matt's experience").
10. **A PROFILING PASS (overnight, when Matt says; the prompt is not yet written).** Native and wasm, engine and explorer as they stand: time every anchor per family and mode, flag anything unusually slow, and where cheap, fix it. General, NOT an A/B. Seed classes worth a look:
    - an arm past LLVM's inline threshold;
    - wasm losing an optimisation native keeps (`simd128` has never been tried on `perturb.wasm`);
    - a specialization arm falling back to the generic loop;
    - cap/escalation changes that move time, not pixels;
    - whether a nucleus reference pays on an off-nucleus frame (unmeasured).

    Unattended rules apply, and it locks both repos.

Parked → `preserve\parked.md`.

## STATUS / KNOWN REDS
None.
- ⚠ A website `builder check` beside a wallpapers merge can throw a transient "not in the candidate ledger" red; retry.
- ⚠ A report just copied to Drive `reports\` can read back EMPTY for minutes; re-read, don't re-write.
- Reboot the box before the next overnight (per fractal-operating).

## RULINGS THIS ERA
ckpt 145 (2026-09-24). Reported prompts:
`deep_figures`, `explorer_nav_layout`, `palette_hold`, `deep_zoom_edits`, `readme_image4`, `iter_buttons_live`, `favicon_sheet`, `find_minibrots_cap2`, `embedded_links`, `favicon_wire`, `find_minibrots_bulbs` (+1), `PLACE_deep_zoom_v3`; `double_descent` (+1) is interim.

- **Explorer:**
  - Render-mode parameters wrap, so the Navigation column never shrinks.
  - Julia is the last Navigation button, beside its preview box.
  - The Deep gallery is always open.
  - "Back to the explorer" is now **Shallow mode**. It fades (with its tooltip kept) when the frame is too deep.
  - **Nothing fades for a render in progress:** a press stops the pass and acts. Halve and Double restart the pass at the new cap and keep the reference orbit.
- **Hold look (Absolute only; UI state, on by default).**
  - Dragging λ re-solves period and phase, holding band density and colour at the frame's median ν.
  - Dragging period re-solves phase.
  - The maths and links are unchanged.
- **Shallow link v4 carries an optional `n`** (Matt). `pins.query_of` writes it.
- **Find minibrots** (Matt: an all-black minibrot is a failure):
  - It pins `n = 32·p` (`nuclei::open_cap`).
  - It frames the copy at about a quarter of the height, from the measured body.
  - It lists copies before bulbs, and bulbs, labelled, only when the view holds no copy.
- **Two iteration ceilings (Matt):** automatic 1e6 and explicit 2e6, as separate constants. Queued as `cap_split`.
- **§Deep zoom v3 (Matt's review):**
  - "Julia sets inside the Mandelbrot set" (Tan Lei at Misiurewicz points) replaces the embedded-Julia section.
  - The seahorse-valley and deep-gallery sections are cut. §Automatic minibrot descents is added, and §The deep gallery becomes a placeholder.
  - "The tab" becomes "the fractal explorer" throughout.
  - The rebasing credit links to Zhuoran's thread.
- **Deploy:**
  - The favicon is F08.
  - Embedded links are invisible metadata.
  - `data/palette_choice/rows/` stays: it is large and regenerable, but not something to commit casually.
  - The decode cache and the Phoenix score grid are closed.
- **Wallpapers README:** `examples/julia_smooth.jpg` is removed from the strip. Its pin stays.

## KEEP LIST
**Drive `prompts\`:** wipe everything EXCEPT `double_descent_ckpt145.md` and its `_addendum1.md` (in flight), `cap_split_ckpt145.md`, and `deep_zoom_slots_ckpt145.md` and its `_addendum1.md` (queued).

**Drive `reports\`:** wipe everything. `double_descent`'s final report is written after the wipe.

The review doc's canonical copy is website `review\deep-zoom.docx`.

**Wallpapers `scratch/`:**
- KEEP `place_radius_sheet/`, `retired_tentative/`, `preclose_ckpt125/off_list_stamps.txt`, `tuning_test/`, `leg_numbers.py`, `parabolic_c_pilot_ckpt139/` (OPEN 8) and `mbc140/` (§Deep zoom's picking sheets).
- WIPE everything else. The f64 proof spec now lives site-side.

**Website:**
- `scratch/`: wipe all except `deep_gallery_sheet/` (the 65-tile sheets, for further picks). The untracked staged set is NOT cleaned; it also holds `explorer/deep-gallery/` (31 thumbnails).
- **KEEP `artifacts/deep-zoom/`** (fields, coloured keyframes, three MP4s; about 5 GB) and **`artifacts/double-descent/`** (the movie's fields, stills and cut). Both are untracked.
- `artifacts/deep-gallery/` is sweepable.

**`preserve\`:** `deep_zoom_section.md` and `minibrot_copies.md` stay until the figure round finishes.

**Outside both repos:** `C:\Tools\fraktaler-3\` stays until Matt removes it.

**Wallpapers records:** the twenty-one kept records are the whole store, and their `recipes.jsonl` stay.

**Hot artifacts:**
- Stay: `artifacts/discovery/minibrot_examples.jsonl`, `artifacts/tuned129x_*`, the d=6 harvest and depth directories, every 2026-09-18/19/21 leg's directories, and the parabolic pilot's legs.
- Sweepable when Matt sweeps: superseded `gallery_grade_head/pool_scores_*`, `curation_backup/`, `tiles/` manifests and `render_dose/*.pt`.

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
