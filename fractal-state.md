# fractal-state — checkpoint 88 (2026-08-28)

## Where we are
**THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE (Matt, ckpt 86):** (1) the high-quality LOCATION hunt · (2) the high-quality WALLPAPER hunt · (3) the final curation SOLVE + release render. This era built selection alignment end to end, mined against it, and — for the first time — crossed the output against Matt's eyes.

**THE HEADLINE: the render judge's `P(≥4)` is a well-calibrated THIRD-cutpoint screen wearing a fourth-cutpoint name, and hard selection preferentially picks its false positives.** Both were measured on one 200-row correction sheet. Calibration gap +0.573 on `P(≥4)` against +0.060 on `P(≥3)`; no threshold anywhere on the column buys tier-4 precision (0.309 / 0.309 / 0.298 / 0.364 at ≥0.50 / 0.99 / 0.999 / 0.9999) while every threshold buys `≥3` purity (0.913 → 1.000). `AUC(≥4)` inside the seats is **0.499**. **Read the column as a ≥3 screen and nothing more.**

**The first absolute reading on a seated floor.** `p2b_n150` is tier 4 at **30.7%** [23.8, 38.5], tier ≥3 at **91.3%** [85.7, 94.9], mean tier 3.21. Its top 20 by head score are 6/20 tier 4 and 20/20 ≥3: a twenty-seat gallery cut off this seating is all-good and mostly-not-excellent, **and the head cannot pick which six.**

**Selection costs quality at matched score.** Seats 0.307 tier-4 against a rule-free control block's 0.640; matched on head score and stratified by store, 0.309 vs 0.640 (`p = 0.0009`), decisive on the smooth side. Mechanism, as far as 200 rows name one: the seating capped palette groups at 1, so its 150 rows sat on 150 distinct maps where the control's 50 sat on 40 — it reaches into worse maps (mean prior map tier 2.53 vs 2.78) *and* stays worse at matched map quality. **A map's own human label history predicts tier 4 inside the seats at AUC 0.643 where the head's `P(≥4)` reads 0.489.** A statistic the head does not use beats the head at its own top.

Saturation is real and smaller: inside the control's two-thousandth-wide band the head has no ordering (Spearman −0.116), but the level is worth 4–7× the corpus base rate. The head's top is worth having; the seating gives most of it back.

## OPEN (ordered)
1. **The palette group cap — RULED, unbuilt.** `max(1, floor(0.025·n))`: 1 up to n=40, 3 at n=150, 25 at n=1000. Build it, re-seat at n=150, and report the realized max-per-map and the map-quality distribution of the seats. This is the cheapest half of the quality gap and it retires `palette_group_cap` as a binding block permanently.
2. **A map-quality term in the seating.** The map's own human label history reads AUC 0.643 where the head reads 0.489, and it needs no weights and no retrain. Cheapest instrument this era produced.
3. **P4 — delete the old pre-solver gallery curation phase.** The SOLVE and the RELEASE RENDER stay. Check first: the website's held `gallery-*` figure makers, and the 1,591 ledger rows backfilled from the release store.
4. **The tracked ledger manifest is stale by 112,362 rows.** `data/curation/candidate_ledger/rows.manifest.json` records 16,006 rows dated 2026-08-26 and predates several merges, so `curate candidate-ledger check` cannot pass. A durability manifest that silently stopped tracking its file needs a decision.
5. **P5 — repo-side doc riders**, README-side only, named in the ckpt-87 audits' disagreement lists.
6. **Judge adoption — OPEN, needs discussion, do not specify a retrain first.** Three things changed. The pinned strange holdout went **4 → 27 tier-4 rows** and ≥3 from 6 to 68, the first material feed for the boundary that starves it. But `input_detail`'s +0.0393 was measured on an *unselected* holdout, and this sheet says the operating point that matters — the top of a hard-selected pool — has `AUC(≥4) = 0.499`; a +0.04 on a broad AUC is not evidence about a population where the incumbent reads chance. And the cheapest instrument here is not weights at all (item 2). Everything a retrain needs → `preserve\judge_training.md`.
7. **Mine**, sized by the census rather than by a wall-clock budget.

## RULINGS THIS ERA (Matt)
- **DIVERSITY IS TWO RULES, NEITHER IN THE SOLVER.** Neutral pre-selection at pool construction (geometric distinctness, cosine radius **0.02**) plus the pixel-cloud twin test as sequential state in `curate seat` (**`ceiling.TAU` = 0.0586**). `solve.RADIUS` is RETIRED — one number for one fact.
- **`solve.MODE_FLOOR` = `floor(N/100)`** — 0 at n=20, 1 at 150, 10 at 1000 — replacing the flat 1-per-mode, with a flag for an artificial floor in debug.
- **The palette group cap becomes `max(1, floor(0.025·n))`.** Slack, not identity. **There is NO coverage requirement on palettes and never will be** — nothing asks that every palette be used; the cap is a ceiling against repetition, and the colour distribution is a separate mechanism over dominant cells read off the finished picture.
- **`teal_conditioned` is MERGED** (Matt): the supply is real, and `hunt.drawn_for` keeps it separable.
- **The slow test lane is OFF by default in prompts** — on only when a prompt says a specific task needs it. A separate prompt to speed it up is planned.

## INVALIDATED WITHOUT AN EDIT
- **The "39% tier-4" rate over all 200 sheet rows is a rate about NEITHER block.** Quote 0.307 seats / 0.640 control, never the pooled number.
- **"108 of the 200 places carry train-side rows, 92 pinnable"** was counted off the candidate ledger. The labeled stores hold a prior same-store row at **66** of the 200 places; the realized pin is **150 of 200**, and all 50 unpinned rows sit on a contested place.
- **"Pairwise diversity moves to pool construction" as a COMPLETE rule.** Neutral descriptor distance against pixel-cloud W1 is Pearson 0.034; the twin pairs sit at a median neutral distance of 0.226, three times the loosest radius. The neutral rule cannot cover colour twins and never could.
- **The ~940 s teal figure is not a conditional cost.** It is total render history over wins and decomposes 17.2 × 3.47 × 40.8; conditioning attacks only the third factor.
- **The 6.96% ledger-wide clear rate is not a draw rate.** It is dominated by near-band and mode-floor draws on already-proven places. A fresh breadth draw on never-opened locations clears **4.70%**, and that is the denominator a new arm is read against.
- **Any `headroom` marginal cost read after the teal merge without a `drawn_for` filter.** `headroom._row` under-prices a teal win by 16% on renders and 24% on seconds; there is no scalar correction, because the two move by different factors.
- **"12 new teal locations against the 35 the ledger held"** is 13 against 42.

## KEEP LIST — survives this boundary
**Nothing.** `prompts\` and `reports\` are wiped entire. Every finding worth keeping is a doc line, or sits in `preserve\selection_design.md` and `preserve\judge_training.md`.

## SESSION-SIDE CHORES
None owed.

## PARKED / SETTLED
Parked → `preserve\parked.md`. Declined and never-re-raise → `preserve\settled_rulings.md`; gained this era: no palette coverage requirement, `solve.RADIUS`, and exact optimization below n=150 (the census–greedy gap is zero at every size tested).

## CLOSED (records were `reports\`, now wiped — verdicts are in the docs)
P2_selection_alignment · P2b_diversity_placement · P3_correction_sheet_and_conditioned_arm (+ addendum 1) · overnight_breadth_mine · read_correction_sheet · merge_teal_conditioned.

## SCRATCH/ARTIFACT FLAGS
KEEP: `artifacts/curation/candidate_ledger/` (128,368 rows) · the candidate JPEGs (archive tier **18.41 GiB** = 14.38 keep + 4.032 prunable; free space 90 GB of 937) · `artifacts/curation/neutral_embeddings.jsonl` · `artifacts/render_cv/` · `artifacts/curation/` (HOT).

⚠ `artifacts/node_views/` does not exist; the location head's own view is `models/location_view.py`.

Nothing else under `scratch/` must survive.

## ROSTER — sizes at ckpt 88
state ~6k (wholesale) · tutorial, discovery, corpus edited by hunk · **operating and engine CLEAN, not emitted**. Preserve: `selection_design` by hunk plus one appended section; `settled_rulings`, `parked` and `judge_training` APPEND; `INDEX` clean (no new files).
