# fractal-state — checkpoint 93 (2026-08-31)

## Where we are
**THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE:** (1) the high-quality LOCATION hunt · (2) the high-quality WALLPAPER hunt · (3) the final curation SOLVE + release render. A solver gallery exists and is live; `MODE_POLICY` is the one place a mode carries a standing; the colour ceiling is still the binding constraint and no era has touched it. **Matt iterates from pictures, not counts.**

This era did two things. **The judge programme was rebuilt from the question end** — the ckpt-92 retrain adopted nothing, and the reason it could not have is that everything it measured was average ranking quality over labeled rows while the decision is about the extreme tail on the mining distribution. Matt's replacement is one run, all the data, and the artifact ships. **And the ledger's hygiene closed out** — the eval side can no longer shrink silently, ~14 GiB of unreferenced colormaps are gone, and two piles that looked like waste turned out not to be.

## ★ IN FLIGHT ACROSS THIS BOUNDARY
**`prompts\TRAIN_render_judge.md` is running. Its report is this era's FIRST READ.** One training run on all label data, 80/20 grouped by lineage, early-stopped on top-slice precision over ≥3, and **the artifact ships from it**. It is the first judge work in three eras that produces a deployable head rather than fold models.

⚠ **Still unverified at the boundary:** the picture restore. **Matt has DEPRIORITIZED it** ("I'll do it later"). Until it lands, `solve.pool` is far below its recorded figure and **every seat, solve and pool number anywhere in these docs predates the accident.** The restore and OPEN 1 are ONE decision, not two — the flip needs a real seating and the twin test opens pictures.

## NEXT CHECKPOINT GOAL
**Matt's to set**, after the training report.

## OPEN (ordered)
1. **The mode-floor FLIP.** The greedy fix landed and the floor rule is BUILT AND INERT behind `mode_policy.STRANGE_SEAT_SHARE = 0.60` with `seat_floors(n)` over the 13 accepted strange modes (weights sum 20), the ILP taking the same mapping. What remains is enabling it against a pre-registered bar and measuring the floored seats against `cell_allowance`, already the largest refusal. **Blocked on the restore.** ⚠ The ILP's floor is SOFT and third in a lexicographic objective, below the count above the bar and the worst seated score — so greedy/ILP agreement means something only where the floor is free.
2. **Does the solve enforce a realized strange share?** `STRANGE_SEAT_SHARE` is declared and is the floor DENOMINATOR only; `run.STRANGE_SHARE` remains a separate supply split in `budget.head_slots`. Seating still enforces nothing by kind and the realized share is emergent. Matt has not decided whether it should be a constraint; he will judge 0.60 from galleries.
3. **`itinerary` composites — 2–3 new strange modes (Matt).** The engine already allows it; mechanism and the two real constraints → fractal-engine. **The only item on this queue that adds pictures rather than machinery.** Needs a design conversation, not a prompt.
4. **`direct_trap_screen` needs a flat draw before any standing is written for it** — the widest on-arm/off-arm gap of the nine modes ever aimed at.
5. **The forward-draw sitting, still deferred (Matt: not now).** Two candidate judges each propose their top k from a live pool, Matt labels the union blind, and the comparison is how many fours each slice held. It is the only instrument that measures what the judge is FOR rather than a proxy for it, and it needs no holdout, no AUC and no level claim. It costs Matt's evening, which is why it keeps being deferred.
6. **The colour ceiling's allowance is binding at n=150.** Write-up → `preserve\selection_design.md`.
7. **n=1000 is not demonstrably feasible** — the constructive lower bound on non-twin capacity sits far below the upper. A mining question.

## RULINGS THIS ERA (Matt)
- **★ EVERYTHING STAYS AT CANDIDATE GEOMETRY. There is no promoted render.** The `input_detail` edge read the same at label geometry and at candidate geometry, and it is spatial resolution for the network to compute over, not detail from the source — so rendering larger and downsampling to network input cannot buy it. **Render geometry is not an axis worth spending on; model input size is a separate axis and the only one with a measured effect.**
- **★ A JUDGE EXPERIMENT MUST NAME THE DECISION ITS NUMBER CHANGES, BEFORE IT RUNS.** The ckpt-92 retrain's number changed none: a ranking win over labeled rows does not imply a better gallery. Full statement → fractal-corpus §Judge method.
- **The scoring ruling (old OPEN 7) is SATISFIED, not implemented.** With no promoted render there is no second stage, no promotion bar and no cross-regime question. Mining already owns scoring and selection already re-scores nothing — `features_for` opens no picture and renders nothing. ⚠ The release-geometry column will be a SELECTED sample; never read an unbiased AUC off it.
- **Train on all the data and ship the head.** 80/20 grouped by lineage, pinned places eval-side, stop on top-slice precision over ≥3, no folds, no seeds, no arms. Calibration is not the goal — quality is. The refit on train+holdout is the right close for a FINAL head and this is not it.
- **Mixed-vintage scores are ACCEPTED; the ledger is re-scored lazily.** A score row must carry which head produced it.
- **Precompute and store per-candidate features at mining time.** They cost under a tenth of the render they describe and all record stores together are ~1.7% of a candidate's disk. **Exception: the pixel-cloud twin signature stays lazy** — a seating makes a couple of hundred, and storing them per candidate would be tens of GB.
- **Leg records are one run's measurement sample, retired WHOLE.** `prune` must never reach them row by row: retention keeps the winners, so dropping the pruned rows would leave every curve, clear rate and stage cost computed over survivors, reading far too high, silently and irreversibly.
- **`eval_only` outranks the clock** — reader-side, nothing stored moved.
- Missing flatness does NOT count as a build failure. · The website's `palette-` prefix keeps its named carve-out; the rule is not absolute. · `depth.contact_sheet` over a pruned leg is a SETTLED non-issue — the arc is shelved and the sheet is a temporary thing built for a live leg; anyone who ever builds one over an old leg should check whether it says it is showing survivors.

## INVALIDATED WITHOUT AN EDIT
- Every seat, solve and pool figure anywhere in these docs. See IN FLIGHT.
- **`preserve\judge_training.md` is substantially superseded** and is the era's one owed doc. It is owed: the three ckpt-92 rulings (rank-key primary, per-mode-as-readout, deploy geometry); a correction that **"arm B" names two different arms across the retrain's own commits** — 768×448 at one, 384×216 at another — so neither its headline table nor its `input_detail` section can be quoted without saying which; and the ckpt-86 stopping-rule stability claim, now INVERTED (cross-entropy chose epochs 4–7 where AUC chose 3–16 including the cap). Its whole method frame is superseded by the ruling above.

## KEEP LIST — survives this boundary
`prompts\TRAIN_render_judge.md` (a live instance's contract) · `reports\label_ingest_tiers.csv` (Matt's working CSV). Both folders are otherwise wiped entire.

## OWED FIXES — ride the next prompt into each repo
1. `preserve\judge_training.md` as above — authored session-side, not by a code prompt.

Done this era and not to be re-raised: `merge` now saves the flatness manifest · `rank_key`'s `hunt.seconds` docstring, whose exclusion stands for a better reason (a wall-clock reading of a loaded machine, 1.53× inflated under three workers, unreproducible as a sort key) · `delete_pictures` takes the sibling levelled colormap · CLAUDE.md's lane figures · the website's five departure entries, its CI atlas suite, its palette-count clause and the `wallpapers-` figure rename.

## PRESERVE
Nine files. `judge_training.md` is owed as above; `INDEX.md` unchanged otherwise.

## SCRATCH/ARTIFACT FLAGS
Standing KEEP: `artifacts/curation/candidate_ledger/` · the flatness sidecar and its manifest · `artifacts/curation/neutral_embeddings.jsonl` (per LOCATION, read not recomputed) · `artifacts/render_cv/` · `artifacts/curation/` HOT · the live release rows · **`artifacts/renders`, which now EXISTS** — rebuilt whole in 3.69 h when the last retrain found it on no tier at all. Fourteen unmerged depth legs keep their own `rows.jsonl` and their pictures and colormaps were excluded from every sweep.

Scratch preservation notice: **nothing under `scratch/` must survive this boundary.**

## CLOSED (records wiped — verdicts are in the docs)
`RETRAIN_render_judge` (nothing adopted) · `SEATING_floor_fix` · `AUDIT_candidate_features` · `PRICE_input_detail` · `DIAGNOSE_split_pin_and_transfer` · `GUARD_and_orphans` · the website's `FIX_explorer_departures` + two addenda and `FIX_claude_md_drift`.

## PARKED / SETTLED
Parked → `preserve\parked.md`. Declined and never-re-raise → `preserve\settled_rulings.md`. **`input_detail` is PARKED, not closed** — adopting it means training at 768 and shipping those weights, which is a judge adoption invalidating every sidecar score, for ~+0.02 strange `AUC(≥3)` plus +7.2% of every mining leg. Carry the input size along free if a future retrain happens for another reason.
