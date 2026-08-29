# fractal-state — checkpoint 89 (2026-08-29)

## Where we are
**THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE:** (1) the high-quality LOCATION hunt · (2) the high-quality WALLPAPER hunt · (3) the final curation SOLVE + release render. This era built a rank key, adopted it on Matt's eyes, deleted the pre-solver pass, and **emitted the first solver gallery.**

**THE HEADLINE: `g1_n150` EXISTS.** 150/150 seats, 18/18 modes, 48/48 cells, `unmet` empty, released at 1280×720 ss2 in 9.4 minutes. Re-seated after an hour of mining: 23 seats in, 23 out. Sheets at `scratch/gallery_n150/` and `scratch/mine1h/`. **Matt now iterates from the gallery** — what is bad, he names; distribution, quality and retrains follow from looking.

**The rank key is shipped and default.** Shared weights over five columns — location `P(≥4)`, `P(≥3)`, `P(≥4)`, the calibration stratum, and `flat16` (Matt's density idea, the only feature earning on both kinds). Out of fold **0.779 smooth / 0.850 strange** against the incumbent's 0.671 / 0.826. Accepted by eye against `incumbent.html`, not by a bar.

**⚠ The incumbent reference line is inflated by train-side contamination.** `P(≥4)` reads 0.804 / 0.873 on the 851 train-side rows and **0.552 / 0.576** on the 200 eval-only ones. Every AUC taken off the joined population is measured against that inflated line — the rank key's win is conservative, and no clean estimate of either exists.

**The palette group cap is built and ruled but is not the quality lever.** Mean prior map tier moves **+0.035**; it buys 16 fewer distinct maps, not better ones, and at n=150 realizes a max of 2 against an allowance of 3.

**The colour ceiling is the binding constraint.** `cell_allowance` is the largest refusal in every arm; 28 of 48 cells sat exactly at their allowance of 7 before the mine, 27 after.

**Mining works and is now 1.92× faster.** One hour, two legs: four modes moved on `best_rank` (`direct_trap_ring` 0.435→0.666, `direct_trap_screen` 0.503→0.709, `gaussian_int`, `direct_trap_multiply`); **no colour cell moved.** `curate depth` runs on the locked three workers, partitioned by LOCATION so the field dump amortises.

## OPEN (ordered)
1. **Implement the scoring ruling.** Mining owns scoring; selection never re-scores. Needs: the second-stage leg priced (release-geometry scoring over the retention keep set — top 5 per (location, mode), labeled rows, reservoir), and per-mode bars fitted at whichever regime selection reads. ⚠ **The release-geometry column will be a SELECTED sample** — retention ranks on the cheap column, so only rows the cheap column liked ever get the expensive reading. Never read an unbiased AUC off it.
2. **Matt examines `g1_n150`** and names what is bad. Everything below reorders around that.
3. **Mine**, sized by the census. Aim at MODES, not colour cells — cells did not move. Merge between legs, not after both (two legs drew 47 places in common). Concurrency is available now.
4. **The colour ceiling's allowance of 7** — binding at n=150. The extra-picks-shaped question is written up in `preserve\selection_design.md`.
5. **Judge retrain — deferred, not refused.** Everything a retrain needs → `preserve\judge_training.md`. An adoption re-scales every probability and invalidates the score sidecar, so it is cheapest after the gallery, never before.
6. **P5 — repo-side doc riders**, README-side only, named in the ckpt-87 audits' disagreement lists.
7. **n=1000 is not demonstrably feasible** — constructive lower bound on non-twin capacity 532 against an upper of 1,038. A mining question, not a solver one.

## RULINGS THIS ERA (Matt)
- **★ MINING OWNS SCORING. SELECTION READS SCORES OFF ROWS AND NEVER RE-SCORES.** A candidate's score is recorded by the leg that made it, at the regime appropriate then. **The old candidate-column rule — "re-score the shortlist at shipping geometry and floor on that" — is DELETED, not deferred**; it was never implemented and the docs asserted it for eras. What is live: candidate-column throughout with per-mode bars, 11 of 18 modes on the `P(≥3)` fallback, no bar at release.
- **★ RUN DURATION (replaces N−2 entirely).** "An N-hour mine/crawl" means **N hours of that leg**, wall clock; build, merge, readout and report sit OUTSIDE it. "Finish by X" means the ENVELOPE: reserve the build and readout actually expected for that prompt, state the reservation so Matt can correct it, size the leg to land on the deadline. The budget is a TARGET, not a cap. A follow-up leg of any length is a new budget question.
- **The rank key: smooth MIRRORS strange** — same form both kinds. No colormap identity, no colormap label history, ever. **A colour DESCRIPTOR read off the finished picture is a legitimate future feature**; the colormap index is not.
- **Shared weights, not per kind.** Per-kind read +0.018 [−0.002,+0.039] on the shipped form — not worth the complexity. Settled.
- **The flatness sidecar stays undurable** — regenerable by `curate flatness sweep` (~33 s per 8,192 rows, ~7 min for the store), no manifest, no copy on merge. ⚠ Regenerable only while the pictures are on disk; a pruned row's flatness cannot be recomputed, and a pruned row is not seatable anyway.
- **An unresolvable picture name REFUSES.** A *missing* picture is expected and is filtered at the pool; an *unresolvable name* is a broken invariant and stops the pass. Applies to `solve.picture_of` and the cloud readers.
- **Colour conditioning is mode-dependent by design**, not defective: it works where the colormap determines the picture's colour, not where a trap does. Field leg delivered 38.4% against 1.27%; composites 10.9% against 0.85%.
- `ceiling.Seating` / `Lens` / `Rule.begin` **pruned**. Three-worker rule now universal. `curate manufacture --step knobs` re-dumps on absence and selects on what a row **is**, never on what is still cached.
- **P4 executed** — the pre-solver curation phase is gone.

## INVALIDATED WITHOUT AN EDIT
- **The ckpt-88 map-history AUC 0.643 is a CROSS-STORE POOLED read.** Split: **+0.248 smooth / −0.217 strange**, both CI-excluding. Never quote the pooled number.
- **"The cap is the cheapest half of the quality gap."** It moves map tier +0.035.
- **4.70% / 1.41% are ROSTER figures, not constants** — measured on a smooth-heavy roster. On weak modes the sign flips: the field leg's conditioned arm cleared 2.7× its own control.
- **A best-available percentile is not a mining readout.** The denominator moves — `trap_circle`, aimed at by nothing, rose 1.86 points. Only `best_rank` separates a move.
- **The incumbent's 0.826 / 0.731 AUCs** are train-side inflated and not carryable.
- **"The combination demoted the tier-4s"** was a pooled-across-store read and does not stand.
- **The scarcity leg is not the seating tail** — `general_pool` holds 34 of the bottom 38. The ckpt-88 "18 of 150" did not generalize.
- **A concurrency ratio is not a speedup** — engine-seconds over wall reads 2.94× on a leg delivering 1.92×.
- **Every rate in the depth table is ONE ENGINE'S**, all measured single-engine. A rate read off a three-worker leg over-prices a serial one by ~1.6×.
- **`128,317` vs `128,368`** was pool vs ledger, no discrepancy. The ledger is **136,560** now.
- **1280×720 ss2 was measured** (gallery4, 3.45 s/row); the candidate render is 640×360 **ss2**, so release is 4× its field samples, not 16×.

## KEEP LIST — survives this boundary
**Nothing.** `prompts\` and `reports\` are wiped entire.

## SESSION-SIDE CHORES
None owed.

## PARKED / SETTLED
Parked → `preserve\parked.md`. Declined and never-re-raise → `preserve\settled_rulings.md`; gained this era: per-kind rank-key weights, the colormap identity / label-history route, the render-block join hypothesis, and the N−2 reserve.

## CLOSED (records were `reports\`, now wiped — verdicts are in the docs)
rank_key_replay · label_join_recovery · disk_reclaim · rank_key_fit · pool_picture_guard · seating_cap_and_key · gallery_n150 · P4_delete_gallery_phase · mine1h · ceiling_prune · cleanup.

## SCRATCH/ARTIFACT FLAGS
KEEP: `artifacts/curation/candidate_ledger/` (**136,560 rows**) · the flatness sidecar (regenerable, ~7 min) · `artifacts/curation/neutral_embeddings.jsonl` · `artifacts/render_cv/` · `artifacts/curation/` (HOT) · the `g1_n150` release rows · `scratch/gallery_n150/` and `scratch/mine1h/` (Matt is still looking at these).

Deleted this era: `manufacture` and `runs` `.f32` dumps (24.05 GiB); `depth` and `mine` dumps KEPT — those legs revisit places. `artifacts/node_views/` was 5.7 GiB and is archived to E: (the old flag saying it does not exist was wrong). 98.56 GiB of Intel XTU logs in `C:\ProgramData` were the real disk problem and will accumulate again.

Nothing else under `scratch/` must survive.

## ROSTER — sizes at ckpt 89
state ~7k (wholesale) · tutorial, corpus, discovery, operating edited by hunk · **engine CLEAN, not emitted**. Preserve: `selection_design`, `settled_rulings` and `parked` APPEND; `judge_training` unchanged; `INDEX` clean (no new files).
