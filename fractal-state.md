# fractal-state — checkpoint 120 (2026-09-10)

## Where we are
THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE: (1) the LOCATION hunt · (2) the WALLPAPER hunt · (3) the final curation SOLVE + release render. `MODE_POLICY` is the one place a mode carries a standing; Matt iterates from pictures, not counts. Phase 3 is Matt's eye on the final seating. **NO PUBLISHING OF ANY KIND until Matt raises it — never ask, never list it.**

**★ THE FINAL GALLERY SHIPS AT n=1000, and THEMED COLLECTIONS OF n=200 ARE PART OF THE PRODUCT.** Nothing has touched themed. n=2000 is not the direction; making n=1000 better is. "Better" means true quality, NOT maximizing `p_fine` — maximizing it would restrict the gallery to a tiny subset.

**★ THE BAR: `DEFAULT_FINE_BAR = 0.030242` ON `p_ge4`, ADOPTED 2026-09-10**, under `fine_head = twelve_sheets_drop_high_asymmetric_auc_ge4_more_k3`. The COLUMN stays `p_ge4`; the band cleared **12 of 12, worst margin +0.115**, over the 466 stopping rows both incumbents are readable on, with the bar registered before any run of the band. The LEVEL is a **matched constant, not a discovered one**: the point admitting the fraction the previous head admitted — 27.76%, 11,743 of 42,300. **★ ⚠ A BAR IS UNREADABLE WITHOUT ITS HEAD, AND THIS IS NOW MEASURED RATHER THAN ARGUED** — two runs of ONE recipe on ONE corpus derived **0.022689 and 0.083975** at the same matched fraction, a factor of 3.7. Never carry a level across a fit; re-derive it against the pool of the day. ⚠ **Six other sites named the old 0.184** — two CLI, two solve, one label-fate, plus `GALLERY.md` and four prose sites. A level really is written down everywhere. ⚠ `solve.Q4_BAR = 0.50` is the RENDER judge's constant and did NOT move. ⚠ There is no CLI spelling for the unbarred population: `--fine-bar 0` is a bar of zero and still excludes every unread row; `fine_bar=None` in process is the only way back. ⚠ `curate growth` and `curate solve k-sweep` inherit the bar. Provenance → `models/gallery_grade/README.md §Adopted 2026-09-10`.

**★ HOLDING THE ADMITTED FRACTION IS NOT RAISING THE BAR.** The gate sits where it sat; the benefit is the ORDER inside the admitted pool, and the n=1000 cutoff does the selecting. Do not let a later reading conflate the two.

**★ THE SHIPPED HEAD'S CORPUS IS TRACKED, AND THAT IS WHAT MAKES THE COLUMN REBUILDABLE.** `data/gallery_grade/corpus/twelve_sheets/` holds `population.jsonl` (2,829 rows), `split.json` (split seed 20260910, 2,263 / 566), `targets.json`, `render_key_of.json`, plus `environment.json` and `checksums.json`; the lane re-hashes all five, both writers refuse a frozen corpus, and two are in `LARGE_TEXT_ALLOWLIST` because the point of tracking them is that their checksum still checks. **Determinism rebuilds heads from seeds; only the corpus makes the seeds mean anything**, and `build_corpus.py` re-run against a grown store does not give it back. ⚠ The promise is also conditional on the box — torch 2.6.0+cu124, cuDNN 90100, RTX 2060 SUPER, `cudnn.benchmark` false.

**★ A FIT DID NOT REPRODUCE, AND THE FIX IS ONE CALL.** Identical seeds, rows and code parted at the **first epoch's training loss** (0.974680 vs 0.972807) on nondeterministic CUDA kernels; a flat AUC surface (mean |Δ| 0.027) turned that into checkpoint epoch 29 against epoch 4, and **516 of 1,000 seats**. Under `use_deterministic_algorithms(True)` + `CUBLAS_WORKSPACE_CONFIG=:4096:8` set before torch imports, a whole 30-epoch run repeats bitwise — 834 checkpoint tensors, zero disagreements. `models/train.make_deterministic` **refuses** when the variable is absent. **Cost is +8% an epoch at the real horizon** (5.40 s vs 5.00); a three-epoch probe cannot see it because the warm-up epoch swamps it. ⚠ **A short verification run shares only EPOCH 0 with a long one** — `CosineAnnealingLR`'s `T_max` is the epoch ceiling — so verify determinism at epoch 0 of the real run, never against a short proxy. **Matt's ruling: `make_deterministic` goes into every trainer, but NO retrain happens on that account** until a retrain is worth doing on its own merits.

**★ THE `p_fine` COLUMN IS NOT IDENTIFIED, AND AVERAGING IS THE LEVER.** Seed-to-seed admitted-set churn 0.750; **replicate churn with nothing varied 0.554**; churn falls as `0.108 + 0.657/√k` out to k=8 **with no knee**, so where to stop is a cost decision and not a discovered point. Average on the PROBABILITY scale, one vote per seed — a mean of logits is a different column and only one of them is the scale a bar cuts on. ⚠ **Averaging buys reproducibility against SEEDS, not against the kernels**: a k=3 ensemble's replicate churn was 0.564, no better than a single head's floor. Full arc → `preserve\gallery_grade_stability.md`.

**★ ⚠ A BEFORE/AFTER ACROSS A REFIT NEEDS A SAME-RECIPE REPLICATE AS CONTROL.** This is a method rule, not a fractal fact. **RETRACTED: the ckpt-119 "93.3% symmetric churn across the adoption" and the 784-of-1,000 seat turnover are not attributable to the adoption** — both sit inside what two runs of one recipe do. The companion ckpt-119 observation that distinct places fell 6,683 → 6,235 carries the same caveat and is not a finding either.

**★ MATT REOPENED K HIMSELF AND SET IT; CLAUDE STILL NEVER PROPOSES REOPENING IT.** The standing instruction is unchanged in force: Claude does not propose reopening K — not as a question, not as a closeout item, however strong the measurement pointing at it. Matt raises it when he wants it.

**★ THE COLOUR RULE IS ONE ARITHMETIC IN ONE UNIT SYSTEM: `ceiling.K = 3`, `ceiling.KF = 1`.** Every cell gets at least one fair share and at most three. Ceiling `floor(K·n/48)+1` = 63 at n=1000; floor `floor(n/48)` = 20, **with no `+1`**. The floor is SOFT — carried as floor shortfall in the lexicographic objective beside the mode floors, after tier order and before worst-seated. **OFF on the themed path.** Both on the tracked manifest as `config.ceiling.{k,kf,floor,floor_rule}`; a manifest with no `kf` predates 2026-09-09. Full argument → `curation/GALLERY.md §K = 3 and Kf = 1`.

**★ ⚠ THE ALLOWANCE COUNTS MEMBERSHIPS, NOT SEATS, AND THAT IS THE TRAP.** ~1.802 memberships a seat at K=2 and ~2.118 at K=3. **Convert a proposed K into membership units before arguing it.** → `GALLERY.md §★ The rule counts MEMBERSHIPS and not seats`, mirrored in `curation/ceiling.py`'s `K` docstring.

**★ A `cell_floor:` STAMP SAYS WHICH LEG PLACED A SEAT, NOT THAT THE FLOOR BOUGHT IT — AND THIS HAS NOW MISLED THREE READINGS.** Under the shipped head the floor stamps 279 seats and **holds 29 memberships**, across three lime cells; the rest are seats the general pool would have placed in a different order. **RETRACTED on the same error: both the "cell_floor buys bad seats at 17.9%" reading and its correction naming `mode_floor` the worse leg.** Held inside one sitting the four legs are indistinguishable (2.09 / 2.01 / 2.00 / 2.18). Never read a leg stamp as a cause.

**★ WHAT HOLDS A THIN COLOUR DOWN IS NOT THE CEILING.** `location` and `the_leg_had_no_seat_left` refuse where `cell_allowance` used to. ⚠ **RETRACTED: the "spiral cap is what refuses thin-cell rows" reading** — raising the cap to 0.15 relieved the lime cells not at all and simply put `dark_vivid_yellow` at the floor beside them. Mining the thin cells remains the instruction. → `GALLERY.md`.

**★ GUARD RULINGS (Matt, 2026-09-10) — LOOSENING ONLY, AND NOTHING WAS LOOSENED.** He raised the guards himself and will consider loosening but nothing more restrictive. **Mode floors are as low as he will take them; the family distribution is fine as it stands; the spiral cap STAYS AT 0.10** — he read the 0.15 delta page and judged it too many spirals — **and the per-cell floor stays at 20.** He judges a constant by what ENTERS and LEAVES the seating, on per-constant delta pages, not by browsing the gallery whole. ⚠ **A delta page pairs departures with arrivals BY THE FREED SLOT** — a solve is global, so it is a budget reallocation and never a 1:1 swap; say so on the page.

**★ ⚠ THE SOLVER IS NOT AT ITS OPTIMUM, WHICH PUTS A NOISE FLOOR UNDER EVERY OBJECTIVE COMPARISON.** Three tightenings out of three returned a **better** objective, two dominating the baseline outright: the seed-plus-1-swap walk leaves at least **1.4 of sum** on the table at n=1000. Both cell-floor doses gained less than or barely more than that, which is why they were not taken. **A shadow price is not askable of this solver** — "demand one more seat and read the cost" only reads as a price at an optimum.

**★ THE COLOUR FLOOR DOES NOT DRAG IN BAD PICTURES (measured, ckpt 119).** Its labeled block was the BEST of four at mean 2.69. The floor's cost is in **which cells it reaches**.

**★ `PRESELECT_RADIUS` STAYS AT 0.02 (Matt, ckpt 118).** Do not reopen it as a question.

**★ THE HUMAN VETO IS AGREED IN PRINCIPLE AND DELIBERATELY NOT SHIPPED (Matt, 2026-09-10).** A row Matt graded 1 should not enter the pool — but building it would **hide bugs and flaws in the method**, because a graded-1 seat is the end-to-end signal that something upstream is broken. Priced: removing every graded-1 row is affordable at grade 1 and opens a `direct_trap_lines` shortfall at ≤2. **The escape count stays ON DEMAND** — something a prompt asks for when Matt wants it, never computed or stored at solve time. Do not propose shipping the veto until he raises it.

**★ ASYMMETRIC COST (Matt, 2026-09-10): KEEPING LOW-GRADED PICTURES LOW MATTERS MORE THAN KEEPING HIGH-GRADED PICTURES HIGH.** A picture graded 1 escaping upward is the expensive error; a 4 falling below the bar is cheap — 42,300 candidates compete for 1,000 seats, so a missed good picture has substitutes and an admitted bad one is visible. He chooses an operating point off an escape-rate / grade-4-loss trade curve, never a single symmetric answer. The shipped arm carries a 2× negative weighting.

**★ THE `p_fine` SEATING IS THE WAY; `rank_key` IS DEPRECATED AS AN OFFER AND NOTHING MORE.** `--key` offers `{cascade, p_ge4}`; `solve.KEYS` still holds all three. **`rank_key` IS NOT RETIRABLE**: the cascade IS the rank key below the bar. ⚠ **`rank_key` does not read the fine head at all**, so a fine-head adoption cannot move it.

**★ `--forced` IS STAGED AND STAYS STAGED INDEFINITELY (Matt, ckpt 119).** Not dead code; retiring it would be a ruling like an adoption. → `GALLERY.md §--forced`.

**★ THE FOLD MERGES INSTEAD OF DELETING, AND IT BOUGHT 71 OF 1,000 SEATS (ckpt 118).** An absorbed place's rows stay in the pool carrying the survivor's cluster id; one-per-location becomes one-per-cluster with no new rule kind. `--fold delete` keeps the old destructive walk selectable. **6,683 places fold into 5,509 clusters.** ⚠ **No transitivity** — a star forest of depth one, and `preselect` raises if that fails.

**★ THE FOLD PICKS ITS SURVIVOR ON THE SEATING KEY** — `distinct.offered_at`, `p_fine` where read and raw `P(≥4)` where not, **stacked and never mixed**. A record with no `key` folded on `p_ge4`.

**★ `solve.strongest_locations` IS `solve.strongest_clusters`, AND IT WAS NEVER USED.** A consistency fix, not a correctness win; `pool.reachable_locations` is `reachable_clusters`, so the old name dates a record.

**★ THE GALLERY-GRADE FATE PAGE IS GALLERY-GRADE ONLY.** ⚠ Its readings span two adoptions now and **no two are comparable** — ceiling, floor, column and level all moved. Whether a coarse 4 is a gallery-grade 4 remains open and is NOT a fate question. → `curation/README.md`.

**★ ⚠ THE `gap` COLUMN ON A FATE CARD IS NOT A MARGIN AND NEVER WAS.** The two rows on a card never competed; the column now reads `p_fine Δ` with the placing leg named ahead of it. Any "how close did this row come" reading off the old column is void.

**★ THERE IS NO HONEST SCORE COLUMN OVER THAT POPULATION, AND IT IS NOW TOTAL.** Every one of the 1,000 seats carries a manual verdict and the store is the head's own training material, so `p_fine` is recognition for every row on the page. **Matt's eye is the only independent read of a seating.**

**★ A FATE QUESTION NEEDS A RECORD TAKEN WITH `--explain-keys`.**

**★ THE 10,664 BARE-DRAWN ROWS ARE REPAIRED AND THE HOLE CLASS IS CLOSED.** Six renderers carried it; all six build through one `release.task_for` with no defaults. ⚠ The ckpt-117 reading that the repair collapsed the mode was SEATS, not population.

**★ A RE-RENDER INVALIDATES EVERY READING TAKEN OFF THE PICTURE, NOT ONLY THE SCORE.** `recolour --keys` is the door and is idempotent.

**★ LEVELLING IS DECIDE-ONCE, REPLAY-UPWARD.** Nothing entered identity; `key_of` byte-identical over 20,000 live rows. **6,466 replayable, 623 no-operator, 0 outstanding.**

**★ THE MINING LOOP DOES NOT ASK THE PALETTE HEAD.** The only live `Colorizer` is `curation.run`; `another_colour` has no caller. ⚠ **In the ARTICLE, act as if the palette network is still the proposal network** (Matt) — a doc fact, not a website correction.

**★ MINING FOCUS (Matt, 2026-09-10): MINE AWAY FROM `tia` AND `stripe`** — overrepresented; he accepts them at roughly **5% of WALL-CLOCK each** (not 5% of attempts), ~90% to the rest. ⚠ Modes differ several-fold in cost a candidate, so a weight is not a share — set whatever the manifest takes and then **report the realized wall-clock share**.

**★ THE `both` SETTINGS CORNER IS RETIRED BY MATT'S EYE**, and **THE FRAME IS A PARAMETER SWEEP, NOT A ROSTER VERDICT**: exclude always-bad ranges and sweep the rest.

**★ AT n=1000 THE GALLERY IS SATURATED.** Mining buys option value for a later re-solve, and quality inside themes, rather than visible movement at this n.

**★ GROUPS ARE PALETTE GROUPS AND MINING CANNOT MOVE THEM.** A new group needs a new MAP. ⚠ `map:river-of-light-25` takes 24 of 25.

**★ THE NEAR BAND'S CEILING IS A MANIFEST/ROSTER MISMATCH, NOT PAIR ROOM (ckpt 118).** All three band arms of the 2026-09-09 leg stopped early on an EMPTY PLAN and were never clock-bound. The fix is one flag: `--modes smooth stripe tia`. **Breadth refills the band at 19–21% of the places it opens.**

**★ `p_fine` COVERAGE IS CHECKABLE BEFORE A SOLVE.** ⚠ **`pool_scores.jsonl` is one-shot**: above-bar rows merged after the last `score-pool` are unseatable. **Mine → merge → score-pool → solve.** Nothing enforces that ordering. ⚠ A re-score PRESERVES the outgoing column automatically. ⚠ `score-pool` now reads **k checkpoints over one decode pass**, and `shipped_runs` is the single place answering *which checkpoints are this recipe's column* — the median seed for `inherited`, every seed for the shipped one.

**★ A THIRD NAMING AXIS LANDED: CORPUS · BAND · RECIPE.** A corpus is which rows, a band is which stopping rule, a recipe is which knobs — and the shipped one moves four at once. `--recipe` is on every verb naming a run; `inherited` keeps bare names. ⚠ **A recipe reproduces only if it consumes the random stream in the order it did the day it was fitted**, which is why the eval slice decodes serially: a `DataLoader` draws a base seed when its iterator is made, so a build-the-cache branch consumes RNG a read-the-cache branch does not.

**★ THE SOLVE APPLIES A BAR OF ITS OWN**, on the WHOLE POOL, before the per-mode `headroom.bars` gate and before `preselect`. Two stacked gates.

**★ ALL THIRTEEN ACCEPTED MODES SEAT AT n=1000.** `ceiling.TAU = 0.034281`, `TWINS = 2`.

**⚠ SEATS-CHANGED IS NOT A MEASURE OF POOL CHANGE.** Never read a seat-for-seat diff as a finding. **★ AND THE SEATING AMPLIFIES THE COLUMN** — an admitted set churning 0.564 gave seats churning 1.032, because the seating is a lexicographic argmax over that set. Two columns this far apart cannot give a near-miss.

**⚠ ESTIMATES ARE MEASURED ON AN IDLE BOX, AND ON THE RIGHT POPULATION.**

**⚠ A NEW COLUMN RESOLUTION INSIDE A HOT PATH COSTS THE LANE.**

**★ ⚠ WEIGH A MEASUREMENT AGAINST THE COST OF THE ACTION IT DECIDES, NOT AGAINST HOW INFORMATIVE IT IS.** When the human input is cheap and the population is well-defined, just do it. A study earns its place when it would stop an expensive commitment or when the target is genuinely ambiguous — the seed-variance study earned it by showing that more labels was the wrong lever; a two-hour experiment to aim a fifteen-minute labelling round did not.

**This era (ckpt 119→120, one day).** The whole era was the `p_fine` head. Instability was traced to the fit rather than the labels (replicate floor 0.554), averaging found to fix it as `1/√k`, an augmentation sweep run (the crop was already there and is worth a third of the divergence; `drop_high` beat every geometric and colour arm), the 60-epoch horizon tried and beaten, the label scale measured and found to carry two thirds of the store's cross-sitting spread, 795 more seats labelled across two sittings, a best head trained with asymmetric weighting, the guards examined and left alone, a nondeterminism bug found at the adoption gate, determinism landed, and the head adopted with its corpus tracked and the n=1000 solve recorded.

**Records.** **`20260911T022330Z` — the official n=1000 record under the adopted head, UNPUBLISHED** (filled 1000/1000, shortfall 0, worst 1.041483, sum 1451.098395, legs 454·279·170·97). ⚠ The sum's last digit differs by 1e-6 from the in-memory solve — floating-point accumulation order; the seats are the same thousand in the same order, which is the claim that matters. Earlier stamps (`20260909T173957Z`, `20260909T193845Z`, `20260909T215815Z`, `20260910T025205Z`) order on superseded columns; the latest is the active one and older stamps are cited **purely for figure generation** unless Matt asks for a comparison. The site cites six stamps across 26 figures and is not to be re-based.

## IN FLIGHT ACROSS THIS BOUNDARY
Nothing.

## QUEUED IN DRIVE `prompts\`
**`smoke_mine_20260910`** — a 30-minute smoke mine under the adopted head, `tia`/`stripe` at 5% of wall-clock each. Not started. ⚠ Its gate line names `adopt_and_record_20260910`, which was superseded by `adopt_deterministic_20260910`; the gate is satisfied. Launch it as written; its report is processed next checkpoint.

## NEXT CHECKPOINT GOAL
**Matt sets it at the top of the checkpoint.** Nothing is scheduled here.

## OPEN (ordered) — Matt raises each
1. **The smoke mine's report**, then a longer mining leg if Matt wants one.
2. **★ PALETTE VARIANTS THROUGH THE PALETTE NETWORK (Matt's named direction, 2026-09-10).** 5–20 variants of each palette — rotation, duplication, and the rest — fed through the palette network, looking for good scores. **Smoke first, then a longer run.** He named this as behaviour that should have been propagated from maker to wallpapers and was not. Axes worth including beyond his two: reversal, stop-repetition count, cyclicity flips (production mirrors non-cyclic maps, and mirroring measured BACKWARDS for `direct_trap_multiply`), phase offset against the levelled curve, and **Oklab chroma/lightness rescaling**, which preserves hue identity while moving vividness and is therefore the most direct lever anyone has on which colour CELL a picture lands in. ⚠ **Settle first whether a palette sweep can ride a DUMPED FIELD** — a recolour from a dump is byte-identical at roughly a fifth the cost and amortises per (location, mode), but `colorize.render` refuses a palette override together with a `fields` directory and it is unknown whether that refusal is about curves specifically. That one answer is the difference between a cheap sweep and an expensive one.
3. **Mining the thin cells**, in order: `dark_vivid_lime`, `dark_muted_lime`, `dark_vivid_cyan`. Buys quality inside those cells and headroom against a later bar, not feasibility.
4. **The labelling protocol.** Matt's scale drifts ~0.4 tiers per 100 cards WITHIN a page and about a tier across an afternoon. Shorter pages, position randomisation, or neither — undecided, and the next sheet will be built without a ruling unless he makes one. ⚠ The standing rule bans calibration duplicates, drift probes and repeat rows, so a common anchor block across sheets would be a reopening and is his alone to raise.
5. **The coarse-4 labeling.** ⚠ A coarse 3 grades as a fine 1 (100 rows, mean 1.18). Roughly a two-tier offset.
6. **Themed collections at n=200.** Part of the product, untouched. ⚠ The colour floor is OFF on the themed path by design.
7. **The parameter sweep for `direct_trap_multiply`.** Opacity and threshold as swept ranges, `both` excluded.
8. **The near band's one-flag fix.** `--modes smooth stripe tia` on the band manifest.
9. **`make_deterministic` in the remaining trainers.** One line each; **no retrain on that account** (Matt).
10. **`pictures/` in the ten `runs` legs.** 5.37 GiB. ⚠ Destructive; isolation must be proven; not for an unattended prompt.
11. **Records-only picture retention.** → `preserve\retention_design.md`.
12. **`carriers.jsonl`** at 65.9% of the 1 MiB guard, a cross-repo seam with the website's `builder/palettes.py:carriers()`; **`itinerary.jsonl`** at 62% of 786,432. Both want a decision about what gets rolled up.
13. **Website — REOPENED for a section-by-section review pass.** Matt brings a review doc for one section; Claude pushes back on anything wrong or not an improvement; once aligned, Claude writes the prose master and the placement prompt. Two sections are through: **Color palettes v6** and **Finding good wallpapers v3**. Per-page status → `docs/page-review.md`.
14. **The reframe channel's cadence.** `g10` converted 384 fires into 2 productive.

Parked → `preserve\parked.md`. ⚠ The parked "K re-sweep (never propose it)" entry is superseded in fact but the instruction to Claude stands: never propose reopening it.

## STATUS / KNOWN REDS
**NO KNOWN REDS.**

Fast lane green throughout the era, last reading **4,207 passed / 132 deselected, 4,339 collected, 137.90 s**; `ruff` clean. ⚠ **The lane refuses the wrong interpreter at the door** (`pytest_configure` raises when the checkout has a `.venv` and this is not it; waived with `FRACTAL_WALLPAPERS_ANY_INTERPRETER=1`).

**★ TEST LANES ARE MATT'S TO MANAGE (ruled 2026-09-09).** He runs them when he judges them important. Claude does not track the slow lane, does not flag it as owed, does not chase a paired reading or a stale collected count, and does not spend a line on it.

## RULINGS THIS ERA
→ `preserve\rulings_method.md §ckpt 120` and `preserve\gallery_grade_stability.md`, plus the domain rulings in the docs themselves.

## KEEP LIST
Drive `prompts\`: **KEEP `smoke_mine_20260910.md`** (queued, not started); **wipe everything else**, including the superseded `retrain_and_compare_20260910.md`, which was never run. `reports\`: **wipe everything** — every report of this era was read and its findings are in these docs or in-repo; if the smoke mine is launched across the boundary, keep its report too. Wallpapers `scratch/`: KEEP `place_radius_sheet/` (it backs the `PRESELECT_RADIUS` ruling); **WIPE everything else** — the gallery-grade corpus is now tracked in-repo and the recipe is ported into the tracked trainer, so nothing under `scratch/best_head_0910/`, `scratch/fit_vs_labels_0909/`, `scratch/stability_20260910/`, `scratch/cell_deltas_0910/`, `scratch/deterministic_refit_20260910/` or `scratch/adopt_and_record_20260910/` is load-bearing. Website `scratch/`: unchanged.

## OWED
Nothing.

## SCRATCH/ARTIFACT FLAGS
**★ THE STANDING KEEP ROSTER LIVES IN THE REPO — `src/fractal_wallpapers/README.md §The standing keep roster`.** ⚠ Nothing on it is protected by `orphans`' reference set.

⚠ **`artifacts/render_folds/` DOES NOT EXIST on either tier.** `read_assignment` refuses, so `renders dose`, `renders grade` and `renders deploy` refuse.

⚠ **`.leveled/` DIRECTORIES ARE SWEEPABLE** — `orphans` reaches them by the name each JPEG would have. → `preserve\leveled_identity.md`.

Per-checkpoint: new records are prune-protected like every record. `artifacts/curation/depth/*/fields` keeps growing at roughly 226 MB a leg and the sweep cannot reach it. ⚠ **Two `label_migration` rows are the only pool rows the plain render path cannot reproduce** — authored-palette recipes; `re_render` correctly refuses them. ⚠ **CRLF drift is real**: files written through Bash rather than Edit come out CRLF, invisible to `git status`; `git ls-files --eol` is the door. ARCHIVED (RESTORE before reuse): unchanged from ckpt 106.

## PARKED / SETTLED
→ `preserve\parked.md`, `preserve\rulings_corpus.md`, `preserve\rulings_curation.md`, `preserve\rulings_sourcing.md`, `preserve\rulings_engine.md`, `preserve\rulings_website.md`, `preserve\rulings_method.md`, `preserve\sourcing_channel_laws.md`, `preserve\retention_design.md`, `preserve\solver_design.md`, `preserve\leveled_identity.md`, `preserve\gallery_grade_stability.md`, `preserve\deep_shelf.md`. The old `settled_rulings.md` is a stub index.
