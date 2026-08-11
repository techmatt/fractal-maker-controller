# fractal-state — checkpoint 39 (2026-08-11)

## Where we are
Ckpt 39 is the COMPRESSION distillation: the set returns to roster targets. Reference-grade material now has repo homes — `docs/design/{crop_batch, exposure_hdr, corpus_batches, sitting_builder}.md`, `discovery_pipeline.md` §5, `verification_practice.md` §4+§11, `storage_classes.md` — and the handoff docs carry verdicts + paths, per operating's four compression rules. Both stage-2 heads run the 2026-08-11 from-scratch flips (wallpaper v4b, mining v3 — pins in fractal-models; floors in fractal-thresholds). Run 26 is the next production run and its era-gate sheet is the review point for both flips.

## OPEN (ordered)
1. **Base-rate audit — FIRST prompt after this checkpoint.** Blind ≥3 on unranked strange material at good locations reads far below every anchored sheet (four-sheet table → fractal-corpus); t_good, the mining gate, and downstream keeper rates were calibrated on anchored labels and may be 5–11× off. Sheet E (150 rows) cannot settle it alone. The mining flip was volume-matched, so current volumes are preserved regardless of the audit's outcome.
2. **Exposure/HDR TODOs (Matt, pending):** (a) per-mode spec edits gated on a ~20-example verification judged by in-mask chroma, never clip share; (b) continuous palette-LUT "auto-adjust" tone mapping. Record + measurements → `docs/design/exposure_hdr.md`. Run-25's two zero-yield strange modes are exposure class B — fix before any strange-mode demote crawl.
3. **Gate-passer readers stay pinned to the v3 universe** (they say why at the constant); repointing them at the v4b universe is a queued CORPUS decision with its own sheet — never a side effect of a head flip.
4. `wallpaper/rerender_bootstrap_ss2.py` scores dead-by-both in `tools/README.md`'s liveness index but was outside the closure sweep's list and is NOT evidence-checked — candidate deletion only.

## CLOSED this era (verdict · record)
- Doc-size → this checkpoint (compression pass; repo homes above).
- `library_seed_v3` REJECTED, artifacts deleted → `aa5ac72`.
- `JUNK_FLOOR` permanent shared-scale, no per-head split → `8496aec` (`test_floors.py` pins both declarations).
- `build_fresh_sheet` serves `INTAKE_CUTS` explicitly, derivation stamped → `1ac30c5`.
- `direct_*` grid self-dups 877 → 0 via one-cell-per-(location, direct mode) + 3×3→1×3 → `f7d0c54` (re-count basis `scratch/closure_sweep/direct_grid_reverify.txt`).
- Attempt budget now SEATED-slots based; unplaceable guarantee recorded, not raised → `d9fb2f5`.
- Units-weighted EMA step landed (`CostToMine.step`) → `8f87191`; `deficit_scheduler.PriceModel` keeps the old estimator on the retired scheduler path, deliberately.
- Dead-code trio (`emit_v1.main` + render tail · `selector_montage` · `family_entropy_trace`) → `211979c`.
- Classic ledger overlay deleted (intake classic 23 → 22) → `e83bec9`.

## Carried notes
- Sheet E's mode→cell map is now permuted per location (the fixed map made ring/lines collide everywhere — a systematic confound, fixed at the closure sweep); 9-cell-grid batches are no longer builder-reproducible — rows carry their own `mode_params`, crops unaffected.
- Slot-guarantee governance concern stands (fractal-discovery owns it).

## Queue
Base-rate audit → run 26 (first with both new heads; era-gate sheet reviews both flips) → convergence/tutorial turn.

## ROSTER — soft size targets (move only with Matt)
operating 13k · state 6k · engine 11k · storage 6k · orchestration 4k · models 8k · thresholds 5k · corpus 8k · discovery 13k · emission 6k
