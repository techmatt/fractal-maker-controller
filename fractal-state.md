# fractal-state — checkpoint 67 (2026-08-22)

## Where we are
Ckpt 67: figure-link registry LIVE (27 links, `zx/zy`, no engine change needed); **Color palettes PLACED** (v3 → placement with seven source corrections; nine figures; all-palettes + make-your-own pages under `palettes/`); `judges-score-to-decision` PLACED and linked; **download-at-dims LIVE** (byte-identity chain CLOSED end-to-end: 0/3.7M px at 2560×1440 ss4 vs CLI); `audit_finishing` banked; **run10 STAGED, not launched** — launch line in `reports\stage_run10_report.md` §8. **Rulings this era:** one wallpaper per location, COLLECTION-wide (built, `location_served`) · perceptual-diversity arc (DINOv2, conservative hard radius + soft bias) queued after run10 · depth vocabulary (f64-pushed = DEPTH; DEEP = the unbuilt perturbation arc) · render-maxiter stays unlinked by design · home-views gallery to be REBUILT from explorer home views · ledgers to move OUT of the archive. 7 of 10 sections placed. Both repos FREE.

## OPEN (ordered)
1. **LAUNCH run10** (Matt, next session): first `fractal-wallpapers storage restore curation` (artifacts/curation is on the archive — release renders would write seek-bound); then the §8 launch line with `--seed` = launch date. Expect under-fill at -n 80 (run9 calibration: 48→27 seats under the location rule). Readout prompt after: `finish_by` terms vs actual; share vs contest medians per partition; saturation; operator prices; `location_served` counts by cause.
2. **Website next prompt** (free now): rebuild `family-home-views` gallery from the explorer's per-family home views (six tiles, full provenance, linked); README per-mode cost table is mandelbrot-only — add the family spread; pool cap 8 on 12 cores (cheap first perf move). ⚠ All perf numbers from this era were measured under CPU contention (wasm + run10 work concurrent) — treat as priors.
3. **Perceptual diversity arc** (wallpapers, after run10 readout): canonical render = dumped smooth field through one fixed cyclic map → DINOv2 embedding once per location; served index in embedding space; HARD radius (start conservative, widen by eye; distance on every refusal card) + SOFT factor on the selection rank key (farthest-point weighted by quality, two params by eye like k/f); retro table of nearest served pairs for Matt. Also: Matt chooses survivors among the 32 served wallpapers over the location rule (`scratch/run10_repeats.json`, 27 groups).
4. **Ledgers out of the archive** (wallpapers, small): three `rglob`s walk the whole archive at startup (11 min); move ledgers to a small hot tree, or one rglob for three consumers.
5. **Native genericity fix** (wallpapers, perf): `field::sample` takes the generic `iterate::run` — the browser's nine specialized call sites beat native 20.5 s vs 30.8 s on one frame; port the specialization (→ fractal-engine). Matt: "bigger performance work coming separately."
6. Prose: From-locations (audit banked; NOT this checkpoint) · Running at scale (after run10 readout) · Deep zoom (after the perturbation arc). Threads spike: buys the shade, not the field — decide after the perf work.
7. Parked (Matt's call each): list → fractal-tutorial §THE REPO.

## CLOSED this era (record = Drive reports)
- figure_link_registry — `explorer/links.jsonl` 43 rows, 27 linked; buckets drawn 3 / incomplete_provenance 3+6 tiles / not_exposed 4 / deep 0; bake 98 maps, 77 offered; `builder check explorer`; `emit.mjs` plans each view (cap mismatch = refusal, fired once: render-maxiter).
- place_color_palettes — seven verification corrections (→ fractal-tutorial); nine figures on q4 rows; 103 baked / 77 offered; pages in `palettes/`; `colormap` in a provenance line is what bakes a map.
- explorer_download — supersample lives in the wasm crate (`SUPERSAMPLE` const was the only gap); bands are output rows, direct traps padded 3·ss; cap 60M samples; shade in its own worker; download holds the view.
- audit_finishing — stage table, selection cuts, mix table, finishing costs, wire kill (fired twice ever, never at a ceiling) → cited by the From-locations draft.
- stage_run10 (+ADDENDUM A) — `--finish-by` (derives, doesn't pace; five reserved terms + 20-min margin); release HUNG_CEILING 2400; `bar_exceptions.jsonl` (4 rows, per-row keys); `CLUSTER_CAP` 1 collection-wide; group-labelling defect fixed (three labellings → one); readout fields, STATE_SCHEMA 5; autopsy GATES sentences; smoke at now+30m.
- Corrections landed: phoenix z₋₁≠0 is 39/48 (ledgers), not 41/47 · "two crops" = two figures + six home-views tiles · NO palette-cluster cap exists at release (draft claim void) · run8h below-bar rows are 4, not 7 · 32/149 releases carry a human label (31 served), not 22 · a release is NOT killed at the wire shallow (max 1084.6 s finished) · authored palettes = 175 (Matt's >175 hunch wrong).

## SCRATCH/ARTIFACT FLAGS
- `scratch/run8h_instrumented/` SURVIVES until run10 + readout. `scratch/run10_repeats.json` — survivor choice pending.
- `artifacts/figures/judges_score_to_decision/` placed — no longer load-bearing. `artifacts/deep_run1/` + `_gallery/` permanent. `preserve\julia_deep_eyetest\` unchanged.
- fractal-website `scratch/_ss_check.mjs` disposable; `scratch/explorer_bench/` disposable. Prose masters live in `prose/old/` (registry updated).

## ROSTER — soft size targets
operating 14k · state 6k · tutorial 15k · corpus 7k · discovery 6k · engine 5k. This distillation: state REPLACED · tutorial REPLACED · engine 2 hunks · discovery 2 hunks · corpus 1 hunk · operating CLEAN.
