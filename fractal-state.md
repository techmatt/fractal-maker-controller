# fractal-state — checkpoint 128 (2026-09-16)

## Where we are
Three phases, each depending strictly on the one before → fractal-discovery. Matt iterates from pictures, not counts; phase 3 is his eye on the final seating.

**★ EVERY COLLECTION HAS A TARGET AND THE TARGETS LIVE IN `curation/targets.py` (2026-09-15).** `TARGETS`, reached by `curate solve run --collection NAME`; `--n` still overrides; a collection with no target REFUSES. The table: the nine ordinary families at **400**, `green` and `cyan` at **300**, `lime` at **150**, `tia` at **1000**, `smooth` and `stripe` at **800**, `threads` at **400**. Changing one is a one-line edit there, never a number retyped into a prompt. The seat count was ckpt 125's largest quality lever → `curation/GALLERY.md`.

**★ ⚠ GALLERY SIZE IS MATT'S DECISION ALONE.** Never raise it, never queue it, never reason about the tradeoffs of shrinking `n`. **"Final gallery quality" is NOT the median** — it is his judgement over many factors; never reframe the goal as maximising a summary statistic.

**★ THE PUBLISHED GALLERY IS `20260914T171846Z`**, the eighth `tentative.PUBLISHED` stamp. **Matt raises any further publishing himself; never ask, never list it.** The viewer is `artifacts/curation/viewer/index.html`. 32 of its 1,000 seats are `itinerary`; all 47 `itinerary` recipes modulate `smooth`. 291 seats carry a tone curve, 612 field/composite seats carry none, 97 are direct/modulate; 15 seats carry a maxiter other than `maxiter::for_width`.

**★ THE REMAINING HORIZON IS ABOUT 100 MORE MINING HOURS (Matt, 2026-09-12), NOT 10,000.** The 10,000-hour frame stays as the way to JUDGE a product choice (→ fractal-operating). Records-only retention is not needed at this scale → `preserve\retention_design.md`.

**★ THE BAR: `DEFAULT_FINE_BAR = 0.030242` ON `p_ge4`**, under `fine_head = twelve_sheets_drop_high_asymmetric_auc_ge4_more_k3` (a k=3 seed ensemble averaged on the probability scale, shipped). The LEVEL is a matched constant. **★ ⚠ A BAR IS UNREADABLE WITHOUT ITS HEAD** — never carry a level across a fit. ⚠ `solve.Q4_BAR = 0.50` is the RENDER judge's constant. ⚠ `--fine-bar 0` still excludes unread rows; `fine_bar=None` in process is the only unbarred spelling. Provenance → `models/gallery_grade/README.md`.

**★ ⚠ THE PUBLISHED MEDIAN SITS AT THE POOL'S 96.55th PERCENTILE.** No knee; places halve per 0.10–0.13 of bar; the per-family spread is a monotone shift. Census → `curation/GALLERY.md`; stale in its counts, not its shape.

**★ `p_fine`, `p_coarse` AND THE QUALITY BARS ARE ALL OPERATING WELL — EVERY TASK THAT WOULD ALTER THEM IS CLOSED (Matt, 2026-09-12).** He re-raises if worth doing.

**★ THE HUMAN VETO IS SHIPPED (Matt, 2026-09-14).** A human `p_fine` label of `1` excludes that ROW from seating, the pool and every future solve; derived, retroactive, latest-wins, human-origin only. Shape → `curation/README.md`. **★ THE REJECTION PASS IS A LABELING MODE: Matt marks ONLY `1`s and an unmarked tile is NOT a label** (`sweep: false` on every sheet). Never build a review sheet whose unmarked state writes anything.

**★ A THEMED PASS RELAXES THE BAR INSIDE ITS OWN CELL (shipped).** `solve.themed_fine_bar` = the lower of the shipped bar and the `p_fine` of the 4n-th best dominant row, floored at 0.01; a cell that cannot fill ships SMALL, no padding → `curation/GALLERY.md`.

**★ ⚠ A HUE FAMILY IS NOT THE UNION OF ITS FOUR CELLS** (`FAMILY_LEAD` 0.20 / `FAMILY_ALONE` 0.30); a row is dominant in at most THREE families → `palettes/README.md`. **★ ⚠ NO FAMILY IS SCARCE AT EITHER BAR** — a weak family is short of DISTINCT material at places held. **★ A THIN CELL IS STOCK-BOUND, NOT CARRIER-BOUND.** **★ THE PALETTE GROUP CAP IS `0.075·n` THEMED, `0.025·n` GENERAL** (446 maps hold the 1,000 seats). **★ ⚠ THE COLOUR ALLOWANCE IS PROPORTIONAL TO `n`.** **★ MATT REOPENED K HIMSELF AND SET IT; CLAUDE STILL NEVER PROPOSES REOPENING IT.**

**★ A GALLERY PAGE IS PRESENTED STRATIFIED, NOT IN QUALITY ORDER** (`curation/page_order.py`; `ORDER_PROGRAM`: a greedy 32-seat window pricing colour cell / mode / family / spiral repeats, embedding as tie-break). The website's `builder seats` now asks that module for the permutation and writes `order` on each row; the explorer and the Galleries page open on the same tiles. ⚠ Any embedding-store rewrite shifts the tie-break; the built Galleries page parts from the explorer past tile 78 until `curate solve browse` is rebuilt (nothing is live; leave it).

**★ THE `p_fine` COLUMN IS NOT IDENTIFIED, AND AVERAGING IS THE LEVER** → `preserve\gallery_grade_stability.md`. **★ ⚠ A BEFORE/AFTER ACROSS A REFIT NEEDS A SAME-RECIPE REPLICATE AS CONTROL.** **★ ⚠ THE ALLOWANCE COUNTS MEMBERSHIPS, NOT SEATS.** **★ GUARD RULINGS (Matt, 2026-09-10): LOOSENING ONLY, AND NOTHING WAS LOOSENED** — spiral cap 0.10, per-cell floor 20. **★ ⚠ THE SOLVER IS NOT AT ITS OPTIMUM** (non-monotone; seats change hands for no reason; two boxes with identical data resolved one swap/augment near-tie differently — Matt: not a concern). **★ `PRESELECT_RADIUS` STAYS AT 0.02.** **★ ASYMMETRIC COST: KEEPING LOW-GRADED PICTURES LOW MATTERS MORE.** **★ `--forced` IS STAGED AND STAYS STAGED.** **★ THE FOLD MERGES INSTEAD OF DELETING.** **★ THERE IS NO HONEST SCORE COLUMN OVER THE SEATED POPULATION — Matt's eye is the only independent read.** **★ A RE-RENDER INVALIDATES EVERY READING TAKEN OFF THE PICTURE** (`recolour --keys`, idempotent). **★ GROUPS ARE PALETTE GROUPS AND MINING CANNOT MOVE THEM.**

**★ `pool_scores.jsonl` IS ONE-SHOT: Mine → merge → score-pool → solve.** **★ A `score-pool` REFRESH MOVES MEMBERSHIP, NOT READINGS.** **⚠ SEATS-CHANGED IS NOT A MEASURE OF POOL CHANGE.** ⚠ A PRE/after read across a merge counts `score-pool`'s re-scoring too (the reframe leg: 220 changed hands, 42 from the leg); **attribute seats to a leg by joining on the leg's own row keys** — the `leg` field of a solve record is the seating stage (`general_pool`, `mandate`, `swap`, `augment`), not a rendering leg.

**★ ⚠ FILL IS THE WRONG SINGLE MEASURE OF A MINING LEG. Report seats AND the seated `p_fine` distribution, always.** **★ ⚠ WEIGH A MEASUREMENT AGAINST THE COST OF THE ACTION IT DECIDES.** **★ ⚠ A SMALL SMOKE MISPRICES A LEG; price off an OBSERVED leg.**

## ROTATION AND PHASE — CLOSED
**★ THE FORWARD DRAW IS ONE RANDOM PHASE PER CANDIDATE (Matt, 2026-09-14)**; best-of-five only on the shareable field path and for depth at a named place; every head fp16 going forward; the direct traps draw bare → `preserve\rotation_phase_economics.md`. **★ A LEG STATES ITS RESOLVED SHARES AND ROSTER BEFORE PLANNING.** ⚠ `--shares` MERGES over `depth.SHARES`. ⚠ `--budget` both sizes a plan and sets its deadline. **Both rotation arms now record the levelling stamp and write `sequence.jsonl`** (`rotation` in `SEQUENCE_STORES`, 2026-09-16); every kept seat store-wide resolves a curve; 10,040 non-seat rotation rows still carry none (~4.4 h serial, unowed).

## THE PALETTE AXIS — PARKED, EXCEPT PHASE
**★ MATT PARKED PALETTE REPLICATION ENTIRELY (2026-09-12).** ⚠ `p_fine` is a CANDIDATE-geometry column.

## MODES AND COLOUR
**★ THE FOUR TARGETED-GALLERY MODES ARE `smooth`, `tia`, `stripe` AND `threads`, AND NOTHING ELSE (Matt, 2026-09-15).** **★ MORE ANGLE-MODE MINING IS A VARIETY GOAL, NEVER A SEAT ONE.** **★ NEVER EXCLUDE A SHAREABLE MODE ON A SEAT ARGUMENT WITHOUT PRICING IT.**

## SOURCING — REOPENED AT ckpt 126
**★ TWO BACKLOGS WERE ADMITTED ON 2026-09-16:** 83,598 production-harvest gate survivors (`curate score --unscored`; 50.3% keeper / 11.2% great; the four dynamical partitions 15–19% great, `mandelbrot` 0.3%, `multibrot5` 0.7%) and **3,110 human-graded places on no ledger** (`curate score --graded`; 87.8% keeper / 44.6% great, 3.9× fresh harvest; 52 ms a place to score). **★ THE GRADED PLACES ARE THE BEST GROUND THE PROJECT HAS.** The 1,607 opened ones took a 95-minute mined-roster leg on 2026-09-15: 607 new locations, 140 honest seats.

**★ ⚠ NO ARM THAT STANDS ON `hunt.scanned` CAN REACH A PLACE WITHOUT A VECTOR** — the doors are `curate score --opened` and `curate score --graded`; with vectors in place `--floor-places` reaches every graded place. ⚠ `curate hunt` renders on ONE engine, no pool. ⚠ `proven_places` → `hunt.spread` is a flat round-robin — priority is delivered by TRUNCATING a manifest.

**★ THE REFRAME CHANNEL: a reframe leg WRITES LOCATIONS, and `curate hunt --places` opens them, at phase 0, on the `mined()` roster** (there is no phase axis on the hunt and no "theta-search" anywhere in the repo — ckpt 127 wrote the leg wrongly and CC corrected it from source). `g11`: 3,627 seeds / 140 productive / 190 locations in 30 min. **`g12` (ckpt 127, 30 min): 888 seeds consumed / 125 productive / 201 locations → 197 scored and embedded → 2,364 candidates (221 over `SEATING_BAR`) → 42 seats in the sixteen solves** (`threads` 14, `smooth` 11). **⚠ g12 is thinning against g11: 32% more seeds for 11% fewer productive, barren share 67% → 74%, 2,249 seeds left unfired.**

**★ SUPPLY IS ROOT-BOUND ON THE TWINS** → `preserve\julia_supply.md`; phoenix → `preserve\phoenix_sampling.md`. **★ AIMING IS FREE AND LARGE.** **★ ⚠ THE RECOLOUR ARM DOES NOT SATURATE WITHIN A LEG — A STALE MANIFEST LOOKS EXACTLY LIKE SATURATION. Rebuild the manifest.** **★ A PROVEN PLACE IS WORTH ABOUT FIVE BLIND ONES TO A COMPOSITE.**

## RETENTION
**★ THE KEEP IS FIVE PER `(place, mode)` PLUS ONE FAMILY ALLOWANCE (`retention.FAMILY_ALLOWANCE = 1`).** Forward-only; lands in `candidate_ledger/family_allowance/<stamp>.jsonl`. **★ THE RANK ITSELF IS STILL COLOUR-BLIND** → `curation/README.md`. **★ A PRUNE WRITES WHAT IT TOOK** (`displaced/<stamp>.jsonl`); ⚠ a pruned row never gets a `p_fine`. A merge record carries `locations_in_leg` and `locations_new` (`locations_added` is gone, 2026-09-16). Ledger 469,586 rows after the ckpt-127 merges.

## RECORDS
**★ ⚠ A RECORD IS DISCARDED BY DEFAULT (Matt, 2026-09-13; in `CLAUDE.md`). PRESERVATION DERIVES FROM THE KEEP LIST ALONE.** **★ ⚠ A RECORD IS TWO DIRECTORIES**; `solve.write_record` refuses to overwrite. The portable reference record (green n=300, `20260916T182649Z`) is off the keep list BY MATT'S CHOICE and wipes at this boundary; `portable.REFERENCE` must be re-pointed at a fresh record before the next `storage export` — Matt: no export until more mining brings the solves near final.

**★ THE SIXTEEN `targets_*` RECORDS OF `20260915T2101–2106Z` ARE THE STANDING BASELINE, BUT THE POOL HAS MOVED** (ckpt-126 admissions, the g12 reframe, the fresh-box merge). **The next mining night runs the sixteen solves as its own PRE baseline before any leg.** ⚠ The standing magenta record holds 397 seats; the post-merge-back magenta solve seated 387/400, unattributed — Matt: resolve along with everything else later. The two undeclared hard-dependency stamps (`20260906T133559Z`, `20260906T133236Z`) are on the standing keep roster.

## THE RECORD'S OWN PROSE
**★ A RECORD CARRIES ITS PROSE WHOLE, AND THE SOURCE CARRIES ONE COPY** (`SCHEMA_NOTES`).

## THE REPO AS A CLONE SEES IT
**★ A FRESH BOX CONTINUES EVERY STAGE FROM `storage export` ALONE (proved 2026-09-16 on a second Windows machine)** → `preserve\fresh_box.md`; the procedure is the wallpapers README §Continuing on another machine (`storage export/import`, `re-render --keys|--seatable|--rest`, `mine package/unpack/merge`). Pictures never travel; a fresh box solves only after a render. **★ THE INSTALL IS `uv sync` NAMING ALL THREE EXTRAS.** **★ ⚠ `p_fine` ROWS ARE STAMPED WITH A WEIGHTS SHA AND A CLONE'S ROWS DIFFER BY DESIGN.** The four release assets carry MIT terms; the three gallery-grade fp32 `best.pt` are NOT release assets — `rotation.score_fine` refuses without them and names the export as their source. No export is kept on disk (`E:\FractalStorage\portable\` deleted 2026-09-16).

## WEBSITE — THE ATLAS AND THE EXPLORER STUDIO
Design → **`preserve\atlas_design.md`**; the repos' READMEs are authoritative. **The explorer as of ckpt 127:** studio panel = DOWNLOAD (button first; "This screen (W×H)" default, presets, custom; 1×/2×; a few-word estimate; a Rendering/Sharpening/Final/Stopped dot) → MODE (13 gallery modes only, seat-count order with `curvature` second-to-last; a link's foreign mode appends) → PALETTE (Popular = top 24 curated at overlap ≥0.7 by pooled hue family, ≤3 per family; display names for all 1,021 maps from `explorer/palette-names.json` `{name, source}` — 511 authored / 510 generated; underlying names in links, filenames, records) → SHADE (gamma, cycles, phase slider, transfer; rolloff removed — single-valued across the record; Reverse/Mirror chips; `Reset shade (N)`) → DETAILS (operator id, both palette names, stat line, provenance). Render pass preview → 1spp → ss2 (Lanczos-3 in linear light, wasm `supersample`). **★ AUTOLEVEL LEVELS ANY VIEW (ported 2026-09-16):** a seat or link carrying `level=` replays it exactly; a link without one stays unlevelled until the first move; every other view derives from its own finished picture in the worker (`shade_level`; +0.5 s default canvas, +1.5 s at 1440p — a warm shade worker is the open follow-up); Copy link writes the five numbers. The derivation is pinned bit-exact to the operator (4,411/4,411 stored curves); a browser curve never equals a stored one for the same recipe (JPEG round trip, geometry, maxiter, percentile method) → that is why seats replay. All copy is plain-language, American spelling. **★ STAGING RULE (Matt): no gallery-sized or library-sized commits until he says deploy** — `seated-candidates`, the blob and the swatch PNG stay untracked in `.git/info/exclude`. Atlas: 35 curved / 72 clean / 0 lost after `autolevel backfill --atlas mandelbrot`; `carriers.jsonl` writes `uncarried` rows (`atlas_grey`) and the website's `library()` skips them. `builder check` is GREEN (18/18) since `c335560`; `wallpapers-three-bands` was re-picked from the ledger at the marked frame (mode pair weak, 0.027 / 0.127 — CC flagged it for Matt's eye). CI had been red since 2026-09-07 on a numpy import; fixed.

## IN FLIGHT ACROSS THIS BOUNDARY
Nothing.

## QUEUED IN DRIVE `prompts\`
Nothing.

## NEXT CHECKPOINT GOAL
**Matt sets it at the top of the checkpoint.**

## OPEN (ordered) — Matt raises each
1. **The next mining night — the unrun legs of `overnight_mine_ckpt126`**: (a) one depth plan over, in order, the 3,110 newly opened graded places by head score → the julia survivors' great tier → the other survivors' great tier → a second palette pass over the 1,607; (b) the sixteen solves before and after. (The `g12` reframe ran at ckpt 127 and the channel is thinning.) Roster `mode_policy.mined()`, one random phase on the forward draw, width from free slots; a reframe, if any, is `reframe` → `hunt --places`. Producing time comes with Matt's launch message; the sixteen PRE solves run first. Rule on unattended prompts → fractal-operating.
2. **Every mining night is composed fresh with Matt.** Arms with a reading: graded places (44.6% great), julia survivors (15–19% great), reframe (g12: 125 productive / 30 min, thinning); arms without one since the manifest fix: aimed recolour, dear/angle modes at held places.
3. **A continuous boundary sampler for the parameter planes (Matt: some future checkpoint)** → `preserve\julia_supply.md`.
4. **The decode cache — a storage decision for Matt** (~33 GB hot; Matt: not yet).
5. **`pictures/` in the ten `runs` legs.** 5.37 GiB. Matt: leave. ⚠ Destructive; attended only.
6. **Website — the section-by-section review pass** (Matt brings a section's review doc). Per-page status → `docs/page-review.md`. The atlas's other planes have placeholder plates; their marks are `curate atlas --plane` runs whenever wanted. Small website leftovers: Copy link during a running derived pass writes the previous frame's curve; the explorer README's seat-curve count reads 98 (it is 291); a warm shade worker if the derive cost is felt; the presentation order vs Galleries page divergence past tile 78.
7. **Whether a second published stamp gets a recipe file**, and whether `data/palette_choice/rows/` belongs in a clone (Matt: leave it entirely).

Parked → `preserve\parked.md`.

## STATUS / KNOWN REDS
None. Website `builder check` green. ⚠ Three orphaned `multiprocessing` workers from 2026-09-15 were on the box on 2026-09-16 — Matt's box to clean; reboot before the next overnight per fractal-operating.

## RULINGS THIS ERA
→ the docs themselves and the in-repo promotions: `curation/LEGS.md`, `curation/README.md`, `curation/GALLERY.md`, `curation/atlas/README.md`, `coloring/README.md`, `supply/README.md`, the wallpapers root README §Continuing on another machine, the `portable` README, website `CLAUDE.md`, `explorer/README.md`, `preserve\atlas_design.md`, `preserve\fresh_box.md`.

## KEEP LIST
Drive `prompts\`: **wipe everything** (nothing queued). `reports\`: **wipe everything**.

Wallpapers `scratch/`: KEEP `place_radius_sheet/`, `retired_tentative/` and `preclose_ckpt125/off_list_stamps.txt`; **WIPE everything else**. Website `scratch/`: wipe `explorer_order_first24.md`; otherwise unchanged. Website untracked (do NOT clean): `assets/images/galleries/seated-candidates/`, `explorer/palettes.bin`, `explorer/palettes-swatch.png` — the staging rule's files, listed in `.git/info/exclude`. The second machine's checkout and hot root are Matt's; nothing there is tracked here.

## OWED
Nothing.

## SCRATCH/ARTIFACT FLAGS
**★ THE STANDING KEEP ROSTER LIVES IN THE REPO — `src/fractal_wallpapers/README.md §The standing keep roster`.** ⚠ `.leveled/` directories are sweepable → `preserve\leveled_identity.md`. ⚠ `orphans` lists pre-existing unmerged legs and a dated orphan verdict goes stale in hours. `artifacts/atlas/` is untracked artifact output. Per-checkpoint: `artifacts/curation/depth/*/fields` grows ~226 MB a leg. ⚠ CRLF drift is real; `git ls-files --eol`. `re_render.json` is last-leg-only with no reader. ARCHIVED (RESTORE before reuse): unchanged from ckpt 106.

## PARKED / SETTLED
→ `preserve\INDEX.md`, which lists every file. Never re-list them here.
