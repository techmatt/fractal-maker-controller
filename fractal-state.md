# fractal-state — checkpoint 96 (2026-09-01)

## Where we are
THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE: (1) the LOCATION hunt · (2) the WALLPAPER hunt · (3) the final curation SOLVE + release render. `MODE_POLICY` is the one place a mode carries a standing; Matt iterates from pictures, not counts.

This era (ckpt 95→96), four moves:
- **The colour ceiling at n=150 was the CAP acting, not a shortage** — every cell holds ≥37 clearing locations, a 1,034-candidate leg moved zero seats. CLOSED; the allowance (7/cell at n=150) is Matt's knob and stays.
- **The exact solver is RETIRED.** `curate solve run` — stratified view → greedy seed → 1-swap to exhaustion, anytime — is the ONE selection leg at every N; `curate seat` and `seating.py` are gone. Tier order filled → floor shortfall → worst → sum; one spelling per rule (`rules.py`); `Demand` unifies floors and targets; census schema 4; a signature sidecar for `headroom --twin`. Single home → `preserve\solver_design.md`.
- **Themed galleries are viable at q3 grade** and the wall is the colour-cloud twin rule, not supply, bar or cap — ruled geometry-only diversity for themed. `--target` exists. Nothing built yet.
- **The minibrot demotion is OVERTURNED.** The reframe channel is BUILT (`fractal-wallpapers reframe`): operators fire at `proven` roots, the operator's own view is a candidate, one nucleus = one `centered` location with rungs as framings. 20-minute smoke: 792 nuclei, 58 head-q4, 290× the pool's median P(≥4); Matt's eye: very strong. Seeds, not clock, were the constraint.
Also: `curate depth run` had been dead since a texture_flat commit (KeyError read as a hang) — fixed with a boundary test.

## IN FLIGHT ACROSS THIS BOUNDARY
**HARVEST_reframe_generations** (fractal-wallpapers, 8h overnight, unattended): merge+embed the smoke ledger · `centered` · rungs 16/24/32/48/64 · seed priority Matt-q4 → Matt-q3 → head-q4 → head-keeper · `MAX_PERIOD` 256 · generations FIRE · a ~500-row stratified sheet cut at the end (Matt labels when he chooses). Its report is the next era's FIRST READ and gets its carry then.

## NEXT CHECKPOINT GOAL
Matt's to set.

## OPEN (ordered)
1. Does the solve enforce a realized strange share? Unchanged; Matt judges 0.60 from galleries.
2. **n=1000: the pool holds 653 seats under the shipped rules** — four mode floors short by 18 total, NO ceiling binding (the old "cap short 248" was a schema-3 artifact). The expand hook's per-constraint shortfall and the schema-4 census are the instruments.
3. **The themed-gallery leg** — a target `Demand` + the geometry-only diversity rule + `--flat-floor` over a `P(≥3) ≥ 0.50` pool; both pieces exist, one prompt. Lime (`dark_vivid_lime`, stocked by the mine's pilot) and green are the cells in hand.
4. **Walk-triggered operator admission** — the walk's own nucleus frames (~6,519 a run, ~24% of the clock) still go to the frontier as nodes only. Same admission as the reframe channel, other trigger. Small build.
5. The reframe sheet's labeling — Matt's, whenever.

## STATUS / KNOWN REDS
- Website `builder check` RED on main (`bake: catalog.js` diverges, 19→20 entries). Unchanged, DEFERRED; resolve at the next engine↔website seam touch; a rebake is a picker-record decision.

## RULINGS THIS ERA
→ `preserve\settled_rulings.md` §ckpt 96: ILP retired · tier order · group cap = count · colour ceiling = cap · themed diversity = geometry-only · the minibrot demotion overturned, `centered` locations · parallel decoding closed · the sidecar's use · the concurrency rule. Parked → `preserve\parked.md`: the last-pass neighbourhood, the 8× rung.

## KEEP LIST
Drive `prompts\`: **HARVEST_reframe_generations.md** (in flight). `reports\`: nothing. `scratch/`: nothing survives (the harvest's outputs belong to the next era).

## OWED
OPEN 3 and OPEN 4 above.

## ROSTER (soft size targets, chars)
operating 27k · tutorial 18k (solver material moved to `preserve\solver_design.md`, ckpt 96) · corpus 15k · discovery 15k · engine 10k · state 5k.

## SCRATCH/ARTIFACT FLAGS
Standing KEEP unchanged: `artifacts/curation/candidate_ledger/` · flatness sidecar + manifest · `neutral_embeddings.jsonl` · `artifacts/render_cv/` · `artifacts/curation/` HOT · live release rows · `artifacts/renders` · `data/coloring/texture_flat.jsonl`. NEW: `artifacts/reframe_g1` (the smoke ledger, merged by the harvest) · the signature sidecar (247 MB, rebuildable by `curate signatures sweep`).

## CLOSED (records wiped — verdicts in the docs, solver_design and settled_rulings)
MINE_color_ceiling_test (+addendum1) · READ_green_gallery_feasibility (+addendum1) · PROBE_ilp_n1000 · FIX_under_fill_and_solve_record · BUILD_greedy_swap_solve (+ the speedups) · AUDIT_minibrot_pipeline · BUILD_minibrot_reframing · FIX_solve_tiers_census_sidecar.

## PARKED / SETTLED
→ `preserve\parked.md`, `preserve\settled_rulings.md`. `input_detail` PARKED on its ckpt-93 terms (→ `preserve\judge_training.md`).
