# fractal-state — checkpoint 127 (2026-09-16)

## Where we are
Three phases, each depending strictly on the one before → fractal-discovery. Matt iterates from pictures, not counts; phase 3 is his eye on the final seating.

**★ EVERY COLLECTION HAS A TARGET AND THE TARGETS LIVE IN `curation/targets.py` (2026-09-15).** `TARGETS`, reached by `curate solve run --collection NAME`; `--n` still overrides; a collection with no target REFUSES. The table: the nine ordinary families at **400**, `green` and `cyan` at **300**, `lime` at **150**, `tia` at **1000**, `smooth` and `stripe` at **800**, `threads` at **400**. Changing one is a one-line edit there, never a number retyped into a prompt. The seat count was ckpt 125's largest quality lever (1,351 fewer seats lifted fifteen of sixteen medians) → `curation/GALLERY.md`.

**★ ⚠ GALLERY SIZE IS MATT'S DECISION ALONE.** Never raise it, never queue it, never reason about the tradeoffs of shrinking `n`. **"Final gallery quality" is NOT the median** — it is his judgement over many factors; never reframe the goal as maximising a summary statistic.

**★ THE PUBLISHED GALLERY IS `20260914T171846Z`**, the eighth `tentative.PUBLISHED` stamp. **Matt raises any further publishing himself; never ask, never list it.** The viewer is `artifacts/curation/viewer/index.html`. 32 of its 1,000 seats are `itinerary`; all 47 `itinerary` recipes modulate `smooth`.

**★ THE REMAINING HORIZON IS ABOUT 100 MORE MINING HOURS (Matt, 2026-09-12), NOT 10,000.** The 10,000-hour frame stays as the way to JUDGE a product choice (→ fractal-operating). Records-only retention is not needed at this scale → `preserve\retention_design.md`.

**★ THE BAR: `DEFAULT_FINE_BAR = 0.030242` ON `p_ge4`**, under `fine_head = twelve_sheets_drop_high_asymmetric_auc_ge4_more_k3` (a k=3 seed ensemble averaged on the probability scale, shipped). The LEVEL is a matched constant. **★ ⚠ A BAR IS UNREADABLE WITHOUT ITS HEAD** — never carry a level across a fit. ⚠ `solve.Q4_BAR = 0.50` is the RENDER judge's constant. ⚠ `--fine-bar 0` still excludes unread rows; `fine_bar=None` in process is the only unbarred spelling. Provenance → `models/gallery_grade/README.md`.

**★ ⚠ THE PUBLISHED MEDIAN SITS AT THE POOL'S 96.55th PERCENTILE.** No knee; places halve per 0.10–0.13 of bar; the per-family spread is a monotone shift (orange 3.4–4.0× azure at every decile). Census → `curation/GALLERY.md`. ⚠ Read before the ckpt-126 admissions (below); the pool is much larger now and the census is stale in its counts, not its shape.

**★ `p_fine`, `p_coarse` AND THE QUALITY BARS ARE ALL OPERATING WELL — EVERY TASK THAT WOULD ALTER THEM IS CLOSED (Matt, 2026-09-12).** He re-raises if worth doing.

**★ THE HUMAN VETO IS SHIPPED (Matt, 2026-09-14).** A human `p_fine` label of `1` excludes that ROW (the exact candidate by recipe key) from seating, the pool and every future solve; derived, retroactive, latest-wins, human-origin only. Shape → `curation/README.md`. **★ THE REJECTION PASS IS A LABELING MODE: Matt marks ONLY `1`s and an unmarked tile is NOT a label** (`sweep: false` on every sheet). Never build a review sheet whose unmarked state writes anything.

**★ A THEMED PASS RELAXES THE BAR INSIDE ITS OWN CELL (shipped).** `solve.themed_fine_bar` = the lower of the shipped bar and the `p_fine` of the 4n-th best dominant row, floored at 0.01; a cell that cannot fill ships SMALL, no padding. `config.theme_bar` / `bar_from` on the manifest → `curation/GALLERY.md`.

**★ ⚠ A HUE FAMILY IS NOT THE UNION OF ITS FOUR CELLS** (`FAMILY_LEAD` 0.20 / `FAMILY_ALONE` 0.30 against summed mass); a row is dominant in at most THREE families → `palettes/README.md`. **★ ⚠ NO FAMILY IS SCARCE AT EITHER BAR** — a weak family is short of DISTINCT material at places held, not of material. **★ A THIN CELL IS STOCK-BOUND, NOT CARRIER-BOUND** — buy rows IN the cell. **★ THE PALETTE GROUP CAP IS `0.075·n` THEMED, `0.025·n` GENERAL**; the collection is not converging on one palette (446 maps hold the 1,000 seats). **★ ⚠ THE COLOUR ALLOWANCE IS PROPORTIONAL TO `n`** — never carry a shortfall across a target change. **★ MATT REOPENED K HIMSELF AND SET IT; CLAUDE STILL NEVER PROPOSES REOPENING IT.**

**★ A GALLERY PAGE IS PRESENTED STRATIFIED, NOT IN QUALITY ORDER** (`curation/page_order.py`; `curate solve browse <stamp> --spacing`). ⚠ A monotone decile profile is the wrong check.

**★ THE `p_fine` COLUMN IS NOT IDENTIFIED, AND AVERAGING IS THE LEVER** (churn `0.108 + 0.657/√k`) → `preserve\gallery_grade_stability.md`. **★ ⚠ A BEFORE/AFTER ACROSS A REFIT NEEDS A SAME-RECIPE REPLICATE AS CONTROL.** **★ ⚠ THE ALLOWANCE COUNTS MEMBERSHIPS, NOT SEATS.** **★ GUARD RULINGS (Matt, 2026-09-10): LOOSENING ONLY, AND NOTHING WAS LOOSENED** — spiral cap 0.10, per-cell floor 20. **★ ⚠ THE SOLVER IS NOT AT ITS OPTIMUM** (≥1.4 of sum on the table at n=1000; non-monotone, so seats change hands for no reason). **★ `PRESELECT_RADIUS` STAYS AT 0.02.** **★ ASYMMETRIC COST: KEEPING LOW-GRADED PICTURES LOW MATTERS MORE THAN KEEPING HIGH-GRADED ONES HIGH.** **★ `--forced` IS STAGED AND STAYS STAGED.** **★ THE FOLD MERGES INSTEAD OF DELETING** (no transitivity; survivor on the seating key). **★ THERE IS NO HONEST SCORE COLUMN OVER THE SEATED POPULATION — Matt's eye is the only independent read.** **★ A RE-RENDER INVALIDATES EVERY READING TAKEN OFF THE PICTURE** (`recolour --keys`, idempotent). **★ GROUPS ARE PALETTE GROUPS AND MINING CANNOT MOVE THEM.**

**★ `pool_scores.jsonl` IS ONE-SHOT: Mine → merge → score-pool → solve.** Nothing enforces it. **★ A `score-pool` REFRESH MOVES MEMBERSHIP, NOT READINGS.** **⚠ SEATS-CHANGED IS NOT A MEASURE OF POOL CHANGE.**

**★ ⚠ FILL IS THE WRONG SINGLE MEASURE OF A MINING LEG. Report seats AND the seated `p_fine` distribution, always.** **★ ⚠ WEIGH A MEASUREMENT AGAINST THE COST OF THE ACTION IT DECIDES.** **★ ⚠ A SMALL SMOKE MISPRICES A LEG; price off an OBSERVED leg; a pilot's winners do not survive n.**

## ROTATION AND PHASE — CLOSED
**★ THE FORWARD DRAW IS ONE RANDOM PHASE PER CANDIDATE (Matt, 2026-09-14)**; best-of-five only on the shareable field path and for depth at a named place; every head fp16 going forward; the direct traps draw bare. → `preserve\rotation_phase_economics.md`. **★ A LEG STATES ITS RESOLVED SHARES AND ROSTER BEFORE PLANNING.** ⚠ `--shares` MERGES over `depth.SHARES` — spell shares whole. ⚠ `--budget` both sizes a plan and sets its deadline; `--from-block` cannot resume a wholly-ranked leg.

## THE PALETTE AXIS — PARKED, EXCEPT PHASE
**★ MATT PARKED PALETTE REPLICATION ENTIRELY (2026-09-12).** ⚠ `labeling/server.py` has no write path. ⚠ `p_fine` is a CANDIDATE-geometry column.

## MODES AND COLOUR
**★ THE FOUR TARGETED-GALLERY MODES ARE `smooth`, `tia`, `stripe` AND `threads`, AND NOTHING ELSE (Matt, 2026-09-15).** **★ MORE ANGLE-MODE MINING IS A VARIETY GOAL, NEVER A SEAT ONE.** **★ NEVER EXCLUDE A SHAREABLE MODE ON A SEAT ARGUMENT WITHOUT PRICING IT** (12–45× cheaper a clear).

## SOURCING — REOPENED AT ckpt 126
**★ ⚠ "THE NEVER-OPENED POOL IS ZERO — BREADTH RETIRED" (ckpt 125) WAS TRUE OF ADMITTED LOCATIONS ONLY, AND TWO LARGE BACKLOGS SAT OUTSIDE IT.** Both were admitted on 2026-09-16:
- **83,598 production-harvest gate survivors** on the three ckpt-123 harvest legs — walk rows that passed the gates and were never scored. `curate score --unscored` reads the walk's own gate render (6 ms a location, the whole set in minutes; **embedding is the bill**, ~40 min). Realised **50.3% keeper / 33.5% at the head's top band / 11.2% great**, and a 20% pilot projected it to a tenth. **Two populations**: the four dynamical partitions clear at 15–19% great, `mandelbrot` 0.3% and `multibrot5` 0.7%. `phoenix:classic` had 4 rows in the whole set.
- **The human-graded places: 6,202 distinct at verdict ≥3, 3,110 of which were on no walk ledger and in no store** (2,025 location-only / 545 smooth / 481 strange / 59 both; the location store holds PLACES, not pictures, so `label-migration` could never derive them). `curate score --graded` mints one row a place at its best verdict and scores it: **87.8% keeper / 44.6% great — 3.9× fresh harvest at the great cut** (`julia:multibrot4` 71.6% great). The 1,607 graded places that had been opened read 77.7% / 37.9%. ⚠ They cost **52 ms a place** to score (deep verdict-4 zooms), 5.7× `--opened`'s rate — budget a graded backlog at its own rate.
Embedding store **51,491 → 88,181**, missing 0; sidecar 197,580 rows. **★ THE GRADED PLACES ARE THE BEST GROUND THE PROJECT HAS.** The 1,607 opened ones took a 95-minute mined-roster leg on 2026-09-15: 607 new locations, 140 honest seats over 83 places, medians up in 10 of 16 collections.

**★ ⚠ NO ARM THAT STANDS ON `hunt.scanned` CAN REACH A PLACE WITHOUT A VECTOR** — `--floor-places`, `--near-places` and `curate hunt --places` all plan zero units there, silently, whatever the manifest says. The doors are `curate score --opened` (candidate-ledger places with no sidecar row) and `curate score --graded` (label-store places); the two populations overlap and a pass may claim only one. **With vectors now in place, `--floor-places` reaches every graded place.** ⚠ `curate hunt` renders on ONE engine, no pool: 3,110 places at `--per-location 3` is ~4.9 h. ⚠ `proven_places` → `hunt.spread` is a flat round-robin — a priority order is delivered by TRUNCATING a manifest, never by ordering inside it.

**★ THE REFRAME CHANNEL IS ALIVE; `g10`'S "RUNNING DRY" WAS A QUEUE DEFECT.** `g10` had been handed only `g9`'s unresolved roots and died on a pin at 4.4 min; both fixed. `g11` was offered 3,627 seeds and in 30 min returned **140 productive / 190 new locations / 132 clearing q4 at ~9.6 s a location**. ⚠ `g9` and `g10` had never been merged, so every supply reading 2026-09-06 → 09-15 under-counted the channel; merged now.

**★ SUPPLY IS ROOT-BOUND ON THE TWINS** (1,401 roots) → `preserve\julia_supply.md`; phoenix → `preserve\phoenix_sampling.md`. **★ AIMING IS FREE AND LARGE** (median 14.6× at the cell; `--draw-cells` saturates in list length and a no-op cut is refused at plan time; `--cell` is a cycle). **★ ⚠ THE RECOLOUR ARM DOES NOT SATURATE WITHIN A LEG — A STALE MANIFEST LOOKS EXACTLY LIKE SATURATION. Rebuild the manifest, don't re-run it.** **★ A PROVEN PLACE IS WORTH ABOUT FIVE BLIND ONES TO A COMPOSITE.**

## RETENTION
**★ THE KEEP IS FIVE PER `(place, mode)` PLUS ONE FAMILY ALLOWANCE (`retention.FAMILY_ALLOWANCE = 1`).** Forward-only by construction; lands in `candidate_ledger/family_allowance/<stamp>.jsonl`; subtract `reached_a_protected_row` or the file is noise. **★ ⚠ THE KEEP BINDS AT ONLY 7.4% OF PAIRS** (read before the ckpt-126 admissions). **★ THE RANK ITSELF IS STILL COLOUR-BLIND** → `curation/README.md §Where colour is a dimension`. **★ A PRUNE WRITES WHAT IT TOOK** (`displaced/<stamp>.jsonl`; a displaced row is buyable back by recipe key); ⚠ a pruned row never gets a `p_fine`.

## RECORDS
**★ ⚠ A RECORD IS DISCARDED BY DEFAULT (Matt, 2026-09-13; in `CLAUDE.md`). PRESERVATION DERIVES FROM THE KEEP LIST ALONE.** **★ ⚠ A RECORD IS TWO DIRECTORIES** (`tentative/<stamp>/`, `solve/<name>/`); `solve.write_record` refuses to overwrite. The store holds 96 stamps / 627 MiB, 80 off the keep list (61.4 MiB; list at `scratch/preclose_ckpt125/off_list_stamps.txt`); none pins anything.

**★ THE SIXTEEN `targets_*` RECORDS OF `20260915T2101–2106Z` ARE THE STANDING BASELINE, BUT THE POOL HAS MOVED SINCE** (one depth leg, the ckpt-126 admissions, four merges). **The next mining night runs the sixteen solves as its own PRE baseline before any leg** and reads the after-solves against both. The two undeclared hard-dependency stamps (`20260906T133559Z`, `20260906T133236Z`) are on the standing keep roster.

## THE RECORD'S OWN PROSE
**★ A RECORD CARRIES ITS PROSE WHOLE, AND THE SOURCE CARRIES ONE COPY** (`SCHEMA_NOTES`; no version integer; an inline-prose record site is refused). `held_out_is` undercounted and the records were left alone.

## THE REPO AS A CLONE SEES IT
**★ A FRESH CLONE CAN BUILD, DRAW THE PUBLISHED GALLERY AND MINE DE NOVO; IT CANNOT SOLVE** (stores untracked; shipping the pool is Matt's undecided call). **★ THE INSTALL IS `uv sync` NAMING ALL THREE EXTRAS**; the pip `--extra-index-url` workaround cannot work (cu124 tops out at the floors). **★ ⚠ `p_fine` ROWS ARE STAMPED WITH A WEIGHTS SHA AND A CLONE'S ROWS DIFFER BY DESIGN** (fp32 stored, fp16 shipped; ~2 seats in / 2 out; reports, never gates). **The four release assets carry MIT terms (2026-09-16)** and the README has a CI badge.

## WEBSITE — THE ATLAS AND THE EXPLORER STUDIO (built this checkpoint)
Design as built → **`preserve\atlas_design.md`** (wholesale, 2026-09-16); the repos' READMEs are authoritative. The atlas is discrete dots over a tight greyscale plate (population = every place above the fine bar, seated first, greedy thinning at a pixel radius, blue = Mandelbrot / red = Julia, three thumbnails a dot); `curate atlas` (wallpapers `curation/atlas/`) writes it to `artifacts/atlas/<plane>/`, the website ingests with `builder atlas --ingest`. `explorer/` is the site's one full-bleed page: gallery grid + atlas on the left, viewer with regrouped controls on the right; all 1,021 (now 1,022 with `atlas_grey`) colormaps baked as a ~1 MB stop blob; autolevel is Python stop-surgery ported exactly to `engine-wasm/src/level.rs` under permalink key `level`. **★ STAGING RULE (Matt): no gallery-sized or library-sized commits until he says deploy** — code and records commit, the staged gallery `seated-candidates` (237 MB), the blob and the swatch PNG stay untracked in `.git/info/exclude`. **★ WHAT MATT WANTS: a gallery tile opens as the picture it shipped.** Standing gap: **`rotation` runs record no tone curve, so 472 of the 1,000 seats open unlevelled** — queued for this checkpoint (OPEN 3). Ten measured seats sit at 2.7–4.9 of 255 with the curve, up to 28 without.

## IN FLIGHT ACROSS THIS BOUNDARY
Nothing.

## QUEUED IN DRIVE `prompts\`
**`atlas_ingest_ckpt127.md`** (website) — repoint `builder atlas --ingest` at `artifacts\atlas\mandelbrot\`, read the record's new gallery-slot fields, pass `level` into the links, re-ingest. Small; run whenever the wallpapers repo is quiet.

## NEXT CHECKPOINT GOAL
**Matt sets it at the top of the checkpoint.** He has said the next mining night is the four legs the ckpt-126 night did not run (OPEN 1); its producing time comes with his launch message.

## OPEN (ordered) — Matt raises each
1. **The next mining night — the four unrun legs of `overnight_mine_ckpt126`**: (a) one depth plan over, in order, the 3,110 newly opened graded places by head score → the julia survivors' great tier → the other survivors' great tier → a second palette pass over the 1,607; (b) a 75-minute `g12` reframe; (c) the sixteen solves before and after. Roster `mode_policy.mined()`, theta-search except direct traps, one random phase, width from free slots. **⚠ The ckpt-126 night was LOST: the prompt carried "do not start while the website prompt runs" and CC ended its turn on "I'll watch for it" with nothing armed — nine idle hours.** Rule → fractal-operating.
2. **Every mining night is composed fresh with Matt.** Arms with a reading: graded places (44.6% great), julia survivors (15–19% great), reframe (140 productive / 30 min); arms without one since the manifest fix: aimed recolour, dear/angle modes at held places.
3. **`rotation` runs must record their tone curve** (wallpapers; `stamps.for_rows` + `SEQUENCE_STORES`), so the 472 seats — and 28 of the atlas's 53 seated dots — open as shipped. Matt: this checkpoint.
4. **A continuous boundary sampler for the parameter planes (Matt: some future checkpoint).** Still the only route to a location that does not already exist. → `preserve\julia_supply.md`.
5. **The decode cache — a storage decision for Matt** (~33 GB hot; Matt: not yet).
6. **`pictures/` in the ten `runs` legs.** 5.37 GiB. Matt: leave. ⚠ Destructive; attended only.
7. **Website — the section-by-section review pass** (Matt brings a section's review doc). Per-page status → `docs/page-review.md`. The atlas's other planes (d=3–5, phoenix) have placeholder plates and empty dot rows; their marks are `curate atlas --plane` runs whenever wanted. `wallpapers-three-bands` names three recipe keys the ledger no longer holds — the only `builder check` red; CC may re-pick.
8. **Whether a second published stamp gets a recipe file**, and whether `data/palette_choice/rows/` belongs in a clone (Matt: leave it entirely).

Parked → `preserve\parked.md`.

## STATUS / KNOWN REDS
⚠ Website `builder check`: `wallpapers-three-bands` (three dead ledger keys). Nothing else red. ⚠ Three orphaned `multiprocessing` workers from 2026-09-15 17:45 were found running with no parent on 2026-09-16 and left alone — Matt's box to clean.

## RULINGS THIS ERA
→ the docs themselves and the in-repo promotions: `curation/LEGS.md`, `curation/README.md`, `curation/GALLERY.md`, `curation/atlas/README.md`, `supply/README.md`, website `CLAUDE.md`, `explorer/README.md`, `atlas/README.md`, `preserve\atlas_design.md`.

## KEEP LIST
Drive `prompts\`: KEEP `atlas_ingest_ckpt127.md`; **wipe everything else**. `reports\`: **wipe everything**.

Wallpapers `scratch/`: KEEP `place_radius_sheet/`, `retired_tentative/` and `preclose_ckpt125/off_list_stamps.txt`; **WIPE everything else** (the atlas scratch folders are already gone). Website `scratch/`: unchanged. Website untracked (do NOT clean): `assets/images/galleries/seated-candidates/`, `explorer/palettes.bin`, `explorer/palettes-swatch.png` — the staging rule's files, listed in `.git/info/exclude`.

## OWED
The queued prompt above; OPEN 3 when Matt raises it.

## SCRATCH/ARTIFACT FLAGS
**★ THE STANDING KEEP ROSTER LIVES IN THE REPO — `src/fractal_wallpapers/README.md §The standing keep roster`.** ⚠ `.leveled/` directories are sweepable → `preserve\leveled_identity.md`. ⚠ `orphans` lists pre-existing unmerged legs and a dated orphan verdict goes stale in hours. `artifacts/atlas/` is untracked artifact output like the rest of `artifacts/`. Per-checkpoint: `artifacts/curation/depth/*/fields` grows ~226 MB a leg. ⚠ CRLF drift is real; `git ls-files --eol`. ARCHIVED (RESTORE before reuse): unchanged from ckpt 106.

## PARKED / SETTLED
→ `preserve\INDEX.md`, which lists every file. Never re-list them here.
