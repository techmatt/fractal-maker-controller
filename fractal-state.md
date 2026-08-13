# fractal-state — checkpoint 43 (2026-08-13)

## Where we are
Ckpt 43 is a POLICY TURN, not a run era: **long runs (100 hr+) must never require labeling in the loop — labeling is an EVAL activity that re-anchors the books when it happens; retrain when needed, never preemptively (Matt).** "Convergence sitting" is DEMOTED out of the queue, and all three of its replacements landed this era: the standing deficit is SELF-UPDATING (it counts machine-scored stock, so a run's allocation no longer waits on human labels), an in-run SCRATCH PRUNER makes a run's footprint window-deep rather than run-length-deep, and a standing HIGH-VALUE LABEL SOURCES accumulator holds the material for an eventual ~500-row sitting. Both ckpt-42 §OPEN items closed. **No runs this era, no flip → no era gate.**
Era commits: `d54870e` seed-table reseed · `6c0dd86` self-updating deficit · `e7d7c8c` small debts · `069feb1` scratch pruner.

## OPEN (ordered)
1. **Gate-passer readers stay pinned to the v3 universe** — repointing at v4b is a CORPUS decision with its own sheet. REFRAMED, not advanced: it is parked under the labeling-is-eval-only principle and **rides whenever the ~500-row sitting happens; it never stands alone as a reason to label.**
2. **Allowlist-scanner flattening pass** — segmented `ROOT / "scratch" / …` joins, a few hundred hits needing classification, its own pass. LOW priority: the run-scratch class it would miss is owned by `PRUNE_RULES` (fractal-storage).
3. **First-100hr-run unknowns** — saturation convergence at that scale is UNMEASURED (a hundreds-of-batches property no smoke can see); the pruner removed the disk blocker, so what remains is a measurement question, not a capability one.

## CLOSED this era (verdict · record)
- Seed table RESEEDED off run 27; `source_defaulted` = [], all 9 rows measured · `d54870e` + reseed report. ⚠ **Correction to ckpt 42's record: "run 27 is the first run to have MEASURED them" was FALSE** — runs 25/26 mined both partitions far above the evidence floor; the rows were defaulted for want of a fresh DERIVATION, not a measurement, so two runs of evidence sat unused. The findings that survive the correction → fractal-discovery.
- **The standing deficit counts machine-scored stock** — per-location precedence, discounted, anchor reads it too · `6c0dd86` + deficit report (+ readout/table). Rule → fractal-discovery; constant → fractal-thresholds.
- **Emission-side `stage_times` DURABLE** (ckpt-42 §OPEN 2) — sink-bound, storage owns the mechanism · `e7d7c8c` + small_debts report. `d73a6c6`'s doc debt PAID in the same commit.
- **In-run scratch pruner** — footprint window-deep, verified across A/B, dive and kill+resume legs · `069feb1` + pruner report.

## Queue
Tutorial turn is NEXT. **Run 28 is fully unblocked** (reseed done, deficit self-updating, pruner in) — a product run on Matt's schedule. The ~500-row sitting is UNDATED, fed by the corpus accumulator.

## ROSTER — soft size targets (re-ratified at ckpt 41)
operating 17k · state 6k · engine 10.5k · storage 6.5k · orchestration 5.5k · models 7k · thresholds 6k · corpus 8k · discovery 11k · emission 6.5k
