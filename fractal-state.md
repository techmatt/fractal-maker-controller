# fractal-state — checkpoint 123 (2026-09-13)

## Where we are
Three phases, each depending strictly on the one before → fractal-discovery. Matt iterates from pictures, not counts; phase 3 is his eye on the final seating. **NO PUBLISHING OF ANY KIND until Matt raises it — never ask, never list it.**

**★ THE FINAL GALLERY SHIPS AT n=1000, AND EVERY THEMED COLLECTION SHIPS AT n=200 (Matt, 2026-09-13).** The seat count is **not** a knob to trade against quality: whatever it takes to get quality at 200 is what we do — pick thresholds to FILL first, then lift quality by aimed mining. n=2000 is not the direction; making n=1000 better is. "Better" means true quality, NOT maximizing `p_fine` — maximizing it would restrict the gallery to a tiny subset.

**★ THE REMAINING HORIZON IS ABOUT 100 MORE MINING HOURS (Matt, 2026-09-12), NOT 10,000.** The multiplier on what is already banked is ×2.76. The 10,000-hour frame stays as the way to JUDGE a product choice (→ fractal-operating) and is not a storage projection. **Records-only picture retention is therefore not needed at this scale** — about 135 GB with every picture kept, against 1.46 TiB free. → `preserve\retention_design.md`.

**★ THE BAR: `DEFAULT_FINE_BAR = 0.030242` ON `p_ge4`**, under `fine_head = twelve_sheets_drop_high_asymmetric_auc_ge4_more_k3`. The COLUMN stays `p_ge4`. The LEVEL is a **matched constant, not a discovered one**. **★ ⚠ A BAR IS UNREADABLE WITHOUT ITS HEAD** — two runs of ONE recipe on ONE corpus derived **0.022689 and 0.083975** at the same matched fraction, a factor of 3.7. Never carry a level across a fit. ⚠ `solve.Q4_BAR = 0.50` is the RENDER judge's constant. ⚠ There is no CLI spelling for the unbarred population: `--fine-bar 0` is a bar of zero and still excludes every unread row; `fine_bar=None` in process is the only way back. ⚠ `curate growth` and `curate solve k-sweep` inherit the bar. Provenance → `models/gallery_grade/README.md §Adopted 2026-09-10`.

**★ `p_fine`, `p_coarse` AND THE QUALITY BARS ARE ALL OPERATING WELL — EVERY TASK THAT WOULD ALTER THEM IS CLOSED (Matt, 2026-09-12).** Closed on his word: the `p_fine` inconsistency plan (750 seated-row labels → retrain → outlier revision → retrain from scratch), the asymmetric-cost escape-rate / grade-4-loss trade curve, the coarse-4 question, and the labelling-protocol drift item. **He re-raises if it is worth doing; never re-open any of it unprompted.** The human veto and the on-demand grade-1 escape count stay parked exactly as they were.

**★ A THEMED PASS RELAXES THE BAR INSIDE ITS OWN CELL (Matt, 2026-09-11; shipped).** `solve.themed_fine_bar` = the lower of the shipped `fine_bar` and the `p_fine` of the **4n-th** best candidate among rows dominant in the cell, **floored at 0.01**; a rich cell keeps the shipped bar, a thin cell relaxes. **If the cell cannot fill even at the floor the gallery ships SMALL — there is no padding branch.** On the manifest as `config.theme_bar`, with **`bar_from`** naming which of the four branches fired. → `curation/GALLERY.md`.

**★ THE CENSUS AT n=200 (2026-09-12) — 35 OF 48 CELLS RELAX.** 13 `shipped`, 6 `reachable`, 22 `floor_below`, 7 `floor_unreachable`. Four cannot fill 200 at any bar: `dark_vivid_lime` 79, `light_vivid_lime` 100, `light_vivid_teal` 191, `dark_muted_lime` 192. Above-bar stock across cells spans **55 to 1,925**. `n` sets the bar through `4n`, so the seat count is what decides quality — the floor only decides how far a pass falls once `4n` has already failed. Table → `curation/GALLERY.md`.

**★ A THIN CELL IS STOCK-BOUND, NOT CARRIER-BOUND (corrected 2026-09-13).** 942 of 942 drawable maps carry a carrier row, and `dark_vivid_lime` is still offered **42 maps at `CELL_LEAD`** (above `CANDIDATES` 32) with 19 groups above the bar. **The mining instruction is to buy rows IN the cell, not maps to aim with.**

**★ THE PALETTE GROUP CAP IS `0.075·n` THEMED, `0.025·n` GENERAL (Matt, 2026-09-12).** The old themed `0.05·n` bound at 10 of 10 in four cells of five and refused 100 rows in `dark_vivid_green`, which finished 165/200. ⚠ It does nothing for a cell that ships small — the cap is computed against requested `n`, not seats filled.

**★ `TAU` IS CLOSED ON THE THEMED PATH (measured 2026-09-12).** It would cost about a **third of the seats** in both cells tested, because `Twins` refuses sequentially and inside one colour cell the metric reads hue rather than repetition. The pairwise share is the wrong number to quote. **The group cap plus the geometry-only `Places` rule is what that path carries.** → `curation/GALLERY.md`.

**★ A GALLERY PAGE IS PRESENTED STRATIFIED, NOT IN QUALITY ORDER (Matt, 2026-09-12).** `curation/page_order.py`, derived at page build, readout `curate solve browse <stamp> --spacing`. No seat, record, ID or digest moves; an existing record gets it on its next `browse`. Attribute spacing (`spiral`, mode, family, `cell`) carries the guarantee; embedding distance is secondary; `p_ge4` seeds the page and breaks ties. ⚠ **A repeat is priced by its excess over what a run CANNOT avoid holding, at the reach's scale as well as the window's** — written without that allowance the adjacency term **hoards**, draining the minority first and stacking the majority at the end, which is the tail clump the module exists to remove. ⚠ A page ordered for spread flattens the quality profile by construction; **a monotone decile profile would mean the page is still in quality order** and is the wrong check.

**★ HOLDING THE ADMITTED FRACTION IS NOT RAISING THE BAR.** The gate sits where it sat; the benefit is the ORDER inside the admitted pool, and the n=1000 cutoff does the selecting.

**★ THE `p_fine` COLUMN IS NOT IDENTIFIED, AND AVERAGING IS THE LEVER.** Seed-to-seed admitted-set churn 0.750; replicate churn with nothing varied 0.554; churn falls as `0.108 + 0.657/√k` out to k=8 with no knee. Average on the PROBABILITY scale, one vote per seed. ⚠ Averaging buys reproducibility against SEEDS, not kernels. → `preserve\gallery_grade_stability.md`.

**★ ⚠ A BEFORE/AFTER ACROSS A REFIT NEEDS A SAME-RECIPE REPLICATE AS CONTROL.**

**★ MATT REOPENED K HIMSELF AND SET IT; CLAUDE STILL NEVER PROPOSES REOPENING IT.** Not as a question, not as a closeout item, however strong the measurement pointing at it.

**★ ⚠ THE ALLOWANCE COUNTS MEMBERSHIPS, NOT SEATS.** ~1.802 memberships a seat at K=2 and ~2.118 at K=3. Convert a proposed K into membership units before arguing it.

**★ A `cell_floor:` STAMP SAYS WHICH LEG PLACED A SEAT, NOT THAT THE FLOOR BOUGHT IT.**

**★ WHAT HOLDS A THIN COLOUR DOWN IS NOT THE CEILING.** `location` and `the_leg_had_no_seat_left` refuse where `cell_allowance` used to. Mining the thin cells remains the instruction.

**★ GUARD RULINGS (Matt, 2026-09-10) — LOOSENING ONLY, AND NOTHING WAS LOOSENED.** Mode floors are as low as he will take them; the family distribution is fine; the spiral cap STAYS AT 0.10; the per-cell floor stays at 20. He judges a constant by what ENTERS and LEAVES the seating, on per-constant delta pages. ⚠ A delta page pairs departures with arrivals BY THE FREED SLOT.

**★ ⚠ THE SOLVER IS NOT AT ITS OPTIMUM**, which puts a noise floor under every objective comparison — the seed-plus-1-swap walk leaves at least 1.4 of sum on the table at n=1000. **A shadow price is not askable of this solver.**

**★ THE COLOUR FLOOR DOES NOT DRAG IN BAD PICTURES (measured, ckpt 119).**

**★ `PRESELECT_RADIUS` STAYS AT 0.02 (Matt, ckpt 118).**

**★ THE HUMAN VETO IS AGREED IN PRINCIPLE AND DELIBERATELY NOT SHIPPED (Matt, 2026-09-10).** A graded-1 seat is the end-to-end signal that something upstream is broken. **The escape count stays ON DEMAND.**

**★ ASYMMETRIC COST (Matt, 2026-09-10): KEEPING LOW-GRADED PICTURES LOW MATTERS MORE THAN KEEPING HIGH-GRADED PICTURES HIGH.** The shipped arm carries a 2× negative weighting.

**★ THE `p_fine` SEATING IS THE WAY; `rank_key` IS DEPRECATED AS AN OFFER AND NOTHING MORE.** Why it is not retirable → fractal-corpus.

**★ `--forced` IS STAGED AND STAYS STAGED INDEFINITELY (Matt, ckpt 119).**

**★ THE FOLD MERGES INSTEAD OF DELETING, AND IT BOUGHT 71 OF 1,000 SEATS.** 6,683 places fold into 5,509 clusters. ⚠ No transitivity. **★ THE FOLD PICKS ITS SURVIVOR ON THE SEATING KEY**, stacked and never mixed.

**★ THE GALLERY-GRADE FATE PAGE IS GALLERY-GRADE ONLY**, and ⚠ its readings span two adoptions — no two are comparable. **★ ⚠ THE `gap` COLUMN ON A FATE CARD IS NOT A MARGIN**; it reads `p_fine Δ`. **★ A FATE QUESTION NEEDS A RECORD TAKEN WITH `--explain-keys`.**

**★ THERE IS NO HONEST SCORE COLUMN OVER THAT POPULATION.** Every one of the 1,000 seats carries a manual verdict and the store is the head's own training material. **Matt's eye is the only independent read of a seating.**

**★ A RE-RENDER INVALIDATES EVERY READING TAKEN OFF THE PICTURE, NOT ONLY THE SCORE.** `recolour --keys` is the door and is idempotent.

**★ AT n=1000 THE GALLERY IS SATURATED.** Mining buys option value for a later re-solve, and quality inside themes.

**★ GROUPS ARE PALETTE GROUPS AND MINING CANNOT MOVE THEM.** A new group needs a new MAP. ⚠ **A palette VARIANT is not a new group — all variants of a map count toward their base map's group cap (Matt, 2026-09-10)**, and `group_of` derives a variant's group from its base.

**★ `p_fine` COVERAGE IS CHECKABLE BEFORE A SOLVE.** ⚠ **`pool_scores.jsonl` is one-shot**: above-bar rows merged after the last `score-pool` are unseatable. **Mine → merge → score-pool → solve.** Nothing enforces that ordering. ⚠ `score-pool` writes `p_fine` **only above the render bar**; the split is a re-read, never a figure to carry.

**★ A `score-pool` REFRESH MOVES MEMBERSHIP, NOT READINGS.** Of 38,813 rows present in both columns, **13 moved at all, by about 1e-7**. A reading that shifts more than float noise across a refresh is a re-render rather than a refresh, and that is checkable.

**★ ALL THIRTEEN ACCEPTED MODES SEAT AT n=1000.** `ceiling.TAU = 0.034281`, `TWINS = 2`.

**⚠ SEATS-CHANGED IS NOT A MEASURE OF POOL CHANGE**, and **★ THE SEATING AMPLIFIES THE COLUMN**.

**★ ⚠ WEIGH A MEASUREMENT AGAINST THE COST OF THE ACTION IT DECIDES, NOT AGAINST HOW INFORMATIVE IT IS.** When the human input is cheap and the population is well-defined, just do it.

**★ ⚠ A SMALL SMOKE MISPRICES A LEG TWICE OVER, IN OPPOSITE DIRECTIONS.** A 40-group smoke priced the owed arm at 18.105 engine-seconds a row against the leg's **24.296**, and read concurrency 2.61 against the leg's **2.945**. Price a leg off an OBSERVED leg. ⚠ Concurrency itself held 2.945–2.989 across three legs; that is not where estimates go wrong. ⚠ **A pilot's winners do not survive n.** ⚠ **A price carried from `MEASUREMENTS.md` can be an order out if the panel differs** — a phase pass staged at 40 minutes on carried prices came in at **108 seconds**, because those prices were measured at a 22,794 cap and the panel was the shallow half of `gallery3`. Pilot; do not carry.

## ROTATION — ERA CLOSED

**★ THE FORWARD DRAW IS STANDING POLICY (Matt, 2026-09-11): every candidate is phase 0 plus four random rotations, keep the best by `p_fine`, repeat fixed at 1.** Every loser's phase and both columns are recorded — a store that keeps only the argmax is the selected-at-one-phase bias one level up. **★ ROTATION IS EXCHANGEABLE WITH PHASE 0 — NO PHASE IS SPECIAL.** ⚠ The store arm's apparent near-phase advantage is SELECTION, not signal. **★ WHAT BEST-OF-FIVE BUYS IS OPTIONALITY, AND THE ARGUMENT IS PRICE.** Full readings → `curation/LEGS.md`, `curation/MEASUREMENTS.md`.

**★ BOTH HALVES OF THE STORE ARE ROTATED AND THE OWED ARM IS FINISHED.** `owed_ckpt122`: 1,464 rows, 6,892 rotations, `rows_remaining: 0`; ledger **383,309**. **Five protections are honoured, not two.** ⚠ `sweep.remove` is a SECOND ledger-deleting transaction and records its loss to the ratchet exactly as a prune does.

**★ ⚠ `rows_remaining` IS NOT THE NEXT LEG'S SIZE AND DOES NOT RESUME.** Only an ADOPTED row falls out of the next plan — it carries a non-zero `palette.phase` and `refusal_of` refuses it `already_rotated`. A `kept` or `held` row carries no mark and is redrawn whole: `owed_ckpt122` re-planned to 1,464 against 237 recorded, **1,223 already decided with zero adoptions among them — 2h51m of a 3h25m leg**. **★ MATT RULED THE DECIDED-ROW MARK IS NOT BUILT (2026-09-13)**: a `kept` verdict means phase 0 won and is indistinguishable on the row from never having been searched, but the backlog only regrows if forward mining fails to search at draw time — and it does search. The 1,223 were legacy stock. **Do not re-propose the mark; the condition to protect is that forward mining keeps doing the search.**

**★ NO LEDGER ROW IS MISFILED.** The 43 "misfiled" rows were a REBUILD failure; `Incumbent.pass_knobs` carries the difference from the plain pass forward onto every rotation.

**★ A LEG STATES ITS RESOLVED SHARES AND ROSTER BEFORE PLANNING.** The merge over `depth.SHARES` is unchanged deliberately — **the defect was the silence**.

**★ ⚠ `--budget` BOTH SIZES A PLAN AND SETS ITS DEADLINE.** ⚠ A shot whose CONTROL never merged returns as a best-of-**four** read against the same control. ⚠ **`--from-block` CANNOT RESUME A WHOLLY-RANKED LEG** — the plan is a deterministic function of the POOL and the pool shrinks by what the last leg merged; the honest resume is to re-run with no index. `refuse_unreachable_resume` runs before the population read; a resume now also names the pool it was planned against. ⚠ `depth.SHARES` defaults `near_band` to 0.25, so a leg that does not spell `--shares` puts a quarter of its clock there. Detail → `curation/LEGS.md`.

**★ SWEEPING A LEG NO LONGER LEAVES IT MERGEABLE.** `orphans --apply` declares the sweep in the leg's own directory and both merge paths refuse a leg carrying it.

## THE PALETTE AXIS — PARKED, EXCEPT PHASE

**★ MATT PARKED PALETTE REPLICATION ENTIRELY (2026-09-12).** Some repeats are better, but the benefit is too scarce and confined to a small part of one mode. **This supersedes the earlier "repetition is a production axis" ruling. All ROTATION work is kept.** `data/repeat_ab/` is a declared, empty attribute store; its code and tests stay by Matt's ruling. ⚠ `labeling/server.py` has **no write path at all**, so an unexported sitting evaporates when the tab closes. What the labels said, before it was parked → `curation/MEASUREMENTS.md`. ⚠ **`p_fine` is a CANDIDATE-geometry column** — re-scoring it at label geometry LOSES agreement, .768 → .714.

**★ NOTHING IS PHASE-FLAT EXCEPT THE FOUR DIRECT TRAPS (measured 2026-09-13).** 0 of 180 non-trap cells byte-identical, smallest mean Oklab ΔE **0.056** against a 0.02 threshold, 98–99% of the frame past a JND in every one of the fifteen modes — and the ranking of the fifteen does not separate (1.51× end to end, no gap). **There is no mode to stop spending phase draws on.** ⚠ **The spread inside a mode is the MAP'S KIND**: folded **0.305** against cyclic **0.148**, 2.07×, while place barely registers and coloring kind not at all. ⚠ **The dose is not monotone** — on a folded map a half-turn lands on the ramp's reflection and is the largest change available; on a cyclic map it comes back toward where it started and reads under half a quarter-turn. ⚠ **Untested: a place with a large interior.** `INTERIOR` is hard black and never goes through the map, and this panel read a median exactly-black share ≤ 1.6%; flatness there is consistent with every row above. It is a PLACE question, not a mode question. Table → `curation/MEASUREMENTS.md`; mechanics → fractal-engine.

## MODES AND COLOUR

**★ `tia` AND `stripe` WERE NEVER PAUSED IN THE TREE (2026-09-12).** Both sit at weight 2, neither is in `UNMINED`, no roster names them. Each is **14.4% of the ledger and 22–23% of everything above the fine bar**, against **5.0% and 4.1% of human labels** (`smooth` holds 54.3% on 23.7% of the store). **They are thin in LABELS, not in supply.** Matt: continue mining them.

**★ THE `direct_trap_multiply` SWEEP PROPOSES NO ROSTER CHANGE (2026-09-12).** 6,885 candidates, 13,463 engine-seconds: nothing outside the shipped cells beats `@opacity=0.6`, which is also the cheapest clear on the leg. ⚠ **The promising axis is the dear one.** The both-knobs corner stays retired (Matt's eye, ckpt 117). ⚠ Phoenix's realised share of both planes was **zero**.

**★ THE ORANGE-ON-BLUE SLICE IS WHY THIS ERA HAPPENED (Matt, 2026-09-10).** Filtering the n=1000 seating to hue family orange plus spiral gives 19 seats that read as one palette look. The gate that answers it is **page order plus the group cap**, not `TAU` — see above.

## SOURCING — WHAT THE NEAR BAND ACTUALLY NEEDS

**★ THE BAND ARMS WERE EMPTIED BY ADMISSION, NOT ROSTER.** All three arms of the 2026-09-09 leg stopped on an **empty plan** at 41%, 13% and 33% of their clock while their log truthfully reported every named place holding an affordable candidate. **★ ⚠ THE 1,636 OPENED-BUT-UNADMITTED LOCATIONS ARE A SCORING BACKLOG, NOT AN EMBEDDING ONE** — 1,607 have no supply-sidecar row at all, `embeddings.admitted` reads the sidecar through the junk floor, and `curate embed` priced at **zero** with nothing to do. **`curate score` owes the work and runs first.** ⚠ The 168 places costing all three arms span **ten** partitions, `julia:mandelbrot` only 14 of them. **The band is not blocked: a fresh `curate depth near-places` cut gets 432 places / 1,253 free slots**, ~87.5% of the places — the old manifests had simply decayed.

**★ 8,103 ADMITTED LOCATIONS HAVE NEVER BEEN OPENED**, 4,482 at the frame they already carry. Logged by every population read and never acted on.

## RECORDS

**★ ⚠ A RECORD IS DISCARDED BY DEFAULT (Matt, 2026-09-13) — AND THAT RULE NOW LIVES IN `CLAUDE.md`.** A leg that recorded a gallery to measure something against deletes it once the measurement is taken and says so in its report. **Keeping needs a reason; discarding does not.** Keep list: the seven `tentative.PUBLISHED` stamps, anything a published or upcoming figure cites, and **`20260911T022330Z`** — which is UNPUBLISHED and must be named explicitly or "keep only what Matt names" reads as licence to delete it. Six in-tree sites had said the opposite and were corrected.

**★ ⚠ A RECORD IS TWO DIRECTORIES** — `tentative/<stamp>/` and `solve/<manifest.solve.name>/` — and deleting the stamp takes only the first. **Only the tentative half holds prune protection**, so a stranded solve directory pins nothing and is invisible; one had outlived its record by a day. ⚠ **Publication, durability and retention are three questions, not two**; `protected_keys()` sweeping the whole store whatever `PUBLISHED` says is the REASON discarding is the default, not a counter to it.

**`20260911T022330Z` — the official n=1000 record under the adopted head, UNPUBLISHED** (filled 1000/1000, shortfall 0, worst 1.041483, sum 1451.098395). ⚠ **It predates several legs and merges.** Earlier stamps order on superseded columns and are cited **purely for figure generation**. The site cites six stamps across 26 figures and is not to be re-based. Store stands at **35 stamps, 7 published, 28 unpublished**.

**★ THE TWO UNDECLARED HARD-DEPENDENCY STAMPS ARE NOW ON THE STANDING KEEP ROSTER.** `20260906T133559Z` backs the site's `modes-gallery` curvature panel; `20260906T133236Z` is the draw behind all three batches of the shipped label corpus and the `K = 2` arm of `curation/k_sweep.py`.

**★ A RECORD'S OWN SEAT COUNT IS NOT WHAT DELETING IT RELEASES.** **Measure `protected_keys()` either side; never sum.** ⚠ A solve directory with no tentative record confers no protection and frees nothing.

## THE RECORD'S OWN PROSE

**★ A RECORD CARRIES ITS PROSE WHOLE, AND THE SOURCE CARRIES ONE COPY.** `SCHEMA_NOTES` beside each `SCHEMA`, read by the builder at write time, guarded so every `*_is` key a record writes comes out of it. **No `"schema": 2`, no version integer, no bump rule** — a record carries the note that was true when it was written, so the only real defect is a note that was **wrong when written**. Those go on a dated *Notes corrected after they shipped* list. ⚠ `NOTES_AT_LEAST` moving DOWN is named at the constant when it happens.

**★ `held_out_is` UNDERCOUNTED, AND THE RECORDS WERE LEFT ALONE.** **Three** choices land on the stopping slice, not one — the epoch inside a run, then the arm and the seed `band` picks off the same numbers — and `_fit_drop_high_asymmetric` has **no early stop at all**, so the old "optimistic by one early stop" was false on that path. **21 tracked `metrics.json` and all three tracked bars ship the old sentence**; the figures stand and the caveat over them was too small.

## IN FLIGHT ACROSS THIS BOUNDARY
Nothing.

## QUEUED IN DRIVE `prompts\`
Nothing.

## NEXT CHECKPOINT GOAL
**Matt sets it at the top of the checkpoint.** Nothing is scheduled here.

## OPEN (ordered) — Matt raises each
1. **Continue mining.** Cut fresh `near-places` manifests rather than reusing a decayed one. ⚠ No valid index resume for the ranked arm — re-run with no index.
2. **Aimed mining for quality at n=200.** The target is the **35 cells that relax**, ranked by their `4n`-th best reading, not only the four that ship small. Buy rows IN the cell.
3. **`curate score` over the 1,607 unscored opened locations**, which is what raises the near band's ceiling. Not a precondition for mining.
4. **The 8,103 never-opened admitted locations** — the largest untouched supply lever.
5. **Themed collections at n=200.** The path solves clean and the pages now order themselves; what is untouched is the product.
6. **A sweep of the solve store against the stamp list** for stranded halves left by this checkpoint's deletions.
7. **The tentative store beyond the keep list** — 35 stamps, now governed by the discard default.
8. **A sweep for rulings that govern a LEG but exist only in these docs.** Each one is a place a leg can follow the docs in good faith into the wrong answer; the record-retention default was one.
9. **`pictures/` in the ten `runs` legs.** 5.37 GiB. **Matt: leave for now.** ⚠ Destructive; not for an unattended prompt.
10. **`carriers.jsonl`** at 65.9% of the 1 MiB guard; **`itinerary.jsonl`** at 62% of 786,432.
11. **Website — REOPENED for a section-by-section review pass.** Matt brings a review doc for one section; Claude pushes back on anything wrong or not an improvement; once aligned, Claude writes the prose master and the placement prompt. Per-page status → `docs/page-review.md`, which is the only record — never keep a per-page list here.
12. **The reframe channel's cadence.**

Parked → `preserve\parked.md`.

## STATUS / KNOWN REDS
**NO KNOWN REDS.**

## RULINGS THIS ERA
→ `preserve\rulings_method.md §ckpt 122`, plus the domain rulings in the docs themselves and the in-repo promotions: `curation/LEGS.md`, `curation/MEASUREMENTS.md`, `curation/README.md`, `curation/GALLERY.md`, `palettes/README.md`.

## KEEP LIST
Drive `prompts\`: **wipe everything** — nothing is queued and nothing is in flight. `reports\`: **wipe everything**.

Wallpapers `artifacts/sheet/`: `repeat_axis_smooth_render` and `repeat_axis_strange_render` are **labelled and ingested**, so the reason they were kept is spent; they are held only until Matt says otherwise.

Wallpapers `scratch/`: KEEP `place_radius_sheet/` (it backs the `PRESELECT_RADIUS` ruling); **WIPE everything else**. Website `scratch/`: unchanged.

## OWED
Nothing beyond the OPEN list.

## SCRATCH/ARTIFACT FLAGS
**★ THE STANDING KEEP ROSTER LIVES IN THE REPO — `src/fractal_wallpapers/README.md §The standing keep roster`.** ⚠ Nothing on it is protected by `orphans`' reference set.

⚠ **`artifacts/render_folds/` DOES NOT EXIST on either tier.**

⚠ **`.leveled/` DIRECTORIES ARE SWEEPABLE** — `orphans` reaches them by the name each JPEG would have. → `preserve\leveled_identity.md`.

⚠ **`orphans` lists pre-existing unmerged legs**, and ⚠ **a dated orphan verdict goes stale in hours** — re-read it, never carry it.

Per-checkpoint: new records are prune-protected like every record. `artifacts/curation/depth/*/fields` keeps growing at roughly 226 MB a leg and the sweep cannot reach it. ⚠ A pass that dumps fields sweeps its own — 50 MB of regenerable array a pass was being left under a name nothing read. ⚠ **CRLF drift is real**; `git ls-files --eol` is the door. ARCHIVED (RESTORE before reuse): unchanged from ckpt 106.

## PARKED / SETTLED
→ `preserve\INDEX.md`, which is current and lists all nineteen files. Never re-list them here.
