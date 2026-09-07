# fractal-state — checkpoint 113 (2026-09-07)

## Where we are
THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE: (1) the LOCATION hunt · (2) the WALLPAPER hunt · (3) the final curation SOLVE + release render. `MODE_POLICY` is the one place a mode carries a standing; Matt iterates from pictures, not counts. Phase 3 is Matt's eye on the final seating. **NO PUBLISHING OF ANY KIND until Matt raises it — never ask, never list it.**

**STANDING DIRECTION (Matt, ckpt 111, unchanged): QUALITY OF THE n=1000 GALLERY.** Thin themes are DE-PRIORITIZED and no cell is owed seats. Mine until the pool is healthy across palettes, modes, locations and families → solve at whatever n → mine longer if a gallery comes up short. Busy-over-sparse is INTENTIONAL. τ 0.90× stands.

**★ THE MINING ROSTER IS `mode_policy.mined()` IN FULL (Matt, ckpt 113) — every ACCEPTED mode less `curvature`, twelve today, BOTH ANGLE MODES IN.** This reverses their ckpt-108 exclusion from the mining goals and is standing, not per-leg. Say **accepted**, never "shipped": the catalogue ships 19, and the six `mode_policy.niche()` modes are out of the draws and out of the gallery already.

**★ THE FINE-TIER HEAD IS ADOPTED AS THE SEATING ORDER (Matt, ckpt 113).** `solve.DEFAULT_KEY = CASCADE_KEY`: above `p_ge4 ≥ 0.5` the order is the head's own `p_ge4`, below the bar nothing changes. **SEATING ONLY — retention is ruled OUT**, because the ceiling contains a bad ranking at the seat and `_prune_ranks` has no such containment and deletes permanently. `_prune_ranks` reaches `curation.rank_key` directly and names neither the default key nor the cascade; `test_seat_sheet.py` pins that by reading its source. `rank_key` and `p_ge4` stay in `KEYS` and stay typeable. ⚠ **The cascade REFUSES without `pool_scores.jsonl`** — an unflagged seating on a machine that never ran `gallery-grade score-pool` now stops, deliberately, and `growth` and `k_sweep` inherit it because both read `DEFAULT_KEY` on purpose.

**★ THE FINE ORDER IS NOT IN THE SHIPPED JUDGE'S REPRESENTATION.** A frozen trunk recovers the coarse boundary and sits at CHANCE on AUC(≥4) — 0.492 / 0.496 against the judge's own 0.528 — while full unfreeze wins monotonically at 0.68–0.72, taking Spearman against Matt's grades from 0.090 to +0.43. That is the ckpt-111 penultimate-layer probe null reproduced from the other side, on the corpus built to answer it. Stopping on AUC(≥4) instead of AP(≥3) also bought reproducibility: seed spread 0.0333 → 0.0023, all three seeds at epoch 7. ⚠ **The standing recipe's AUC(≥3) FALLBACK WAS UNREACHABLE** — `average_precision` and `auc` return `None` under one condition — and has been deleted. Recipe → `preserve\judge_training.md`.

**This era (ckpt 112→113, one day).** The head was trained, re-fitted on the right boundary and adopted; `expressed` and the retired gate store were retired; `LEGS.md`'s K=3 rot was fixed; four claims were promoted to READMEs; `settled_rulings.md` was split into six subject parts; the deep files were folded; the locations captions were placed and the *Leveling* → *Autolevel* rename finished across the site; and two mining legs ran, the second still in flight. Ledger 308,419 → **320,014**, locations 27,939 → **28,808**, distinct places 21,583 → **22,274**.

**Records.** Unchanged from ckpt 109 except as noted. Published, and the four the site stands on: `20260902T161757Z` · `20260902T164622Z` · `20260904T023748Z` · `20260904T233233Z`. `20260906T133236Z` is the post-mine n=1000 record the browse page and the `gallery_grade` draw stand on — TENTATIVE, keep it. Every n=1000 solve run this era was a COUNTERFACTUAL with NO RECORD.

## IN FLIGHT ACROSS THIS BOUNDARY
**`MINE_ckpt113_band_weighted_with_displacement_0907`** — a band-weighted leg finishing by 1:30 pm PT on 2026-09-07, that deadline INCLUDING merges, readout and the sheet. Three units: A breadth opener, B near band, and **B2 the displacement half** — roughly 1,991 places sitting AT the keep, where the only way in is beating an incumbent, which has never been measured. B2's share is reserved up front and is never the residual; B's spare falls back to A. It ends by building a viewing sheet of the seats where `cascade` and `rank-key` disagree. **Its report has not been read.** Its prompt file stays in Drive `prompts\` across the wipe.

## QUEUED IN DRIVE `prompts\` — none.

## NEXT CHECKPOINT GOAL — NOT SET. Matt raises it.

## OPEN (ordered) — Matt raises each
1. **What displacement buys**, pending the leg above. Last night's arm B was 7.6× arm A on kept clears an engine-hour and took 24 gallery seats against 18 on a third of the clock, but it is SUPPLY-LIMITED: the re-cut band held 542 places with room and 910 free slots, and only the opener refills it.
2. **The roster trade.** The full roster is **4–8× less efficient at clears and 1.8× at seats** than the three shareable modes, while reaching material they cannot: in the near band `direct_trap_multiply` converts at 45.45% and `direct_trap_screen` at 34.38%, against `smooth` 18.04%, `stripe` 16.23%, `tia` 12.69%. The mode `MODE_POLICY` rates worst on tier-4 is the best converter in the band. A leg with breadth on shareable modes and the full roster only in the band is a shape neither night has run.
3. **Retiring `rank_key`**, now that the head has landed. Matt's stated intent; `population.jsonl` and its 1 MiB allowlist line retire with it. ⚠ The retirement argument must NOT rest on the key having failed: on the finished-render stores it no longer beats the judge, but **inside the gate's top it does** — AUC(≥4) 0.543 against 0.528, Spearman 0.138 against 0.090. It is a population difference, not a defeat.
4. **Grading the disagreement set.** The two keys share **173 of 1,000 seats**; of the 827 departures, **166 are a different candidate at a place the cascade still seats and 661 are places that left the gallery entirely**. Both keys seat 1,000 of 1,000 above the bar from the same 38,884 rows, so this is the head disagreeing about WHICH PLACE, four times in five. Those rows are the live decision boundary and a better population to grade than the original store, which was 700 seats plus 300 runners-up under the old ordering.
5. **`render_train.population` was corrected to 11,849** (117 renders counted twice). **No retrain was run**; the shipped render judge was fitted on the uncorrected population.
6. **Records-only picture retention.** The sweep premise is dead; the cost is one-off at build. What survives is **regeneration determinism** — signatures invalidate on picture identity, and a regenerated picture that is not byte-identical re-costs its row. Direction → `preserve\retention_design.md`.
7. **`carriers.jsonl`** sits at 65.9% of the 1 MiB history guard, 4.3 drops away. **A cross-repo seam**: the website's `builder/palettes.py:carriers()` derives the same two columns and holds the header's dominance sentence to its two thresholds.
8. **`itinerary.jsonl`'s guard** was raised to 786,432 and sits at 62%. The real horizon is roughly nine drops, a design question rather than a constant.
9. **Website** (Matt's pace). **Per-page status, masters, sweep state, figure holds and review rounds live in `docs/page-review.md` — cite it, never restate it here.** The locations page's caption sweep is OPEN at three corrections. `locations-highly-rated`'s ALT still asserts sixteen panels *spread across the families*, the claim just removed from its caption. One round remains named and unscheduled: a re-base onto a newer record. Stale figures and prose are NOT tracked or refreshed until "ready for publishing".
10. **The reframe channel's cadence.** Label-bound rather than clock-bound; a short follow-on after a sitting, never a night. Sizing → `curation/MEASUREMENTS.md`.
11. **A field-dump policy.** `artifacts/curation/depth/*/fields` holds **11 GB**, about 226 MB a leg, and the orphan sweep does not reach it. A ruling, not a fix.

Parked → `preserve\parked.md`: augment at n=2000; the rung-frame overwrite; the `mine` leg's autolevel stamp gap; medium refactors; the `tia` bound question; the `groups.jsonl` re-cut (do not build the axis).

## STATUS / KNOWN REDS
⚠ **ONE KNOWN RED, deliberately left red.** `tests/test_leveled_identity.py::test_no_two_ledger_rows_name_one_picture` holds `run_index_named >= 13,526` as a *the store only grows* floor and the store reads 13,510 — a census constant 16 rows out of date. It fails identically on a stashed clean tree at HEAD. Repointing a census floor to green a lane is the one edit that would make the guard worthless; named in `CLAUDE.md` and `tests/README.md` so the next lane knows the expected reading.

Fast lane 3,881 passed / 124 deselected, 121.89 s. Slow 7:38 over 4,005 with the red above. `cargo test` 216 passed; `ruff` clean. Website `builder check` 17 green with nothing skipped, 47 JS tests.

## RULINGS THIS ERA
→ `preserve\rulings_*.md §ckpt 113`.

## KEEP LIST
Drive `prompts\`: wipe everything **EXCEPT `MINE_ckpt113_band_weighted_with_displacement_0907.md`**, which is in flight. `reports\`: wipe everything — all nine were read. Wallpapers `scratch/`: KEEP the in-flight leg's own output and its disagreement sheet; WIPE everything else, including `seat_sheet/cascade_vs_rank_key/` and `two_arm_pilot_0906/`. Website `scratch/`: KEEP `_modes_render_times.py`, the walk-descent figure rig, and `three_bands/pick_seats.py`.

## OWED
Nothing.

## SCRATCH/ARTIFACT FLAGS
Standing KEEP: `artifacts/curation/candidate_ledger/` · the FIVE Durables · `neutral_embeddings.jsonl` · `artifacts/curation/` HOT · live release rows · `artifacts/reframe_g1…g10` · `artifacts/curation/tentative/<stamp>/` — every record (prune-protected) · `artifacts/votes/` kits · `artifacts/curation/growth/20260902T150756Z/` · `data/coloring/texture_flat.jsonl` · `data/spiral/` · `models/spiral/` · `models/render/` weights-v6 beside v5 · `models/gallery_grade/` · `artifacts/render_folds/` · `artifacts/top_slice_probe/` · `artifacts/gallery_grade/n1000_0906/*/plan.jsonl` — a graded row carries `leveled` as a BOOLEAN and never a path, so these plans are the only thing that can rebuild the 373 levelled pictures as they were judged; not regenerable, 736 KB, and reached by no sweep, so the guard is against a hand.

**`gallery_grade` protection is STRUCTURAL, not a hold** — `retention.labeled_renders` reads the store beside the two `finished.HEADS`, so all 1,000 rows sit in `RETAINED_LABELED` and a prune takes zero of them [`tests/test_gallery_grade_retention.py`].

**★ `artifacts/curation/gallery/` — 53 MB, 14,438 gate attempt rows — is KEPT (Matt, ckpt 113).** No reader since `gallery_store.py` went. It is NOT the last copy: all four passes verify byte-for-byte against their sha256 at `<archive>/fractal-wallpapers/artifacts/curation_backup/gallery/`, and the manifests carrying those hashes now live only at `git show f208911^:data/curation/gallery/<pass>/gate.manifest.json`. Not to be swept without a ruling. Reasons → `curation/README.md`.

⚠ **`.leveled/` DIRECTORIES ARE NOT SWEEPABLE** (→ fractal-engine). ARCHIVED (RESTORE before reuse): unchanged from ckpt 106. Walk ledgers: `discovered_priors` reads BOTH tiers while a harvest defaults to hot, so every header records which it read.

## CLOSED (records wiped — verdicts in the docs and the rulings parts)
TRAIN_ckpt113_fine_tier_head_0906 · AUDIT_ckpt113_doc_guard_inventory_0906 · REORG_ckpt113_preserve_split_0906 · PLACE_ckpt113_locations_captions_0906 · REFIT_ckpt113_fine_tier_head_and_seat_sheet_0906 · FIX_ckpt113_legs_k_rot_and_retirements_0906 · PLACE_ckpt113_color_palettes_autolevel_0906 · AUDIT_ckpt113_two_arm_pilot_band_0906 · MINE_ckpt113_overnight_0906 · PLACE_ckpt113_gallery_curation_autolevel_and_caption_0907 · ADOPT_ckpt113_cascade_and_cleanups_0907.

## PARKED / SETTLED
→ `preserve\parked.md`, `preserve\rulings_corpus.md`, `preserve\rulings_curation.md`, `preserve\rulings_sourcing.md`, `preserve\rulings_engine.md`, `preserve\rulings_website.md`, `preserve\rulings_method.md`, `preserve\sourcing_channel_laws.md`, `preserve\retention_design.md`, `preserve\solver_design.md`. The old `settled_rulings.md` is now a stub index.
