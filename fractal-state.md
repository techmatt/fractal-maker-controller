# fractal-state — checkpoint 83 (2026-08-26)

## Where we are
gallery4 landed 249/250 and the colour ceiling worked — 48/48 cells, 12/12 families, green 1→24 with no targets set. The cost was rank, and diagnosing why led to a **redesign of selection**: propose-then-solve, ruled this era, NOTHING BUILT. Design record → `preserve\selection_design.md` (cite, never restate). Five prompts closed this era: `reason_codes`, `palette_mass_census`, `palette_mass_sweep`, `AUDIT_selection_redesign`, `cleanup_and_map`. **`frame_refit_scan` IS LIVE in fractal-wallpapers** — a 28k-location framing scan, record-only, with an addendum on resume identity and per-partition pricing. **Its report is the FIRST READ of the next era.** Website FREE.

## OPEN (ordered)
1. **`frame_refit_scan` report → readout.** Per-partition coverage (it may not have finished all nine — a rate quoted off a partial population is wrong), the adoption rate at 28k against gallery4's 26.9% on 751, and the ×1.0 rung at scale (gallery4 saw 51 of 132 adoptions recentre-only). Do not rule on the rung; it is a design input.
2. **Build propose-then-solve.** Three prompts in order, per `preserve\selection_design.md`: (a) the recipe type + the durable cache — **there is no recipe object today**, five shapes and three adapters, so defining the type IS the first step; (b) the proposal path, free/stratified split over cells; (c) the solver, scipy/HiGHS into the torch venv, lexicographic count-above-q4. Each stands on the audit's answers; do not re-derive them.
3. **Refinement moves to HARVEST.** `walk.refine_framings` exists and HAS NEVER FIRED — zero `refined` rows in any ledger. Untested code, and the migration also needs a re-embed (29,051 rows; the embedding store keys on a viewport function, so refinement APPENDS keys rather than rewriting them). The interim ruling that greened `test_each_collection_holds_one_wallpaper_per_location` is superseded when this lands.
4. **Website figures WAIT.** The first solver pass supersedes gallery4 as the gallery the article shows, so `gallery-output` and the four `gallery-*` makers stay held. `pipeline-yield-decay` off `artifacts/harvest_run10/` does NOT depend on that and can go whenever.
5. **Full pipeline placement.** `prose\Full pipeline v2.md` awaits Matt's review → verbatim placement, verify list at its foot. Decide `pool-stages`: move it here or no second diagram. Note v2's colour section describes the CEILING, which propose-then-solve supersedes — one prose round after the first solve.
6. **Fractal atlases** — unchanged from ckpt 82; (a) wallpapers maker / (b) website tool page / (c) prose → `preserve\atlas_design.md`. Order is Matt's.
7. run11 (proven channel ON) — UNSCHEDULED; a new budget question; precedes any pass wanting new ground rather than a new selection.

## SESSION-SIDE CHORES (claude.ai edits Drive `preserve\` — NOT the apply prompt's job)
- `color_coverage_floor_design.md` — SUPERSEDED by `selection_design.md`. Park or delete; it is the record of what gallery1–4 did and nothing forward-looking reads out of it. Same for `gallery_pass_design.md`'s forward-looking half.
- `preserve\INDEX.md` — add `selection_design.md`, mark the two superseded files.
- **`fractal-operating.md` was NOT edited this era** — it was outside the session's context. Two price-method lessons want a home there next era: an estimate off another population's rate ran **2.5× over** (composites scale superlinearly in maxiter — mandelbrot cost 9.6× julia:multibrot5 for 4.2× the iterations), and **a filename that encodes a split is not an identity** (a chunked resume must subtract measured identities; the sweep skipped 5,524 of 13,020 pairs per location while reporting success).

## PARKED / SETTLED
Parked → `preserve\parked.md`. **Cross-partition radius is UNPARKED and RULED** (partition-blind, in `selection_design.md`). Declined and never-re-raise → `preserve\settled_rulings.md`; the ckpt-83 block carries this era's.

## CLOSED (records = Drive `reports\`)
reason_codes · palette_mass_census · palette_mass_sweep · AUDIT_selection_redesign (18 answers, four unanswerable without fresh measurement) · cleanup_and_map.

## SCRATCH/ARTIFACT FLAGS
KEEP: `artifacts/curation/` (HOT) · `artifacts/node_views/` (90,548 stamped views) · the census artifact. The sweep log is ARCHIVED and its hot copy deleted — `curate mass-sweep restore` is its only rebuild, since it ran out of `scratch/palette_mass_sweep/` and no subcommand makes it again. `scratch/ceiling_replay.py` must still survive.

## ROSTER — sizes at ckpt 83
state ~4.6k (wholesale) · tutorial, corpus, discovery, engine edited by hunk · operating UNCHANGED (see chores). Preserve: `selection_design.md` created session-side; `settled_rulings` APPEND (ckpt-83 block) by this apply prompt.
