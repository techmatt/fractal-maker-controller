# fractal-state — checkpoint 121 (2026-09-11)

## Where we are
THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE: (1) the LOCATION hunt · (2) the WALLPAPER hunt · (3) the final curation SOLVE + release render. `MODE_POLICY` is the one place a mode carries a standing; Matt iterates from pictures, not counts. Phase 3 is Matt's eye on the final seating. **NO PUBLISHING OF ANY KIND until Matt raises it — never ask, never list it.**

**★ THE FINAL GALLERY SHIPS AT n=1000, and THEMED COLLECTIONS OF n=200 ARE PART OF THE PRODUCT.** Nothing has touched themed. n=2000 is not the direction; making n=1000 better is. "Better" means true quality, NOT maximizing `p_fine` — maximizing it would restrict the gallery to a tiny subset.

**★ THE BAR: `DEFAULT_FINE_BAR = 0.030242` ON `p_ge4`**, under `fine_head = twelve_sheets_drop_high_asymmetric_auc_ge4_more_k3`. The COLUMN stays `p_ge4`. The LEVEL is a **matched constant, not a discovered one**. **★ ⚠ A BAR IS UNREADABLE WITHOUT ITS HEAD** — two runs of ONE recipe on ONE corpus derived **0.022689 and 0.083975** at the same matched fraction, a factor of 3.7. Never carry a level across a fit; re-derive it against the pool of the day. ⚠ `solve.Q4_BAR = 0.50` is the RENDER judge's constant. ⚠ There is no CLI spelling for the unbarred population: `--fine-bar 0` is a bar of zero and still excludes every unread row; `fine_bar=None` in process is the only way back. ⚠ `curate growth` and `curate solve k-sweep` inherit the bar. Provenance → `models/gallery_grade/README.md §Adopted 2026-09-10`.

**★ HOLDING THE ADMITTED FRACTION IS NOT RAISING THE BAR.** The gate sits where it sat; the benefit is the ORDER inside the admitted pool, and the n=1000 cutoff does the selecting.

**★ THE SHIPPED HEAD'S CORPUS IS TRACKED, AND THAT IS WHAT MAKES THE COLUMN REBUILDABLE.** `data/gallery_grade/corpus/twelve_sheets/` holds `population.jsonl` (2,829 rows), `split.json` (split seed 20260910, 2,263 / 566), `targets.json`, `render_key_of.json`, plus `environment.json` and `checksums.json`. **Determinism rebuilds heads from seeds; only the corpus makes the seeds mean anything.** ⚠ Conditional on the box — torch 2.6.0+cu124, cuDNN 90100, RTX 2060 SUPER, `cudnn.benchmark` false.

**★ A FIT DID NOT REPRODUCE, AND THE FIX IS ONE CALL.** `models/train.make_deterministic` + `CUBLAS_WORKSPACE_CONFIG=:4096:8` set before torch imports; a whole 30-epoch run repeats bitwise. Cost +8% an epoch at the real horizon. ⚠ **A short verification run shares only EPOCH 0 with a long one.** **Matt's ruling: `make_deterministic` goes into every trainer, but NO retrain happens on that account.**

**★ THE `p_fine` COLUMN IS NOT IDENTIFIED, AND AVERAGING IS THE LEVER.** Seed-to-seed admitted-set churn 0.750; replicate churn with nothing varied 0.554; churn falls as `0.108 + 0.657/√k` out to k=8 with no knee. Average on the PROBABILITY scale, one vote per seed. ⚠ Averaging buys reproducibility against SEEDS, not kernels. Full arc → `preserve\gallery_grade_stability.md`.

**★ ⚠ A BEFORE/AFTER ACROSS A REFIT NEEDS A SAME-RECIPE REPLICATE AS CONTROL.**

**★ MATT REOPENED K HIMSELF AND SET IT; CLAUDE STILL NEVER PROPOSES REOPENING IT.** Not as a question, not as a closeout item, however strong the measurement pointing at it.

**★ THE COLOUR RULE IS ONE ARITHMETIC IN ONE UNIT SYSTEM: `ceiling.K = 3`, `ceiling.KF = 1`.** Ceiling `floor(K·n/48)+1` = 63 at n=1000; floor `floor(n/48)` = 20, with no `+1`. The floor is SOFT. **OFF on the themed path.** Full argument → `curation/GALLERY.md §K = 3 and Kf = 1`.

**★ ⚠ THE ALLOWANCE COUNTS MEMBERSHIPS, NOT SEATS.** ~1.802 memberships a seat at K=2 and ~2.118 at K=3. Convert a proposed K into membership units before arguing it.

**★ A `cell_floor:` STAMP SAYS WHICH LEG PLACED A SEAT, NOT THAT THE FLOOR BOUGHT IT.** Never read a leg stamp as a cause.

**★ WHAT HOLDS A THIN COLOUR DOWN IS NOT THE CEILING.** `location` and `the_leg_had_no_seat_left` refuse where `cell_allowance` used to. Mining the thin cells remains the instruction.

**★ GUARD RULINGS (Matt, 2026-09-10) — LOOSENING ONLY, AND NOTHING WAS LOOSENED.** Mode floors are as low as he will take them; the family distribution is fine; the spiral cap STAYS AT 0.10; the per-cell floor stays at 20. He judges a constant by what ENTERS and LEAVES the seating, on per-constant delta pages. ⚠ A delta page pairs departures with arrivals BY THE FREED SLOT.

**★ ⚠ THE SOLVER IS NOT AT ITS OPTIMUM**, which puts a noise floor under every objective comparison — the seed-plus-1-swap walk leaves at least 1.4 of sum on the table at n=1000. **A shadow price is not askable of this solver.**

**★ THE COLOUR FLOOR DOES NOT DRAG IN BAD PICTURES (measured, ckpt 119).**

**★ `PRESELECT_RADIUS` STAYS AT 0.02 (Matt, ckpt 118).**

**★ THE HUMAN VETO IS AGREED IN PRINCIPLE AND DELIBERATELY NOT SHIPPED (Matt, 2026-09-10).** A graded-1 seat is the end-to-end signal that something upstream is broken. **The escape count stays ON DEMAND.**

**★ ASYMMETRIC COST (Matt, 2026-09-10): KEEPING LOW-GRADED PICTURES LOW MATTERS MORE THAN KEEPING HIGH-GRADED PICTURES HIGH.** The shipped arm carries a 2× negative weighting.

**★ THE `p_fine` SEATING IS THE WAY; `rank_key` IS DEPRECATED AS AN OFFER AND NOTHING MORE.** **`rank_key` IS NOT RETIRABLE**: the cascade IS the rank key below the bar. ⚠ It does not read the fine head at all.

**★ `--forced` IS STAGED AND STAYS STAGED INDEFINITELY (Matt, ckpt 119).**

**★ THE FOLD MERGES INSTEAD OF DELETING, AND IT BOUGHT 71 OF 1,000 SEATS.** 6,683 places fold into 5,509 clusters. ⚠ No transitivity. **★ THE FOLD PICKS ITS SURVIVOR ON THE SEATING KEY**, stacked and never mixed.

**★ THE GALLERY-GRADE FATE PAGE IS GALLERY-GRADE ONLY**, and ⚠ its readings span two adoptions — no two are comparable. **★ ⚠ THE `gap` COLUMN ON A FATE CARD IS NOT A MARGIN**; it now reads `p_fine Δ`. **★ A FATE QUESTION NEEDS A RECORD TAKEN WITH `--explain-keys`.**

**★ THERE IS NO HONEST SCORE COLUMN OVER THAT POPULATION.** Every one of the 1,000 seats carries a manual verdict and the store is the head's own training material. **Matt's eye is the only independent read of a seating.**

**★ A RE-RENDER INVALIDATES EVERY READING TAKEN OFF THE PICTURE, NOT ONLY THE SCORE.** `recolour --keys` is the door and is idempotent.

**★ LEVELLING IS DECIDE-ONCE, REPLAY-UPWARD.** Nothing entered identity. ⚠ **But a recipe key carries the operator and the band and NEVER the curve the operator derived** — so a candidate that is a different recipe derives its own, and an inherited curve would file a picture under a name a re-render reproduces differently. 0.21 s a candidate.

**★ THE MINING LOOP DOES NOT ASK THE PALETTE HEAD.** The only live `Colorizer` is `curation.run`; `another_colour` has no caller. ⚠ **In the ARTICLE, act as if the palette network is still the proposal network** (Matt).

**★ AT n=1000 THE GALLERY IS SATURATED.** Mining buys option value for a later re-solve, and quality inside themes.

**★ GROUPS ARE PALETTE GROUPS AND MINING CANNOT MOVE THEM.** A new group needs a new MAP. ⚠ **A palette VARIANT is not a new group — all variants of a map count toward their base map's group cap (Matt's ruling, 2026-09-10)**, and `group_of` derives a variant's group from its base.

**★ `p_fine` COVERAGE IS CHECKABLE BEFORE A SOLVE.** ⚠ **`pool_scores.jsonl` is one-shot**: above-bar rows merged after the last `score-pool` are unseatable. **Mine → merge → score-pool → solve.** Nothing enforces that ordering. ⚠ `score-pool` writes `p_fine` **only above the render bar** — 43,022 of 374,309 rows read, 283,534 below the bar and not read. ⚠ `shipped_runs` is the single place answering *which checkpoints are this recipe's column*.

**★ A `score-pool` REFRESH MOVES MEMBERSHIP, NOT READINGS.** Of 38,813 rows present in both the old and new columns, **13 moved at all, by about 1e-7**. So a reading that shifts more than float noise across a refresh is a re-render rather than a refresh, and that is checkable.

**★ A THIRD NAMING AXIS: CORPUS · BAND · RECIPE.** ⚠ A recipe reproduces only if it consumes the random stream in the order it did the day it was fitted.

**★ THE SOLVE APPLIES A BAR OF ITS OWN**, on the WHOLE POOL, before the per-mode `headroom.bars` gate and before `preselect`. Two stacked gates.

**★ ALL THIRTEEN ACCEPTED MODES SEAT AT n=1000.** `ceiling.TAU = 0.034281`, `TWINS = 2`.

**⚠ SEATS-CHANGED IS NOT A MEASURE OF POOL CHANGE**, and **★ THE SEATING AMPLIFIES THE COLUMN**.

**⚠ ESTIMATES ARE MEASURED ON AN IDLE BOX, AND ON THE RIGHT POPULATION.**

**★ ⚠ WEIGH A MEASUREMENT AGAINST THE COST OF THE ACTION IT DECIDES, NOT AGAINST HOW INFORMATIVE IT IS.** When the human input is cheap and the population is well-defined, just do it.

## THE PALETTE AXIS — this era's subject

**★ PALETTE VARIATION RIDES `Palette.phase` AND `Palette.cycles`, THE ENGINE'S OWN `KEYED` MEMBERS.** No derived maps, no library admission, no carrier rows, none of the colour bookkeeping a new map costs. Continuous phase and `cycles = 1` are expressible, which the baked variants axis cannot do. A variant is a new row with its own key, never a mutation of the row it came from.

**★ THE PALETTE AXIS IS A BYTE-FOR-BYTE NO-OP ON THE FOUR DIRECT TRAPS** — no field, nothing for the traversal to act on. They draw bare and are excluded from every varied draw and every palette sheet.

**★ `mirror` IS A BAKE AND `cycles` IS AN INDEX; THEY COMPOSE MULTIPLICATIVELY.** The fold happens before the OKLab conversion, so a folded map is a different 4096-entry table; `Palette::place` wraps the index into whatever table was baked. **Mirror on with `cycles = 2` is FOUR traversals of the base ramp.** For a non-cyclic map, "double it once" is `cycles = 1` **with the mirror on** — which is what production already spells, so **every non-cyclic picture this project ships is already a 2× traversal** and the repetition ladder there is EVEN-ONLY: 2×, 4×, 6×, with no 3× reachable.

**★ `mirror` IS DERIVED FROM THE MAP'S `kind`, NEVER DRAWN.** `hunt.Maker.palette_for` refuses a draw that sets it. Over all 374,309 ledger rows and all 80 gallery records the rule holds without exception in both directions: **non-cyclic unmirrored is ZERO, cyclic mirrored is ZERO.** **Matt's ruling: we are not shipping unmirrored non-cyclic pictures, so we do not start.** The arm is closed.

**★ THE FOLDED TABLE CLOSES, SO A REPEAT HAS NO SEAM.** `mirror()` writes the opening colour again at position 1.0; across all 156 sequential maps the folded wrap step is **exactly 0.0** in OKLab against an inside step up to 7.0e-3, while the same maps unfolded wrap at a median 0.693 — 284× to 956× their own gradient. `finished_import`'s refusal of `mirror` + `cycles != 1` was wrong and is **gone**, and the `phase != 0` half went with it: a closed table has no privileged start. ⚠ **`finished_import` governs MAKER-ERA paths only and never new labels** — `label build` → `sheets.finished_source` → page → `label ingest` carries the recipe whole. Reading it as if it gated new labels is the trap.

**★ ROTATION IS EXCHANGEABLE WITH PHASE 0 — NO PHASE IS SPECIAL.** On 2,217 shots whose phase-0 control nothing selected on, a single rotation beats the control 53.0% of the time and the win rate is FLAT across the turn (50.3–55.0%). ⚠ **The store arm's apparent near-phase advantage (41.3% inside 0.05 turns against 12–15% past 0.20) is SELECTION, not signal** — a store row is above the bar *because its phase-0 reading was*, so its near neighbours inherit the hill. The score surface has 4–10 turning points a turn, so there is nothing to hill-climb toward and dense sampling buys only near-neighbours.

**★ WHAT BEST-OF-FIVE BUYS IS OPTIONALITY, AND THE ARGUMENT IS PRICE.** Control clears the fine bar 167 times against best-of-five's 414 — +147.9% — but the median lift is +0.0004 and the 82.0% win rate is what any exchangeable axis gives at best-of-5. Five different maps would buy the same lift at five times the cost. **Six candidates cost one and a quarter renders, not six** — 0.516 engine-seconds a rotation against 2.579 a row, because the field dump amortises per (location, mode).

**★ THE FORWARD DRAW IS STANDING POLICY (Matt, 2026-09-11): every candidate is phase 0 plus four random rotations, keep the best by `p_fine`, repeat fixed at 1.** Every loser's phase and both columns are recorded — a store that keeps only the argmax is the selected-at-one-phase bias one level up.

**★ THE STORE WAS A SELECTED-AT-PHASE-0 POPULATION AND THE DUMPABLE HALF IS NOW ROTATED.** The whole rotatable passing set went through `curate rotate` — 9,402 rows, 0 remaining, 47,010 rotations. Adopted and the row removed 3,468 · adopted and kept beside it 1,391 · left alone 4,543. **Five protections are honoured, not two**: seated in any tentative gallery, carrying a human label, in a live release row, and the prune's own list. ⚠ **`sweep.remove` is a SECOND ledger-deleting transaction** and records its loss to the ratchet exactly as a prune does — the property was never that there is one deletion site, it is that every site writes down what it took.

**★ ⚠ SWEEPING A LEG DOES NOT UN-DECIDE IT.** `orphans --leg … --apply` takes pictures and nothing else, so a swept leg keeps `rows.jsonl`, `scores.jsonl` and `removed.jsonl` — and `curate rotate merge` would still run on them, upserting rows naming pictures that no longer exist and removing live rows in exchange. Neither merge path asks whether a picture is on disk. Closed for `owed_smoke_ckpt120` by deleting its three merge inputs; **whether the sweep itself should do that is Matt's decision and is open.** → `curation/README.md`.

**★ NO LEDGER ROW IS MISFILED.** All 374,309 digest back to the key they are filed under. The 43 "misfiled" rows were a REBUILD failure: `_resolve` reconstructed phase 0 at default palette knobs while all 43 carry a tuned `gamma` (20 with `reverse`, 18 with a different `transfer`) written by the label-import path, and all 43 carry a human label. `Incumbent.pass_knobs` now carries **the difference from the plain pass** forward onto every rotation — the difference and not the whole pass — and all 6,036 rotatable rows reproduce.

**★ A LEG STATES ITS RESOLVED SHARES AND ROSTER BEFORE PLANNING.** `depth.resolve_split` announces both and records the resolved table, what was asked, what was inherited, and whether the roster defaulted. The merge over `depth.SHARES` is unchanged deliberately — merging is the better default; **the defect was the silence**. ⚠ **RETRACTED: the claim that merged shares cost `mine_ckpt120` half its clock is FALSE.** Its resolved shares were `ranked_bands 1.0` with every other arm at 0, all 2,954 decision rows carry that arm, and `MINE_SHARES` was already spelled whole before that leg ran.

**★ ⚠ `--budget` BOTH SIZES A PLAN AND SETS ITS DEADLINE**, so a leg handed its remaining clock plans a *smaller* draw and starts at the beginning. `--plan-budget` (rebuild the first leg's plan exactly) plus `--from-block` (skip what it did) is the resume. ⚠ A shot whose CONTROL never merged returns as a best-of-**four** read against the same control — a different number under the same name.

**★ THE OWED ARM IS PRICED AND DEFERRED.** 1,989 passing rows on the composites and `itinerary` cannot dump and rotate at **18.105 engine-seconds a row against the dumpable arm's 2.579 — 7.0×**, projecting to about **3 h 50 m**. Matt ruled it worth the price; the leg is deferred, not cancelled. `--owed` **swaps** arms rather than widening, because a dumpable row's four losers are freed rather than merged and the dedupe would not stop a re-run of the cheap half. Composites rotate slightly BETTER: 56.7% against 51.7%.

**★ REPETITION IS A PRODUCTION AXIS (Matt) AND THE HEADS CANNOT READ IT.** `cycles != 1` is 2,262 rows of 374,309, and **1,713 of those also carry a rotation**, so the pool's existing repeat coverage is confounded with the axis `curate rotate` just measured. Holding phase at 0 in a repetition batch is load-bearing, not tidiness. ⚠ **The coarse-versus-fine split does not survive measurement**: the two heads move the same direction on 69.9% of pairs and their disagreements split 18/19 — noise, not a systematic miscalibration.

**★ THE REPEAT SHEETS ARE RENDERED AND AWAIT MATT'S EYE.** `artifacts/sheet/repeat_axis_smooth_render` (70 tiles) and `repeat_axis_strange_render` (176) — **246 tiles in 123 pairs**, every pair whole on one sheet, matched within recipe at phase 0. Serve with `label serve --sheet <dir> --port 8020`; drops land at `labels/<head>.repeat_axis_<head>_20260911.json`. ⚠ **The batch oversamples the axis ~82×** (0.605% of the ledger against 50% of the batch) and **the rows are pair-dependent** — only the within-pair difference is readable, and 246 rows are not 246 draws. Filed as `OVERSAMPLED-AXIS` in `data/batch_caveats.md`. The heads' own reading, for Matt to overrule: the folded 4× arm is liked and the cyclic arm is not (62.5% against 38.6% on P≥4), and `smooth` is liked while everything else is not (68.6% against 36.4% on the fine head). **Whether any of it survives his eye is the point.**

**★ THE ORANGE-ON-BLUE SLICE IS WHY THIS ERA HAPPENED (Matt, 2026-09-10).** Filtering the n=1000 seating to hue family orange plus spiral gives 19 seats that read as one palette look. ⚠ **That slice is a preview of a themed n=200 collection, and the themed path swaps the twin test for the geometry-only `Places` rule** — τ is not in the themed path, so nothing in a themed slice refuses two pictures for looking alike. Palette variety is at best a patch over that; the missing gate is the thing.

## RECORDS
**`20260911T022330Z` — the official n=1000 record under the adopted head, UNPUBLISHED** (filled 1000/1000, shortfall 0, worst 1.041483, sum 1451.098395, legs 454·279·170·97). ⚠ **It predates every merge of this era** — the ledger stood at 370,018 then and stands at **374,309** now, and `score-pool` has been refreshed since. Earlier stamps order on superseded columns and are cited **purely for figure generation**. The site cites six stamps across 26 figures and is not to be re-based.

## IN FLIGHT ACROSS THIS BOUNDARY
Nothing.

## QUEUED IN DRIVE `prompts\`
Nothing.

## NEXT CHECKPOINT GOAL
**Matt sets it at the top of the checkpoint.** Nothing is scheduled here.

## OPEN (ordered) — Matt raises each
1. **The repeat sheets** — Matt labels them next checkpoint. Then he decides for himself whether a retrain follows; the decision is his and is not Claude's to propose.
2. **The owed composite / `itinerary` rotation.** 1,989 rows, ~3 h 50 m, ruled worth the price, deferred.
3. **Resume the mining arm.** 560 of 960 blocks unstarted: `curate rotate mine --name m2 --plan-budget 14400 --from-block 400 --budget <clock>`.
4. **`tia` and `stripe` are PAUSED.** Matt wants the total accepted-recipe count per rendering type and will judge from that — a next-session TODO, and the near band's `--modes smooth stripe tia` fix waits on the same decision.
5. **Should `orphans --leg … --apply` delete a swept leg's merge inputs?** A decision about what naming a leg means.
6. **Mining the thin cells**, in order: `dark_vivid_lime`, `dark_muted_lime`, `dark_vivid_cyan`.
7. **The labelling protocol.** Matt's scale drifts ~0.4 tiers per 100 cards within a page and about a tier across an afternoon. ⚠ The standing rule bans calibration duplicates, drift probes and repeat rows.
8. **The coarse-4 labeling.** ⚠ A coarse 3 grades as a fine 1 (100 rows, mean 1.18).
9. **Themed collections at n=200.** Part of the product, untouched. ⚠ The colour floor is OFF and the twin test is swapped for `Places` on the themed path.
10. **The parameter sweep for `direct_trap_multiply`.** Opacity and threshold as swept ranges, `both` excluded.
11. **`make_deterministic` in the remaining trainers.** Folded into `palette_variant_smoke_ckpt120`; confirm it landed before relying on it. **No retrain on that account.**
12. **`pictures/` in the ten `runs` legs.** 5.37 GiB. ⚠ Destructive; not for an unattended prompt.
13. **Records-only picture retention.** → `preserve\retention_design.md`.
14. **`carriers.jsonl`** at 65.9% of the 1 MiB guard; **`itinerary.jsonl`** at 62% of 786,432.
15. **Website — REOPENED for a section-by-section review pass.** Matt brings a review doc for one section; Claude pushes back on anything wrong or not an improvement; once aligned, Claude writes the prose master and the placement prompt. Two sections are through: **Color palettes v6** and **Finding good wallpapers v3**. Per-page status → `docs/page-review.md`.
16. **The reframe channel's cadence.**

Parked → `preserve\parked.md`. ⚠ The parked "K re-sweep (never propose it)" entry is superseded in fact but the instruction to Claude stands.

## STATUS / KNOWN REDS
**NO KNOWN REDS.** Last reading: fast **4,317 selected / 136 deselected — 4,453 collected — 148.91 s**; slow **4,453 of 4,453 in 542.82 s**; `cargo test` 217 passed, clippy clean. ⚠ **The lane refuses the wrong interpreter at the door** (waived with `FRACTAL_WALLPAPERS_ANY_INTERPRETER=1`).

**★ TEST LANES ARE MATT'S TO MANAGE (ruled 2026-09-09).** He runs them when he judges them important. Claude does not track the slow lane, does not flag it as owed, does not chase a paired reading or a stale collected count, and does not spend a line on it.

⚠ **`test_nested_verbs.py`'s surface table pins the flags each verb's handler reads** — it is the only thing in the tree that catches a flag wired to a parser and never read, so it is MEANT to go red when a command group or flag is added.

## RULINGS THIS ERA
→ `preserve\rulings_method.md §ckpt 121`, plus the domain rulings in the docs themselves and the in-repo promotions: `curation/LEGS.md`, `curation/MEASUREMENTS.md`, `curation/README.md`, `labeling/README.md`, `palettes/README.md`.

## KEEP LIST
Drive `prompts\`: **wipe everything** — nothing is queued and nothing is in flight. `reports\`: **wipe everything** — every report of this era was read and its findings are in these docs or in-repo.

Wallpapers `artifacts/sheet/`: **★ KEEP `repeat_axis_smooth_render` AND `repeat_axis_strange_render`** — 246 unlabelled tiles awaiting Matt's eye. Wiping them throws away the batch.

Wallpapers `scratch/`: KEEP `place_radius_sheet/` (it backs the `PRESELECT_RADIUS` ruling); **WIPE everything else**. Website `scratch/`: unchanged.

## OWED
Nothing beyond the OPEN list.

## SCRATCH/ARTIFACT FLAGS
**★ THE STANDING KEEP ROSTER LIVES IN THE REPO — `src/fractal_wallpapers/README.md §The standing keep roster`.** ⚠ Nothing on it is protected by `orphans`' reference set.

⚠ **`artifacts/render_folds/` DOES NOT EXIST on either tier.**

⚠ **`.leveled/` DIRECTORIES ARE SWEEPABLE** — `orphans` reaches them by the name each JPEG would have. → `preserve\leveled_identity.md`.

⚠ **`orphans` lists 10 pre-existing unmerged legs.** The picture census reads **374,309 rows, 374,309 with a picture on disk, 0 naming an absent one**.

Per-checkpoint: new records are prune-protected like every record. `artifacts/curation/depth/*/fields` keeps growing at roughly 226 MB a leg and the sweep cannot reach it. ⚠ **CRLF drift is real**; `git ls-files --eol` is the door. ARCHIVED (RESTORE before reuse): unchanged from ckpt 106.

## PARKED / SETTLED
→ `preserve\parked.md`, `preserve\rulings_corpus.md`, `preserve\rulings_curation.md`, `preserve\rulings_sourcing.md`, `preserve\rulings_engine.md`, `preserve\rulings_website.md`, `preserve\rulings_method.md`, `preserve\sourcing_channel_laws.md`, `preserve\retention_design.md`, `preserve\solver_design.md`, `preserve\leveled_identity.md`, `preserve\gallery_grade_stability.md`, `preserve\deep_shelf.md`. The old `settled_rulings.md` is a stub index.
