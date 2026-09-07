# fractal-state — checkpoint 114 (2026-09-07)

## Where we are
THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE: (1) the LOCATION hunt · (2) the WALLPAPER hunt · (3) the final curation SOLVE + release render. `MODE_POLICY` is the one place a mode carries a standing; Matt iterates from pictures, not counts. Phase 3 is Matt's eye on the final seating. **NO PUBLISHING OF ANY KIND until Matt raises it — never ask, never list it.**

**★ STANDING DIRECTION (Matt, ckpt 114, superseding ckpt 111's "mine until the pool is healthy"): BURN DOWN A DESIRE LIST.** Given the constraints exactly as they stand, the desire list is the set of **mining targets** that, if each were satisfied by a candidate at quality ≥ X, would solve the n=1000 problem. Derive it by holding every constraint and the rest of the seating FIXED and asking, of each seat below X, whether that cell has any candidate at or above X the solve could actually have used; if not, the cell is a target and its coordinates are the spec. **This is NOT "relax the constraints"** — the limit of that move is the top-1000-by-score gallery, which is the thing the constraints exist to prevent (Matt, ckpt 114). A target splits by cause: places clear the gate but reach nowhere near X (depth) · the cell has almost no places (breadth) · nothing in that palette plausibly reaches X (an **unwinnable** cell, reviewed by eye and never by the head that called it unwinnable). **The list is not static** — filling one cell changes the assignment, retiring some targets and creating others, so it is re-derived after each leg rather than worked down as a fixed inventory. **X IS NOT RATIFIED.** Derive the sub-target count as a function of X and pick the X that gives a list worth working; the blind sheet sampled only 0.0018–0.0149 and says nothing about where between there and 0.5 the line sits. Busy-over-sparse is INTENTIONAL, τ 0.90× stands, and no cell is owed seats.

**★ THE GROUP CAP COSTS NOTHING AT n=1000 — MEASURED, AND THE ckpt-113 CENSUS LINE THAT SAID IT BINDS WAS WRONG.** Cap = `max(1, floor(0.025 × n))` = 25; `group_cap` refuses **0** times, the busiest map takes 23 of 25, `at_the_cap` is 0. Three seatings over one pool and one cascade order — cap 25, cap 50, cap removed — change **zero seats** and give a bit-identical objective. "942 groups against 1,000 seats" is a count of the drawable palette pool; a gallery seats **473**. **What binds is `cell_allowance`, 28,889 refusals against `location` 4,204 and `group_cap` 0.** Relief never needed colormaps. ⚠ 461 groups hold readable rows (median 23, median best 0.826) and take no seat, and only 70 of 236 weak-half groups have their seat as the best row that group owns — **those are assignment outcomes, not deficits**: the solve considered those rows and declined them.

**★ THE FINE HEAD'S LEVEL IS TRUSTED, NOT ONLY ITS ORDER (Matt, 2026-09-07, by eye).** `p_fine(≥4)` reads as an absolute quality target; he revisits only if galleries produced under that reading come out bad. This supersedes ckpt 113's seating-only-because-the-level-is-untrusted framing. The blind sheet confirmed the extreme is junk and calibrated nothing else. **Do not re-open this by sheet.**

**★ SEATS ARE THE MEASURE; KEPT CLEARS IS THE WRONG HEADLINE (ckpt 114, measured).** In the near band the field dump is worth **4.8–6.7×** on price and the dear modes convert only **1.3–1.6×** better, so the field half wins kept clears outright (405 an engine-hour against 87). **On seats the halves are level** — the dear half took 8 of arm B's 10 off a tenth of its clock and 11 of B2's 22 off a ninth of its candidates. ⚠ `direct_trap_multiply` clears best in both arms and has taken **NO seat in either**. Decomposition → `curation/LEGS.md`.

**★ DISPLACEMENT AND THE FREE-SLOT BAND ARE NOT SUBSTITUTES (ckpt 114).** B2 is the cheapest arm the project has run, 0.795 s a candidate, because a place already at the keep holds a cheap shareable incumbent; it is the only arm that can take a seat at a place the gallery already holds. Arm B wins per engine-hour on seats and on the objective and is bounded at about its opener's yield. **Run B to exhaustion first, then give the rest of the band's clock to B2.** ⚠ A displacement arm's counterfactual is an UPPER BOUND — holding it out cannot restore the incumbents it deleted. ⚠ `--rate` must sit below the **cheapest** arm a leg runs, because the plan is what stops the cheap one.

**This era (ckpt 113→114, one day).** The near band was decomposed; the group cap was disproved as a constraint; the prune's above-bar share was counted; the cascade's record fields stopped lying about the key; `gallery_floor` retired and six stale gate claims were corrected across two repos; Training judges v6 was placed and the location bars were renamed site-wide; the locations caption round closed; and the two pilots were swept. Ledger 320,014 → **325,099**, locations 28,808 → **29,194**, distinct places 22,274 → **22,594**.

**Records.** Unchanged from ckpt 109 except as noted. Published, and the four the site stands on: `20260902T161757Z` · `20260902T164622Z` · `20260904T023748Z` · `20260904T233233Z`. `20260906T133236Z` is the post-mine n=1000 record the browse page and the `gallery_grade` draw stand on — TENTATIVE, keep it. Every n=1000 solve this era was a COUNTERFACTUAL with NO RECORD.

## IN FLIGHT ACROSS THIS BOUNDARY — none.

## QUEUED IN DRIVE `prompts\` — none.

## NEXT CHECKPOINT GOAL — NOT SET. Matt raises it.

## OPEN (ordered) — Matt raises each
1. **Derive the desire list.** The direction above is the frame; nobody has built the list. It needs X, and X is chosen from the sub-target count as a function of X rather than from a sheet.
2. **The re-materialization audit (Matt, ckpt 114: AUDIT).** `curation/README.md`'s *Dry-run 2026-09-02* said the ten backfilled `runs` legs held only ledger-named pictures. **3,615 across those ten carry no row today, every one dated 2026-09-03**, and the per-leg 09-03 file counts match the per-leg unnamed counts exactly on all ten. The 09-02 sweep deleted 3,610 from those same legs. No archived `runs` copy exists and nothing identifies the writer. Until it is found, **sweeping those legs reclaims nothing durably**, and something is rendering into directories no ledger names.
3. **The known red's floor is the wrong SHAPE, and the ratchet is the ruling (Matt, ckpt 114).** `run_index_named >= 13,526` asserts the store only grows; displacement mining deletes by design and the reading has fallen to **13,504**. Build: store count + deletions recorded since the high-water mark == the high-water mark, so loss is allowed when a transaction accounts for it and caught when nothing does. Fallback if the prune records will not carry it: check the census against an independent count rather than a constant. **Repointing the floor stays the one forbidden edit.** Left red until built.
4. **The ten `runs` legs** — 14,995 pictures, 2.28 GiB, all large-`ledger_named` and un-re-mergeable. Deleting them is a judgement about a superseded era, and it is **void until item 2 names the writer**.
5. **`render_train.population` was corrected to 11,849** (117 renders counted twice). **No retrain was run**; the shipped render judge was fitted on the uncorrected population.
6. **Records-only picture retention.** The sweep premise is dead; the cost is one-off at build. What survives is **regeneration determinism**. Direction → `preserve\retention_design.md`.
7. **`carriers.jsonl`** sits at 65.9% of the 1 MiB history guard, 4.3 drops away. **A cross-repo seam**: the website's `builder/palettes.py:carriers()` derives the same two columns.
8. **`itinerary.jsonl`'s guard** was raised to 786,432 and sits at 62%. The real horizon is roughly nine drops, a design question rather than a constant.
9. **Website** (Matt's pace). **Per-page status, masters, sweep state, figure holds and review rounds live in `docs/page-review.md` — cite it, never restate it here.** Still open there: `locations-walk-lengths` letters a run identifier into its own picture (a redraw that re-reads the walk ledgers next door); five pages unswept for em-dashes; the re-base onto a newer record, named and unscheduled. Stale figures and prose are NOT tracked or refreshed until "ready for publishing".
10. **The reframe channel's cadence.** Label-bound rather than clock-bound. Sizing → `curation/MEASUREMENTS.md`.
11. **`python -m builder figure <id>` dies** with a `UnicodeEncodeError` on cp1252 stdout, on the figure-open mark. An alt edit must therefore be applied to the page by hand with `check`'s regenerate-and-diff as the guard.

Parked → `preserve\parked.md`: augment at n=2000; the rung-frame overwrite; the `mine` leg's autolevel stamp gap; medium refactors; the `tia` bound question; the `groups.jsonl` re-cut (do not build the axis — and the group cap costing nothing makes that parking stronger, not weaker).

## STATUS / KNOWN REDS
⚠ **ONE KNOWN RED, deliberately left red** — item 3 above. `tests/test_leveled_identity.py::test_no_two_ledger_rows_name_one_picture` reads 13,504 against a floor of 13,526, and the gap **widens with mining**. Named in `CLAUDE.md` and `tests/README.md`.

Fast lane 3,886 passed / 124 deselected, ~121 s (four tests added this era). **The slow lane was not run this era and should next read 4,010.** `ruff` clean both repos. Website `builder check` 17 green with nothing skipped, 47 JS tests.

## RULINGS THIS ERA
→ `preserve\rulings_*.md §ckpt 114`.

## KEEP LIST
Drive `prompts\`: **wipe everything** — nothing is queued. `reports\`: **wipe everything** — all nine were read. Wallpapers `scratch/`: KEEP `ckpt113_fine_head_weak_seats/`, the blind sheet and its key, since X is unratified and it is the only visual anchor; WIPE everything else, including `seat_sheet/cascade_vs_rank_key_0907/`. Website `scratch/`: KEEP `_modes_render_times.py`, the walk-descent figure rig, and `three_bands/pick_seats.py`.

## OWED
Nothing.

## SCRATCH/ARTIFACT FLAGS
Standing KEEP: `artifacts/curation/candidate_ledger/` · the FIVE Durables · `neutral_embeddings.jsonl` · `artifacts/curation/` HOT · live release rows · `artifacts/reframe_g1…g10` · `artifacts/curation/tentative/<stamp>/` — every record (prune-protected) · `artifacts/votes/` kits · `artifacts/curation/growth/20260902T150756Z/` · `data/coloring/texture_flat.jsonl` · `data/spiral/` · `models/spiral/` · `models/render/` weights-v6 beside v5 · `models/gallery_grade/` · `artifacts/gallery_grade_head/pool_scores.jsonl` — the cascade REFUSES without it · `artifacts/render_folds/` · `artifacts/top_slice_probe/` · `artifacts/gallery_grade/n1000_0906/*/plan.jsonl` — the only thing that can rebuild the 373 levelled pictures as they were judged.

**★ THE FIELD DUMPS ARE KEPT (Matt, 2026-09-07).** `artifacts/curation/depth/*/fields` holds roughly 11 GB, about 226 MB a leg, and it accumulates. The orphan sweep is **structurally** unable to reach it — `picture_dirs` enumerates `<subtree>/<leg>/pictures` at a fixed depth — so this is a ruling about growth, not an exemption anything could violate. ⚠ A leg directory's size is dominated by `fields/`, so a picture count is a bad estimate of what deleting one frees: the two ckpt-113 pilots read 0 pictures and were 606 MB.

**★ `artifacts/curation/gallery/` — 53 MB, 14,438 gate attempt rows — is KEPT (Matt, ckpt 113).** Not the last copy: all four passes verify byte-for-byte against `<archive>/fractal-wallpapers/artifacts/curation_backup/gallery/`, and the manifests carrying those hashes live only at `git show f208911^:data/curation/gallery/<pass>/gate.manifest.json`. It is not in `POOL_SUBTREES`, so the sweep never looks there. Reasons → `curation/README.md`. ⚠ `runs/gallery1`–`gallery4` are a DIFFERENT path and are not covered by that ruling — they are item 4.

⚠ **`.leveled/` DIRECTORIES ARE NOT SWEEPABLE** (→ fractal-engine). ARCHIVED (RESTORE before reuse): unchanged from ckpt 106. Walk ledgers: `discovered_priors` reads BOTH tiers while a harvest defaults to hot, so every header records which it read.

## CLOSED (records wiped — verdicts in the docs and the rulings parts)
AUDIT_ckpt113_rank_key_retirement_and_arm_rosters_0907 · MINE_ckpt113_band_weighted_with_displacement_0907 · PLACE_ckpt113_training_judges_v6_0907 · FIX_ckpt113_cascade_records_and_pool_reads_0907 · PRECLOSEOUT_ckpt113_doc_corrections_and_promotions_0907 · FIX_ckpt113_website_caption_round_and_consistency_0907 · SHOW_ckpt113_fine_head_weak_seats_0907 · FIX_ckpt113_website_leftovers_0907 · SWEEP_ckpt113_pilots_0907.

## PARKED / SETTLED
→ `preserve\parked.md`, `preserve\rulings_corpus.md`, `preserve\rulings_curation.md`, `preserve\rulings_sourcing.md`, `preserve\rulings_engine.md`, `preserve\rulings_website.md`, `preserve\rulings_method.md`, `preserve\sourcing_channel_laws.md`, `preserve\retention_design.md`, `preserve\solver_design.md`. The old `settled_rulings.md` is a stub index.
