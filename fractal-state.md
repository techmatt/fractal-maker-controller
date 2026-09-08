# fractal-state — checkpoint 115 (2026-09-08)

## Where we are
THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE: (1) the LOCATION hunt · (2) the WALLPAPER hunt · (3) the final curation SOLVE + release render. `MODE_POLICY` is the one place a mode carries a standing; Matt iterates from pictures, not counts. Phase 3 is Matt's eye on the final seating. **NO PUBLISHING OF ANY KIND until Matt raises it — never ask, never list it.**

**★ THE BAR IS RATIFIED AND ADOPTED (Matt, ckpt 115): `p_fine(≥4) ≥ 0.50`, fill n=1000.** He judged the ≥0.50 gallery good. Deliberately NOT higher — a higher bar trades breadth for flawlessness and admits only flawless pictures rather than creative ones; he re-evaluates only if the 0.5–0.7 band looks bad by eye. **It stays a PARAMETER while the rest of the parameters settle** (`--fine-bar`, recorded always, default `None`), and **the default flips in the same act that makes the first cascade record**. ⚠ Adopting the bar is NOT putting `p_fine` in the objective — separate moves, and the objective is untouched.

**★ THE DESIRE LIST IS GUIDANCE, NOT AN INSTRUMENT (Matt, ckpt 115 — supersedes ckpt 114's standing direction).** At the ratified bar every cell fills, so there is no set of unfillable cells to derive; the explicit version cannot exist without raising the bar, which Matt has declined. What survives, for designing the next mining rather than as a list to maintain: **`direct_trap_multiply` is the only mode provably short on supply** (7 places against a floor of 16) and it also clears best in both mining arms while taking NO seat in either; **lime and cyan are the only two hues that thin as the bar rises** and the head scores them honestly, so more of them at real quality is a real want; and `light_vivid_lime` is good at some modes and bad at `smooth_curvature`, so an aim is a hue CROSSED WITH a mode. Re-read these from a fresh solve; never maintain a standing list. ⚠ **Nothing has ever measured whether a mining leg aimed at a coordinate produces candidates in it** — measure the hit rate inside the next aimed leg, or a disappointing result cannot be told from a bad target.

**★ AT 0.50 SUPPLY IS NOT THE PROBLEM (ckpt 115, measured).** A view narrowed to `p_fine(≥4) ≥ 0.50` fills 1000, and so does 0.60; 0.70 read 943 but the chain stage stopped on its budget with sweep 2 still finding chains, so **0.70 is OPEN**, and 0.80/0.90 were never run. The filter RAISES the objective — 1786.5 → 1876.6 — while filling the same thousand seats, so the unfiltered solve leaves objective on the table; the median barely moves (0.9343 → 0.9314) because the bar deletes the worst fifth rather than improving the gallery. 581/1000 seats and 649/1000 places shared with the control. **The chain stage is what makes any of these galleries** — the seed alone never fills (993 / 792 / 775 / 719). Coverage is not a hole: the fine head has read exactly the 40,127 clearing rows, `clearing == above_bar` set for set. Everything → `curation/GALLERY.md` and `curation/MEASUREMENTS.md`.

**★ WHICH AXES ARE HELD UP BY A RULE (ckpt 115).** `cell_allowance` is the single largest consumer, levelling 39 of 48 held cells at exactly 42 seats; `spiral` binds exactly at its cap in every run; `family_allowance`, `mode_ceiling` and `group_cap` refuse ZERO in all four runs. Hue family, partition, plane, centered, tone and flatness are EMERGENT, riding on the cell cap. ⚠ **Refusal shares are compared against the view the run solved over, never against the whole pool** — pool-relative they look violently hue-skewed and it is an artifact of the filter.

**This era (ckpt 114→115, one day).** The known red was closed by building the ratchet; the re-materialization writer was named and the sweep/re-render loop disarmed by unioning `orphans`' reference set; two seat-identical solve speedups landed (control 71.7 → 63.4 s, narrowed 127.7 → 93.0 s); `BOUND_BLOCKS` 8 was priced, measured a LOSS and reverted; the augment inner clock failed its gate and was not applied; 6.39 GiB of unreferenced recolour cache was deleted from the ten `runs` legs; two artifacts-tier fixture leaks were fixed; the quality bar became a recorded solve parameter; the eye check closed the hue-bias question; and the website took the em-dash rule as its eighteenth check.

**Records.** Unchanged from ckpt 109 except as noted. Published, and the four the site stands on: `20260902T161757Z` · `20260902T164622Z` · `20260904T023748Z` · `20260904T233233Z`. `20260906T133236Z` is the tentative the browse page and the `gallery_grade` draw stand on — TENTATIVE, keep it. ⚠ **Every one of the 62 recorded stamps is `rank-key` seated; NO cascade record exists**, and one comes only once Matt settles the parameters. Every n=1000 solve this era was a COUNTERFACTUAL with NO RECORD.

## IN FLIGHT ACROSS THIS BOUNDARY — none.

## QUEUED IN DRIVE `prompts\` — none.

## NEXT CHECKPOINT GOAL — NOT SET. Matt raises it.

## OPEN (ordered) — Matt raises each
1. **`pictures/` in the ten `runs` legs.** 5.37 GiB remains after the `candidates/` deletion. It is held three independent ways, any one sufficient: 644 keys are `tentative.protected_keys()` and all 62 stamps name at least one leg picture; `absent_pictures()` would go 0 → 1,556 against TRACKED release rows, so rows and pictures cannot go as one transaction; and the gallery-grade head's population names 118. Replayability is total and is not the obstacle. `framings/` and `release/` were held for the same class of reason.
2. **Where the bar breaks.** 0.60 fills, 0.70 is a budget artifact, 0.80/0.90 unrun. The narrowed solve is 1.37× cheaper than it was, so it is cheaper to settle than when it was parked.
3. **The augment inner clock — a proposal, not applied.** `chain_at` has no clock check inside its walk, so `--augment-seconds` is tested only between seats and a pass overran a 300 s budget by 74%. The gate failed: two n=2000 tentative records were produced under a bound stage (`20260904T234133Z`, `20260905T001615Z`), so the change would re-seat records that exist.
4. **Records-only picture retention.** The sweep premise is dead; the cost is one-off at build. What survives is regeneration determinism. Direction → `preserve\retention_design.md`.
5. **`carriers.jsonl`** sits at 65.9% of the 1 MiB history guard, 4.3 drops away. **A cross-repo seam**: the website's `builder/palettes.py:carriers()` derives the same two columns.
6. **`itinerary.jsonl`'s guard** was raised to 786,432 and sits at 62%. The real horizon is roughly nine drops, a design question rather than a constant.
7. **Website** (Matt's pace). **Per-page status, masters, sweep state, figure holds and review rounds live in `docs/page-review.md` — cite it, never restate it here.** Still open there: `locations-walk-lengths` letters a run identifier into its own picture; the re-base onto a newer record, named and unscheduled; **the front page's Gallery curation blurb still makes two claims the Overview v2 placement retracted** — quality-first-then-constraints, and every rendering mode represented, the second of which the adopted bar makes definitely false; and `palettes/all-palettes.html`'s 13 em-dashes, generated, so `builder/palettes.py`'s to rule on. Stale figures and prose are NOT tracked or refreshed until "ready for publishing".
8. **The reframe channel's cadence.** Label-bound rather than clock-bound. Sizing → `curation/MEASUREMENTS.md`.

Parked → `preserve\parked.md`: augment at n=2000; the rung-frame overwrite; the `mine` leg's autolevel stamp gap; medium refactors; the `tia` bound question; the `groups.jsonl` re-cut; **`BOUND_BLOCKS` 8** (priced at 260.94 s and a 298 → 517 MB store, seat-identical, and 1.10–1.17× SLOWER — the bound already settles 99.905% of seat comparisons, so the aim was at the wrong denominator; verdict in `rules.BOUND_BLOCKS`); **the K re-sweep under the cascade** (dropped by Matt, ckpt 115); **the desire list as an explicit instrument**.

## STATUS / KNOWN REDS
**NO KNOWN REDS.** The ckpt-114 floor red is closed: `run_index_named`'s constant floor became a ratchet — store count plus deletions recorded since the high-water mark equals the mark, marks kept PER COUNTER, the 22 lost rows entered once as a reconciliation against a mark held at 13,526.

Fast lane 3,925 passed / 124 deselected, ~123 s. **The slow lane last read 4,043 in 6:55 and should next read 4,049.** `ruff` clean both repos. Website `builder check` **18** green with nothing skipped, 47 JS tests.

## RULINGS THIS ERA
→ `preserve\rulings_*.md §ckpt 115`.

## KEEP LIST
Drive `prompts\`: **wipe everything** — nothing is queued. `reports\`: **wipe everything** — all thirteen were read. Wallpapers `scratch/`: KEEP `filtered_view_p_fine_0907/` (the adopted ≥0.50 gallery sheet), `gallery_by_p_fine_0907/sheet_lib.py` (the builder every later sheet reuses), and `eye_check_calibration_0907/`; **WIPE everything else, including `ckpt113_fine_head_weak_seats/`** — the blind sheet was kept only because X was unratified, and X is ratified. Website `scratch/`: KEEP `_modes_render_times.py`, the walk-descent figure rig, and `three_bands/pick_seats.py`.

## OWED
Nothing.

## SCRATCH/ARTIFACT FLAGS
Standing KEEP: `artifacts/curation/candidate_ledger/` · the FIVE Durables · `neutral_embeddings.jsonl` · `artifacts/curation/` HOT · live release rows · `artifacts/reframe_g1…g10` · `artifacts/curation/tentative/<stamp>/` — every record (prune-protected) · `artifacts/votes/` kits · `artifacts/curation/growth/20260902T150756Z/` · `data/coloring/texture_flat.jsonl` · `data/spiral/` · `models/spiral/` · `models/render/` weights-v6 beside v5 · `models/gallery_grade/` · `artifacts/gallery_grade_head/pool_scores.jsonl` — the cascade REFUSES without it · `artifacts/render_folds/` · `artifacts/top_slice_probe/` · `artifacts/gallery_grade/n1000_0906/*/plan.jsonl` — the only thing that can rebuild the 373 levelled pictures as they were judged · `data/curation/candidate_ledger/ratchet.jsonl` — tracked, append-only, the ratchet's whole history.

**★ THE FIELD DUMPS ARE KEPT (Matt, 2026-09-07).** `artifacts/curation/depth/*/fields` holds roughly 11 GB, about 226 MB a leg, and it accumulates. The orphan sweep is **structurally** unable to reach it — `picture_dirs` enumerates `<subtree>/<leg>/pictures` at a fixed depth — so this is a ruling about growth, not an exemption anything could violate. ⚠ A leg directory's size is dominated by `fields/`, so a picture count is a bad estimate of what deleting one frees.

**★ `artifacts/curation/gallery/` — 53 MB, 14,438 gate attempt rows — is KEPT (Matt, ckpt 113; reaffirmed ckpt 115 for figure and tracking reasons).** ⚠ **It is now LOAD-BEARING in a second way**: since ckpt 114 `orphans` reads those attempt rows and is their only reader, so removing the hot copy would drop 3,530 names from the reference set and re-arm the sweep/re-render loop the union was built to stop. Moving it to archive means teaching the reference set to read the archive copy FIRST. All four passes verify byte-for-byte against `<archive>/fractal-wallpapers/artifacts/curation_backup/gallery/`, and the manifests carrying those hashes live only at `git show f208911^:data/curation/gallery/<pass>/gate.manifest.json`.

⚠ **`.leveled/` DIRECTORIES ARE NOT SWEEPABLE** → `preserve\leveled_identity.md`. ARCHIVED (RESTORE before reuse): unchanged from ckpt 106. Walk ledgers: `discovered_priors` reads BOTH tiers while a harvest defaults to hot, so every header records which it read.

## CLOSED (records wiped — verdicts in the docs and the rulings parts)
SHOW_ckpt114_n1000_gallery_by_p_fine_0907 · AUDIT_ckpt114_runs_rematerialization_writer_0907 · AUDIT_ckpt114_desire_list_shape_0907 · AUDIT_ckpt114_filtered_view_resolve_at_p_fine_0907 · FIX_ckpt114_named_picture_ratchet_0907 · FIX_ckpt114_solve_profiling_and_speedups_0907 · FIX_ckpt114_wallpapers_leftovers_0907 · FIX_ckpt114_bound_clock_and_legs_0907 · FIX_ckpt114_website_leftovers_0907 · FIX_ckpt114_website_emdash_check_0907 · SHOW_ckpt114_eye_check_calibration_0907 · PRECLOSEOUT_ckpt114_promotions_0907 · FIX_ckpt114_recorded_p_fine_bar_0907.

## PARKED / SETTLED
→ `preserve\parked.md`, `preserve\rulings_corpus.md`, `preserve\rulings_curation.md`, `preserve\rulings_sourcing.md`, `preserve\rulings_engine.md`, `preserve\rulings_website.md`, `preserve\rulings_method.md`, `preserve\sourcing_channel_laws.md`, `preserve\retention_design.md`, `preserve\solver_design.md`, `preserve\leveled_identity.md`. The old `settled_rulings.md` is a stub index.
