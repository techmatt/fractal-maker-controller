# fractal-state — checkpoint 94 (2026-08-31)

## Where we are
THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE: (1) the LOCATION hunt · (2) the WALLPAPER hunt · (3) the final curation SOLVE + release render. `MODE_POLICY` is the one place a mode carries a standing; Matt iterates from pictures, not counts.

This era: **weights-v5 shipped** (all-data retrain, Matt's design after the ckpt-93 holdout error) and the whole scoring plane moved onto it — the flip emptied the pool by design and the full rescore closed it. **The picture accident closed better than pre-accident** (PRUNE3 + the pool re-render; 0 absent anywhere; guard green). **The mode floor was measured by flag.** And **`itinerary` was exposed: 55.3% of its entire record — and 9 of its 14 current gallery seats — is bit-for-bit `smooth` + `transfer:{"kind":"rank"}`** (all 1,962 rows shift-pair rendered), and Matt's labels are indifferent to the difference within any one batch.

## IN FLIGHT ACROSS THIS BOUNDARY
Nothing. Every prompt reported and committed.

## NEXT CHECKPOINT GOAL
Matt's to set. The queue's head is OPEN 1.

## OPEN (ordered)
1. **The itinerary ROUTING RULING (Matt).** What a degenerate row is: `smooth`-with-rank (moves 110 labeled rows across judge stores — `finished.check` refuses that without a ruling; `hunt.kind_of:847` is the router) versus flagged-but-still-itinerary. Blocks 2–4. Matt's stated principle: itinerary only counts as itinerary if it actually modulates something.
2. **The flat-texture FLAG build.** The engine computes the degeneracy exactly and throws it away: `Stretch::over`'s span else-branch (`coloring.rs:748-754`) at the modulate call; wire it up the `RenderReport.interior_fraction` precedent (`colorize.render` currently DISCARDS the report at `curation/colorize.py:609`); carry it on the ledger row as a bare boolean (`at_candidate_regime`'s shape per `candidate_ledger.row:294-299`, NOT the flatness sidecar — `flat16` measured blind to it, 0.182 vs 0.170). Readers that route on it: `solve.py:405`, `headroom.bars/clearing`, `mode_policy`, the label-store router. The near band never sees itinerary (not shareable).
3. **`tail_itinerary` — the first NEW mode.** "Last `depth` symbols before escape": a third `AddressStart` variant, exact only at `weight_base` 4 (rolling window `frac(value·base)+sector·base^-k`), nothing renamed (`skip_serializing_if` default), NECESSARILY a new catalog mode — changing itinerary's own constants renames every cached itinerary picture. Two ruling spots, not hacks: `Symbols.spells_z0` bool→three-valued; `agrees_with_family` matches `start: Z1` by name, so a third variant is silently legal on both planes (correct for a tail start). The only pictures-adding item on the queue.
4. **The mode-floor FLIP — now MEASURED** (report on KEEP). Floors fill, `starved` empty, census bound met exactly (45 = 45); 3 of 13 floors bind (`itinerary` +7, two direct traps +1); the rule moved 52 of 150 seats, not 7 — the 45 early scarcity seats drain cells/locations/groups from the general leg; `cell_allowance` 2,111→3,012, twins 97→73; floored is BETTER on raw p̂₄ (127 vs 123 above 0.90, sum +0.89) and WORSE on the fitted key (−2.02, floor 0.4217 vs 0.4564). An eye call — and it waits on 1–3, since itinerary's binding floor is ~half wrong-named rows on the measured base rate.
5. Does the solve enforce a realized strange share? Unchanged; Matt judges 0.60 from galleries.
6. **The forward-draw sitting** (the only instrument for what the judge is FOR). New this era: the restored ledger rows carry BOTH v4 and v5 scores (sidecar is per-artifact), so the top-k disagreement is computable offline — caveat: the pool was retained under v4.
7. **The colour ceiling binds at n=150** — still the largest live refusal either side of the floor flag. → `preserve\selection_design.md`.
8. n=1000 not demonstrably feasible — a mining question.

## RULINGS THIS ERA (Matt)
- **★ STOP CONSTRUCTING HOLDOUTS.** The ckpt-93 TRAIN design withheld every post-cut row (634 fours, more than train held) into a comparison slice the incumbent had saturated — so the head never saw the new fours and the comparison had no headroom. Retrain = ALL data, random 80/20 grouped by lineage, no date carve-out, no pin-driven construction; early-stop on AP(≥3) (AUC(≥3) fallback), patience 6 cap 20, precision@k as readout only; THREE split seeds, ship the best by stopping-slice AP; NO incumbent comparison — the forward draw is the comparison.
- **★ A JUDGE FLIP EMPTIES THE POOL** (measured, twice): `scores_by_recipe` reads live-artifact rows only. Adoption + floor refit + FULL rescore are ONE act. "Mixed vintages accepted / lazy rescore" is RETRACTED as a description of the code; score rows do carry `judge_artifact` and old rows persist beside new.
- **The rank key STAYS AS SHIPPED; the complexity question is CLOSED.** The preference is not in the labels: within kind, tier runs marginally AGAINST busyness (grad_energy −0.14/−0.18); conditional on the judge `bpp` is +0.003 AUC. Matt: no strong motivation to change. `curation/detail.py` deleted.
- **Itinerary counts as itinerary only if it modulates something** — OPEN 1 operationalizes this.
- **★ UNATTENDED PROMPTS NEVER CONTAIN A STOP-AND-ASK GATE** (an overnight envelope was wasted on one). Wrong-repo guard is the only STOP; every other gate is a branch; stop time may arrive in the launch message.

## CLOSED CAVEATS
The ckpt-93 "every seat, solve and pool figure predates the accident" caveat is CLOSED: PRUNE3 verified the pre-accident numbers at v4 (pool 97,557; floor 0.994846; `direct_trap_screen` gained a seat), then the plane moved to v5 (97,423 candidates, 11,137 clearing, 4,480 places; `smoke5_v5` at 150/150, 14 modes, is the floor-inert baseline).

## KEEP LIST — survives this boundary
`reports\TRAIN_render_judge_v5_report.md` · `reports\AUDIT_itinerary_degenerate_report.md` · `reports\CLOSE_pool_rescore_and_floor_measure_report.md` (the material for OPEN 1–4 and the owed doc) · `reports\label_ingest_tiers.csv`. Both Drive folders otherwise wiped entire.

## OWED
1. `preserve\judge_training.md` — still owed, now with its material on the KEEP list: the three ckpt-92 rulings, the all-data method above, the saturation finding, and the stopping-resolution law. Session-authored, never by a code prompt.
2. Two module-README notes ride the next wallpapers prompt: `curation/flatness.py` must say its column is blind to a dead TEXTURE layer as distinct from dead space (0.182 vs 0.170); `models/renders.py` `FIELD_IDENTITY` block records that an itinerary field is never cached (mode not shareable).

Done this era, not re-raised: `curate re-render` exists (`recipes.live_stamp` is the one autolevel-stamp spelling; a pool row is not a picture — `origin_of` chains) · `mode_policy`'s census basis corrected (per RENDER, row basis stated beside; flat-draw counterweight in) · `engine_fingerprint` docstring honest · the floor guard is `test_the_floor_rule_is_reachable_only_by_naming_it` (cli.py only, parser default off) · slow lane re-priced by data, recorded in the lane entry.

## SCRATCH/ARTIFACT FLAGS
Standing KEEP unchanged: `artifacts/curation/candidate_ledger/` · flatness sidecar + manifest · `neutral_embeddings.jsonl` · `artifacts/render_cv/` · `artifacts/curation/` HOT · live release rows · `artifacts/renders`. **Nothing under `scratch/` survives this boundary.**

## CLOSED (records wiped — verdicts are in the docs)
`TRAIN_render_judge` (nothing adopted; design superseded) · `TRAIN_render_judge_v5` (SHIPPED, floors refit in-run) · the PRUNE3 recovery · `MINE_v5_first_seating` v1/v2+addendum (superseded unrun) · `SMOKE_v5_first_seating` · `DESCRIBE_rank_key_complexity` (closed, no change) · `AUDIT_itinerary_modulate` · `SHEET_itinerary_texture_axes` · `AUDIT_itinerary_degenerate` · `CLOSE_pool_rescore_and_floor_measure`.

## PARKED / SETTLED
Unchanged → `preserve\parked.md`, `preserve\settled_rulings.md`. `input_detail` stays PARKED on its ckpt-93 terms.
