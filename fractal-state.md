# fractal-state — checkpoint 92 (2026-08-30)

## Where we are
**THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE:** (1) the high-quality LOCATION hunt · (2) the high-quality WALLPAPER hunt · (3) the final curation SOLVE + release render. A solver gallery exists and is live; `MODE_POLICY` is the one place a mode carries a standing; the colour ceiling is still the binding constraint and no era has touched it. **Matt iterates from pictures, not counts.**

This era did one thing: **the candidate ledger stopped growing with work.** Rows per location are bounded by `RETAIN_PER_PAIR` × the modes tried there plus four protections, and are no longer a function of the attempts made. 30 GiB came off the hot tier and the rule runs from `merge`. A render-judge retrain is IN FLIGHT across this boundary.

## ★ IN FLIGHT ACROSS THIS BOUNDARY
**`prompts\RETRAIN_render_judge.md` is running. Its report is this era's FIRST READ** — plan nothing around a retrain outcome before reading it. It trains and grades three arms and adopts nothing.

⚠ **Also unverified at the boundary:** a recovery leg re-renders ~57,000 candidate pictures a test deleted, then re-runs seat and solve. Until it reports, **`solve.pool` is 50,673 where it was 97,519**, and every seat/solve figure recorded anywhere predates the accident. Matt reports the outcome only if it fails; otherwise the recovery leg's own numbers stand.

## NEXT CHECKPOINT GOAL
**Matt's to set**, after the retrain report. Dependency-ordered candidates: OPEN 1 (which unblocks both ckpt-90 rulings), then OPEN 2–3 together, then judge ADOPTION if an arm won.

## OPEN (ordered)
1. **The mode floor cannot exceed 1, and it blocks both ckpt-90 rulings.** UNENFORCED and verified: `seating.py:629` is the `break`, `scarcity()` yields one `(mode, subpool)` per mode so the outer `continue` at 622 can never see a second, and no test runs floor ≥ 2. Until it lands, "promoted" changes no seat. Fix + what reads the leg → fractal-tutorial §Selection.
2. **Matt's emission-weight design, unbuilt.** Within the strange share, `2·promoted + 1·normal` defines a fully-distributed target and the floor is half of it, so floors sum to exactly half the strange budget by construction. It needs a floor rule for `normal` too (or `direct_trap_multiply`, which Matt wants present, keeps a bare 1), and a measurement of the floored seats against a `cell_allowance` that is already the largest refusal.
3. **Make the smooth/strange emission split EXPLICIT** (Matt). `run.STRANGE_SHARE` is a SUPPLY split in `budget.head_slots`; **seating enforces nothing by kind** and the realized smooth share is emergent, though stable across four seatings. Every number in OPEN 2 hangs off this.
4. **`itinerary` composites — 2–3 new strange modes (Matt).** The engine already allows it; mechanism and the two real constraints → fractal-engine.
5. **`direct_trap_screen` needs a flat draw before any standing is written for it** — the widest on-arm/off-arm gap of the nine modes ever aimed at.
6. **Judge retrain — IN FLIGHT.** Method and evidence → `preserve\judge_training.md`. **The missing eval instrument no longer blocks (Matt, ckpt 92):** the retrain grades arms on identical rows and makes no level claim, so an eval-eligible draw is deferred, not required. ⚠ `judge_training.md` is OWED three rulings, held this era so the running instance was not reading a moving file — the rank-key primary, per-mode-as-readout, and the deploy-geometry answer. Apply them with the retrain's own evidence next era.
7. **Implement the scoring ruling.** Mining owns scoring; selection never re-scores. Needs the second-stage leg priced and per-mode bars fitted at whichever regime selection reads. **The second stage is no longer unpriced** — retention keeps about a third, so re-scoring only what it keeps is roughly 1.33× the base render bill, not 4×. ⚠ The release-geometry column will be a SELECTED sample — never read an unbiased AUC off it.
8. **The colour ceiling's allowance is binding at n=150.** Write-up → `preserve\selection_design.md`.
9. **n=1000 is not demonstrably feasible** — the constructive lower bound on non-twin capacity sits far below the upper. A mining question.

## RULINGS THIS ERA (Matt)
- **★ A DURABLE RECORD'S SIZE MUST SCALE WITH KNOWLEDGE GAINED, NEVER WITH WORK DONE.** The full standing position, with its corollaries → fractal-operating.
- **The ckpt-86 pool rule is RELAXED.** What accumulates across runs and is never pruned is admitted LOCATIONS and the recipes that primed them, not every judged render. A run still never refuses a place because an earlier run released it. **Immortality attaches to human labels and deep-net training data only** — candidate rows and candidate pictures are prunable, replaceable, and re-derivable from their keys.
- **Retention is mode-only, K=3.** Top-3 per (location, mode) by the rank key. No cell arm — a row is dominant in about two cells of forty-eight, so a per-cell arm opens more arms than a location has rows and refuses almost nothing.
- **A picture is kept if and only if its row is.** One ranking, one constant.
- **The wide ledger is DELETED, not archived** — nobody should have to work out later what it was.
- **The retrain proceeds on the grouped holdout over the grown stores, with no level claim made.**
- **Grade on the refit rank key, not the judge's AUC.** The key is what orders seats and refitting it per arm makes the CORN scale shift drop out. Per-mode is a pre-declared readout that gates nothing — per-mode tier-4 counts are single digits and a bar there would fit noise.
- **Deploy geometry does NOT change.** Label-geometry and candidate-geometry columns are indistinguishable on both boundaries; the problem is not where the head reads. Model input resolution is a separate axis from deploy render geometry.

## ★ TWO COMMITS IN ONE REPO COLLIDE EVEN WHEN BOTH PROMPTS OBEY THE RULE
Second instance, and the first one's lesson was written too weakly. **Explicit-path staging does NOT make the index private** — a concurrent `git commit` takes whatever is staged, by whoever staged it. `548506c` carried six files across two authors; it was recovered only because the other instance noticed and reset. **"Read-only audits beside anything" is WRONG as written: an audit commits its report.** The only mechanism is not overlapping two commits in time. → fractal-operating §WORKING STYLE.

## INVALIDATED WITHOUT AN EDIT
- Every seat, solve and pool figure anywhere in these docs predates the picture accident. See IN FLIGHT.

## KEEP LIST — survives this boundary
`prompts\RETRAIN_render_judge.md` (a live instance's contract) · `reports\label_ingest_tiers.csv` (Matt's working CSV). Both folders are otherwise wiped entire.

## OWED FIXES — ride the next prompt into each repo
1. fractal-wallpapers: `CLAUDE.md:27-34` is a seven-line paragraph whose whole subject is `tests/test_banned_vocabulary.py`, now deleted. Every clause is false and it is the last place in the repo describing the term list.
2. fractal-wallpapers: `labeling/corpus_import.py:91` points at the same deleted file. The two `SOURCES` keys it excuses are still there and still correct; nothing names them as exceptions any more.
3. fractal-website: two entries in `explorer/README.md`'s departure list still open with a quotation from a retired design doc and no longer stand alone.

Done this era and not to be re-raised: `ceiling.GROUP_CAP_RATE`'s comment, `LABEL_RESOLUTION`'s double spelling, and the two stale ledger sizes in `hunt.py` and `rank_key.py`.

## PRESERVE
Nine files, unchanged this era. `judge_training.md` is owed the three rulings named in OPEN 6.

## SCRATCH/ARTIFACT FLAGS
Standing KEEP: `artifacts/curation/candidate_ledger/` · the flatness sidecar, now durable with a manifest · `artifacts/curation/neutral_embeddings.jsonl` · `artifacts/render_cv/` · `artifacts/curation/` HOT · the live release rows. Fourteen unmerged depth legs keep their own `rows.jsonl` because the ledger does not hold their recipes.

⚠ **`artifacts/renders` does not exist on this machine.** A head's training cache must be built before it trains, and that build may dominate any retrain's wall.

## CLOSED (records wiped — verdicts are in the docs)
`AUDIT_record_growth` · `AUDIT_guards_and_names` + addendum 1 · `PRUNE1_replay_bestk` · `PRUNE2_compact_ledger` · `PRUNE3_delete_and_wire`.

## PARKED / SETTLED
Parked → `preserve\parked.md`. Declined and never-re-raise → `preserve\settled_rulings.md`.
