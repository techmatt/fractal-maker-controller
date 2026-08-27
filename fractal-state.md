# fractal-state — checkpoint 84 (2026-08-26)

## Where we are
**Propose-then-solve is BUILT and has run end to end.** The recipe type + candidate ledger (16,006 recipes over 1,439 places), the lexicographic solver, a 20-minute hunt that closed a colour shortage, and a scaling pass that reaches n=160. **The gallery pass is DELETED** — git log is the only copy. Design record → `preserve\selection_design.md` (cite, never restate). Six prompts closed this era: `test_speed` · `candidate_ledger` · `gallery_solve` · `candidate_hunt` · `atlas_page` (WEBSITE) · `solve_at_scale`.

**The ledger is 8% of what we own** — 1,078 of its places are q3+q4 against 18,097 admitted on named runs. Every quality number below is a statement about that sliver, not about the pipeline.

## THE OPERATING RULE THIS ERA BOUGHT
**The floor is a READOUT ON SUPPLY, NOT A SETTING.** "Floor" = stage 2 of the objective: the MINIMUM render-judge `P(≥4)` among seated candidates — the worst wallpaper in the set. Nothing to do with the harvest keeper/junk floors, the mode floors, or the breadth floor. Measured on today's pool: n=20 → 0.9931 · n=80 → 0.9410 · n=120 → 0.8637 · n=160 → 0.6134. **Ruled (Matt): a hard floor of 0.90, every seat clears it, N is whatever the pool supports — underfill is the signal.** If a solve at that bar runs past ~10 min, LOWER THE BAR rather than fight it; Matt adjusts on seeing results. The bar is on the render judge's `P(≥4)` and is strictly stronger than stage 1's 0.50, which therefore stops acting. **A judge retrain moves the scale under it — restate the number, never carry it across.**

## OPEN (ordered)
1. **Hunt expansion with the DEEPEN leg — the next prompt, discuss before writing.** Breadth into the unopened pool buys constraint satisfaction, not quality (644 candidates, median `P(≥4)` 0.00087, 9 clearing the bar, the n=20 gallery unmoved). A location counts as **PRIMED** at `P(≥4)` with reasonable confidence — DERIVED, never stored, so a retrain moves the boundary without a migration. Mining is the whole next era; N up to ~1000 is the target and supply is the binding thing.
2. **The correction sheet on the first real solve.** The floor is a learned proxy whose bars were volume-matched, never crossed against eyes — until the sheet runs, a floor number compares two solves and means nothing absolute.
3. **Collections.** Matt: gallery emission logs are not worth keeping officially; the old emission path is abandoned. Before deleting, one report on what actually reads them (the ledger backfilled 1,591 rows from the release store). **Website provenance is NOT a reason to keep anything** — Matt refreshes every figure by hand.
4. **The gallery4 record fix.** `test_each_collection_holds_one_wallpaper_per_location` has been red for four reports: `group#225` in multibrot5 holds two gallery4 wallpapers of one location. One-per-location is now an absolute solver constraint. Matt: fix the record.
5. **The signature cache.** 1,787 signatures for ~800 distinct candidates at n=160, 168 s of the 500; `SIGNATURE_CACHE` is 512. Next lever, not pulled.
6. **Atlas (a) the wallpapers maker** — writes to the schema `atlas_page` defined (E: archive mounted) — **and (c) prose.** (b) is BUILT.
7. run11 (proven channel ON) — UNSCHEDULED; a new budget question.

## RULINGS THIS ERA (Matt)
- **One wallpaper per location is ABSOLUTE within a curation set**; a later gallery may reuse a location.
- **`framing.MARGIN` stays at 2.0.** Framing is done FIRST and eventually BY THE RUNS, locations born already-framed — which dissolves most of the refinement migration rather than scheduling it. The frame is part of the recipe, so candidates hunted at 2.0 stay valid if it moves.
- **The ~1.5N draw is not a solver parameter.** The hunt is decoupled and continuous; the solve ranges over the whole ledger.
- **The cache stores recipes AND pictures** (archive tier, 2.53 GB / 15,488 JPEGs) so a judge adoption re-scores rather than re-renders. Dumped fields are the disposable half (8.17 GB) — they regenerate from recipes.
- **A colour TARGET raises the allowance of the cells it structurally implies**, derived from the carrier table's MEASURED co-dominance, never a wheel adjacency.
- **Colour targets are a PRODUCTION instrument.** A themed collection is mined then solved over a filtered pool, not forced out of a mixed one — the n=60 lime failure was supply, not structure. **Default design target: generally multichromatic with good colour distribution.** ⚠ Themed collections will need their own radius or a colour-invariant metric component — the diversity metric is over the colour cloud, so a monochrome set sits far closer together. Deal with it when it comes up.
- **Lime scoring low is expected and accepted** — never build an algorithm that spends its time failing to optimize lime.
- **Randomize location supply per gallery** so galleries don't all emit the same few rare-colour q4s. Design item, recorded not built.
- `prose\Full pipeline v2.md` is PARKED — re-enter after the first solve at a real N, expect a rewrite of its selection and colour sections.

## SESSION-SIDE CHORES (claude.ai edits Drive `preserve\` — NOT the apply prompt's job)
- `selection_design.md` — record: the floor rule and the 0.90 bar · targets as a production instrument + the themed-collection radius caveat · randomized supply per gallery as OPEN · what is now BUILT.
- `atlas_design.md` — the record schema is DEFINED and is the maker's contract (`at` is a place not an identity; a partition names the plane its dots are drawn over; density sparse, a bin holds a whole place); `plates` is the shipped treatment; (b) BUILT.
- `INDEX.md` and `parked.md` were both rewritten this session; sizes are current.

## PARKED / SETTLED
Parked → `preserve\parked.md`. Declined and never-re-raise → `preserve\settled_rulings.md`; the ckpt-84 block carries this era's.

## CLOSED (records = Drive `reports\`)
test_speed · candidate_ledger · gallery_solve · candidate_hunt · atlas_page · solve_at_scale.

## SCRATCH/ARTIFACT FLAGS
KEEP: `artifacts/curation/candidate_ledger/` (rows 40.7 MB + scores 7.4 MB, untracked, tracked manifests) · the candidate JPEGs (2.53 GB, archive tier) · `artifacts/curation/` (HOT) · `artifacts/node_views/`. `frame_refit/scan.jsonl` (98 MB) stays UNTRACKED — regenerates in 3.4 h, resumable; `curate hunt frames` derives its index in 2 s.

## ROSTER — sizes at ckpt 84
state ~5.5k (wholesale) · tutorial, corpus, discovery, engine, operating edited by hunk. Preserve: `settled_rulings` APPEND (ckpt-84 block) by this apply prompt; `selection_design` and `atlas_design` are session-side chores above.
