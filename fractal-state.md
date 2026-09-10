# fractal-state — checkpoint 119 (2026-09-09)

## Where we are
THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE: (1) the LOCATION hunt · (2) the WALLPAPER hunt · (3) the final curation SOLVE + release render. `MODE_POLICY` is the one place a mode carries a standing; Matt iterates from pictures, not counts. Phase 3 is Matt's eye on the final seating. **NO PUBLISHING OF ANY KIND until Matt raises it — never ask, never list it.**

**★ THE FINAL GALLERY SHIPS AT n=1000, and THEMED COLLECTIONS OF n=200 ARE PART OF THE PRODUCT.** Nothing has touched themed. n=2000 is not the direction; making n=1000 better is. "Better" means true quality, NOT maximizing `p_fine` — maximizing it would restrict the gallery to a tiny subset.

**★ THE BAR: `DEFAULT_FINE_BAR = 0.184` ON `p_ge4`, ADOPTED 2026-09-09.** The COLUMN was ruled to stay `p_ge4` — it is one of the two gated statistics and the band cleared 12 of 12 on it, where `p_ge3` was never gated and cutting on it would ship a column the pre-registration never judged. The LEVEL is a **matched constant, not a discovered one**: the point at which the refit admits the fraction the previous head admitted, fitted on a seeded 8,000-row sample and confirmed on the full pool at 27.95% against 27.51%. It is not principled to three digits and mining into the thin cells will quietly stop the match holding. **★ ⚠ A BAR IS UNREADABLE WITHOUT ITS HEAD** — `config.fine_head` is new on the tracked manifest, and 0.50 under `auc_ge4_more_seed2` and 0.184 under the refit mean the same thing while 0.50 under the refit does not. ⚠ `solve.Q4_BAR = 0.50` is the RENDER judge's constant and did NOT move. ⚠ There is no CLI spelling for the unbarred population: `--fine-bar 0` is a bar of zero and still excludes every unread row; `fine_bar=None` in process is the only way back. ⚠ `curate growth` and `curate solve k-sweep` inherit the bar. Provenance → `models/gallery_grade/README.md §Adopted 2026-09-09`.

**★ HOLDING THE ADMITTED FRACTION IS NOT RAISING THE BAR.** At 0.184 the gate sits where it sat; the refit's benefit is the ORDER inside the admitted pool, and the n=1000 cutoff does the selecting. Do not let a later reading conflate the two.

**★ MATT REOPENED K HIMSELF AND SET IT; CLAUDE STILL NEVER PROPOSES REOPENING IT.** He raised the colour allowance at this checkpoint, swept it, and ruled `ceiling.K = 3` with a new colour FLOOR. The standing instruction is unchanged in force: Claude does not propose reopening K — not as a question, not as a closeout item, however strong the measurement pointing at it. Matt raises it when he wants it.

**★ THE COLOUR RULE IS ONE ARITHMETIC IN ONE UNIT SYSTEM: `ceiling.K = 3`, `ceiling.KF = 1`.** Every cell gets at least one fair share and at most three. Ceiling `floor(K·n/48)+1` = 63 at n=1000; floor `floor(n/48)` = 20, **with no `+1`** (48 cells rounded up would ask 1,008 of 1,000 seats). The floor is SOFT — carried as floor shortfall in the lexicographic objective beside the mode floors, after tier order and before worst-seated, so a cell the pool cannot fill reports a shortfall instead of making the solve infeasible. **OFF on the themed path**, where a pass is deliberately one cell. Both on the tracked manifest as `config.ceiling.{k,kf,floor,floor_rule}`; a manifest with no `kf` predates 2026-09-09. **This REVERSES the ckpt-111 position that no cell is owed seats — it is a change of position, not a parameter.** Full argument → `curation/GALLERY.md §K = 3 and Kf = 1 — the ceiling and the floor are one arithmetic`.

**★ ⚠ THE ALLOWANCE COUNTS MEMBERSHIPS, NOT SEATS, AND THAT IS THE TRAP.** ~1.802 memberships a seat at K=2 and ~2.118 at K=3. The shipped K=2 read as "twice a fair share" in SEAT units and landed at about **1.12×** the realized mean in the units the rule actually counts, which is why 32 of 48 cells pinned at 42; K=3 is **1.68×**. **Convert a proposed K into membership units before arguing it.** → `GALLERY.md §★ The rule counts MEMBERSHIPS and not seats, and that is the trap`, mirrored in `curation/ceiling.py`'s `K` docstring.

**★ A `cell_floor:` STAMP SAYS WHICH LEG PLACED A SEAT, NOT THAT THE FLOOR BOUGHT IT.** 287 seats stamped against a **162-seat** counterfactual measured on the un-floored arm; the mandate leg went 300 → 520 and the ranked walk 506 → 426 while the augmenting chain went **194 → 0**, so the seed fills all thousand on its own now. → `GALLERY.md`.

**★ WHAT HOLDS A THIN COLOUR DOWN IS NOT THE CEILING.** 18 of 23 falling cells finished strictly below their own allowance with unseated clearing places spare; `location` and `the_leg_had_no_seat_left` refuse where `cell_allowance` used to, and the pass turns colour-bound → seat-bound between K=2.5 and 3.0. **★ MATT HAS RULED THE SPIRAL CAP STAYS** — it is now what refuses thin-cell rows, and that is a mining instruction, not a rule to re-litigate. → `GALLERY.md §What actually holds a thin colour down, and it is NOT the ceiling`.

**★ THE COLOUR FLOOR DOES NOT DRAG IN BAD PICTURES (measured, ckpt 119).** Its labeled block was the BEST of four at mean 2.69, beating the judge's own top band at like-for-like on every sheet. The floor's cost is in **which cells it reaches** — rows carrying one of the six short cells scored 2.44 against 3.02 for the rest of the block.

**★ `PRESELECT_RADIUS` STAYS AT 0.02 (Matt, ckpt 118) — NOT RAISED AND NOT SHRUNK.** He read every folded pair on `the-72.html` and judged them the same geometric location, so the radius is not too large; shrinking would only refuse to fold real duplicates. Do not reopen it as a question.

**★ THE `p_fine` SEATING IS THE WAY; `rank_key` IS DEPRECATED AS AN OFFER AND NOTHING MORE.** `--key` offers `{cascade, p_ge4}` through `solve.OFFERED_KEYS`; `solve.KEYS` still holds all three. **`rank_key` IS NOT RETIRABLE**: `cascade_order` is built on `ranking_for`'s mapping and lays the fine head over its top, so the cascade IS the rank key below the bar. Reopening it means proposing a replacement below-bar order, never deleting a key. ⚠ **`rank_key` does not read the fine head at all** — its four columns are `loc_p_ge4`, `p_ge3`, the render judge's `p_ge4` off the candidate, and `flat16_1.0`, so a fine-head adoption cannot move it and retention never sees it.

**★ `--forced` IS STAGED AND STAYS STAGED INDEFINITELY (Matt, ckpt 119).** A population lifted to the top of the fine column at load, before `at_fine_bar` and the fold, ordered internally by its own `p_fine` (`FORCED_LIFT`, `config.forced`). He is unlikely to adopt it and it is to remain available as an instrument for future experiments. **It is NOT dead code** and retiring it would be a ruling like an adoption. → `GALLERY.md §--forced`.

**★ THE FOLD MERGES INSTEAD OF DELETING, AND IT BOUGHT 71 OF 1,000 SEATS (ckpt 118).** `distinct.preselect` took `fold=POOL` as its default: an absorbed place's rows stay in the pool carrying the survivor's cluster id, `Candidate.cluster` is `folded_into or location`, and `rules.State.places` keys on it, so the existing one-per-location rule becomes one-per-cluster with no new rule kind. `--fold delete` keeps the old destructive walk selectable and `config.fold` is on the tracked manifest. **6,683 places fold into 5,509 clusters**; 446 clusters hold more than one place, largest 56. Cost: solve +11.9%, the diversity rule +12.0% over +52.7% measured pairs. ⚠ **No transitivity** — the folds are a star forest of depth one and `preselect` raises if that ever fails.

**★ THE FOLD PICKS ITS SURVIVOR ON THE SEATING KEY.** It ordered on raw `P(≥4)` while the seating ordered on the cascade key. It now offers each place by `distinct.offered_at` — `p_fine` where the head has read it, raw `P(≥4)` where it has not, **stacked and never mixed**, so unknown never outranks measured. The record carries `key`, `ordered_on`, `places_on_the_fallback`; a record with no `key` folded on `p_ge4`.

**★ `solve.strongest_locations` IS `solve.strongest_clusters`, AND IT WAS NEVER USED.** It now ranks clusters under `offered_at` and runs AFTER `preselect`. **130 hot records swept, exactly one names `pool.truncated_to`**, so no record moves and this is a consistency fix and not a correctness win. `pool.reachable_locations` is `reachable_clusters`, so the old name dates a record.

**★ THE GALLERY-GRADE FATE PAGE IS GALLERY-GRADE ONLY**, and its 312 rows read **0 off the roster · 0 below the coarse bar · 64 below the fine bar · 175 refused · 73 seated** at K=2 with no floor at 0.50. The rebuild under K=3 + floor read 0/0/64/168/80. **⚠ NO TWO OF THOSE ARE COMPARABLE** — the adoption moved rung 2 itself, and the readings differ in ceiling, floor, column and level at once. Whether a coarse 4 is a gallery-grade 4 is a separate open question and NOT a fate question. → `curation/README.md §The subtraction on a card is not a margin, and the card now says which leg placed the seat`.

**★ ⚠ THE `gap` COLUMN ON A FATE CARD IS NOT A MARGIN AND NEVER WAS.** `cell_allowance` is a count against the allowance with neither score in it, so the two rows on the card **never competed**; the competitor is picked after the fact as the weakest seat in the full cell, and 105 of them were placed by `swap`, `augment` or a mode-floor mandate — legs the rank key does not order. That is why 127 of 173 paired cards carried a NEGATIVE gap. The column now reads `p_fine Δ` with the placing leg named ahead of it, and **the leg column is MORE load-bearing under the floor, not less** (competitor placed by a mandate on 103 of 144 cards). Any "how close did this row come" reading taken off the old column is void.

**★ THERE IS NO HONEST SCORE COLUMN OVER THAT POPULATION.** The gallery-grade rows are the fine head's own training and stopping material, so `p_fine` is recognition for every row on the page. On a gallery-grade card the human grade is the only independent thing.

**★ A FATE QUESTION NEEDS A RECORD TAKEN WITH `--explain-keys`.** A record without a `rejection.explained` block cannot answer one.

**★ THE 10,664 BARE-DRAWN ROWS ARE REPAIRED AND THE HOLE CLASS IS CLOSED.** `mine.make` never passed `mode_params`, so every varied candidate was drawn bare under its own varied key. **Six** renderers carried the class, not three. All six now build through one `release.task_for` with no defaults, and the guards that missed it counted named members per builder. ⚠ **The ckpt-117 reading that the repair collapsed the mode was SEATS, not population** — seats are selected for scoring high, so re-reading them regresses.

**★ A RE-RENDER INVALIDATES EVERY READING TAKEN OFF THE PICTURE, NOT ONLY THE SCORE.** Both sidecars are incremental on the recipe key and a re-render keeps the key and the path. Flatness feeds `rank_key`. `recolour --keys` is the door and is idempotent.

**★ LEVELLING IS DECIDE-ONCE, REPLAY-UPWARD.** The curve is derived at candidate geometry and higher-resolution renders inherit it. **Nothing entered identity** — `key_of` byte-identical over 20,000 live rows. ⚠ The release comparison was taken at 1280×720 ss2, so the magnitude at 2560×1440 ss4 is unmeasured. The store-wide gap is closed: **6,466 replayable, 623 no-operator, 0 outstanding**.

**★ THE MINING LOOP DOES NOT ASK THE PALETTE HEAD.** The only live `Colorizer` is `curation.run`. `hunt` is defined in its own docstring as not asking the head anything; a conditioned leg bypasses it; `depth` samples maps with a seeded RNG through `mine.make`. `another_colour` has no caller in the tree. ⚠ **In the ARTICLE, act as if the palette network is still the proposal network** (Matt) — a doc fact, not a website correction.

**★ THE `both` SETTINGS CORNER IS RETIRED BY MATT'S EYE, OVERRIDING THE ckpt-104 RULE**, and **THE FRAME IS A PARAMETER SWEEP, NOT A ROSTER VERDICT**: exclude always-bad ranges and sweep the rest. The whitewash fix works and is small — near-white 3.8% → 0.000, chroma only 0.021 → 0.027 against 0.067–0.138 elsewhere; losing white is not gaining colour.

**★ AT n=1000 THE GALLERY IS SATURATED.** Mining buys option value for a later re-solve, and quality inside themes, rather than visible movement at this n.

**★ GROUPS ARE PALETTE GROUPS AND MINING CANNOT MOVE THEM.** `groups.group_of` is total, so a new group needs a new MAP. `group_cap` refuses zero; ⚠ `map:river-of-light-25` takes 24 of 25.

**★ THE NEAR BAND'S CEILING IS A MANIFEST/ROSTER MISMATCH, NOT PAIR ROOM (ckpt 118).** `band.py` cuts its manifest over twelve modes while `plan_held_mode` admits only `depth.field_modes()` — three since `curvature` left the mines. Band 2 is the clean read: 284 places with room, **219 with a field-mode incumbent, 87 planned**. All three band arms of the 2026-09-09 leg stopped early on an EMPTY PLAN and were never clock-bound. The fix is one flag: `--modes smooth stripe tia` on the band manifest. **Breadth refills the band at 19–21% of the places it opens.**

**★ `p_fine` COVERAGE IS CHECKABLE BEFORE A SOLVE.** `headroom.bars` carries `with_p_fine` beside `q4_rows` per mode plus a `fine_head` block. ⚠ **`pool_scores.jsonl` is one-shot**: above-bar rows merged after the last `score-pool` are unread and therefore unseatable. **Mine → merge → score-pool → solve.** Nothing enforces that ordering. ⚠ **A re-score now PRESERVES the outgoing column automatically** — `score_pool` moves the live file to `pool_scores_<run>.jsonl` before writing, reading the run off the file's own first row, so an older record stays reproducible; this is not a flag and cannot be forgotten.

**★ THE SOLVE APPLIES A BAR OF ITS OWN**, on the WHOLE POOL, before the per-mode `headroom.bars` gate on the render judge's `p_ge4`, and before `preselect`. Two stacked gates.

**★ ALL THIRTEEN ACCEPTED MODES SEAT AT n=1000.** The six absent are weight-0 and refused at pool construction. `ceiling.TAU = 0.034281`, `TWINS = 2`.

**⚠ SEATS-CHANGED IS NOT A MEASURE OF POOL CHANGE.** 96 seats and 73 places moved for **six** rows leaving the pool. Never read a seat-for-seat diff as a finding.

**⚠ ESTIMATES ARE MEASURED ON AN IDLE BOX, AND ON THE RIGHT POPULATION.** A pilot prices the population the leg actually draws.

**⚠ A NEW COLUMN RESOLUTION INSIDE A HOT PATH COSTS THE LANE.** Both instances of this were found by timing one file, not by review.

**This era (ckpt 118→119, one day).** The fate page's `cell_allowance` refusals were explained and the `gap` column found not to be a margin; `--forced` was built, run and staged; the colour ceiling was swept to K=3.75 and Matt set K=3 plus a new soft colour floor at one fair share; a 750-row `p_fine` sitting was built, labelled and ingested; the fine head was refit over everything, adopted, and the bar moved to 0.184 on the same column.

**Records.** `20260909T173957Z` (K=2, no floor, `--explain-keys`; the old fate page's record) · `20260909T193845Z` (`--forced`, unpublished) · **`20260909T215815Z`** (first K=3 + floor record; unpublished). ⚠ **Everything above predates the adoption**, so all of them order on the outgoing fine column, preserved at `artifacts/gallery_grade_head/pool_scores_auc_ge4_more_seed2.jsonl`. There is no "base record we reason from": the latest is the active one, and older stamps are cited **purely for figure generation** unless Matt asks for a comparison. The site cites six stamps across 26 figures, newest `20260908T211552Z`, and is not to be re-based.

**★ ⚠ THE ADOPTION CHANGED WHICH POOL IS SEATABLE, NOT HOW BIG IT IS.** The admitted fraction held at 27.95% against 27.51%, but only **6,302 rows are admitted by both heads** — 5,335 left and 5,522 arrived, a 93.3% symmetric churn. A post-adoption gallery is a **different pool of the same size**, not a re-ranking of the old one, so a before/after across the adoption compares two populations.

**⚠ DISTINCT PLACES FELL 6,683 → 6,235 WHILE ADMITTED ROWS ROSE**, because the refit's admitted set is more concentrated per location — 1.90 rows a place against 1.74. That is 448 fewer places available to a seating, and places rather than rows are what a seating spends. **It was not predicted and nothing has been ruled about it.** Open observation, not a problem.

## IN FLIGHT ACROSS THIS BOUNDARY
**`tentative_solve_20260909` on `fractal-wallpapers`** — the first n=1000 solve under the adopted refit and the 0.184 bar, with K=3 and the colour floor acting. Its record stamp, its floor shortfall and its thin-cell counts are **not in this doc**; read its report in Drive `reports\` (kept for this reason).

## QUEUED IN DRIVE `prompts\` — none.

## NEXT CHECKPOINT GOAL
**Matt sets it at the top of the checkpoint.** Nothing is scheduled here.

## OPEN (ordered) — Matt raises each
1. **The tentative solve's gallery under the refit.** The first seating on the new column, with the floor acting and the admitted set 93.3% turned over from the one every earlier record was drawn from.
2. **The new fallen list.** Matt does not want the ckpt-119 one (taken at 0.50, before the level moved); he expects to want the one taken under the adopted head and bar.
3. **Mining the thin cells**, in order: `dark_vivid_lime`, `dark_muted_lime`, `dark_vivid_cyan`. Under the adopted head at 0.184 all six clear comfortably (52 / 116 / 221 / 185 / 264 / 405 places against a floor of 20), so this buys quality inside those cells and headroom against a later bar, not feasibility.
4. **The coarse-4 labeling.** ⚠ **A coarse 3 grades as a fine 1** — measured on 100 unconditioned coarse-3 rows at 84×1, 14×2, 2×3, no 4s, mean 1.18, flat across modes and kinds. Roughly a two-tier offset, so the coarse-4 population's fine grade is an open question with a measured neighbour.
5. **The palette network as a PROPOSAL network.** Sampling replicated palettes, varying phase and the other recipe knobs. Its original purpose, lost in the maker → wallpapers transition. Unscoped, nothing tried.
6. **Themed collections at n=200.** Part of the product, untouched. Which cells they are FOR is undecided. ⚠ The colour floor is OFF on the themed path by design.
7. **The parameter sweep for `direct_trap_multiply`.** Opacity and threshold as swept ranges, `both` excluded. Unblocked by the `mine.make` fix; still not run.
8. **The near band's one-flag fix.** `--modes smooth stripe tia` on the band manifest; the arms of a night like 2026-09-09 are three to four times the size for the same clock.
9. **`pictures/` in the ten `runs` legs.** 5.37 GiB. ⚠ A destructive sweep whose isolation must be proven before it runs once; not for an unattended prompt.
10. **Records-only picture retention.** → `preserve\retention_design.md`.
11. **`carriers.jsonl`** at 65.9% of the 1 MiB guard, a cross-repo seam with the website's `builder/palettes.py:carriers()`; **`itinerary.jsonl`** at 62% of 786,432. Both want a decision about what gets rolled up, not a mechanical fix.
12. **Website — REOPENED for a section-by-section review pass.** Matt brings a review doc of proposed corrections for one section; Claude pushes back on anything wrong or not an improvement; once aligned, Claude writes the prose master and the placement prompt. Two sections are through: **Color palettes v6** and **Finding good wallpapers v3**. Per-page status → `docs/page-review.md`, and a placement prompt names the row it updates.
13. **The reframe channel's cadence.** `g10` converted 384 fires into 2 productive.

Parked → `preserve\parked.md`: augment at n=2000; the rung-frame overwrite; medium refactors; the `tia` bound question; the `groups.jsonl` re-cut; `BOUND_BLOCKS` 8; the desire list as an explicit instrument; the `inventory.feasibility` colour-allowance formula on paper. ⚠ The parked "K re-sweep (never propose it)" entry is superseded in fact — the sweep ran at Matt's own instruction — but the instruction to Claude stands: never propose reopening it.

## STATUS / KNOWN REDS
**NO KNOWN REDS.**

Fast lane green throughout the era on an idle box, last reading **4,178 selected / 132 deselected, 4,310 collected**. ⚠ **The lane refuses the wrong interpreter at the door** (`pytest_configure` raises when the checkout has a `.venv` and this is not it; waived with `FRACTAL_WALLPAPERS_ANY_INTERPRETER=1`): a torch-less interpreter collected and passed a SMALLER suite, nine modules skipped whole, 82 tests short, green. `ruff` clean; `cargo build` clean. ⚠ `CLAUDE.md`'s collected figure pairs a fast reading with a slow one and was deliberately left — moving half of it breaks the claim it makes.

**★ TEST LANES ARE MATT'S TO MANAGE (ruled 2026-09-09).** He runs them when he judges them important. Claude does not track the slow lane, does not flag it as owed, does not chase a paired reading or a stale collected count, and does not spend a line on it.

## RULINGS THIS ERA
→ `preserve\rulings_method.md §ckpt 119`, and the domain rulings in the docs themselves.

## KEEP LIST
Drive `prompts\`: **wipe everything** — nothing is queued and every prompt landed. `reports\`: **KEEP `tentative_solve_20260909_report.md`** (its record is in flight across the boundary and this doc deliberately holds none of its numbers); **wipe everything else** — all were read and their findings are in these docs or in-repo. Wallpapers `scratch/`: KEEP `place_radius_sheet/` (it backs the `PRESELECT_RADIUS` ruling); **WIPE everything else** — every sheet, histogram and figure from this era is superseded by the tentative solve or owned in-repo. Website `scratch/`: unchanged.

## OWED
Nothing.

## SCRATCH/ARTIFACT FLAGS
**★ THE STANDING KEEP ROSTER LIVES IN THE REPO — `src/fractal_wallpapers/README.md §The standing keep roster`.** Read it there; this doc keeps no copy. ⚠ Nothing on it is protected by `orphans`' reference set.

⚠ **`artifacts/render_folds/` DOES NOT EXIST on either tier.** `read_assignment` refuses, so `renders dose`, `renders grade` and `renders deploy` refuse.

⚠ **`.leveled/` DIRECTORIES ARE SWEEPABLE** — `orphans` reaches them by the name each JPEG would have. What cannot be written is a BOUNDED sweep of the rest. → `preserve\leveled_identity.md`, whose ckpt-111 "NOT SWEEPABLE" wording was corrected 2026-09-09 along with a second stale line claiming a re-measurement derives a different curve.

⚠ **`preserve\INDEX.md` HAS NO ENTRY FOR `leveled_identity.md`**, though this doc, fractal-engine, fractal-tutorial and the INDEX's own tail all cite it. Its own rule — delete nothing here without grepping for citations — is unenforceable on a file the index does not list.

Per-checkpoint: new records are prune-protected like every record. `artifacts/curation/depth/*/fields` keeps growing at roughly 226 MB a leg and the sweep cannot reach it. ⚠ **Two `label_migration` rows are the only pool rows the plain render path cannot reproduce** — authored-palette recipes; `re_render` correctly refuses them. ⚠ **CRLF drift is real**: twelve files written through Bash rather than Edit came out CRLF, invisible to `git status`; `git ls-files --eol` is the door. ARCHIVED (RESTORE before reuse): unchanged from ckpt 106.

## PARKED / SETTLED
→ `preserve\parked.md`, `preserve\rulings_corpus.md`, `preserve\rulings_curation.md`, `preserve\rulings_sourcing.md`, `preserve\rulings_engine.md`, `preserve\rulings_website.md`, `preserve\rulings_method.md`, `preserve\sourcing_channel_laws.md`, `preserve\retention_design.md`, `preserve\solver_design.md`, `preserve\leveled_identity.md`, `preserve\deep_shelf.md`. The old `settled_rulings.md` is a stub index.
