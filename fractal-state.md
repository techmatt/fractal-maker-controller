# fractal-state — checkpoint 90 (2026-08-30)

## Where we are
**THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE:** (1) the high-quality LOCATION hunt · (2) the high-quality WALLPAPER hunt · (3) the final curation SOLVE + release render. This era mined hard, learned that mining does not raise ceilings, labeled 1,224 rows, and turned what Matt saw into a **mode policy**.

**THE HEADLINE: `MODE_POLICY` EXISTS AND IS THE ONE PLACE A MODE CARRIES A STANDING.** Eighteen modes → `{0,1,2}`, **4 niche · 7 normal · 7 promoted**, fourteen accepted; `depth.DEMOTED` deleted, `BREADTH_DEMOTED` emptied to a per-run knob. Weight 0 is wired three ways; **weights 1 and 2 are recorded and bind nothing.** Live gallery `mode_policy_switch_n150` — 150 seats, `unmet` empty, 275,822 candidates, `cell_allowance` 4,652, weakest general-pool seat 66.52.

**Matt now iterates from pictures, not counts.** The niche cut was made by eye on a per-mode top-20 page and the label record agreed almost exactly; the two places it disagreed (`exp_smoothing` up, `direct_trap_screen`/`smooth_curvature` down) were both resolved by Matt on grounds no statistic holds.

**The era's negative result is the important one.** 45,508 renders over four legs moved one mode's `best_rank` by +0.0001. Mining buys SEATS, not CEILINGS. The one big operating lever it found is the near band, at 20.6× breadth in seats per wall hour.

**The colour ceiling is still the binding constraint** and this era did not touch it: 47 cells held, the same 28 sitting at their allowance of 7 before and after every change.

## NEXT CHECKPOINT GOAL (Matt)
**SHRINK THE TOTAL HANDOFF DOCUMENT SIZE** using the standard tactics — the deletion test, a number in a tracked file never appearing here, closed arcs to ≤3 lines, tombstones to `settled_rulings.md`. Two known targets: fractal-engine's autolevel passage and this doc's invalidation list, both written while live and now settled enough to compress hard. Two tables landed in `curation/README.md` this era (mode capability, historical per-candidate rates) precisely so the docs can delete what they restate.

## OPEN (ordered)
1. **The mode floor cannot exceed 1, and it blocks both of this era's rulings.** `seating.seat`'s scarcity leg `break`s on the first seat per mode, so floor 1 and floor 2 seat identically while the ILP honours the floor correctly — greedy and exact silently disagree. Until it lands, "promoted" changes no seat: `itinerary` was promoted and came out one seat FEWER. Fix + what reads the leg → fractal-tutorial.
2. **Matt's emission-weight design, unbuilt.** Within the strange share, `2·promoted + 1·normal` defines a fully-distributed target; the floor is `0.5 ×` that target. Floors then sum to exactly half the strange budget by construction. Two things it needs: a floor rule for `normal` too (or `direct_trap_multiply`, which Matt wants present, keeps a bare 1), and a measurement — 45 of 90 floored seats against a `cell_allowance` that is already the largest refusal.
3. **Make the smooth/strange emission split EXPLICIT** (Matt: a future checkpoint task). `run.STRANGE_SHARE = 0.6` is a SUPPLY split in `budget.head_slots`; **seating enforces nothing by kind** and `g2_n150`'s 55 smooth of 150 is emergent, though stable across four seatings (0.367–0.387). Every number in OPEN 2 hangs off this.
4. **`itinerary` composites — 2–3 new strange modes (Matt), before the retrain.** The engine already allows it; mechanism and the two real constraints → fractal-engine.
5. **`direct_trap_screen` needs a flat draw before any standing is written for it** — 40.4% tier-4 on its aimed arm against 0.6% on every row outside it, the widest gap of the nine modes ever aimed at.
6. **Judge retrain — deferred, not refused.** Everything it needs → `preserve\judge_training.md`. ⚠ **No eval instrument exists to grade it with**: all 1,224 new rows are train-side and the stores sit at 245 eval of 4,656 strange, 300 of 5,896 smooth. An eval-eligible draw must be registered BEFORE the retrain.
7. **Implement the scoring ruling.** Mining owns scoring; selection never re-scores. Needs the second-stage leg priced and per-mode bars fitted at whichever regime selection reads. ⚠ The release-geometry column will be a SELECTED sample — never read an unbiased AUC off it.
8. **The colour ceiling's allowance of 7** — binding at n=150. Write-up → `preserve\selection_design.md`.
9. **n=1000 is not demonstrably feasible** — constructive lower bound on non-twin capacity 532 against an upper of 1,038. A mining question.
10. **Intel XTU is Matt's to kill** — 885.96 MiB in one log, `XtuService` running and writing, bursty regrowth. Delete and truncate both refuse without elevation. The durable fix is stopping or uninstalling the service, not clearing the file again.

## RULINGS THIS ERA (Matt)
- **★ ONE TABLE CARRIES EVERY MODE STANDING.** Niche = excluded from labeling rosters, mining default rosters and gallery emission. Niche: `gaussian_int`, `trap_circle`, `smooth_trap_circle`, `direct_trap_ring`. Promoted: `tia`, `stripe`, `threads`, `smooth_stripe`, `smooth_mean_angle`, `smooth_angle_min`, `itinerary`.
- **★ "TOP UP LABELS" MEANS ACCEPTED MODES ONLY** — niche modes are out of labeling, mining and emission alike.
- **`exp_smoothing` stays NORMAL on REDUNDANCY, not quality** — it is the highest q3+ mode in the store (68.5%) and looks too much like `smooth`. **Every quality instrument we have scores a picture alone and is blind to redundancy against another mode.** `neutral_embeddings` centroid distance is the available instrument if that ever needs measuring.
- **`direct_trap_multiply` must have some presence in a final gallery**, judged on q3+ rather than q4 — the direct-trap family splits on q3+ (multiply 28.7%, lines 23.2%, screen 18.9%, ring 11.7%) the opposite way to q4.
- **A per-mode bar of "q4, or the top X% of what we can mine, whichever is higher"** is the shape Matt wants eventually; `headroom.bars` already does the supply-triggered version. Not worth building before the retrain.
- **A SHEET SHOWS ONE RESULT PER LOCATION.** **Sparse-mode harvests label the BEST ONLY** — no flat control stratum.
- **A demotion that stops a mode being mined is self-confirming** — `trap_circle` went from 0 fours ever to 12 in 260 the first time it was mined anyway.

## INVALIDATED WITHOUT AN EDIT
- **`renders.job_name` does NOT carry the mode catalog** — measured; adding a mode renames nothing. Two eras of docs said otherwise (fixed this closeout).
- **"11 of 18 modes on the `P(≥3)` fallback"** — now 8 default / 6 fallback / 4 with no bar, over `accepted()` only, and it is a fact about the pool on the day.
- **A concurrency ratio is not a speedup — and 1.92× was itself an estimate.** Three engines deliver **1.69×** against a bit-exact serial replication; the record's `concurrency` field over-reads 1.75×.
- **"Aim at MODES, not colour cells"** — the cells half stands, the modes half does not.
- **`colorize.render` cannot re-render a stored label row** — it builds its own recipe and would overwrite the curve, trap or palette pass on 58% of store rows. `renders.spec_of` is the route.
- **A short pilot is a floor, not an estimate** — pilot to a fixed fraction of the leg.
- **`--top-bands` does not cut the ranked draw**; `--band-weights` with lower bands at 0 is the flag.
- **`gallery_int`-era per-mode rates are historical** — every figure now lives once in `curation/README.md` with its conditions, headed "not comparable across rows".
- **The `strange_mode_census` page is a frame around 340 deleted images** in both copies; `table.md` and its report carry the numbers.

## KEEP LIST — survives this boundary
`reports\label_ingest_tiers.csv` (Matt's working CSV). `prompts\` and `reports\` are otherwise wiped entire.

## SESSION-SIDE CHORES
`preserve\settled_rulings.md` gains this era's tombstones (the two-strata blind design for sparse harvests; per-mode standings outside `MODE_POLICY`).

## PARKED / SETTLED
Parked → `preserve\parked.md`. Declined and never-re-raise → `preserve\settled_rulings.md`.

## CLOSED (records wiped — verdicts are in the docs)
mine_weak_modes · sparse_mode_harvest · smooth_500 · strange_mode_census · mode_policy · label_ingest · mode_policy_switch · cleanup_and_riders.

## SCRATCH/ARTIFACT FLAGS
**Ledger 366,236 rows**, all with a picture, 0 recipe-only, over **18,424 locations** (mean 19.88 recipes each, median 12, max 332); 18,407 embedded. Flatness sidecar **336,196 rows / 39.95 MiB = 91.8%**, undurable, regenerable while the pictures are on disk.

`artifacts/` is two tiers: hot `C:\Code\fractal-wallpapers\artifacts` **97.12 GiB / 664,757 files**; archive `E:\FractalStorage\...\artifacts` **99.18 GiB / 1,469,233 files** (`tiles` 65.91, `palette` 10.66, `node_views` 5.35, `location_views` 4.99).

KEEP: `artifacts/curation/candidate_ledger/` · the flatness sidecar · `artifacts/curation/neutral_embeddings.jsonl` · `artifacts/render_cv/` · `artifacts/curation/` (HOT) · the `mode_policy_switch_n150` release rows.

Deleted this era: 1.63 GiB (the stale 998-unit `sparse_mode_head_top` cut, the census renders and images in both copies, four decided contact sheets, a derived ledger index). `scratch/` went 771 MiB → **14.16 MiB / 205 files** and nothing under it must survive. Free: C 173.8 / 936.8 GB · D 164.7 / 931.4 · E 1,494.9 / 1,863.0 · G 165.2 / 936.8.

## ROSTER — sizes at ckpt 90
state ~7k (wholesale) · **engine, tutorial, corpus, discovery, operating all edited by hunk.** Preserve: `settled_rulings` APPENDS; `selection_design`, `parked`, `judge_training` unchanged; `INDEX` clean (no new files).
