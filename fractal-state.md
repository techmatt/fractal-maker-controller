# fractal-state — checkpoint 124 (2026-09-13)

## Where we are
Three phases, each depending strictly on the one before → fractal-discovery. Matt iterates from pictures, not counts; phase 3 is his eye on the final seating. **NO PUBLISHING OF ANY KIND until Matt raises it — never ask, never list it.**

**★ THE FINAL GALLERY SHIPS AT n=1000, AND EVERY THEMED COLLECTION SHIPS AT n=200 (Matt, 2026-09-13).** The seat count is **not** a knob to trade against quality: pick thresholds to FILL first, then lift quality by aimed mining. n=2000 is not the direction; making n=1000 better is. "Better" means true quality, NOT maximizing `p_fine`.

**★ THE REMAINING HORIZON IS ABOUT 100 MORE MINING HOURS (Matt, 2026-09-12), NOT 10,000.** The multiplier on what is banked is ×2.76. The 10,000-hour frame stays as the way to JUDGE a product choice (→ fractal-operating) and is not a storage projection. **Records-only picture retention is not needed at this scale** — about 135 GB with every picture kept against 1.46 TiB free. → `preserve\retention_design.md`.

**★ THE BAR: `DEFAULT_FINE_BAR = 0.030242` ON `p_ge4`**, under `fine_head = twelve_sheets_drop_high_asymmetric_auc_ge4_more_k3`. The COLUMN stays `p_ge4`. The LEVEL is a **matched constant, not a discovered one**. **★ ⚠ A BAR IS UNREADABLE WITHOUT ITS HEAD** — two runs of ONE recipe on ONE corpus derived **0.022689 and 0.083975** at the same matched fraction, a factor of 3.7. Never carry a level across a fit. ⚠ `solve.Q4_BAR = 0.50` is the RENDER judge's constant. ⚠ There is no CLI spelling for the unbarred population: `--fine-bar 0` still excludes every unread row; `fine_bar=None` in process is the only way back. ⚠ `curate growth` and `curate solve k-sweep` inherit the bar. Provenance → `models/gallery_grade/README.md §Adopted 2026-09-10`.

**★ `p_fine`, `p_coarse` AND THE QUALITY BARS ARE ALL OPERATING WELL — EVERY TASK THAT WOULD ALTER THEM IS CLOSED (Matt, 2026-09-12).** Closed on his word: the `p_fine` inconsistency plan, the asymmetric-cost trade curve, the coarse-4 question, the labelling-protocol drift item. **He re-raises if it is worth doing; never re-open any of it unprompted.** The human veto and the on-demand grade-1 escape count stay parked.

**★ A THEMED PASS RELAXES THE BAR INSIDE ITS OWN CELL (Matt, 2026-09-11; shipped).** `solve.themed_fine_bar` = the lower of the shipped `fine_bar` and the `p_fine` of the **4n-th** best candidate among rows dominant in the cell, **floored at 0.01**. **If the cell cannot fill even at the floor the gallery ships SMALL — there is no padding branch.** On the manifest as `config.theme_bar`, with **`bar_from`** naming which branch fired. → `curation/GALLERY.md`.

**★ THE CENSUS AT n=200 (2026-09-12) — 35 OF 48 CELLS RELAX.** 13 `shipped`, 6 `reachable`, 22 `floor_below`, 7 `floor_unreachable`. Four cannot fill 200 at any bar: `dark_vivid_lime` 79, `light_vivid_lime` 100, `light_vivid_teal` 191, `dark_muted_lime` 192. Above-bar stock spans **55 to 1,925**. `n` sets the bar through `4n`. Table → `curation/GALLERY.md`.

**★ A THIN CELL IS STOCK-BOUND, NOT CARRIER-BOUND (corrected 2026-09-13).** 942 of 942 drawable maps carry a carrier row; `dark_vivid_lime` is offered **42 maps at `CELL_LEAD`** against `CANDIDATES` 32, 19 groups above the bar. **Buy rows IN the cell, not maps to aim with.**

**★ THE PALETTE GROUP CAP IS `0.075·n` THEMED, `0.025·n` GENERAL (Matt, 2026-09-12).** ⚠ It does nothing for a cell that ships small — computed against requested `n`, not seats filled.

**★ `TAU` IS CLOSED ON THE THEMED PATH (measured 2026-09-12).** It would cost about a **third of the seats**: `Twins` refuses sequentially and inside one colour cell the metric reads hue rather than repetition. **The group cap plus the geometry-only `Places` rule is what that path carries.**

**★ A GALLERY PAGE IS PRESENTED STRATIFIED, NOT IN QUALITY ORDER (Matt, 2026-09-12).** `curation/page_order.py`, derived at page build, readout `curate solve browse <stamp> --spacing`. No seat, record, ID or digest moves. Attribute spacing carries the guarantee; embedding distance is secondary; `p_ge4` seeds and breaks ties. ⚠ **A repeat is priced by its excess over what a run CANNOT avoid holding, at the reach's scale as well as the window's** — without that allowance the adjacency term hoards. ⚠ **A monotone decile profile would mean the page is still in quality order** and is the wrong check.

**★ HOLDING THE ADMITTED FRACTION IS NOT RAISING THE BAR.**

**★ THE `p_fine` COLUMN IS NOT IDENTIFIED, AND AVERAGING IS THE LEVER.** Seed-to-seed admitted-set churn 0.750; replicate churn 0.554; churn falls as `0.108 + 0.657/√k` out to k=8 with no knee. Average on the PROBABILITY scale, one vote per seed. ⚠ Buys reproducibility against SEEDS, not kernels. → `preserve\gallery_grade_stability.md`.

**★ ⚠ A BEFORE/AFTER ACROSS A REFIT NEEDS A SAME-RECIPE REPLICATE AS CONTROL.**

**★ MATT REOPENED K HIMSELF AND SET IT; CLAUDE STILL NEVER PROPOSES REOPENING IT.**

**★ ⚠ THE ALLOWANCE COUNTS MEMBERSHIPS, NOT SEATS.** ~1.802 a seat at K=2, ~2.118 at K=3.

**★ A `cell_floor:` STAMP SAYS WHICH LEG PLACED A SEAT, NOT THAT THE FLOOR BOUGHT IT.**

**★ WHAT HOLDS A THIN COLOUR DOWN IS NOT THE CEILING.** `location` and `the_leg_had_no_seat_left` refuse where `cell_allowance` used to.

**★ GUARD RULINGS (Matt, 2026-09-10) — LOOSENING ONLY, AND NOTHING WAS LOOSENED.** Mode floors are as low as he will take them; the family distribution is fine; the spiral cap STAYS AT 0.10; the per-cell floor stays at 20. ⚠ A delta page pairs departures with arrivals BY THE FREED SLOT.

**★ ⚠ THE SOLVER IS NOT AT ITS OPTIMUM** — the seed-plus-1-swap walk leaves at least 1.4 of sum on the table at n=1000. **A shadow price is not askable of this solver.**

**★ THE COLOUR FLOOR DOES NOT DRAG IN BAD PICTURES (measured, ckpt 119).** **★ `PRESELECT_RADIUS` STAYS AT 0.02 (Matt, ckpt 118).**

**★ THE HUMAN VETO IS AGREED IN PRINCIPLE AND DELIBERATELY NOT SHIPPED (Matt, 2026-09-10).** **The escape count stays ON DEMAND.**

**★ ASYMMETRIC COST (Matt, 2026-09-10): KEEPING LOW-GRADED PICTURES LOW MATTERS MORE THAN KEEPING HIGH-GRADED PICTURES HIGH.** The shipped arm carries a 2× negative weighting.

**★ THE `p_fine` SEATING IS THE WAY; `rank_key` IS DEPRECATED AS AN OFFER AND NOTHING MORE.** Why it is not retirable → fractal-corpus. **★ `--forced` IS STAGED AND STAYS STAGED INDEFINITELY (Matt, ckpt 119).**

**★ THE FOLD MERGES INSTEAD OF DELETING, AND IT BOUGHT 71 OF 1,000 SEATS.** 6,683 places into 5,509 clusters. ⚠ No transitivity. **It picks its survivor on the seating key**, stacked and never mixed.

**★ THE GALLERY-GRADE FATE PAGE IS GALLERY-GRADE ONLY**; ⚠ its readings span two adoptions. **★ ⚠ THE `gap` COLUMN IS NOT A MARGIN** — it reads `p_fine Δ`. **A FATE QUESTION NEEDS `--explain-keys`.**

**★ THERE IS NO HONEST SCORE COLUMN OVER THAT POPULATION.** Every one of the 1,000 seats carries a manual verdict and the store is the head's own training material. **Matt's eye is the only independent read of a seating.**

**★ A RE-RENDER INVALIDATES EVERY READING TAKEN OFF THE PICTURE, NOT ONLY THE SCORE.** `recolour --keys` is the door and is idempotent.

**★ AT n=1000 THE GALLERY IS SATURATED.** Mining buys option value for a later re-solve, and quality inside themes.

**★ GROUPS ARE PALETTE GROUPS AND MINING CANNOT MOVE THEM.** A new group needs a new MAP. ⚠ A palette VARIANT is not a new group; `group_of` derives a variant's group from its base.

**★ `p_fine` COVERAGE IS CHECKABLE BEFORE A SOLVE.** ⚠ **`pool_scores.jsonl` is one-shot**: above-bar rows merged after the last `score-pool` are unseatable. **Mine → merge → score-pool → solve.** Nothing enforces it. ⚠ `score-pool` writes `p_fine` only above the render bar.

**★ A `score-pool` REFRESH MOVES MEMBERSHIP, NOT READINGS.** Of 38,813 rows in both columns, 13 moved, by about 1e-7.

**★ ALL THIRTEEN ACCEPTED MODES SEAT AT n=1000.** `ceiling.TAU = 0.034281`, `TWINS = 2`.

**⚠ SEATS-CHANGED IS NOT A MEASURE OF POOL CHANGE**, and **★ THE SEATING AMPLIFIES THE COLUMN**.

**★ ⚠ WEIGH A MEASUREMENT AGAINST THE COST OF THE ACTION IT DECIDES, NOT AGAINST HOW INFORMATIVE IT IS.** When the human input is cheap and the population well-defined, just do it.

**★ ⚠ A SMALL SMOKE MISPRICES A LEG TWICE OVER, IN OPPOSITE DIRECTIONS.** Price a leg off an OBSERVED leg. ⚠ **A pilot's winners do not survive n.** ⚠ **A price carried from `MEASUREMENTS.md` can be an order out if the panel differs.** Pilot; do not carry.

## ROTATION — ERA CLOSED
**★ THE FORWARD DRAW IS STANDING POLICY (Matt, 2026-09-11): every candidate is phase 0 plus four random rotations, keep the best by `p_fine`, repeat fixed at 1.** Every loser's phase and both columns are recorded. **★ ROTATION IS EXCHANGEABLE WITH PHASE 0 — NO PHASE IS SPECIAL.** ⚠ The store arm's apparent near-phase advantage is SELECTION. **★ BOTH HALVES OF THE STORE ARE ROTATED AND THE OWED ARM IS FINISHED** (`owed_ckpt122`, `rows_remaining: 0`, ledger 383,309). ⚠ `sweep.remove` is a SECOND ledger-deleting transaction. **★ MATT RULED THE DECIDED-ROW MARK IS NOT BUILT (2026-09-13)** — the backlog only regrows if forward mining stops searching at draw time, and it does search. **Do not re-propose the mark.** **★ NO LEDGER ROW IS MISFILED.** **★ A LEG STATES ITS RESOLVED SHARES AND ROSTER BEFORE PLANNING** — the defect was the silence. ⚠ **`--budget` both sizes a plan and sets its deadline**; **`--from-block` cannot resume a wholly-ranked leg** — re-run with no index; `depth.SHARES` defaults `near_band` to 0.25. **★ SWEEPING A LEG NO LONGER LEAVES IT MERGEABLE.** Full readings → `curation/LEGS.md`, `curation/MEASUREMENTS.md`.

## THE PALETTE AXIS — PARKED, EXCEPT PHASE
**★ MATT PARKED PALETTE REPLICATION ENTIRELY (2026-09-12).** This supersedes the earlier "repetition is a production axis" ruling. **All ROTATION work is kept.** `data/repeat_ab/` is a declared, empty attribute store; its code and tests stay by Matt's ruling. ⚠ `labeling/server.py` has **no write path at all** — an unexported sitting evaporates when the tab closes. ⚠ **`p_fine` is a CANDIDATE-geometry column** — re-scoring at label geometry loses agreement, .768 → .714.

**★ NOTHING IS PHASE-FLAT EXCEPT THE FOUR DIRECT TRAPS (measured 2026-09-13).** 0 of 180 non-trap cells byte-identical, smallest mean Oklab ΔE 0.056, 98–99% of the frame past a JND in all fifteen modes, and the ranking does not separate. **There is no mode to stop spending phase draws on.** ⚠ The spread inside a mode is the MAP'S KIND (folded 0.305 against cyclic 0.148). ⚠ **The dose is not monotone.** ⚠ Untested: a place with a large interior — a PLACE question, not a mode question. Table → `curation/MEASUREMENTS.md`; mechanics → fractal-engine.

## MODES AND COLOUR
**★ `tia` AND `stripe` WERE NEVER PAUSED IN THE TREE (2026-09-12).** Each is 14.4% of the ledger and 22–23% of everything above the fine bar, against 5.0% and 4.1% of human labels. **They are thin in LABELS, not in supply.** Matt: continue mining them.

**★ THE `direct_trap_multiply` SWEEP PROPOSES NO ROSTER CHANGE (2026-09-12).** Nothing outside the shipped cells beats `@opacity=0.6`. ⚠ **The promising axis is the dear one.** The both-knobs corner stays retired.

**★ THE ORANGE-ON-BLUE SLICE IS WHY THIS ERA HAPPENED (Matt, 2026-09-10).** The gate that answers it is **page order plus the group cap**, not `TAU`.

## SOURCING
**★ THE BAND ARMS WERE EMPTIED BY ADMISSION, NOT ROSTER.** **★ ⚠ THE 1,636 OPENED-BUT-UNADMITTED LOCATIONS ARE A SCORING BACKLOG, NOT AN EMBEDDING ONE** — 1,607 have no supply-sidecar row; `curate embed` priced at zero. **`curate score` owes the work.** **The band is not blocked: a fresh `curate depth near-places` cut gets 432 places / 1,253 free slots.** ⚠ A band manifest needs `--modes smooth stripe tia`.

**★ 8,103 ADMITTED LOCATIONS HAVE NEVER BEEN OPENED** (pre-ckpt-123 reading), 4,482 at the frame they already carry.

**★ THE CKPT-123 JULIA ERA — SUPPLY IS ROOT-BOUND.** The overnight harvest added **+12,579 admitted locations, 3,106 of them q4, +64 distinct `c`**, then **ran out of roots at 311 of 405 active minutes**: 1,401 roots was the entire standing supply of the seven partitions named. Depth is spent, roots are the constraint. Mechanism, the channel map, the degree split, the expansion budget and the incidents → **`preserve\julia_supply.md`**. Phoenix, and the archive's closed-form sampler → **`preserve\phoenix_sampling.md`**.

## RECORDS
**★ ⚠ A RECORD IS DISCARDED BY DEFAULT (Matt, 2026-09-13) — AND THAT RULE LIVES IN `CLAUDE.md`.** **Keeping needs a reason; discarding does not.** Keep list: the seven `tentative.PUBLISHED` stamps, anything a published or upcoming figure cites, and **`20260911T022330Z`**, which is UNPUBLISHED and must be named explicitly.

**★ ⚠ A RECORD IS TWO DIRECTORIES** — `tentative/<stamp>/` and `solve/<manifest.solve.name>/`. **Only the tentative half holds prune protection.** ⚠ **Publication, durability and retention are three questions, not two.**

**`20260911T022330Z` — the official n=1000 record under the adopted head, UNPUBLISHED** (1000/1000, shortfall 0, worst 1.041483, sum 1451.098395). ⚠ It predates several legs and merges. The site cites six stamps across 26 figures and is not to be re-based. Store stands at **35 stamps, 7 published, 28 unpublished**.

**★ THE TWO UNDECLARED HARD-DEPENDENCY STAMPS ARE ON THE STANDING KEEP ROSTER.** `20260906T133559Z` backs the site's `modes-gallery` curvature panel; `20260906T133236Z` is the draw behind all three batches of the shipped label corpus and the `K = 2` arm.

**★ A RECORD'S OWN SEAT COUNT IS NOT WHAT DELETING IT RELEASES.** **Measure `protected_keys()` either side; never sum.**

## THE RECORD'S OWN PROSE
**★ A RECORD CARRIES ITS PROSE WHOLE, AND THE SOURCE CARRIES ONE COPY.** `SCHEMA_NOTES` beside each `SCHEMA`, read at write time. **No version integer, no bump rule** — the only real defect is a note that was **wrong when written**, and those go on a dated *Notes corrected after they shipped* list. ⚠ `NOTES_AT_LEAST` moving DOWN is named at the constant.

**★ `held_out_is` UNDERCOUNTED, AND THE RECORDS WERE LEFT ALONE.** Three choices land on the stopping slice; `_fit_drop_high_asymmetric` has no early stop at all. **21 tracked `metrics.json` and all three tracked bars ship the old sentence**; the figures stand.

## IN FLIGHT ACROSS THIS BOUNDARY
Nothing.

## QUEUED IN DRIVE `prompts\`
Nothing.

## NEXT CHECKPOINT GOAL
**Matt sets it at the top of the checkpoint.** Nothing is scheduled here. Direction as of the boundary: **mining** (Matt, 2026-09-13).

## OPEN (ordered) — Matt raises each
1. **Mining.** The stated direction out of ckpt 123. Cut fresh `near-places` manifests rather than reusing a decayed one. ⚠ No valid index resume for the ranked arm — re-run with no index.
2. **The 8,103 never-opened admitted locations** — the largest untouched supply lever, and the population the ckpt-123 contact sheet was drawn from.
3. **Aimed mining for quality at n=200.** The target is the **35 cells that relax**. Buy rows IN the cell.
4. **`curate score` over the 1,607 unscored opened locations**, which raises the near band's ceiling.
5. **Themed collections at n=200.** The path solves clean and the pages order themselves; what is untouched is the product.
6. **A continuous boundary sampler for the parameter planes (Matt: build it some future checkpoint).** `nucleus_grid` is a finite enumerated pool that empties permanently; `viewport_sampler` is `PINNED_PLANES` only. Every plane location it produced would also be a candidate twin parameter. → `preserve\julia_supply.md`, `preserve\phoenix_sampling.md`.
7. **The decode cache — a storage decision for Matt.** Absent, documented as the lever that speeds every arm at once, buys training throughput, costs ~33 GB of hot tier.
8. **A sweep of the solve store against the stamp list** for stranded halves.
9. **The tentative store beyond the keep list** — 35 stamps, governed by the discard default.
10. **A sweep for rulings that govern a LEG but exist only in these docs.**
11. **`pictures/` in the ten `runs` legs.** 5.37 GiB. **Matt: leave for now.** ⚠ Destructive; not for an unattended prompt.
12. **`carriers.jsonl`** at 65.9% of the 1 MiB guard; **`itinerary.jsonl`** at 62% of 786,432.
13. **Website — REOPENED for a section-by-section review pass.** Matt brings a review doc for one section; Claude pushes back on anything wrong or not an improvement; once aligned, Claude writes the prose master and the placement prompt. Per-page status → `docs/page-review.md`.
14. **The reframe channel's cadence.**

Parked → `preserve\parked.md`.

## STATUS / KNOWN REDS
**NO KNOWN REDS.**

## RULINGS THIS ERA
→ `preserve\rulings_method.md §ckpt 122`, plus the domain rulings in the docs themselves and the in-repo promotions: `curation/LEGS.md`, `curation/MEASUREMENTS.md`, `curation/README.md`, `curation/GALLERY.md`, `palettes/README.md`, `supply/README.md`, `models/README.md`, `data/discovery/README.md`.

## KEEP LIST
Drive `prompts\`: **wipe everything** — nothing queued, nothing in flight. `reports\`: **wipe everything**.

Wallpapers `artifacts/sheet/`: `repeat_axis_smooth_render` and `repeat_axis_strange_render` are labelled and ingested; held only until Matt says otherwise.

Wallpapers `scratch/`: KEEP `place_radius_sheet/`; **WIPE everything else**. Website `scratch/`: unchanged.

⚠ **`artifacts/overnight_harvest_ckpt123/` holds the ckpt-123 contact sheet Matt read.** The walk ledger under it is a run record and stays; the contact sheet itself is spent.

## OWED
Nothing beyond the OPEN list.

## SCRATCH/ARTIFACT FLAGS
**★ THE STANDING KEEP ROSTER LIVES IN THE REPO — `src/fractal_wallpapers/README.md §The standing keep roster`.** ⚠ Nothing on it is protected by `orphans`' reference set.

⚠ **`artifacts/render_folds/` DOES NOT EXIST on either tier.** ⚠ **`.leveled/` DIRECTORIES ARE SWEEPABLE** → `preserve\leveled_identity.md`. ⚠ **`orphans` lists pre-existing unmerged legs**, and a dated orphan verdict goes stale in hours.

Per-checkpoint: new records are prune-protected like every record. `artifacts/curation/depth/*/fields` grows at roughly 226 MB a leg and the sweep cannot reach it. ⚠ A pass that dumps fields sweeps its own. ⚠ **CRLF drift is real**; `git ls-files --eol` is the door. ARCHIVED (RESTORE before reuse): unchanged from ckpt 106.

## PARKED / SETTLED
→ `preserve\INDEX.md`, which lists every file. Never re-list them here.
