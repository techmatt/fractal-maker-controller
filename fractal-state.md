# fractal-state — checkpoint 125 (2026-09-14)

## Where we are
Three phases, each depending strictly on the one before → fractal-discovery. Matt iterates from pictures, not counts; phase 3 is his eye on the final seating.

**★ THE FINAL GALLERY SHIPS AT n=1000, AND EVERY THEMED COLLECTION SHIPS AT n=200 (Matt, 2026-09-13).** The seat count is **not** a knob to trade against quality: pick thresholds to FILL first, then lift quality by aimed mining. n=2000 is not the direction; making n=1000 better is. "Better" means true quality, NOT maximizing `p_fine`.

**★ THE FIRST PUBLICATION HAPPENED (Matt raised it, 2026-09-14): `20260914T171846Z` IS THE PUBLISHED n=1000 GALLERY**, the eighth `tentative.PUBLISHED` stamp and the one going on the website. **The standing rule is unchanged — Matt raises any further publishing himself; never ask, never list it.** The viewer is `artifacts/curation/viewer/index.html` (unstamped, follows the newest published record); the old `scratch/deterministic_refit_20260910/page/` path forwards.

**★ THE REMAINING HORIZON IS ABOUT 100 MORE MINING HOURS (Matt, 2026-09-12), NOT 10,000.** The 10,000-hour frame stays as the way to JUDGE a product choice (→ fractal-operating) and is not a storage projection. **Records-only picture retention is not needed at this scale** → `preserve\retention_design.md`.

**★ THE BAR: `DEFAULT_FINE_BAR = 0.030242` ON `p_ge4`**, under `fine_head = twelve_sheets_drop_high_asymmetric_auc_ge4_more_k3` — **a k=3 ensemble of seeds 0/1/2 averaged on the probability scale**, now a shipped head. The COLUMN stays `p_ge4`. The LEVEL is a **matched constant, not a discovered one**. **★ ⚠ A BAR IS UNREADABLE WITHOUT ITS HEAD** — two runs of ONE recipe on ONE corpus derived **0.022689 and 0.083975** at the same matched fraction. Never carry a level across a fit. ⚠ `solve.Q4_BAR = 0.50` is the RENDER judge's constant. ⚠ There is no CLI spelling for the unbarred population: `--fine-bar 0` still excludes every unread row; `fine_bar=None` in process is the only way back. ⚠ `curate growth` and `curate solve k-sweep` inherit the bar. Provenance → `models/gallery_grade/README.md`.

**★ `p_fine`, `p_coarse` AND THE QUALITY BARS ARE ALL OPERATING WELL — EVERY TASK THAT WOULD ALTER THEM IS CLOSED (Matt, 2026-09-12).** **He re-raises if it is worth doing; never re-open any of it unprompted.**

**★ THE HUMAN VETO IS SHIPPED (Matt, 2026-09-14).** A human `p_fine` label of `1` excludes that ROW — the exact candidate by recipe key, never the place, pair, mode or map — from seating, the pool and every future solve. Derived and never written; retroactive; latest-wins, so a verdict can be revoked by a later one; human-origin only, never a model score. Costs ~10.6 s a pool build, the `(mode, colormap)` prefilter refused deliberately. Shape → `curation/README.md`. **The on-demand grade-1 escape count stays parked.**

**★ THE REJECTION PASS IS A LABELING MODE (Matt, 2026-09-14): he marks ONLY `1`s and an unmarked tile is NOT a label.** The sheet's sweep button would have written the head's own decode onto ~900 unmarked tiles as `origin: human`; it is off three ways on a rejection sheet and every sheet now records `sweep: false` so "off" and "predates the flag" stay distinguishable. **Never build a review sheet whose unmarked state writes anything.**

**★ A THEMED PASS RELAXES THE BAR INSIDE ITS OWN CELL (Matt, 2026-09-11; shipped).** `solve.themed_fine_bar` = the lower of the shipped `fine_bar` and the `p_fine` of the **4n-th** best candidate among rows dominant in the cell, **floored at 0.01**. **If the cell cannot fill even at the floor the gallery ships SMALL — there is no padding branch.** On the manifest as `config.theme_bar`, with **`bar_from`** naming which branch fired. → `curation/GALLERY.md`.

**★ ⚠ THE FOUR CELLS THAT "COULD NOT FILL 200 AT ANY BAR" NOW FILL (census, 2026-09-14).** All sixteen green / lime / teal / cyan cells reach 200 at the shipped bar; greens run 600–998 places against lime at 305/337/366, the thinnest. **Any plan resting on those four being unfillable is resting on a retired fact.** ⚠ **And the modes that produce those rows are `smooth`/`tia`/`stripe` — about 80% of them pooled, the whole dear roster under 9%.** Table → `curation/GALLERY.md`.

**★ A THIN CELL IS STOCK-BOUND, NOT CARRIER-BOUND.** 942 of 942 drawable maps carry a carrier row. **Buy rows IN the cell, not maps to aim with.**

**★ THE PALETTE GROUP CAP IS `0.075·n` THEMED, `0.025·n` GENERAL (Matt, 2026-09-12).** ⚠ It does nothing for a cell that ships small. **★ AND THE COLLECTION IS NOT CONVERGING ON ONE PALETTE (measured 2026-09-14)** — 446 distinct maps hold the 1,000 seats, top map 2.0%, top ten 10.1%, the top map well under the group cap. The mono-palette worry is answered; the instrument that would catch it is the per-cell fill readout.

**★ `TAU` IS CLOSED ON THE THEMED PATH.** **★ A GALLERY PAGE IS PRESENTED STRATIFIED, NOT IN QUALITY ORDER (Matt, 2026-09-12).** `curation/page_order.py`, derived at page build, readout `curate solve browse <stamp> --spacing`. ⚠ **A repeat is priced by its excess over what a run CANNOT avoid holding.** ⚠ **A monotone decile profile would mean the page is still in quality order** and is the wrong check.

**★ HOLDING THE ADMITTED FRACTION IS NOT RAISING THE BAR.**

**★ THE `p_fine` COLUMN IS NOT IDENTIFIED, AND AVERAGING IS THE LEVER.** Churn falls as `0.108 + 0.657/√k` out to k=8 with no knee. ⚠ Buys reproducibility against SEEDS, not kernels. → `preserve\gallery_grade_stability.md`.

**★ ⚠ A BEFORE/AFTER ACROSS A REFIT NEEDS A SAME-RECIPE REPLICATE AS CONTROL.**

**★ MATT REOPENED K HIMSELF AND SET IT; CLAUDE STILL NEVER PROPOSES REOPENING IT.**

**★ ⚠ THE ALLOWANCE COUNTS MEMBERSHIPS, NOT SEATS.** **★ A `cell_floor:` STAMP SAYS WHICH LEG PLACED A SEAT, NOT THAT THE FLOOR BOUGHT IT.** **★ WHAT HOLDS A THIN COLOUR DOWN IS NOT THE CEILING.**

**★ GUARD RULINGS (Matt, 2026-09-10) — LOOSENING ONLY, AND NOTHING WAS LOOSENED.** Mode floors are as low as he will take them; the spiral cap STAYS AT 0.10; the per-cell floor stays at 20. ⚠ A delta page pairs departures with arrivals BY THE FREED SLOT.

**★ ⚠ THE SOLVER IS NOT AT ITS OPTIMUM** — at least 1.4 of sum on the table at n=1000. **A shadow price is not askable of this solver.** ⚠ **Its non-monotonicity is real and shows up as seats changing hands for no reason in the pool** — 83 seats moved on a re-solve that removed nine rows.

**★ THE COLOUR FLOOR DOES NOT DRAG IN BAD PICTURES.** **★ `PRESELECT_RADIUS` STAYS AT 0.02.**

**★ ASYMMETRIC COST (Matt, 2026-09-10): KEEPING LOW-GRADED PICTURES LOW MATTERS MORE THAN KEEPING HIGH-GRADED PICTURES HIGH.**

**★ THE `p_fine` SEATING IS THE WAY; `rank_key` IS DEPRECATED AS AN OFFER AND NOTHING MORE.** **★ `--forced` IS STAGED AND STAYS STAGED INDEFINITELY.**

**★ THE FOLD MERGES INSTEAD OF DELETING, AND IT BOUGHT 71 OF 1,000 SEATS.** ⚠ No transitivity. **It picks its survivor on the seating key.**

**★ THERE IS NO HONEST SCORE COLUMN OVER THAT POPULATION.** Every seat carries a manual verdict and the store is the head's own training material. **Matt's eye is the only independent read of a seating.**

**★ A RE-RENDER INVALIDATES EVERY READING TAKEN OFF THE PICTURE, NOT ONLY THE SCORE.** `recolour --keys` is the door and is idempotent.

**★ AT n=1000 THE GALLERY IS SATURATED.** Mining buys option value for a later re-solve, and quality inside themes.

**★ GROUPS ARE PALETTE GROUPS AND MINING CANNOT MOVE THEM.** A new group needs a new MAP.

**★ `p_fine` COVERAGE IS CHECKABLE BEFORE A SOLVE.** ⚠ **`pool_scores.jsonl` is one-shot**: above-bar rows merged after the last `score-pool` are unseatable. **Mine → merge → score-pool → solve.** Nothing enforces it.

**★ A `score-pool` REFRESH MOVES MEMBERSHIP, NOT READINGS.**

**⚠ SEATS-CHANGED IS NOT A MEASURE OF POOL CHANGE**, and **★ THE SEATING AMPLIFIES THE COLUMN**.

**★ ⚠ WEIGH A MEASUREMENT AGAINST THE COST OF THE ACTION IT DECIDES, NOT AGAINST HOW INFORMATIVE IT IS.** When the human input is cheap and the population well-defined, just do it.

**★ ⚠ A SMALL SMOKE MISPRICES A LEG TWICE OVER, IN OPPOSITE DIRECTIONS.** Price a leg off an OBSERVED leg. ⚠ **A pilot's winners do not survive n.** Pilot; do not carry.

## ROTATION AND PHASE — CLOSED
**★ THE FORWARD DRAW IS ONE RANDOM PHASE PER CANDIDATE (Matt, 2026-09-14).** This SUPERSEDES the best-of-five rule: best-of-five costs 5× for 3.12× yield at full render price, and a single uniform draw is a better realisation of proper phase mixing than a winner-keeps rule, which biases the corpus toward flattering phases. A shot is one render. Best-of-five stays available only on the shareable field path and for depth at a named place. **Matt also ruled that ideally every head is fp16 going forward.** ⚠ The direct traps draw bare — phase is a byte-for-byte no-op there. **★ NOTHING ELSE IS PHASE-FLAT.** The whole economics, the measured numbers and the control-sizing lesson → `preserve\rotation_phase_economics.md`. **Do not re-propose the decided-row mark.**

**★ A LEG STATES ITS RESOLVED SHARES AND ROSTER BEFORE PLANNING** — the defect was the silence. ⚠ **`--budget` both sizes a plan and sets its deadline**; **`--from-block` cannot resume a wholly-ranked leg**.

## THE PALETTE AXIS — PARKED, EXCEPT PHASE
**★ MATT PARKED PALETTE REPLICATION ENTIRELY (2026-09-12).** All ROTATION work is kept. ⚠ `labeling/server.py` has **no write path at all**. ⚠ **`p_fine` is a CANDIDATE-geometry column**.

## MODES AND COLOUR
**★ `tia`, `stripe` AND `threads` ARE ALL BACK IN THE MINING ROSTER (Matt, 2026-09-14)** — a general re-admission, and especially wanted for the false colours. This supersedes the 2026-09-13 exclusion: they were excluded on seat grounds and the exclusion was paid for in engine seconds, because the shareable modes are 12–45× cheaper a clear. **Never exclude a shareable mode on a seat argument without pricing it.**

**★ MORE ANGLE-MODE MINING IS A VARIETY GOAL, NEVER A SEAT ONE (Matt).** The point is to SAMPLE THE VISUAL BEST — many good results across palettes at good places, to choose from. There is no seat shortage there and that does not mean quality cannot improve. **Never re-frame an "I want more of X" as a seat-count argument.**

**★ THE `direct_trap_multiply` SWEEP PROPOSES NO ROSTER CHANGE.** **★ THE ORANGE-ON-BLUE SLICE IS WHY THIS ERA HAPPENED.**

## SOURCING
**★ 6,821 ADMITTED LOCATIONS HAVE NEVER BEEN OPENED**, 1,787 of them needing a fresh framing. The arm that opens them needs no roots at all.

**★ SUPPLY IS ROOT-BOUND ON THE TWINS.** 1,401 roots was the entire standing supply of the seven partitions named; depth is spent. Mechanism → **`preserve\julia_supply.md`**; phoenix → **`preserve\phoenix_sampling.md`**.

**★ ⚠ THE OPENED-BUT-UNADMITTED LOCATIONS ARE A SCORING BACKLOG, NOT AN EMBEDDING ONE.** **`curate score` owes the work.** ⚠ A band manifest needs `--modes smooth stripe tia`.

## RECORDS
**★ ⚠ A RECORD IS DISCARDED BY DEFAULT (Matt, 2026-09-13) — AND THAT RULE LIVES IN `CLAUDE.md`.** **Keeping needs a reason; discarding does not.** **★ AND PRESERVATION NOW DERIVES FROM THE KEEP LIST ALONE (2026-09-14)** — a record's mere existence on disk no longer pins its seats, which was the policy backwards and the reason sweeping kept landing on Matt's desk as a recurring approval. 24 unpublished records were retired to untracked scratch, releasing 2,788 rows. **No sweep step belongs in a future prompt.**

**★ ⚠ A RECORD IS TWO DIRECTORIES** — `tentative/<stamp>/` and `solve/<manifest.solve.name>/`. ⚠ **Publication, durability and retention are three questions, not two.**

Store stands at **16 stamps, 8 published**. `protected_keys()` is 5,188 over the 16. **★ A RECORD'S OWN SEAT COUNT IS NOT WHAT DELETING IT RELEASES — measure `protected_keys()` either side; never sum.**

**★ THE TWO UNDECLARED HARD-DEPENDENCY STAMPS ARE ON THE STANDING KEEP ROSTER.** `20260906T133559Z` backs the site's `modes-gallery` curvature panel; `20260906T133236Z` is the draw behind all three batches of the shipped label corpus.

## THE RECORD'S OWN PROSE
**★ A RECORD CARRIES ITS PROSE WHOLE, AND THE SOURCE CARRIES ONE COPY.** `SCHEMA_NOTES` beside each `SCHEMA`, read at write time. **No version integer, no bump rule.** ⚠ `NOTES_AT_LEAST` moving DOWN is named at the constant.

**★ `held_out_is` UNDERCOUNTED, AND THE RECORDS WERE LEFT ALONE.**

## THE REPO AS A CLONE SEES IT
**★ A FRESH CLONE CAN BUILD, DRAW THE PUBLISHED GALLERY AND MINE UNSCORED LOCATIONS DE NOVO; IT CANNOT SOLVE.** The stores are untracked and shipping the pool is a separate decision Matt has not taken — the shrunk above-bar projection is 4.96 MB gzipped if he ever does. Clone is 25.05 MiB packed; `[models]` is 4.34 GiB of torch, which dwarfs everything else.

**★ ⚠ `p_fine` SCORES ARE STAMPED WITH A WEIGHTS SHA, AND A CLONE'S ROWS WILL DIFFER BY DESIGN** — the 46,090 stored rows record the fp32 checkpoints that produced them, while the release ships fp16. That is the guard working, not a mismatch; it is written at `SCHEMA_NOTES["weights_are"]`, in `GALLERY.md` and in the head's README. ⚠ fp16 costs 4 bar crossings of 8,000 rows and **2 seats in and 2 out of the top 1,000** — Matt accepts that as a minor inconsistency; **it reports rather than gates, and no bound is ratified**. He would be surprised past about ten.

## IN FLIGHT ACROSS THIS BOUNDARY
Nothing.

## QUEUED IN DRIVE `prompts\`
Nothing.

## NEXT CHECKPOINT GOAL
**Matt sets it at the top of the checkpoint.** Nothing is scheduled here.

## OPEN (ordered) — Matt raises each
1. **Mining.** Every mining night is composed fresh with Matt — arms, roster and shares are discussed anew each time and nothing here pre-decides them.
2. **The never-opened admitted locations** — the largest untouched supply lever and the one arm root exhaustion cannot touch.
3. **Aimed mining for quality at n=200**, now that the four thin cells fill.
4. **`curate score` over the unscored opened locations**, which raises the near band's ceiling.
5. **Themed collections at n=200.** Matt has built and looked at these: "okay but obviously need improvement."
6. **A continuous boundary sampler for the parameter planes (Matt: build it some future checkpoint).** `nucleus_grid` empties permanently; `viewport_sampler` is `PINNED_PLANES` only. Would widen the twins too. → `preserve\julia_supply.md`.
7. **The decode cache — a storage decision for Matt.** ~33 GB of hot tier, speeds every arm at once.
8. **A sweep of the solve store against the stamp list** for stranded halves.
9. **A sweep for rulings that govern a LEG but exist only in these docs.**
10. **`pictures/` in the ten `runs` legs.** 5.37 GiB. **Matt: leave for now.** ⚠ Destructive; not for an unattended prompt.
11. **Website — REOPENED for a section-by-section review pass.** Matt brings a review doc for one section; Claude pushes back on anything wrong or not an improvement; once aligned, Claude writes the prose master and the placement prompt. Per-page status → `docs/page-review.md`.
12. **The reframe channel's cadence.**
13. **Whether a second published stamp gets a recipe file**, and whether `data/palette_choice/rows/` belongs in a clone (Matt: leave it entirely).
14. **The shipped weights have no stated licence.** The repo is MIT (`LICENSE`, matching `pyproject.toml`) and DINOv2 is Apache-2.0 and fetched rather than redistributed, but `weights.json`'s four release assets carry hashes and provenance and no terms. Whether MIT reaches artifacts served from Releases is Matt's call.

Parked → `preserve\parked.md`.

## STATUS / KNOWN REDS
⚠ **CI IS RED ON `main` AND HAS BEEN FOR AT LEAST FOUR RUNS** — #23 through #26, all three jobs (ubuntu, windows, `models` extra), each failing at the Test step. **The local lanes are green on this tree**, so it is an environment difference rather than a broken tree. Unexamined beyond confirming it, and the reason the README carries no badges. Nothing else is red.

## RULINGS THIS ERA
→ the domain rulings in the docs themselves and the in-repo promotions: `curation/LEGS.md`, `curation/MEASUREMENTS.md`, `curation/README.md`, `curation/GALLERY.md`, `palettes/README.md`, `supply/README.md`, `models/README.md`, `models/gallery_grade/README.md`, `data/discovery/README.md`.

## KEEP LIST
Drive `prompts\`: **wipe everything** — nothing queued, nothing in flight. `reports\`: **wipe everything**.

Wallpapers `artifacts/sheet/`: ⚠ **`gallery_rejection_20260914/` no longer holds the published fulls** — they were hard-linked into the record's own tree, so the sheet is free to go when Matt says.

Wallpapers `scratch/`: KEEP `place_radius_sheet/`; **WIPE everything else** — the `weights-2026-09-14/` staging directory is spent now that the release is cut. Website `scratch/`: unchanged.

## OWED
Nothing beyond the OPEN list.

## SCRATCH/ARTIFACT FLAGS
**★ THE STANDING KEEP ROSTER LIVES IN THE REPO — `src/fractal_wallpapers/README.md §The standing keep roster`.** ⚠ Nothing on it is protected by `orphans`' reference set.

⚠ **`.leveled/` DIRECTORIES ARE SWEEPABLE** → `preserve\leveled_identity.md`. ⚠ **`orphans` lists pre-existing unmerged legs**, and a dated orphan verdict goes stale in hours.

Per-checkpoint: `artifacts/curation/depth/*/fields` grows at roughly 226 MB a leg and the sweep cannot reach it. ⚠ A pass that dumps fields sweeps its own. ⚠ **CRLF drift is real**; `git ls-files --eol` is the door. ARCHIVED (RESTORE before reuse): unchanged from ckpt 106.

## PARKED / SETTLED
→ `preserve\INDEX.md`, which lists every file. Never re-list them here.
