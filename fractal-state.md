# fractal-state — checkpoint 126 (2026-09-15)

## Where we are
Three phases, each depending strictly on the one before → fractal-discovery. Matt iterates from pictures, not counts; phase 3 is his eye on the final seating.

**★ EVERY COLLECTION HAS A TARGET AND THE TARGETS LIVE IN `curation/targets.py` (2026-09-15).** `TARGETS`, reached by `curate solve run --collection NAME`; `--n` still overrides; a collection with no target REFUSES. The table as it stands: the nine ordinary families at **400**, `green` and `cyan` at **300**, `lime` at **150**, `tia` at **1000**, `smooth` and `stripe` at **800**, `threads` at **400**. Changing one is a one-line edit there and never a number retyped into a prompt.

**★ ⚠ THIS SUPERSEDES "n=1000 AND EVERY THEMED COLLECTION AT n=200, AND THE SEAT COUNT IS NOT A KNOB" (ckpt 125).** The seat count turned out to be the checkpoint's largest quality lever: 1,351 fewer seats lifted **fifteen of sixteen** medians, `tia` unchanged as the control because its target did not move. Mechanism and the `4n` consequence → `curation/GALLERY.md`.

**★ ⚠ GALLERY SIZE IS MATT'S DECISION ALONE.** Never raise it, never queue it as a question, never reason about the tradeoffs of shrinking `n` — he knows them. And **"final gallery quality" is NOT the median**: it is his own judgement over many factors. n=10 would maximise the median and is obviously not what he wants. Never reframe the goal as maximising a summary statistic.

**★ THE PUBLISHED GALLERY IS `20260914T171846Z`**, the eighth `tentative.PUBLISHED` stamp and the one going on the website. **Matt raises any further publishing himself; never ask, never list it.** The viewer is `artifacts/curation/viewer/index.html` (unstamped, follows the newest published record); the old `scratch/deterministic_refit_20260910/page/` path forwards. **32 of its 1,000 seats are `itinerary` and 47 of its recipes are; all 47 modulate `smooth` and no other base appears** — the 15-row gap is the degenerate modulates carrying `texture_flat` and routing to `smooth`.

**★ THE REMAINING HORIZON IS ABOUT 100 MORE MINING HOURS (Matt, 2026-09-12), NOT 10,000.** The 10,000-hour frame stays as the way to JUDGE a product choice (→ fractal-operating) and is not a storage projection. **Records-only picture retention is not needed at this scale** → `preserve\retention_design.md`.

**★ THE BAR: `DEFAULT_FINE_BAR = 0.030242` ON `p_ge4`**, under `fine_head = twelve_sheets_drop_high_asymmetric_auc_ge4_more_k3` — **a k=3 ensemble of seeds 0/1/2 averaged on the probability scale**, now a shipped head. The COLUMN stays `p_ge4`. The LEVEL is a **matched constant, not a discovered one**. **★ ⚠ A BAR IS UNREADABLE WITHOUT ITS HEAD** — two runs of ONE recipe on ONE corpus derived **0.022689 and 0.083975** at the same matched fraction. Never carry a level across a fit. ⚠ `solve.Q4_BAR = 0.50` is the RENDER judge's constant. ⚠ There is no CLI spelling for the unbarred population: `--fine-bar 0` still excludes every unread row; `fine_bar=None` in process is the only way back. ⚠ `curate growth` and `curate solve k-sweep` inherit the bar. Provenance → `models/gallery_grade/README.md`.

**★ ⚠ THE PUBLISHED MEDIAN SITS AT THE POOL'S 96.55th PERCENTILE.** 1,170 distinct places pool-wide clear `p_fine` 0.533, there is no knee — places halve per 0.10–0.13 of bar, evenly — and the per-family spread is a **monotone shift rather than a heavier tail**, orange running 3.4–4.0× azure at every decile d3–d9. A flat quality line is therefore a different ask in each hue. Census → `curation/GALLERY.md`.

**★ `p_fine`, `p_coarse` AND THE QUALITY BARS ARE ALL OPERATING WELL — EVERY TASK THAT WOULD ALTER THEM IS CLOSED (Matt, 2026-09-12).** **He re-raises if it is worth doing; never re-open any of it unprompted.**

**★ THE HUMAN VETO IS SHIPPED (Matt, 2026-09-14).** A human `p_fine` label of `1` excludes that ROW — the exact candidate by recipe key, never the place, pair, mode or map — from seating, the pool and every future solve. Derived and never written; retroactive; latest-wins, so a verdict can be revoked by a later one; human-origin only, never a model score. Costs ~10.6 s a pool build, the `(mode, colormap)` prefilter refused deliberately. Shape → `curation/README.md`. **The on-demand grade-1 escape count stays parked.**

**★ THE REJECTION PASS IS A LABELING MODE (Matt, 2026-09-14): he marks ONLY `1`s and an unmarked tile is NOT a label.** Every sheet records `sweep: false` so "off" and "predates the flag" stay distinguishable. **Never build a review sheet whose unmarked state writes anything.**

**★ A THEMED PASS RELAXES THE BAR INSIDE ITS OWN CELL (Matt, 2026-09-11; shipped).** `solve.themed_fine_bar` = the lower of the shipped `fine_bar` and the `p_fine` of the **4n-th** best candidate among rows dominant in the cell, **floored at 0.01**. **If the cell cannot fill even at the floor the gallery ships SMALL — there is no padding branch.** On the manifest as `config.theme_bar`, with **`bar_from`** naming which branch fired. → `curation/GALLERY.md`.

**★ ⚠ A HUE FAMILY IS NOT THE UNION OF ITS FOUR CELLS.** Family dominance (`dominance.Reading.families`, `FAMILY_LEAD` 0.20 / `FAMILY_ALONE` 0.30) takes twice the cell threshold against a summed mass, so a family pool can be narrower than its cells suggest. No CLI flag reaches it; the family route splices the family name onto `cells`. **A row is dominant in at most THREE families, mean 1.2505** — bounded by arithmetic, not by policy → `palettes/README.md`.

**★ ⚠ NO FAMILY IS SCARCE AT EITHER BAR.** Even `lime` holds 242 places above the shipped fine bar against a 150 target. **A weak family is short of DISTINCT material at places we already hold, not short of material** — which is why a store-derived scarce set comes back empty and any named scarce set is a judgement, not a reading. → `curation/GALLERY.md`.

**★ A THIN CELL IS STOCK-BOUND, NOT CARRIER-BOUND.** 942 of 942 drawable maps carry a carrier row. **Buy rows IN the cell, not maps to aim with.**

**★ THE PALETTE GROUP CAP IS `0.075·n` THEMED, `0.025·n` GENERAL (Matt, 2026-09-12).** ⚠ It does nothing for a cell that ships small. **★ THE COLLECTION IS NOT CONVERGING ON ONE PALETTE** — 446 distinct maps hold the published 1,000 seats, top map 2.0%, top ten 10.1%.

**★ ⚠ THE COLOUR ALLOWANCE IS PROPORTIONAL TO `n`**, so a collection's gap at one target is not its gap at another: `threads` seats 484 of 1000 and 423 of 500 off the same store. Never carry a shortfall across a target change.

**★ `TAU` IS CLOSED ON THE THEMED PATH.** **★ A GALLERY PAGE IS PRESENTED STRATIFIED, NOT IN QUALITY ORDER (Matt, 2026-09-12).** `curation/page_order.py`, derived at page build, readout `curate solve browse <stamp> --spacing`. ⚠ **A repeat is priced by its excess over what a run CANNOT avoid holding.** ⚠ **A monotone decile profile would mean the page is still in quality order** and is the wrong check.

**★ HOLDING THE ADMITTED FRACTION IS NOT RAISING THE BAR.**

**★ THE `p_fine` COLUMN IS NOT IDENTIFIED, AND AVERAGING IS THE LEVER.** Churn falls as `0.108 + 0.657/√k` out to k=8 with no knee. ⚠ Buys reproducibility against SEEDS, not kernels. → `preserve\gallery_grade_stability.md`.

**★ ⚠ A BEFORE/AFTER ACROSS A REFIT NEEDS A SAME-RECIPE REPLICATE AS CONTROL.**

**★ MATT REOPENED K HIMSELF AND SET IT; CLAUDE STILL NEVER PROPOSES REOPENING IT.**

**★ ⚠ THE ALLOWANCE COUNTS MEMBERSHIPS, NOT SEATS.** **★ A `cell_floor:` STAMP SAYS WHICH LEG PLACED A SEAT, NOT THAT THE FLOOR BOUGHT IT.** **★ WHAT HOLDS A THIN COLOUR DOWN IS NOT THE CEILING.**

**★ GUARD RULINGS (Matt, 2026-09-10) — LOOSENING ONLY, AND NOTHING WAS LOOSENED.** Mode floors are as low as he will take them; the spiral cap STAYS AT 0.10; the per-cell floor stays at 20. ⚠ A delta page pairs departures with arrivals BY THE FREED SLOT.

**★ ⚠ THE SOLVER IS NOT AT ITS OPTIMUM** — at least 1.4 of sum on the table at n=1000. **A shadow price is not askable of this solver.** ⚠ **Its non-monotonicity is real and shows up as seats changing hands for no reason in the pool.**

**★ THE COLOUR FLOOR DOES NOT DRAG IN BAD PICTURES.** **★ `PRESELECT_RADIUS` STAYS AT 0.02.**

**★ ASYMMETRIC COST (Matt, 2026-09-10): KEEPING LOW-GRADED PICTURES LOW MATTERS MORE THAN KEEPING HIGH-GRADED PICTURES HIGH.**

**★ THE `p_fine` SEATING IS THE WAY; `rank_key` IS DEPRECATED AS AN OFFER AND NOTHING MORE.** **★ `--forced` IS STAGED AND STAYS STAGED INDEFINITELY.**

**★ THE FOLD MERGES INSTEAD OF DELETING, AND IT BOUGHT 71 OF 1,000 SEATS.** ⚠ No transitivity. **It picks its survivor on the seating key.**

**★ THERE IS NO HONEST SCORE COLUMN OVER THAT POPULATION.** Every seat carries a manual verdict and the store is the head's own training material. **Matt's eye is the only independent read of a seating.**

**★ A RE-RENDER INVALIDATES EVERY READING TAKEN OFF THE PICTURE, NOT ONLY THE SCORE.** `recolour --keys` is the door and is idempotent.

**★ GROUPS ARE PALETTE GROUPS AND MINING CANNOT MOVE THEM.** A new group needs a new MAP.

**★ `p_fine` COVERAGE IS CHECKABLE BEFORE A SOLVE.** ⚠ **`pool_scores.jsonl` is one-shot**: above-bar rows merged after the last `score-pool` are unseatable. **Mine → merge → score-pool → solve.** Nothing enforces it.

**★ A `score-pool` REFRESH MOVES MEMBERSHIP, NOT READINGS.**

**⚠ SEATS-CHANGED IS NOT A MEASURE OF POOL CHANGE**, and **★ THE SEATING AMPLIFIES THE COLUMN**.

**★ ⚠ FILL IS THE WRONG SINGLE MEASURE OF A MINING LEG.** Roughly every second seat taken displaces an incumbent, so net fill under-reports the work about twofold — and a collection at full fill scores zero on fill while its median moves. `tia` gained nothing on seats, replaced 229 of its thousand and rose 0.241 → 0.300. **Report seats AND the seated `p_fine` distribution, always.**

**★ ⚠ WEIGH A MEASUREMENT AGAINST THE COST OF THE ACTION IT DECIDES, NOT AGAINST HOW INFORMATIVE IT IS.** When the human input is cheap and the population well-defined, just do it.

**★ ⚠ A SMALL SMOKE MISPRICES A LEG TWICE OVER, IN OPPOSITE DIRECTIONS.** Price a leg off an OBSERVED leg. ⚠ **A pilot's winners do not survive n.** Pilot; do not carry.

## ROTATION AND PHASE — CLOSED
**★ THE FORWARD DRAW IS ONE RANDOM PHASE PER CANDIDATE (Matt, 2026-09-14).** This SUPERSEDES the best-of-five rule: best-of-five costs 5× for 3.12× yield at full render price, and a single uniform draw is a better realisation of proper phase mixing than a winner-keeps rule, which biases the corpus toward flattering phases. A shot is one render. Best-of-five stays available only on the shareable field path and for depth at a named place. **Matt also ruled that ideally every head is fp16 going forward.** ⚠ The direct traps draw bare — phase is a byte-for-byte no-op there. **★ NOTHING ELSE IS PHASE-FLAT.** Economics and control-sizing → `preserve\rotation_phase_economics.md`. **Do not re-propose the decided-row mark.**

**★ A LEG STATES ITS RESOLVED SHARES AND ROSTER BEFORE PLANNING** — the defect was the silence. ⚠ **`--shares` MERGES OVER `depth.SHARES` rather than replacing them**: a partial map inherits the rest, and a `FLOOR 1.0` shorthand once planned 12,760 of 35,520 shots onto a written-off band before the resolved-shares readout caught it. **Spell shares whole.** ⚠ **`--budget` both sizes a plan and sets its deadline**; **`--from-block` cannot resume a wholly-ranked leg**.

## THE PALETTE AXIS — PARKED, EXCEPT PHASE
**★ MATT PARKED PALETTE REPLICATION ENTIRELY (2026-09-12).** All ROTATION work is kept. ⚠ `labeling/server.py` has **no write path at all**. ⚠ **`p_fine` is a CANDIDATE-geometry column**.

## MODES AND COLOUR
**★ THE FOUR TARGETED-GALLERY MODES ARE `smooth`, `tia`, `stripe` AND `threads`, AND NOTHING ELSE (Matt, 2026-09-15).** The product logic is that someone who likes one rendering mode can see only that mode in quantity. Every other mode, `itinerary` included, appears in the general and family collections as usual — there is nothing missing and no fifth is wanted.

**★ MORE ANGLE-MODE MINING IS A VARIETY GOAL, NEVER A SEAT ONE (Matt).** The point is to SAMPLE THE VISUAL BEST — many good results across palettes at good places, to choose from. **Never re-frame an "I want more of X" as a seat-count argument.**

**★ NEVER EXCLUDE A SHAREABLE MODE ON A SEAT ARGUMENT WITHOUT PRICING IT** — the shareable modes are 12–45× cheaper a clear.

**★ THE `direct_trap_multiply` SWEEP PROPOSES NO ROSTER CHANGE.** **★ THE ORANGE-ON-BLUE SLICE IS WHY THIS ERA HAPPENED.**

## SOURCING
**★ ⚠ THE NEVER-OPENED POOL IS ZERO ACROSS ALL TEN PARTITIONS (2026-09-15).** Every admitted location this project holds has been opened at least once — 40,454 admitted against 42,113 opened over a 459,548-row ledger. **Breadth is retired as an arm.** Any plan, document or estimate treating never-opened stock as an available lever is wrong. The last 177 were `phoenix:classic`, closed stripe-only at **233.9 engine-seconds a clear**, 33× the recolour arm — right as a closing decision and wrong as a queueing one. **Read the drawable count before planning anything that assumes stock.**

**★ EVERY FUTURE ROW LANDS AT A PLACE WE ALREADY HOLD.** The consequences follow from that and none of them are reversible by mining: a collection takes one seat per place, so a second row at a place already seating in that family buys nothing, and the levers left are more colourings and more modes at the 13,643 places in hand.

**★ SUPPLY IS ROOT-BOUND ON THE TWINS.** 1,401 roots was the entire standing supply of the seven partitions named; depth is spent. Mechanism → **`preserve\julia_supply.md`**; phoenix → **`preserve\phoenix_sampling.md`**.

**★ ⚠ THE OPENED-BUT-UNADMITTED LOCATIONS ARE A SCORING BACKLOG, NOT AN EMBEDDING ONE.** **`curate score` owes the work.** ⚠ A band manifest needs `--modes smooth stripe tia`.

**★ AIMING IS FREE AND LARGE.** 5.9×–40.5× at the cell, median 14.6×, **53.4% of a conditioned draw landing in the exact cell asked**; a matched flat control cleared 40.30% against the aimed arm's 44.89%, so the lift costs no quality at the family read. ⚠ **`--draw-cells` saturates in the length of its list** and a plan whose cut keeps essentially everything is now REFUSED at plan time — the narrowing claim is stamped on every row as `drawn_cells` and on the record as `cells_narrowed`, so a silent no-op wrote false provenance onto 21,000 rows. ⚠ **`--cell` is a cycle and nothing deduplicates it**, which is how a gap-weighted aim is spelled with a flag typed as a set.

**★ ⚠ THE RECOLOUR ARM DOES NOT SATURATE WITHIN A LEG — A STALE MANIFEST LOOKS EXACTLY LIKE SATURATION.** Two passes over one manifest read 42.6% → 27.7% and +27 net; a manifest rebuilt the same hour read 40.2% and +1,941, with retention flat across all ten deciles of its own draw order. **Rebuild the manifest, don't re-run it.**

**★ A PROVEN PLACE IS WORTH ABOUT FIVE BLIND ONES TO A COMPOSITE.** The 8.2%-conversion prior was wrong by 5×.

## RETENTION
**★ THE KEEP IS FIVE PER `(place, mode)` PLUS ONE FAMILY ALLOWANCE (`retention.FAMILY_ALLOWANCE = 1`, 2026-09-15).** A third verdict, `kept_for_a_family`, beside `ranked` and `dropped`: one further row a pair, best-in-a-family the kept five miss. **Forward-only by construction, with no flag** — the allowance can only keep a row below the top keep, so it binds at a full pair and a store already at the keep holds nothing for it to reach. Its effect lands in `candidate_ledger/family_allowance/<stamp>.jsonl` carrying `for_family`. ⚠ **A protected row also sits below the top keep, so the rule REACHES rows it did not buy** — subtract `reached_a_protected_row` or the file is noise — and the new reason counts LAST, after the five protections, whose counts are read across months.

**★ ⚠ THE KEEP BINDS AT ONLY 7.4% OF PAIRS** (14,933 of 202,093) and the store can grow **2.2×** before it binds anywhere new. The colour term is a cheap improvement, not an unlock, and its value grows as pairs fill. → `curation/README.md`.

**★ THE RANK ITSELF IS STILL COLOUR-BLIND** — `(loc_p_ge4, p_ge3, p_ge4, flatness)`, no colormap identity, no palette group. Stage-by-stage map of where colour is and is not a dimension → `curation/README.md §Where colour is a dimension, and where it is not`. Two gaps stand: `ceiling.parse_target` refuses a family outright, and `retention.by_place_cell` has no caller but a CLI print.

**★ A PRUNE NOW WRITES WHAT IT TOOK** — `displaced/<stamp>.jsonl`, carrying key, place, mode, settings, `cells`, `families`, `p_ge3`, `p_ge4` and `rank_value`. The recipe key is what `re-render` keys on, so a displaced row is buyable back. ⚠ **A pruned row dies before `score-pool` and so never gets a `p_fine`.**

## RECORDS
**★ ⚠ A RECORD IS DISCARDED BY DEFAULT (Matt, 2026-09-13) — AND THAT RULE LIVES IN `CLAUDE.md`.** **Keeping needs a reason; discarding does not.** **★ PRESERVATION DERIVES FROM THE KEEP LIST ALONE** — a record's mere existence on disk does not pin its seats. **No sweep step belongs in a future prompt.**

**★ ⚠ A RECORD IS TWO DIRECTORIES** — `tentative/<stamp>/` and `solve/<manifest.solve.name>/`. ⚠ **Publication, durability and retention are three questions, not two.** ⚠ **`solve.write_record` used to mkdir and overwrite unconditionally**, so `--solve-name` collided and `20260902T161757Z` lost its decision through that door; it refuses now, and `curate solve run` is the only caller passing `over=True`.

**★ ⚠ A COUNT OF FOLDERS IS NOT A COUNT OF KEPT RECORDS.** The store holds **96 stamps / 627.0 MiB**, of which the published `20260914T171846Z` alone is 548.5 MiB. **80 are off the keep list, 61.4 MiB**, in five batches; the per-stamp list is at `scratch/preclose_ckpt125/off_list_stamps.txt`. `protected_keys()` reads 5,188 either way — none of the 80 pins anything.

**★ THE SIXTEEN `targets_*` RECORDS OF `20260915T2101–2106Z` ARE THE STANDING BASELINE** — the *before* the next mining prompt reads, at the current table with `lime` at 150. The other 64 off-list records are superseded by them.

**★ THE TWO UNDECLARED HARD-DEPENDENCY STAMPS ARE ON THE STANDING KEEP ROSTER.** `20260906T133559Z` backs the site's `modes-gallery` curvature panel; `20260906T133236Z` is the draw behind all three batches of the shipped label corpus.

## THE RECORD'S OWN PROSE
**★ A RECORD CARRIES ITS PROSE WHOLE, AND THE SOURCE CARRIES ONE COPY.** `SCHEMA_NOTES` beside each `SCHEMA`, read at write time. **No version integer, no bump rule.** ⚠ `NOTES_AT_LEAST` moving DOWN is named at the constant. ⚠ **A record site carrying its prose inline is refused** by `test_no_record_site_writes_its_own_prose`.

**★ `held_out_is` UNDERCOUNTED, AND THE RECORDS WERE LEFT ALONE.**

## THE REPO AS A CLONE SEES IT
**★ A FRESH CLONE CAN BUILD, DRAW THE PUBLISHED GALLERY AND MINE UNSCORED LOCATIONS DE NOVO; IT CANNOT SOLVE.** The stores are untracked and shipping the pool is a separate decision Matt has not taken — the shrunk above-bar projection is 4.96 MB gzipped if he ever does. Clone is 25.05 MiB packed; `[models]` is 4.34 GiB of torch, which dwarfs everything else.

**★ THE PRIMARY DOCUMENTED INSTALL IS `uv sync`, NAMING ALL THREE EXTRAS.** ⚠ **The pip `--extra-index-url` workaround cannot work and never could**: the cu124 index tops out at exactly `pyproject.toml`'s floors (torch 2.6.0, torchvision 0.21.0), so any newer PyPI release wins the pooled resolve and installs CPU-only torch silently. There is zero slack and a new torch release always exists. ⚠ `numpy` was never missing — `scipy` supplied it transitively the whole time. `uv.lock` is gitignored, keeping the README's no-lockfile claim self-enforcing.

**★ ⚠ `p_fine` SCORES ARE STAMPED WITH A WEIGHTS SHA, AND A CLONE'S ROWS WILL DIFFER BY DESIGN** — the 46,090 stored rows record the fp32 checkpoints that produced them, while the release ships fp16. That is the guard working, not a mismatch. ⚠ fp16 costs 4 bar crossings of 8,000 rows and **2 seats in and 2 out of the top 1,000** — Matt accepts that as a minor inconsistency; **it reports rather than gates, and no bound is ratified**. He would be surprised past about ten.

## IN FLIGHT ACROSS THIS BOUNDARY
Nothing.

## QUEUED IN DRIVE `prompts\`
Nothing.

## NEXT CHECKPOINT GOAL
**Matt sets it at the top of the checkpoint.** Nothing is scheduled here.

## OPEN (ordered) — Matt raises each
1. **Mining.** Every mining night is composed fresh with Matt — arms, roster and shares are discussed anew each time and nothing here pre-decides them. With breadth retired, the arms left are aimed recolour and more modes at places in hand.
2. **`curate score` over the unscored opened locations**, which raises the near band's ceiling.
3. **A continuous boundary sampler for the parameter planes (Matt: build it some future checkpoint).** `nucleus_grid` empties permanently; `viewport_sampler` is `PINNED_PLANES` only. Would widen the twins too, and it is now the only route to a location that does not already exist. → `preserve\julia_supply.md`.
4. **The decode cache — a storage decision for Matt.** ~33 GB of hot tier, speeds every arm at once.
5. **A sweep for rulings that govern a LEG but exist only in these docs.**
6. **`pictures/` in the ten `runs` legs.** 5.37 GiB. **Matt: leave for now.** ⚠ Destructive; not for an unattended prompt.
7. **Website — REOPENED for a section-by-section review pass.** Matt brings a review doc for one section; Claude pushes back on anything wrong or not an improvement; once aligned, Claude writes the prose master and the placement prompt. Per-page status → `docs/page-review.md`.
8. **The reframe channel's cadence.** `g10` reads 6 barren / 376 unresolved / 2 productive.
9. **Whether a second published stamp gets a recipe file**, and whether `data/palette_choice/rows/` belongs in a clone (Matt: leave it entirely).
10. **The shipped weights have no stated licence.** The repo is MIT (`LICENSE`, matching `pyproject.toml`) and DINOv2 is Apache-2.0 and fetched rather than redistributed, but `weights.json`'s four release assets carry hashes and provenance and no terms. Whether MIT reaches artifacts served from Releases is Matt's call.
11. **A README CI badge**, once a green run exists to point at.

Parked → `preserve\parked.md`.

## STATUS / KNOWN REDS
⚠ **CI's last observed run is #28 on `485674b`, failing.** The cause was found and fixed: **`pillow` was absent from the `dev` extra**, which accounted for 113 of 118 failures, and three modules importing it at module level turned that into a collection error that aborted the whole lane in under four seconds. `dev` now names `numpy` and `pillow`, so those tests run rather than skip, and two guards cover the module-level and call-time shapes from a table that already exists. ⚠ The fix has not been observed green, because the commit carrying it is not the commit CI last ran. Nothing else is red.

## RULINGS THIS ERA
→ the domain rulings in the docs themselves and the in-repo promotions: `curation/LEGS.md`, `curation/MEASUREMENTS.md`, `curation/README.md`, `curation/GALLERY.md`, `palettes/README.md`, `supply/README.md`, `models/README.md`, `models/gallery_grade/README.md`, `data/discovery/README.md`, `curation/targets.py`.

## KEEP LIST
Drive `prompts\`: **wipe everything** — nothing queued, nothing in flight. `reports\`: **wipe everything**.

Wallpapers `artifacts/sheet/`: ⚠ **`gallery_rejection_20260914/` no longer holds the published fulls** — they were hard-linked into the record's own tree, so the sheet is free to go when Matt says.

Wallpapers `scratch/`: KEEP `place_radius_sheet/`, `retired_tentative/` and `preclose_ckpt125/off_list_stamps.txt`; **WIPE everything else**. Website `scratch/`: unchanged.

## OWED
Nothing beyond the OPEN list.

## SCRATCH/ARTIFACT FLAGS
**★ THE STANDING KEEP ROSTER LIVES IN THE REPO — `src/fractal_wallpapers/README.md §The standing keep roster`.** ⚠ Nothing on it is protected by `orphans`' reference set.

⚠ **`.leveled/` DIRECTORIES ARE SWEEPABLE** → `preserve\leveled_identity.md`. ⚠ **`orphans` lists pre-existing unmerged legs** — ten of them holding 14,804 pictures, listed and left — and a dated orphan verdict goes stale in hours.

Per-checkpoint: `artifacts/curation/depth/*/fields` grows at roughly 226 MB a leg and the sweep cannot reach it. ⚠ A pass that dumps fields sweeps its own. ⚠ **CRLF drift is real**; `git ls-files --eol` is the door. ARCHIVED (RESTORE before reuse): unchanged from ckpt 106.

## PARKED / SETTLED
→ `preserve\INDEX.md`, which lists every file. Never re-list them here.
