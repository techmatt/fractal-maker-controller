# fractal-state — checkpoint 85 (2026-08-27)

## Where we are
**The mining era opened, and it found the judge's ceiling.** Field sharing made a candidate ~5× cheaper, an overnight run took the ledger from 22,029 recipes over 1,439 places to **85,129 over 4,956**, and a 246-row calibration sheet established that the render judge does not order Matt's 3-vs-4 verdict at the top of its own scale. Eight prompts closed this era.

**Primed locations: 718 at 0.90 and 1,254 at 0.50 — both RAW.** Raw counts are maxima over noisy scores and run ~0.70 of calibrated at the 0.90 bar (→ fractal-discovery §Mining economics). Every prime count in any record predates that correction unless it says otherwise.

## THE OPERATING RULE THIS ERA BOUGHT
**The render judge is a GATE, not a top-end ranker.** It separates junk from keepers well and barely orders quality inside `P(≥4) ∈ [0.60, 0.95)`. Two things follow and govern the next era: hard optimization of the score in that band is optimizing noise, and **no bar is currently set** — 0.90 is retired, nothing replaces it. Matt's plan: mine, retrain, then set the cutoff from the quality the mining actually finds. Numbers and the resolvable composite-vs-colour offset → fractal-corpus §Judge method.

## OPEN (ordered)
1. **Ingest and fit `under_seen_modes`** — 504 rows LABELED and waiting, the first read of the next session. Matt labeled through ~250 and accepted the remainder as scored. It decides whether the nine under-represented modes are weak or the judge is blind to them; no demotion beyond `trap_circle` until it has run. Record `reports\mode_sheet_report.md`.
2. **The retrain that can rank the top.** The calibration rows and the mode rows are its evidence, and it is the only thing that fixes the gate/ranker limit rather than working around it. Winner rule and restatement modes → fractal-corpus.
3. **Set the bar.** After (1), (2) and more mining. Also unbuilt and required before any real solve: the floor must be re-scored at shipping geometry rather than read off the candidate column (→ `preserve\selection_design.md`).
4. **`autolevel`'s Python half** — 33.5% of the candidate loop, 53.4% where the mode is held. The largest optimization left and worth building before another long mine. Record `reports\field_sharing_report.md`.
5. **The two-layer composite dump.** Composites cannot share a field and are a permanent output requirement, so their cost is paid forever until this is built. Record `reports\depth_curve_report.md` §0.
6. **The correction sheet on the first real solve** — ruled ckpt 83, still not run; the solver has never been crossed against eyes.
7. **Collections · Atlas (a) maker and (c) prose · run11 (proven channel ON, UNSCHEDULED).** Unchanged from ckpt 84.

## RULINGS THIS ERA (Matt)
- **`trap_circle` is DEMOTED TO NICHE**; composite modes are a HARD output requirement never cut on cost; nine modes are Q3-ADMITTED; the per-mode floor is ~N/100. All four → `preserve\settled_rulings.md` §ckpt 85.
- **Hunting for labels draws the judge's own TOP, unfiltered.** The population's bad examples come along inside it; no spread or systematic draw for its own sake.
- **Drive edits split by edit size** — wholesale by claude.ai, small and targeted by a trivial CC prompt (→ fractal-operating §Tier 0.5).
- Depth runs on shareable field modes; composites get a reduced draw share, never zero.

## INVALIDATED WITHOUT AN EDIT
- **Every "primed" count quoted before ckpt 85 is raw and optimistic.** Not wrong, uncorrected.
- **`p_ge4_calibration_*` is not a clean-blind sheet** — the page carried the mode name and the score. Its near-null result is conservative rather than void (→ fractal-corpus).
- The ~1,164 in-band candidate figure describes today's ledger, never the reachable pool: 18,097 admitted locations have no candidates because nothing has rendered them yet.

## SESSION-SIDE CHORES
None owed. `preserve\` edits now go through CC prompts; `selection_design.md` and `atlas_design.md` were brought current at ckpt 84 and are edited by hunk in this closeout.

## PARKED / SETTLED
Parked → `preserve\parked.md`. Declined and never-re-raise → `preserve\settled_rulings.md`; the ckpt-85 block carries this era's.

## CLOSED (records = Drive `reports\`)
preserve_chores_ckpt84 · primed_supply_mine · field_sharing · calibration_sheet · calibration_fit · depth_curve · mode_sheet · cleanup_batch.

## SCRATCH/ARTIFACT FLAGS
KEEP: `artifacts/curation/candidate_ledger/` (now 85,129 recipes) · the candidate JPEGs (archive tier — **the overnight run multiplied this; check free space before sizing another**) · `artifacts/curation/calibration/paired.jsonl` and `artifacts/curation/mode_sheet/paired.jsonl` (both readings per row, the only record of the regime pairing) · `artifacts/under_seen_modes/` until its drop is ingested · `artifacts/curation/` (HOT) · `artifacts/node_views/`.

Nothing else under `scratch/` must survive. `scratch/cleanup_batch_group225_contact_sheet.html` is Matt's to keep or wipe once he accepts or overrides the gallery4 choice.

## LOOSE END
`prompts\AUDIT_readme_homes (1).md` is NOT a conflict copy — it is a separate prompt whose name collides case-insensitively with `audit_readme_homes.md`, and fractal-discovery cites `AUDIT_readme_homes` for the julia ∂M-screen question. Renaming either breaks something; needs a name that is not a case-variant. Untouched deliberately.

## ROSTER — sizes at ckpt 85
state ~4.5k (wholesale) · tutorial, corpus, discovery, engine, operating edited by hunk. Preserve: `settled_rulings` APPEND (ckpt-85 block) and `selection_design` by hunk, both in this apply prompt.
