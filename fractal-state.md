# fractal-state — checkpoint 142 (2026-09-23: a doc-shrink checkpoint — mining laws and the minibrot census moved verbatim to `preserve\`; tutorial and engine rewritten to pointers; the website READMEs took over the explorer's facts; Deep undo/Cancel/zoom-out polish; `REFERENCE` is a kept record)

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

## LAWS STATE STILL CARRIES
- **★ The degree-6 plane is never labelled** (`partitions.NEVER_LABELLED`).
- **★ Inside a minibrot copy is a named phenomenon** → `preserve\minibrot_copies.md` (the §Deep zoom source, OPEN 9).
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
| Explorer: tabs, keys, Deep/Cancel/undo, zoom-out stop, screensaver, Walk, Phoenix | `explorer/README.md` |
| Deep kernel, oracle, calibration, closed verdicts | `explorer/perturb-wasm/README.md` |
| Atlas | `atlas/README.md` |
| Builder, figures, the split rule, `seats.py`, the staged set, site size | `builder/README.md` |
| Traps: native exe rebuild, perturb rebake, repo links | `CLAUDE.md` |
| Per-page status | `docs/page-review.md` |

- **★ STAGING RULE (Matt):** no gallery-sized or library-sized commits until he says deploy.
- Shallow contract **v3**; deep contract **v3**.

**★ THE SITE IS RE-BASED ON `final139_*` + `final140_general2000` — DATA ONLY. Prose and captions wait for "ready for publishing".** Held until then:
- `gallery-curation.html`'s prose, which describes a mode-floor shortfall the current record lacks.
- Its `gallery-pool` chart. Its maker reads `places_refused`, a stage `fold: pool` records do not write, so decide then whether the chart still belongs.

**★ Figure recipes are never lost.** `article/figure-recipes.jsonl` is site-owned and tracked; a `spec` panel's recipe is its registry row. ★ Every composite figure that can be split is split (Matt).

**★ THE EXPLORER'S BAR (Matt):**
- Complexity is a cost to the person using a tool; only clear wins are added (→ `preserve\rulings_website.md §2026-09-20`).
- Its text is for the artist, and every keyed button wears its key. "Render mode" is the term everywhere.
- Left panel changes the view; right panel manipulates this view.
- It targets the desktop.
- Explorer-only fast paths are allowed only where the pixel difference from the pipeline is easy to bound. Wasm threads are out.
- ⚠ This box drifts ~30% between identical runs; alternate before/after.

**★ Deep (perturbation) is explorer-only; nothing deep enters the pipeline (Matt)** (→ fractal-engine §Deep render). The Inflection tab is paged out (`explorer/paged-inflection/`), and gets an article mention only (OPEN 9). **★ The Walk is a short demonstration of how the galleries were made.** Parked → `preserve\parked.md`.

## IN FLIGHT ACROSS THIS BOUNDARY
Nothing.

## QUEUED IN DRIVE `prompts\`
`lanes_log_ckpt142.md` (wallpapers: delete the lane readings log from `CLAUDE.md`), unless it ran beside this closeout. Its report needs no carry.

## NEXT CHECKPOINT GOAL
Matt raises it at the top of the checkpoint.

## OPEN (ordered) — Matt raises each
1. **Mining is CLOSED; he reopens it.** Read `preserve\mining_laws.md`, then the reopen inventory in wallpapers `curation/LEGS.md`. The `final139_*` set is the PRE baseline, and `gallery-grade score-pool` runs before any solve.
2. **"Truly finalized": the commits (Matt raises it).** What waits on it: the twenty-one kept records and their recipes (tracking = publishing), the staged website assets, and the pre-final history rewrite and CDN question.
3. **The decode cache** — a storage decision for Matt (~33 GB hot; Matt: not yet).
4. **Website: the section-by-section review pass** (Matt brings a section's review doc).
5. **Deploy preparation (preparing, not deploying).** The choices left — a CDN in front of the big fetches, a history rewrite before the final commit, embedded links in full-size wallpapers, and a real favicon (Matt's tile pick) — are listed HERE only.
6. **Whether `data/palette_choice/rows/` belongs in a clone** (Matt: leave it entirely).
7. **The Deep tab's follow-ups:**
   - A hand-picked Deep gallery of ~20 links inside the tab (unblocked).
   - What a Nearby-minibrots entry should show at depth (Matt is testing).
   - Stopping a Newton jump early at a 2^k-fold symmetry stage (needs the feature bar's verdict).
   - Whether a nucleus reference pays on an off-nucleus frame (unmeasured).
8. **LONG-TERM: rich SHALLOW Julia pictures at `c` near a parabolic point.** The explorer half exists (the Julia preview under the pointer). The pipeline residue: the sub-floor regime needs a cap field on `expand.rs`'s `Node` and the route from the seed row. After that, ungated spot renders per stratum are the primary read, and the walk comes second (sheets in wallpapers `scratch/parabolic_c_pilot_ckpt139/`). The source list is `preserve\art_techniques_links.md`.
9. **THE WRITEUP (Matt raises it; the session authors a prose master plus a placement prompt).**
   - (a) **§Deep zoom is unwritten** (`article/deep-zoom.html`). Its claims, figure source and numbers → `preserve\minibrot_copies.md` (delete that file once the section is placed). The Deep tab's sentence gains its link to the section then (→ `explorer/README.md`).
   - (b) A ***Future work / Other artistic techniques*** section, with inflection first ("not worth integrating in Matt's experience").
10. **A PROFILING PASS (overnight, when Matt says; the prompt is not yet written).** Native and wasm, engine and explorer as they stand: time every anchor per family and mode, flag anything unusually slow, and where cheap, fix it. General, NOT an A/B. Seed classes worth a look:
    - an arm past LLVM's inline threshold;
    - wasm losing an optimisation native keeps;
    - a specialization arm falling back to the generic loop;
    - cap/escalation changes that move time, not pixels.

    Unattended rules apply, and it locks both repos.
11. **Phoenix tab, second step (optional):** a precomputed judge-score grid over the plane, shipped as a small PNG overlay with a checkbox and suggested markers. A wallpapers job, then a website one. Look at the plane first.

Parked → `preserve\parked.md`.

## STATUS / KNOWN REDS
None.
- ⚠ A website `builder check` beside a wallpapers merge can throw a transient "not in the candidate ledger" red; retry.
- ⚠ A report just copied to Drive `reports\` can read back EMPTY for minutes; re-read, don't re-write.
- Reboot the box before the next overnight (per fractal-operating).

## RULINGS THIS ERA
ckpt 142 (2026-09-23), six prompts. All are reported except `lanes_log_ckpt142`, which is queued above.
- **Doc shrink (Matt):**
  - Mining laws and the minibrot census move verbatim to `preserve\`.
  - The explorer's facts are owned by the website READMEs.
  - Operating is canonical, and the preference lines stay terse.
  - State no longer carries a per-checkpoint "what Claude got wrong"; a pattern that repeats becomes one line in operating.
  - Verbatim moves are script steps. Only newly authored large text is presented.
- **Backups are Matt's:** exports run only at his direction and are never proposed.
- **`REFERENCE` = the kept `final139_green`.**
- **The Deep tab:**
  - Undo is a recolour.
  - Cancel after an auto-started pass reverts to the last finished picture.
  - Zoom-out stops at the family's home (Julia and the Phoenix plane at 2× home), with the centre eased home.
  - A new tab sentence, with no link until §Deep zoom exists.
  - A palette change mid-pass lands in the new palette.
- **`CLAUDE.md` holds rules only**, so the lane log goes.

## KEEP LIST
Drive `prompts\`: wipe everything except `lanes_log_ckpt142.md` if still unrun. `reports\`: wipe everything.

Wallpapers `scratch/`:
- KEEP `place_radius_sheet/`, `retired_tentative/`, `preclose_ckpt125/off_list_stamps.txt`, `tuning_test/`, `leg_numbers.py`, `parabolic_c_pilot_ckpt139/` (OPEN 8) and `mbc140/` (§Deep zoom's picking sheets).
- WIPE everything else.

Website `scratch/`: wipe all. The untracked staged set is NOT cleaned.

Wallpapers records: the twenty-one kept are the whole store, and their `recipes.jsonl` stay.

Hot artifacts:
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
