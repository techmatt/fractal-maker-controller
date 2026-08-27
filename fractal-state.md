# fractal-state — checkpoint 86 (2026-08-27)

## Where we are
**THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE (Matt, ckpt 86):** (1) the high-quality LOCATION hunt · (2) the high-quality WALLPAPER hunt · (3) the final curation SOLVE + release render. This is the spine of the plan and of the website write-up. This era worked phase 2: the mode question closed, the candidate loop's largest optimization landed, the judge retrain was screened, and the exchange folder became wipeable. Seven prompts closed it.

**The judge's ceiling is NARROWER than ckpt 85 said.** Unbanded, over rows a human called 3 or 4, the head orders at AUC 0.650 out-of-sample — 3-vs-4 is not irreducible from the picture. What resists is ordering inside the head's OWN uncertainty band, and a band-restricted AUC strips most of the variance it reads. → fractal-corpus §Judge method.

## OPEN (ordered)
1. **The judge retrain, adoption grade.** The ckpt-85 screen was a null on 43 rows (±0.19) and its declared cut gave 13 — not a measurement. Re-declare the bar on the UNBANDED 3-vs-4 statistic; carry `input_detail` further (every arm so far reads 384×224 of a 1280×720 picture) against a selection rule nearer the ranking peak; four folds are already dealt; TWO seeds, because nothing yet separates an arm from its seed. Evidence and dead ends → fractal-corpus.
2. **Set the bar.** Needs (1) and more mining. TWO parts now: the ≥4 cut, and a ≥3 criterion for the q3-target modes — the per-mode floor cuts on `P(≥4) ≥ 0.50` and no instrument looks below 0.60, so those modes' seats fill on a scale that barely applies to them. The floor must be re-scored at shipping geometry, never read off the candidate column (→ `preserve\selection_design.md`).
3. **Mine.** Cheaper per candidate now; every prime count is RAW unless it says CALIBRATED, and the winner's-curse multiplier is k-dependent (→ fractal-discovery §Mining economics).
4. **The correction sheet on the first real solve** — ruled ckpt 83, still not run; the solver has never been crossed against eyes. Merge it with the retrain's sitting rather than spending two.
5. **The two-layer composite dump — DEFERRED with a trigger** (`depth_curve` §0C): composites now draw only their floor deficit, ~1,900 a cycle, so the dump's prize is ~29 min of repaint against a two-layer format plus a two-field recolour spec. Revisit only if the composite floor rises.
6. **The gallery-pass code decision.** Its SEATING and SELECTION role is retired by propose-then-solve; the SOLVE and RELEASE RENDER are critical and stay (Matt, ckpt 86). Whether the retired half comes out of the tree is unruled and unscheduled — nothing blocks on it.

## RULINGS THIS ERA (Matt)
- **THE THREE PHASES** (above) — the plan's spine and the site's structure.
- **`trap_circle` DEMOTED; the other eight under-seen modes stay Q3-ADMITTED.** Novelty is worth a 3: `gaussian_int` and `curvature` are "3s will have to do" and keep their floor seats. → `preserve\settled_rulings.md` §ckpt 86.
- **The gallery pass's seating role is dead; the solve and release render are not.** 1280×720 ss2 is Matt's DESIGN-PHASE eval geometry, not the release regime — full wallpaper resolution is phase 3, on his say-so.
- **`reports\` and `prompts\` are SCRATCH, wiped at every checkpoint boundary** (→ fractal-operating §Tier 0.5).

## KEEP LIST — survives this boundary
`prompts\`: nothing. `reports\`: nothing. Everything else in both folders is wiped at this closeout. The era's own reports are on the keep list by default until their hunks land, which is what this closeout does.

## INVALIDATED WITHOUT AN EDIT
- **The docs said the gallery pass was deleted at ckpt 84. It never was** — `curate gallery`, seating, radius, seat-identity pinning and step 5a are all live, 4,606 lines. Every gallery-pass line in the docs was read as history and is not. Corrected in tutorial this closeout; assume any pre-ckpt-86 statement about what was removed is unverified.
- **Every "primed" count quoted before ckpt 85 is raw and optimistic**, and the ×0.70 correction only applies at k≥20.
- **`p_ge4_calibration_*` is not a clean-blind sheet** — the page carried the mode name and the score. Its near-null is conservative, and it was band-restricted, which weakens it further.

## SESSION-SIDE CHORES
None owed. `preserve\` edits go through CC prompts; `gallery_pass_design.md` and `maker_transfer_cautions.md` were retired this era and `INDEX.md` is current.

## PARKED / SETTLED
Parked → `preserve\parked.md` (gained this era: the regime-robustness re-measure; Collections; Atlas (a) maker and (c) prose; run11). Declined and never-re-raise → `preserve\settled_rulings.md`.

## CLOSED (records were `reports\`, now wiped — verdicts are in the docs)
mode_sheet_ingest_fit · autolevel_measure · render_judge_cv · AUDIT_record_pointers · AUDIT_doc_claims · wipe_exchange_scratch · exchange_tidy · fix_ci_digest_pin.

## SCRATCH/ARTIFACT FLAGS
KEEP: `artifacts/curation/candidate_ledger/` · the candidate JPEGs (archive tier — **check free space before sizing another mine**) · `artifacts/curation/calibration/paired.jsonl`, `artifacts/curation/calibration/bars.json` and `artifacts/curation/mode_sheet/paired.jsonl` (both readings per row and the bar table — the only records of the regime pairing) · `artifacts/render_cv/` (four folds dealt and unfitted; the adoption run fills them in without re-deriving) · `artifacts/curation/` (HOT) · `artifacts/node_views/`.

Nothing else under `scratch/` must survive.

## ROSTER — sizes at ckpt 86
state ~5k (wholesale) · discovery (wholesale) · corpus, engine, operating, tutorial edited by hunk. Preserve: `settled_rulings` and `parked` APPEND, both in this apply prompt.
