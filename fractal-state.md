# fractal-state — checkpoint 122 (2026-09-12)

## Where we are
Three phases, each depending strictly on the one before → fractal-discovery. Matt iterates from pictures, not counts; phase 3 is his eye on the final seating. **NO PUBLISHING OF ANY KIND until Matt raises it — never ask, never list it.**

**★ THE FINAL GALLERY SHIPS AT n=1000, AND THEMED COLLECTIONS OF n=200 ARE PART OF THE PRODUCT.** n=2000 is not the direction; making n=1000 better is. "Better" means true quality, NOT maximizing `p_fine` — maximizing it would restrict the gallery to a tiny subset.

**★ THE REMAINING HORIZON IS ABOUT 100 MORE MINING HOURS (Matt, 2026-09-12), NOT 10,000.** The multiplier on what is already banked is ×2.76. The 10,000-hour frame stays as the way to JUDGE a product choice (→ fractal-operating) and is not a storage projection. **Records-only picture retention is therefore not needed at this scale** — about 135 GB with every picture kept, against 1.46 TiB free. → `preserve\retention_design.md`.

**★ THE BAR: `DEFAULT_FINE_BAR = 0.030242` ON `p_ge4`**, under `fine_head = twelve_sheets_drop_high_asymmetric_auc_ge4_more_k3`. The COLUMN stays `p_ge4`. The LEVEL is a **matched constant, not a discovered one**. **★ ⚠ A BAR IS UNREADABLE WITHOUT ITS HEAD** — two runs of ONE recipe on ONE corpus derived **0.022689 and 0.083975** at the same matched fraction, a factor of 3.7. Never carry a level across a fit. ⚠ `solve.Q4_BAR = 0.50` is the RENDER judge's constant. ⚠ There is no CLI spelling for the unbarred population: `--fine-bar 0` is a bar of zero and still excludes every unread row; `fine_bar=None` in process is the only way back. ⚠ `curate growth` and `curate solve k-sweep` inherit the bar. Provenance → `models/gallery_grade/README.md §Adopted 2026-09-10`.

**★ A THEMED PASS RELAXES THE BAR INSIDE ITS OWN CELL (Matt, 2026-09-11; shipped).** `solve.themed_fine_bar` = the lower of the shipped `fine_bar` and the `p_fine` of the **4n-th** best candidate among rows dominant in the cell, **floored at 0.01**; a rich cell keeps the shipped bar, a thin cell relaxes. **If the cell cannot fill even at the floor the gallery ships SMALL — there is no padding branch.** On the manifest as `config.themed_bar`. ⚠ The old defect is closed: the cell used to be taken from post-bar survivors, so its own stock was never what got measured. → `curation/GALLERY.md`.

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

**★ ⚠ A SMALL SMOKE MISPRICES A LEG TWICE OVER, IN OPPOSITE DIRECTIONS.** A 40-group smoke priced the owed arm at 18.105 engine-seconds a row against the leg's **24.296**, and read concurrency 2.61 against the leg's **2.945** — slow per row and slow to overlap at once, and one multiplied wall figure hides both. Price a leg off an OBSERVED leg. ⚠ Concurrency itself held 2.945–2.989 across three legs; that is not where estimates go wrong. ⚠ **A pilot's winners do not survive n.** The `direct_trap_multiply` pilot had two apparent winners at 487 candidates and neither margin held at 14× that.

## ROTATION — this era's subject

**★ THE FORWARD DRAW IS STANDING POLICY (Matt, 2026-09-11): every candidate is phase 0 plus four random rotations, keep the best by `p_fine`, repeat fixed at 1.** Every loser's phase and both columns are recorded — a store that keeps only the argmax is the selected-at-one-phase bias one level up.

**★ ROTATION IS EXCHANGEABLE WITH PHASE 0 — NO PHASE IS SPECIAL.** On 2,217 shots whose phase-0 control nothing selected on, a single rotation beats the control 53.0% of the time, flat across the turn (50.3–55.0%). ⚠ **The store arm's apparent near-phase advantage is SELECTION, not signal** — a store row is above the bar *because its phase-0 reading was*. The score surface has 4–10 turning points a turn, so there is nothing to hill-climb toward.

**★ WHAT BEST-OF-FIVE BUYS IS OPTIONALITY, AND THE ARGUMENT IS PRICE.** Control clears the fine bar 167 times against best-of-five's 414 — +147.9% — but the median lift is +0.0004 and the 82.0% win rate is what any exchangeable axis gives at best-of-5. Five different maps would buy the same lift at five times the cost. The dump economics that make it cheap → fractal-engine.

**★ BOTH HALVES OF THE STORE ARE NOW ROTATED.** The dumpable half went first — 9,402 rows, 0 remaining, 47,010 rotations; adopted and the row removed 3,468 · adopted and kept beside it 1,391 · left alone 4,543. The owed arm ran 2026-09-12 at **24.296 engine-seconds a row**, taking 1,752 of its 1,989 rows in its budget; **237 rows remain, about 33 minutes**. Verdict reproduced: 55.8% of rows won by a rotation against the smoke's 56.7%, and 62.3% on the mining arm. **Five protections are honoured, not two**: seated in any tentative gallery, carrying a human label, in a live release row, and the prune's own list. ⚠ **`sweep.remove` is a SECOND ledger-deleting transaction** and records its loss to the ratchet exactly as a prune does.

**★ NO LEDGER ROW IS MISFILED.** Every row digests back to the key it is filed under. The 43 "misfiled" rows were a REBUILD failure: `_resolve` reconstructed phase 0 at default palette knobs while all 43 carry a tuned `gamma` written by the label-import path. `Incumbent.pass_knobs` now carries **the difference from the plain pass** forward onto every rotation.

**★ A LEG STATES ITS RESOLVED SHARES AND ROSTER BEFORE PLANNING.** `depth.resolve_split` records the resolved table, what was asked, what was inherited, and whether the roster defaulted. The merge over `depth.SHARES` is unchanged deliberately — **the defect was the silence**.

**★ ⚠ `--budget` BOTH SIZES A PLAN AND SETS ITS DEADLINE**, so a leg handed its remaining clock plans a *smaller* draw and starts at the beginning. ⚠ A shot whose CONTROL never merged returns as a best-of-**four** read against the same control.

**★ ⚠ `--from-block` CANNOT RESUME A WHOLLY-RANKED LEG, AND DID NOT (2026-09-12).** The plan is a deterministic function of the POOL, and the pool shrinks by what the last leg merged: `ranked_bands` draws `hunt.drawable` **less `hunt.opened_locations`**, and a merge opens every location the leg decided, for good. Reconstructed both ways — put the 376 opened locations back and leg 1's blocks return 247 of 247 in order; take them out and the resume's return at indices 248–376 with **none of leg 1's anywhere in that plan**. So `--from-block 247` skipped 247 blocks of a *different* plan and bought a different slice. *Block N here is block N there* is true of the flags and false of the population. **Nothing was lost either night** — an unrendered location stays drawable — but on a wholly-ranked leg the index can neither re-render nor continue, and **the honest resume is to re-run with no index at all**.

**★ ⚠ THE DEDUPE FIRES ON ONE OF FIVE, AND ONLY ON ARMS THAT DRAW AT OPENED LOCATIONS.** `already_in_ledger` reading 0 is CORRECT on a ranked leg and is evidence of nothing. Unprotected are `near_band`, `mode_floor` and `conditioned`, which draw over `world["best"]`: there a re-run re-draws the same `(location, mode, colormap)` and the dedupe catches only the **winner**, since the four losers were freed and no row names them. Winner was the `k=0` control → the whole shot is discarded; winner was a rotation → best-of-**four** against the same control. On leg 1's split a re-entered block silently drops **38.5%** of its shots and re-prices **61.5%**. ⚠ `depth.SHARES` defaults `near_band` to 0.25, so a leg that does not spell `--shares` puts a quarter of its clock there. **The fix is to skip the whole SHOT on a hit — reported, not built.**

**★ A RECORD NOW SAYS WHERE TO RESUME FROM.** `counts.blocks_decided` and top-level **`resume_from_block`**; `resume_index(name)` recomputes it off the files, so older records answer too — `mine_ckpt120` → **247**, its resume → **376**, not the 647 the old arithmetic gives. `blocks_done` is unchanged and still counts whole chunks. `refuse_unreachable_resume` runs **before the population read** and refuses an index above the best matching leg on record; ⚠ it also catches an omitted `--rate`, since `rate=2.5` matches no record. ★ **A zero share is deliberately not part of the resume identity.** Store arm: `counts.groups_decided` beside `groups_done`, and **`rows_remaining` is the field to read** — `groups_done` rounds to whole chunks and does not convert.

**★ SWEEPING A LEG NO LONGER LEAVES IT MERGEABLE (2026-09-12).** `orphans --apply` declares the sweep in the leg's own directory and **both** merge paths refuse a leg carrying it — the shared door, and `rotation.merge`, which calls `sweep.remove` before reaching that door and whose removal of live rows is the irreversible half. Merge inputs are kept: they are a rounding error on disk and they are the leg's own history.

## THE PALETTE AXIS — PARKED

**★ MATT PARKED PALETTE REPLICATION ENTIRELY (2026-09-12).** Some repeats are better, but the benefit is too scarce and confined to a small part of one mode. **This supersedes the earlier "repetition is a production axis" ruling. All ROTATION work is kept.** `data/repeat_ab/` is a declared, empty attribute store; its code and tests stay by Matt's ruling. The partial A/B verdicts were released — ⚠ `labeling/server.py` has **no write path at all**, so an unexported sitting evaporates when the tab closes.

**★ WHAT THE LABELS SAID, BEFORE IT WAS PARKED.** 242 rows of 246 ingested, 121 usable pairs. Repeats lose overall — 17W/65T/39L, −0.273 tiers, p = 0.0046 — and the rungs separate: folded 4× exactly neutral, cyclic ×2 −0.171 (ns), cyclic ×3 a rout at 1 win against 20 losses and 0 of 29 on strange. On `smooth` alone: folded 4× +0.571, cyclic ×2 ≈ 0.000, cyclic ×3 −0.167. **65 of 121 pairs are ties, so the readable sample is 56.** The heads got both orderings right and every level wrong. ⚠ **`p_fine` is a CANDIDATE-geometry column** — re-scoring it at label geometry LOSES agreement, .768 → .714.

**★ THE PALETTE AXIS IS A BYTE-FOR-BYTE NO-OP ON THE FOUR DIRECT TRAPS.** The mechanics of `mirror`, `cycles` and the folded table → fractal-engine.

## MODES AND COLOUR

**★ `tia` AND `stripe` WERE NEVER PAUSED IN THE TREE (2026-09-12).** Both sit at weight 2, neither is in `UNMINED`, no roster names them — every leg has been drawing them throughout. The count Matt asked for: each is **14.4% of the ledger and 22–23% of everything above the fine bar**, the highest share after `smooth`, against **5.0% and 4.1% of human labels** (`smooth` holds 54.3% on 23.7% of the store). **They are thin in LABELS, not in supply.** Matt: continue mining them.

**★ THE `direct_trap_multiply` SWEEP PROPOSES NO ROSTER CHANGE (2026-09-12).** 6,885 candidates, 13,463 engine-seconds: nothing outside the shipped cells beats `@opacity=0.6`, which is also the **cheapest clear on the leg** at 26.4 engine-seconds. The only cell that reads higher, `@threshold=0.3`, covers the control in interval and costs 1.8× a candidate — 37% worse per clear. Opacity falls monotonically above 0.6; threshold peaks by 0.3. ⚠ **The promising axis is the dear one** — `threshold=0.45` is 2.57× `opacity=1` a candidate. The both-knobs corner stays retired (Matt's eye, ckpt 117). ⚠ Phoenix's realised share of both planes was **zero** and was cut from the sweep manifest.

**★ THE ORANGE-ON-BLUE SLICE IS WHY THIS ERA HAPPENED (Matt, 2026-09-10).** Filtering the n=1000 seating to hue family orange plus spiral gives 19 seats that read as one palette look. ⚠ **The themed path swaps the twin test for the geometry-only `Places` rule**, so nothing in a themed slice refuses two pictures for looking alike. Palette variety is at best a patch; the missing gate is the thing.

## RECORDS
**`20260911T022330Z` — the official n=1000 record under the adopted head, UNPUBLISHED** (filled 1000/1000, shortfall 0, worst 1.041483, sum 1451.098395, legs 454·279·170·97). ⚠ **It now predates three legs and two merges** — the ledger stood at 370,018 at the seating and reads **383,070** today. Earlier stamps order on superseded columns and are cited **purely for figure generation**. The site cites six stamps across 26 figures and is not to be re-based.

**★ ⚠ TWO STAMPS ARE UNDECLARED HARD DEPENDENCIES.** `20260906T133559Z` backs the site's `modes-gallery` curvature panel, seat `0cb93bec2bec2baf`, and `builder/picks.py` resolves it out of the wallpapers checkout — the website keeps no copy. `20260906T133236Z` is named by `data/gallery_grade/batches.jsonl` as the draw behind all three batches of the shipped label corpus, and `curation/k_sweep.py` reproduces its seating as the `K = 2` arm. **Neither is on any keep roster.**

**★ A RECORD'S OWN SEAT COUNT IS NOT WHAT DELETING IT RELEASES.** The 2026-09-12 clear summed to 8,200 against a measured release of **1,582** — 59 records deleted, 64.55 MiB, store 80 stamps → 35. The overstatement is structural where one cell is re-solved under many labels. **Measure `protected_keys()` either side; never sum.** ⚠ A solve directory with no tentative record confers no protection and frees nothing. ⚠ A diagnostic solve's records are swept at the boundary — `curation/GALLERY.md`.

## IN FLIGHT ACROSS THIS BOUNDARY
Nothing.

## QUEUED IN DRIVE `prompts\`
Nothing.

## NEXT CHECKPOINT GOAL
**Matt sets it at the top of the checkpoint.** Nothing is scheduled here.

## OPEN (ordered) — Matt raises each
1. **Continue mining.** ⚠ There is no valid index resume for the ranked arm — re-run with no index and let the shrunken pool define the plan.
2. **The owed remainder** — 237 rows, about 33 minutes.
3. **Mining the thin cells**, in order: `dark_vivid_lime`, `dark_muted_lime`, `dark_vivid_cyan`. ⚠ The themed bar relaxation does not manufacture candidates that do not exist — `dark_vivid_lime` held 51 rows at 48 places above the old bar, so its shortfall is supply.
4. **Themed collections at n=200.** The bar relaxation shipped and the path solves clean across eight cells; what is untouched is the product.
5. **The shot-level dedupe fix** — skip the whole shot on a hit, and make a resume name the pool it was planned against. Diagnosed, not built.
6. **The labelling protocol.** Matt's scale drifts ~0.4 tiers per 100 cards within a page and about a tier across an afternoon. ⚠ The standing rule bans calibration duplicates, drift probes and repeat rows.
7. **The coarse-4 labeling.** ⚠ A coarse 3 grades as a fine 1 (100 rows, mean 1.18).
8. **The tentative store beyond the keep list** — 35 stamps. Matt ruled on the themed series and the five baselines; the rest is unruled.
9. **The two undeclared hard-dependency stamps** — whether they go on the standing keep roster.
10. **`make_deterministic` in the remaining trainers.** Confirm it landed before relying on it. **No retrain on that account.**
11. **`pictures/` in the ten `runs` legs.** 5.37 GiB. **Matt: leave for now.** ⚠ Destructive; not for an unattended prompt.
12. **`carriers.jsonl`** at 65.9% of the 1 MiB guard; **`itinerary.jsonl`** at 62% of 786,432 (horizon → `palettes/README.md`).
13. **Website — REOPENED for a section-by-section review pass.** Matt brings a review doc for one section; Claude pushes back on anything wrong or not an improvement; once aligned, Claude writes the prose master and the placement prompt. Per-page status → `docs/page-review.md`, which is the only record — never keep a per-page list here.
14. **The reframe channel's cadence.**

Parked → `preserve\parked.md`.

## STATUS / KNOWN REDS
**NO KNOWN REDS.**

## RULINGS THIS ERA
→ `preserve\rulings_method.md §ckpt 122`, plus the domain rulings in the docs themselves and the in-repo promotions: `curation/LEGS.md`, `curation/MEASUREMENTS.md`, `curation/README.md`, `curation/GALLERY.md`, `labeling/README.md`, `palettes/README.md`, `tests/README.md`.

## KEEP LIST
Drive `prompts\`: **wipe everything** — nothing is queued and nothing is in flight. `reports\`: **wipe everything**.

Wallpapers `artifacts/sheet/`: `repeat_axis_smooth_render` and `repeat_axis_strange_render` are **labelled and ingested**, so the reason they were kept is spent; they are held only until Matt says otherwise. `repeat_ab_ckpt121` is gone.

Wallpapers `scratch/`: KEEP `place_radius_sheet/` (it backs the `PRESELECT_RADIUS` ruling); **WIPE everything else**. Website `scratch/`: unchanged.

## OWED
Nothing beyond the OPEN list.

## SCRATCH/ARTIFACT FLAGS
**★ THE STANDING KEEP ROSTER LIVES IN THE REPO — `src/fractal_wallpapers/README.md §The standing keep roster`.** ⚠ Nothing on it is protected by `orphans`' reference set.

⚠ **`artifacts/render_folds/` DOES NOT EXIST on either tier.**

⚠ **`.leveled/` DIRECTORIES ARE SWEEPABLE** — `orphans` reaches them by the name each JPEG would have. → `preserve\leveled_identity.md`.

⚠ **`orphans` lists pre-existing unmerged legs**, and ⚠ **a dated orphan verdict goes stale in hours** — re-read it, never carry it.

Per-checkpoint: new records are prune-protected like every record. `artifacts/curation/depth/*/fields` keeps growing at roughly 226 MB a leg and the sweep cannot reach it. ⚠ **CRLF drift is real**; `git ls-files --eol` is the door. ARCHIVED (RESTORE before reuse): unchanged from ckpt 106.

## PARKED / SETTLED
→ `preserve\INDEX.md`, which is current and lists all nineteen files. Never re-list them here.
