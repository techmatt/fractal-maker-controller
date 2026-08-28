# fractal-state — checkpoint 87 (2026-08-28)

## Where we are
**THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE (Matt, ckpt 86):** (1) the high-quality LOCATION hunt · (2) the high-quality WALLPAPER hunt · (3) the final curation SOLVE + release render. This era did not advance a phase; it closed the gap between what the docs said the pipeline does and what it does. Two audits, a judge grade, a preserve edit and the alignment build closed it.

**The production mining loop is `curate depth run`, not `curate hunt run`.** `hunt` has made 644 of the ledger's 85,129 rows; `depth` made 48,994 in one night. The docs named the wrong command for two eras, and both of this era's audits had to correct for it before they could answer anything. **Assume any pre-ckpt-87 statement about "the hunt" describes a loop that is not in production.**

**The judge was graded and NOT adopted.** `input_detail` at 768×448 is a real, seed-stable +0.0393 on the whole strange ≥4 boundary and clears every guard, but adoption moves the CORN scale and costs a re-score for a gain that may not survive at candidate geometry. Everything a future retrain needs → `preserve\judge_training.md`. **Read that before specifying any retrain.**

## OPEN (ordered) — the alignment plan
1. **P2 — selection alignment.** The census with a score floor (counts must be DISTINCT LOCATIONS, not rows), per-constraint headroom *and* the marginal cost of buying it, `curate seat` as a greedy over the ledger with a ledger-backed `Lens`, the rejection ledger as the product, and neutral pre-selection so pairwise diversity stops being a coupled constraint. Design, rulings and the fitted bars → `preserve\selection_design.md` §Greedy-first selection. Cite, never restate.
2. **P3 — does conditioning move the QUALITY column?** The dominance column is answered (→ fractal-discovery §Mining economics). Whether the `P(≥4) ≥ 0.50` rate survives conditioning is unmeasured, and it is what decides whether a colour target is cheap. One conditioned arm beside a control, ~1 h.
3. **Mine**, sized by P2's census rather than by a wall-clock budget. **The pool supports N≈150 and is nowhere near N≈1000** — 1,254 distinct locations clear 0.50 in total, against 1,000 seats before the diversity radius takes its cut.
4. **P4 — delete the old pre-solver gallery curation phase**, and the colour map with it (→ fractal-tutorial). The SOLVE and the RELEASE RENDER stay. Check first: the website's held `gallery-*` figure makers, and the 1,591 ledger rows backfilled from the release store.
5. **P5 — repo-side doc riders.** Most doc drift was absorbed this closeout; what remains is README-side and named in the audits' disagreement lists.
6. **The correction sheet on the first real solve** — ruled ckpt 83, still not run; the solver has never been crossed against eyes.
7. **Judge adoption** — deferred, not rejected. Re-entry instrument is the candidate-geometry check (→ `preserve\judge_training.md`).

## RULINGS THIS ERA (Matt)
- **GREEDY FIRST.** A trivial greedy satisfies the current need: find which hard constraints are unsatisfiable so mining can target them, and what the worst results are so the soft objectives can be tuned. Tighter optimization only once a reasonable satisfying solution exists. **A slow solve that reports "there are no light greens at all" is a MAJOR FAILURE** — that answer comes from a cheap pre-solve census. **Do not engage a solver until every constraint is individually easy** (not 5 light greens for 5 seats, but ~25). → `preserve\selection_design.md`.
- **Pairwise diversity moves to POOL CONSTRUCTION** via the neutral descriptors — if the neutral descriptors differ enough, the coloured ones almost certainly will.
- **NOT SHIPPING THE JUDGE.** Deferred on cost, not rejected.
- **RETENTION: store the successes.** Keep the top 5 per (location, mode) by within-mode rank, every human-labeled row, and a 1-in-200 reservoir. **Rows are never dropped, only pictures** (test-pinned). Storage scales with locations explored, not attempts made.
- **The colour map is deleted** — superseded by measurement (→ fractal-tutorial).
- **The old pre-solver gallery curation phase goes; the solve and release render stay.**

## KEEP LIST — survives this boundary
**Nothing.** `prompts\` and `reports\` are wiped entire at this closeout. Every fact worth keeping from this era's reports has landed in a doc line or in `preserve\`; the per-mode crossover table — the only thing too numeric for these docs — is in `selection_design.md` §Greedy-first selection, and the retrain method is in `judge_training.md`.

## INVALIDATED WITHOUT AN EDIT
- **Every "the hunt does X" statement** predating this checkpoint. The production loop is `depth`, which is location-blocked with the roster cycled inner (one palette per mode per turn), terminates nothing adaptively, and knows no "cycle" — that word names nothing in code and meant "one overnight run".
- **The palette head is not in the production mining loop at all.** `depth` draws colormaps uniformly from the 822-map collapsed pool. The 0.17× green-carrier pick deficit is a true fact about the retired gallery pass and **cannot explain anything in the current ledger**.
- **`AUC(≥4)` does not peak at epoch 11–13** on a lineage-grouped stop slice; it peaks at 5–6. Never re-quote "87% of each run's wall is past the kept epoch".
- **The 7× per-mode cost spread and the 1.6× flat-vs-ranked signal** are both wrong as stated — one is roster-dependent, the other is a mean-vs-median confusion. Corrected in fractal-discovery §Mining economics; never re-quote either from an older doc.

## SESSION-SIDE CHORES
None owed. `preserve\judge_training.md` was created this era and `selection_design.md` gained §Greedy-first selection; both INDEX entries and the two INDEX corrections land in this apply prompt.

## PARKED / SETTLED
Parked → `preserve\parked.md` (gained this era: the judge adoption with its re-entry instrument; the aspect-ratio training arm). Declined and never-re-raise → `preserve\settled_rulings.md`.

## CLOSED (records were `reports\`, now wiped — verdicts are in the docs)
AUDIT_mine_loop_cost · AUDIT_targeted_supply · render_judge_grade · edit_selection_design · loop_alignment.

## SCRATCH/ARTIFACT FLAGS
KEEP: `artifacts/curation/candidate_ledger/` · the candidate JPEGs (archive tier — **check free space before sizing another mine**; a retention prune would free 3.735 GiB of 12.18) · `artifacts/curation/neutral_embeddings.jsonl` (29,381 rows, complete) · `artifacts/render_cv/` (five folds dealt and reusable) · `artifacts/curation/` (HOT).

⚠ **`artifacts/node_views/` does not exist** and previous keep lists were wrong to name it; the location head's own view is `models/location_view.py`.

Nothing else under `scratch/` must survive.

## ROSTER — sizes at ckpt 87
state ~5k (wholesale) · tutorial, discovery, corpus edited by hunk · operating one hunk · **engine CLEAN, not emitted**. Preserve: `settled_rulings` and `parked` APPEND, `INDEX` and `selection_design` by hunk, all in this apply prompt.
