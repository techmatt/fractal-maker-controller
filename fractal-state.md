# fractal-state — checkpoint 118 (2026-09-09)

## Where we are
THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE: (1) the LOCATION hunt · (2) the WALLPAPER hunt · (3) the final curation SOLVE + release render. `MODE_POLICY` is the one place a mode carries a standing; Matt iterates from pictures, not counts. Phase 3 is Matt's eye on the final seating. **NO PUBLISHING OF ANY KIND until Matt raises it — never ask, never list it.**

**★ THE FINAL GALLERY SHIPS AT n=1000, and THEMED COLLECTIONS OF n=200 ARE PART OF THE PRODUCT.** Nothing has touched themed. n=2000 is not the direction; making n=1000 better is. "Better" means true quality, NOT maximizing `p_fine` — maximizing it would restrict the gallery to a tiny subset.

**★ THE BAR: `p_fine(≥4) ≥ 0.50`, `DEFAULT_FINE_BAR = 0.50`, fill n=1000.** Ratified ckpt 115 and **CLOSED**. ⚠ There is no CLI spelling for the unbarred population: `--fine-bar 0` is a bar of zero and still excludes every unread row; `fine_bar=None` in process is the only way back. ⚠ `curate growth` and `curate solve k-sweep` inherit the bar.

**★ NEVER PROPOSE REOPENING K.** Not as a question, not as a closeout item, however strong the measurement pointing at it. Matt has had to say this repeatedly. The colour-cell allowance is assumed good; he raises it himself if he ever wants to. The `cell_allowance` measurement below does NOT reopen it.

**★ `PRESELECT_RADIUS` STAYS AT 0.02 (Matt, ckpt 118) — NOT RAISED AND NOT SHRUNK.** He read every folded pair on `the-72.html` and judged them the same geometric location, so the radius is not too large; shrinking would only refuse to fold real duplicates. Do not reopen it as a question.

**★ THE `p_fine` SEATING IS THE WAY; `rank_key` IS DEPRECATED AS AN OFFER AND NOTHING MORE.** `--key` offers `{cascade, p_ge4}` through `solve.OFFERED_KEYS`; `solve.KEYS` still holds all three. **`rank_key` IS NOT RETIRABLE**: `cascade_order` is built on `ranking_for`'s mapping and lays the fine head over its top, so the cascade IS the rank key below the bar. Reopening it means proposing a replacement below-bar order, never deleting a key.

**★ THE FOLD MERGES INSTEAD OF DELETING, AND IT BOUGHT 71 OF 1,000 SEATS (ckpt 118).** `distinct.preselect` took `fold=POOL` as its default: an absorbed place's rows stay in the pool carrying the survivor's cluster id, `Candidate.cluster` is `folded_into or location`, and `rules.State.places` keys on it, so the existing one-per-location rule becomes one-per-cluster with no new rule kind. `--fold delete` keeps the old destructive walk selectable and `config.fold` is on the tracked manifest. **6,683 places fold into 5,509 clusters**; 446 clusters hold more than one place, largest 56. **71 seats are held by a row at a place the destructive fold would have absorbed**, and `itinerary` met its floor at 32 for the first time. Cost: solve +11.9%, the diversity rule +12.0% over +52.7% measured pairs; `rules.Twins` now records its own seconds. ⚠ **No transitivity** — `suppress` compares each place only against places already kept, so the folds are a star forest of depth one and `preselect` raises if that ever fails.

**★ THE FOLD PICKS ITS SURVIVOR ON THE SEATING KEY.** It ordered on raw `P(≥4)` while the seating ordered on the cascade key, and discarded the higher-`p_fine` place in **435 of 1,042** folds. It now offers each place by `distinct.offered_at` — `p_fine` where the head has read it, raw `P(≥4)` where it has not, **stacked and never mixed**, so unknown never outranks measured. The record carries `key`, `ordered_on`, `places_on_the_fallback`; a record with no `key` folded on `p_ge4`. ⚠ The trade is exact rather than free: **496 of 1,174 now discard the higher-`p_ge4` place**, and the fine column is the one the seating reads.

**★ `solve.strongest_locations` IS `solve.strongest_clusters`, AND IT WAS NEVER USED.** It ranked places on raw `P(≥4)` one line after `at_fine_bar`, and cut places while the fold pooled them. It now ranks clusters under `offered_at` and runs AFTER `preselect`. **130 hot records swept, exactly one names `pool.truncated_to`, taken 2026-08-26**, so no record moves and this is a consistency fix and not a correctness win. Moving it also took the per-mode bars off the truncated tail, and `keep=None` is now free. `pool.reachable_locations` is `reachable_clusters`, so the old name dates a record.

**★ THE "SEVEN IN TEN" READING IS RETIRED — IT WAS TWO STORES READ AS ONE.** The gallery-grade page is now gallery-grade only, and its 312 rows are **0 off the roster · 0 below the coarse bar · 64 below the fine bar · 175 refused · 73 seated**. The sitting was drawn FROM the pool, so every one of these is a ledger row above the coarse bar by construction; the old page's 117 off-roster and 492 below-coarse rows were all finished-store rows, and reading them beside these read a fact about the carry-back join as a fact about the pipeline. Whether a coarse 4 is a gallery-grade 4 is a separate open question and NOT a fate question. Page → `scratch/label4_fate_gallery_0909/`.

**★ `cell_allowance` IS WHAT STOPS A WALLPAPER MATT WANTED.** Of the 175 refused: **`cell_allowance` 120, `location` 51, `twin` 3, `spiral` 1, and zero `another_place_is_the_same_place`** — the vocabulary change confirmed on a live record. 173 paired over 77 distinct competitors, **87 where one departure would have been enough**, 2 unpairable. The colour ceiling refuses more than twice as often as another picture at the row's own place. ⚠ This is a measurement, NOT an argument to reopen K.

**★ THERE IS NO HONEST SCORE COLUMN OVER THAT POPULATION.** `FINE_TRAIN` 245 + `FINE_STOPPING` 67 = **312**, the whole page, so `p_fine` is recognition for every row on it. The page says so in its lede and its first legend line. On a gallery-grade card the human grade is the only independent thing.

**★ A FATE QUESTION NEEDS A RECORD TAKEN WITH `--explain-keys`.** The standing record carries no `rejection.explained` block and cannot answer one. `20260909T173957Z` is `165641Z`'s config plus the flag, and is the page's record.

**★ THE 10,664 BARE-DRAWN ROWS ARE REPAIRED AND THE HOLE CLASS IS CLOSED.** `mine.make` never passed `mode_params`, so every varied candidate was drawn bare under its own varied key. **Six** renderers carried the class, not three: `checks`, `run` and `votes` had `solve`'s omission too. All six now build through one `release.task_for` with no defaults, and the guards that missed it counted named members per builder and were green through all four `curve`/`palette` drops. Repair: 10,664 rows, all reproducing their keys, movement symmetric (4,727 down, 4,208 up, median |Δ| 0.0031). ⚠ **The ckpt-117 reading that the repair collapsed the mode was SEATS, not population** — seats are selected for scoring high, so re-reading them regresses. `direct_trap_multiply` went **248 → 328 clearing places** and now holds its floor.

**★ A RE-RENDER INVALIDATES EVERY READING TAKEN OFF THE PICTURE, NOT ONLY THE SCORE.** The colour census, all 10,664 flatness readings and 949 signatures were stale after the repair, because both sidecars are incremental on the recipe key and a re-render keeps the key and the path. Flatness feeds `rank_key`. A re-solve run straight after a repair would have ordered on pictures that no longer existed. `recolour --keys` is the door and is idempotent.

**★ LEVELLING IS DECIDE-ONCE, REPLAY-UPWARD.** The curve is derived at candidate geometry and higher-resolution renders inherit it. **Nothing entered identity** — `key_of` byte-identical over 20,000 live rows. `measured` still means this render's own base statistics; provenance names where the curve came from. ⚠ The release comparison was taken at 1280×720 ss2, not release geometry, so the magnitude at 2560×1440 ss4 is unmeasured. The store-wide gap is closed: **6,466 replayable, 623 no-operator (the direct-trap family, nothing to recover), 0 outstanding**.

**★ THE MINING LOOP DOES NOT ASK THE PALETTE HEAD.** The only live `Colorizer` is `curation.run` — the end-to-end `curate run` pipeline the repo ships, which draws an anchor, builds the 32-map neighbourhood, recolours the smooth field and takes the head's pick. `hunt` is defined in its own docstring as not asking the head anything, because the head's argmax concentrates and takes the green carriers at 0.17× its base rate; a conditioned leg bypasses it outright; `depth` samples maps with a seeded RNG through `mine.make`. `another_colour` has no caller in the tree. ⚠ **In the ARTICLE, act as if the palette network is still the proposal network** (Matt) — this is a doc fact, not a website correction.

**★ THE `both` SETTINGS CORNER IS RETIRED BY MATT'S EYE, OVERRIDING THE ckpt-104 RULE**, and **THE FRAME IS A PARAMETER SWEEP, NOT A ROSTER VERDICT**: exclude always-bad ranges and sweep the rest. Opacity and threshold are a hand-enumerated roster of five cells while the palette side samples gamma across a continuum, which is the wrong shape for a knob that should be swept. The whitewash fix works and is small — near-white 3.8% → 0.000, chroma only 0.021 → 0.027 against 0.067–0.138 elsewhere; losing white is not gaining colour.

**★ AT n=1000 THE GALLERY IS SATURATED.** Mining buys option value for a later re-solve, and quality inside themes, rather than visible movement at this n.

**★ GROUPS ARE PALETTE GROUPS AND MINING CANNOT MOVE THEM.** `groups.group_of` is total, so a new group needs a new MAP. 942 seatable · 934 scored by the fine head. `group_cap` refuses zero; ⚠ `map:river-of-light-25` takes 24 of 25.

**★ THE NEAR BAND'S CEILING IS A MANIFEST/ROSTER MISMATCH, NOT PAIR ROOM (ckpt 118).** `band.py` cuts its manifest over twelve modes while `plan_held_mode` admits only `depth.field_modes()` — `smooth`, `stripe`, `tia`, three since `curvature` left the mines on 2026-09-06. Band 2 is the clean read: 284 places with room, **219 with a field-mode incumbent, 87 planned**. All three band arms of the 2026-09-09 leg stopped early on an EMPTY PLAN at 41%, 13% and 33% of their caps and were never clock-bound, while every breadth arm was. The fix is one flag: `--modes smooth stripe tia` on the band manifest. **Breadth refills the band at 19–21% of the places it opens** — a fifth reading, above `LEGS.md`'s 16.2%.

**★ THE GENERAL LEG IS THE SOURCE, AND AIMING IS CLOSED AS A POLICY.** The 2026-09-09 leg: **15,650 candidates, 843 clears, 275 gallery-grade rows, 1,205 new places, 19.0 engine-hours, nothing pruned across seven merges**. 32.6% of clears reach gallery grade against 29.0%, at **248.7 engine-seconds a gallery-grade row against 415**. The band buys one for 31.8–90.5 against breadth's 269–350. Width to free slots chose 4 at every cut and kept every row rendered.

**★ `p_fine` COVERAGE IS CHECKABLE BEFORE A SOLVE.** `headroom.bars` carries `with_p_fine` beside `q4_rows` per mode plus a `fine_head` block, exact because `q4_rows` is the set `score-pool` reads. ⚠ **`pool_scores.jsonl` is one-shot**: above-bar rows merged after the last `score-pool` are unread and therefore unseatable. **Mine → merge → score-pool → solve.** Nothing enforces that ordering. Second reopening route: a mode under `FALLBACK_LOCATIONS` clears on `p_ge3`, which the fine head does not read.

**★ THE SOLVE APPLIES A BAR OF ITS OWN.** `fine_bar` at 0.50 on the WHOLE POOL, before the per-mode `headroom.bars` gate on the render judge's `p_ge4`, and before `preselect`. Two stacked gates. `solve.Q4_BAR = floors.RELEASE_ADVISORY = 0.50`.

**★ ALL THIRTEEN ACCEPTED MODES SEAT AT n=1000.** The six absent are weight-0 and refused at pool construction. `ceiling.TAU = 0.034281`, `TWINS = 2`.

**⚠ SEATS-CHANGED IS NOT A MEASURE OF POOL CHANGE.** 96 seats and 73 places moved for **six** rows leaving the pool. Never read a seat-for-seat diff as a finding.

**⚠ ESTIMATES ARE MEASURED ON AN IDLE BOX, AND ON THE RIGHT POPULATION.** The two bad estimates of this era were both the wrong population rather than bad arithmetic. A pilot prices the population the leg actually draws.

**⚠ A NEW COLUMN RESOLUTION INSIDE A HOT PATH COSTS THE LANE.** Twice this era: a store read inside `headroom.bars` took `test_headroom.py` 2.10 s → 12.60 s, and the fold's column resolution made every synthetic census parse a 9.2 MiB store. Both were found by timing one file, not by review.

**This era (ckpt 117→118, one day).** The bare-drawn rows were repaired across six renderers and every reading taken off those pictures re-read; the pool was re-solved twice and then a third time under a pooled fold that closed the last mode floor; `preselect` stopped ordering on the coarse key and stopped deleting; the fate page was split to gallery-grade only and its headline number retired; a general leg ran to 07:00; two article sections went through the review pass.

**Records.** `20260909T061451Z` · `20260909T161932Z` (folded on `p_fine`) · `20260909T165641Z` (first `--fold pool`, **shortfall 0, every floor met**) · `20260909T165848Z` (its delete-arm twin) · `20260909T173957Z` (**active**; `165641Z` plus `--explain-keys`, same 1,000 seats in the same order). ⚠ `165641Z` and `165848Z` predate `config.fold` on the tracked manifest and answer on `preselection.fold` only. There is no "base record we reason from": the latest is the active one, and older stamps are cited **purely for figure generation** unless Matt asks for a comparison. The site cites six stamps across 26 figures, newest `20260908T211552Z`, and is not to be re-based. `20260906T133236Z`'s hold is still undecided.

## IN FLIGHT ACROSS THIS BOUNDARY — none.

## QUEUED IN DRIVE `prompts\` — none.

## NEXT CHECKPOINT GOAL
**Explore the gallery-grade fate page, and possibly make changes because of it.** Matt set this. `scratch/label4_fate_gallery_0909/` is the first thing to open.

## OPEN (ordered) — Matt raises each
1. **The gallery-grade fate page.** 64 of 312 below the fine bar, 175 refused, `cell_allowance` 120 of them. Next checkpoint's goal.
2. **Forced mode, and the coarse-4 labeling.** Matt's concern is that the head is UNDER-fitted to his labels, not over-fitted. A `--forced` option setting `p_fine = 1.0001` on his labeled 4s, overriding the column at load rather than filtering after — `at_fine_bar` runs before clearing and the fold, so a post-hoc boost arrives too late. Expectation: they nearly all seat, except on a geometric threshold or a group reason. Anything else is a bug. What can still refuse a forced row: one seat per cluster, the twin test, `cell_allowance`, the mode ceilings, the spiral cap. Separately: labeling `p_fine` for the coarse 4s, worst-agreement first. **Matt will set aside 100 labels for eval at that last step.**
3. **The palette network as a PROPOSAL network.** Sampling replicated palettes, varying phase and the other recipe knobs. Its original purpose, lost in the maker → wallpapers transition. Unscoped, nothing tried.
4. **Themed collections at n=200.** Part of the product, untouched. Which cells they are FOR is undecided.
5. **The parameter sweep for `direct_trap_multiply`.** Opacity and threshold as swept ranges, `both` excluded. Unblocked for the first time by the `mine.make` fix.
6. **The near band's one-flag fix.** `--modes smooth stripe tia` on the band manifest; the arms of a night like 2026-09-09 are three to four times the size for the same clock.
7. **`pictures/` in the ten `runs` legs.** 5.37 GiB. ⚠ A destructive sweep whose isolation must be proven before it runs once; not for an unattended prompt.
8. **Records-only picture retention.** → `preserve\retention_design.md`.
9. **`carriers.jsonl`** at 65.9% of the 1 MiB guard, a cross-repo seam with the website's `builder/palettes.py:carriers()`; **`itinerary.jsonl`** at 62% of 786,432. Both want a decision about what gets rolled up, not a mechanical fix.
10. **Website — REOPENED for a section-by-section review pass.** Matt brings a review doc of proposed corrections for one section; Claude pushes back on anything wrong or not an improvement; once aligned, Claude writes the prose master and the placement prompt. Two sections are through: **Color palettes v6** and **Finding good wallpapers v3**. He brings the next one. Per-page status → `docs/page-review.md`, and a placement prompt names the row it updates.
11. **The reframe channel's cadence.** `g10` converted 384 fires into 2 productive.

Parked → `preserve\parked.md`: augment at n=2000; the rung-frame overwrite; medium refactors; the `tia` bound question; the `groups.jsonl` re-cut; `BOUND_BLOCKS` 8; the K re-sweep (**never propose it**); the desire list as an explicit instrument; the `inventory.feasibility` colour-allowance formula on paper.

## STATUS / KNOWN REDS
**NO KNOWN REDS.**

Fast lane **4,127 selected / 132 deselected in 122.63 s**, green on an idle box. ⚠ **The slow lane has not run since before the pooled fold**, so the two lanes do not agree on the collected count and `CLAUDE.md`'s figure was deliberately not repointed — that figure pairs a fast and a slow reading and moving half of it breaks the claim it exists to make. Whoever takes the next paired reading moves it. `tests/README.md` says so at the reading. ⚠ **The lane now refuses the wrong interpreter at the door** (`pytest_configure` raises when the checkout has a `.venv` and this is not it; waived with `FRACTAL_WALLPAPERS_ANY_INTERPRETER=1`): a torch-less interpreter collected and passed a SMALLER suite, nine modules skipped whole, 82 tests short, green. `ruff` clean. Website `builder check` fully green at `a843f93`, 79 s, eighteen checks, nothing skipped.

## RULINGS THIS ERA
→ `preserve\rulings_method.md §ckpt 118`, and the domain rulings in the docs themselves.

## KEEP LIST
Drive `prompts\`: **wipe everything** — nothing is queued and every prompt landed. `reports\`: **wipe everything** — all were read. Wallpapers `scratch/`: KEEP `label4_fate_gallery_0909/`, `place_radius_sheet/`, `dtm_whitewash_0908/`; **WIPE everything else**, including the superseded `label4_fate_0908/`, `label4_fate_after_repair/` and `label_migration_0908/`. Website `scratch/`: unchanged.

## OWED
The slow lane, and the paired reading that repoints `CLAUDE.md`'s collected count.

## SCRATCH/ARTIFACT FLAGS
**★ THE STANDING KEEP ROSTER LIVES IN THE REPO — `src/fractal_wallpapers/README.md §The standing keep roster`.** Read it there; this doc keeps no copy. ⚠ Nothing on it is protected by `orphans`' reference set.

⚠ **`artifacts/render_folds/` DOES NOT EXIST on either tier.** `read_assignment` refuses, so `renders dose`, `renders grade` and `renders deploy` refuse.

⚠ **`.leveled/` DIRECTORIES ARE SWEEPABLE** — `orphans` reaches them by the name each JPEG would have. What cannot be written is a BOUNDED sweep of the rest. → `preserve\leveled_identity.md`.

Per-checkpoint: new records are prune-protected like every record. `artifacts/curation/depth/*/fields` keeps growing at roughly 226 MB a leg and the sweep cannot reach it. ⚠ **Two `label_migration` rows are the only pool rows the plain render path cannot reproduce** — authored-palette recipes; `re_render` correctly refuses them. ⚠ **CRLF drift is real**: twelve files written through Bash rather than Edit came out CRLF, invisible to `git status`; `git ls-files --eol` is the door. ARCHIVED (RESTORE before reuse): unchanged from ckpt 106.

## PARKED / SETTLED
→ `preserve\parked.md`, `preserve\rulings_corpus.md`, `preserve\rulings_curation.md`, `preserve\rulings_sourcing.md`, `preserve\rulings_engine.md`, `preserve\rulings_website.md`, `preserve\rulings_method.md`, `preserve\sourcing_channel_laws.md`, `preserve\retention_design.md`, `preserve\solver_design.md`, `preserve\leveled_identity.md`, `preserve\deep_shelf.md`. The old `settled_rulings.md` is a stub index.
