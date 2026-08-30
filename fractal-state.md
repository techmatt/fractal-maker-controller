# fractal-state — checkpoint 91 (2026-08-29)

## Where we are
**THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE:** (1) the high-quality LOCATION hunt · (2) the high-quality WALLPAPER hunt · (3) the final curation SOLVE + release render. A solver gallery exists and is live; `MODE_POLICY` is the one place a mode carries a standing; the colour ceiling is still the binding constraint and no era has touched it. **Matt now iterates from pictures, not counts.**

**This era ran no code.** Its whole job was Matt's ckpt-90 goal — shrink the handoff set — and it did that by the deletion test, by moving repo mechanics to the READMEs that own them, by dropping the measurement bodies that `preserve\judge_training.md` and `curation/README.md` already hold, and by collapsing three star tiers to one. No measurement changed and no OPEN item moved.

## NEXT CHECKPOINT GOAL
**Matt's to set.** The dependency-ordered candidates are OPEN 1 (which unblocks both of the previous era's rulings), then OPEN 2–3 together, then the retrain — which OPEN 6 blocks until an eval-eligible draw is registered.

## OPEN (ordered)
1. **The mode floor cannot exceed 1, and it blocks both of the previous era's rulings.** `seating.seat`'s scarcity leg `break`s on the first seat per mode, so floor 1 and floor 2 seat identically while the ILP honours the floor — greedy and exact silently disagree. Until it lands, "promoted" changes no seat. Fix + what reads the leg → fractal-tutorial §Selection.
2. **Matt's emission-weight design, unbuilt.** Within the strange share, `2·promoted + 1·normal` defines a fully-distributed target and the floor is half of it, so floors sum to exactly half the strange budget by construction. Two things it needs: a floor rule for `normal` too (or `direct_trap_multiply`, which Matt wants present, keeps a bare 1), and a measurement of the floored seats against a `cell_allowance` that is already the largest refusal.
3. **Make the smooth/strange emission split EXPLICIT** (Matt). `run.STRANGE_SHARE` is a SUPPLY split in `budget.head_slots`; **seating enforces nothing by kind** and the realized smooth share is emergent, though stable across four seatings. Every number in OPEN 2 hangs off this.
4. **`itinerary` composites — 2–3 new strange modes (Matt), before the retrain.** The engine already allows it; mechanism and the two real constraints → fractal-engine.
5. **`direct_trap_screen` needs a flat draw before any standing is written for it** — the widest on-arm/off-arm gap of the nine modes ever aimed at.
6. **Judge retrain — deferred, not refused.** Everything it needs → `preserve\judge_training.md`. ⚠ **No eval instrument exists to grade it with** — the whole recent intake is train-side. **An eval-eligible draw must be registered BEFORE the retrain.**
7. **Implement the scoring ruling.** Mining owns scoring; selection never re-scores. Needs the second-stage leg priced and per-mode bars fitted at whichever regime selection reads. ⚠ The release-geometry column will be a SELECTED sample — never read an unbiased AUC off it.
8. **The colour ceiling's allowance is binding at n=150.** Write-up → `preserve\selection_design.md`.
9. **n=1000 is not demonstrably feasible** — the constructive lower bound on non-twin capacity sits far below the upper. A mining question.
10. **Intel XTU is Matt's to kill** — a service that writes bursty multi-hundred-MB logs and refuses deletion and truncation without elevation. The durable fix is stopping or uninstalling the service, not clearing the file again.

## RULINGS THIS ERA (Matt)
- **Preserve is not a free destination.** `preserve\` files may themselves be DELETED or REFACTORED where that is efficient; closed-arc detail with no named open item is DROPPED rather than moved.
- **fractal-engine keeps only claude.ai-facing truths** — per-family render mechanics live in `engine/README.md`.
- **ONE star tier.** `★` marks a line a future session must not skim past; bold marks the load-bearing clause inside it.
- **The closeout procedure stays in fractal-operating** — not worth risking that process to save bytes.
- **A rule bought by a failure may be cut only when a shipped guard now enforces it, or when it is a strict subcase of a rule already present.** Unenforceable measurement-validity caveats are never cut on those grounds.

## INVALIDATED WITHOUT AN EDIT
None outstanding — the ckpt-90 list was applied into the docs this closeout and is deleted.

## KEEP LIST — survives this boundary
`reports\label_ingest_tiers.csv` (Matt's working CSV). `prompts\` and `reports\` are otherwise wiped entire.

## PRESERVE — SETTLED THIS ERA
`INDEX.md` rewritten wholesale and **it no longer records sizes** (four of nine were wrong, and they went stale every era). `judge_training.md` corrected — the map-history AUC was a cross-store pooled read, invalid, never to be quoted — and given the ckpt-89/90 evidence that bounds any grade. `settled_rulings.md` gained the era's tombstones, with the geometry-join duplicate folded back into its ckpt-89 entry. `selection_design.md` gained the unseen-colour intent, Matt's unbuilt distribution design, and the colour-ceiling evidence carried out of `color_coverage_floor_design.md`, which is now DELETED along with `visitor_explorer_design.md`. Nine files remain.
- ⚠ **A DELETE FROM `preserve\` IS A GRAPH OPERATION, NOT A FILE OPERATION** — sweep both repos AND all of `preserve\` for citations as its OWN step BEFORE the delete. Here the sweep ran beside the delete and a TRACKED website file was left citing a retired design doc, with three pronouns in that paragraph pointing at nothing. Rule now heads `INDEX.md`.
- Merging `audit_deep_descent_report.md` + `deep_kernel_plan.md` into one deep-arc file is a candidate, unpriced and unstarted.
- **Two tiny fixes are OWED, to ride the next prompt into each repo.** fractal-wallpapers: `ceiling.GROUP_CAP_RATE`'s comment claims it is not shipped while `seating.DEFAULT_GROUP_CAP` next door is the proportional cap — adjacent files contradicting each other. fractal-website: two entries in `explorer/README.md`'s departure list still open with a quotation from the retired design doc and no longer stand alone (the offered-map count, which now reads as a typo, and the byte-accuracy bar, whose measurement survives without it). Nothing enforces either.

## README OWNERSHIP — VERIFIED THIS ERA
`curation/README.md` owns the historical per-candidate rate table (means AND medians, labelled per arm), the mode capability table, the `curate depth` plan shape and retention policy, and the `merge → flatness sweep → seat` order. `palettes/README.md` owns the library → pool → drawn chain, the held-back map, and the bake-comparison method. `engine/README.md` owns per-family symmetry, the fractional branch cut, mirror folds, palette storage, the specialization story and the wasm build. ⚠ **The wasm half is not in this repo at all** — bindings, build and the byte-identity measurement live in the fractal-website checkout, which takes the crate as a path dep; nothing in fractal-wallpapers builds a wasm target or tests one.

## PARKED / SETTLED
Parked → `preserve\parked.md`. Declined and never-re-raise → `preserve\settled_rulings.md`.

## SCRATCH/ARTIFACT FLAGS
No run this era; nothing new under `scratch/` must survive. Ledger, artifact-tree and free-space figures are re-derived on demand and are not carried here — the last measured set is in the ckpt-90 disk and mining reports. Standing KEEP: `artifacts/curation/candidate_ledger/` · the flatness sidecar (undurable, regenerable while the pictures are on disk) · `artifacts/curation/neutral_embeddings.jsonl` · `artifacts/render_cv/` · `artifacts/curation/` HOT · the live release rows.

## CLOSED (records wiped — verdicts are in the docs)
`readme_absorb` · `preserve_edits` 1–4. All documentation passes; every finding is in the READMEs, the preserve files, or the owed-fix note above. **The method lesson they bought is in fractal-operating §WORKING STYLE** — a mechanical-edit prompt states the goal and treats its anchor as a hint, because every failure in the chain was Claude over-specifying mechanism and leaving CC no room to act on what it could plainly see.

## ROSTER — sizes at ckpt 91
All six emitted WHOLESALE. state 8.6k · engine 8.1k · discovery 14.5k · corpus 16.3k · tutorial 20.5k · operating 22.9k; **set 90.9k against 119.1k at ckpt 90 — 24% off.** Preserve: `INDEX` rewritten, `settled_rulings` and `selection_design` APPEND, two files deleted, `judge_training` corrected.
