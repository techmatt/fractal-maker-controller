# fractal-state — checkpoint 46 (2026-08-15)

## Where we are
Ckpt 46 closes the tutorial era's first transfer cycle: FOUR slices landed in fractal-wallpapers, all green on main — strange modes (`63b310b`), discovery walk (`1a5fb49`), supply engine, labels+rig (`25afd2b`). The repo now holds a working engine (smooth + 15 strange modes + dump-field/recolor), the harvesting walk with reframing operators and seed pools, the full supply engine (allocator/deficit/prices/floor-carry/refill/τ_h/harvest loop), and a populated label store — 11,303 locations exported from the big corpus — with the minimal labeling rig. Details, deviations, cautions → fractal-tutorial §TRANSFER STATE; the four reports live in `fractal-drive-sync\reports\`.
Big-repo side: untouched this era (read-only extraction only) — no runs, no flips. **Head training is the next slice and is GATED on two pending Matt decisions: GPU availability and the backbone_search_v1 verdict.** Standing direction (Matt): new work goes to fractal-wallpapers when possible; fractal-maker is mostly retired.

## OPEN (ordered)
1. **`backbone_search_v1` STILL RUNNING — BUILD, not flip** (unchanged handling: when its report lands, read it, state what it changes and what the prompt got wrong; facts route to fractal-models at the next distillation). Its verdict now ALSO gates OPEN 2 and the quantization item in fractal-tutorial's queue.
2. **Location-head training slice** — aug/tile build + training + acceptance bar only (the data half landed at `25afd2b`); gated on GPU + backbone. The acceptance bar must respect the realized 8.86% eval share and thin per-partition eval sides (fractal-tutorial).
3. Run 28's emission leg = `--release-workers` first live run (unchanged; Matt's schedule).
4. Gate-passer readers stay pinned to the v3 universe — rides the ~500-row sitting (unchanged).
5. Allowlist-scanner flattening pass (unchanged, LOW).
6. First-100hr-run unknowns — saturation convergence at scale unmeasured (unchanged).
Transfer-project queue → fractal-tutorial.

## CLOSED this era (verdict · record)
- **Strange modes + recolor utility transferred, parity attributed per mode** (15 modes — the registry's truth; the doc's 13 was stale) · `63b310b` + `engine_strange_slice_report.md`.
- **Discovery walk + reframing operators + pools + the single ledger schema** · `1a5fb49` + `discovery_walk_report.md`.
- **Supply engine complete** (allocator, self-updating deficit, prices, floor-carry, refill, τ_h deriver, harvest loop; cold start measured) · `supply_engine_report.md`.
- **Label store + flat export (11,303 locations) + minimal rig** · `25afd2b` + `labels_and_rig_report.md`.
- **Doc erratum corrected**: fractal-discovery's `classic: true` description (real-P mode, not real-c) · this distill.

## Queue
Next: location-head training (on GPU/backbone verdicts) → then per fractal-tutorial's queue. Run 28 on Matt's schedule. The ~500-row sitting stays undated, fed by the corpus accumulator.

## ROSTER — soft size targets (unchanged from ckpt 45)
operating 17k · state 6k · engine 10.5k · storage 6.5k · orchestration 5.5k · models 7k · thresholds 6k · corpus 8k · discovery 11k · emission 6.5k · tutorial 20k
