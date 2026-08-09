# fractal-state — ckpt 36, 2026-08-09

**Rewritten in full at EVERY distillation — the only doc guaranteed to be.** Holds NO FACTS: status, plan, flags, open/parked, roster.

**This checkpoint = the v11 / crop-batch / workflow era (~1 day):** full-rebuild decision (Matt: "we have time") → Rust `crop-batch` extended-field executor (one iteration pass/location; 4.8–7.3× over legacy) → v11 cache (361,696 tiles / 22.57 GiB / 3.09 h; 32 tiles/loc independent draws, q60..95) → v11 trained + certified (all gating arms; the 3|4 cutpoint tightened, ordering intact) → ADOPTED (full recal cluster together; ranker deleted; weights retention policy active+previous) → storage cleanup (caches deleted; v8/v9/v10 plan-pairs all bulk; feats moved; force-add class near-closed) → τ_h enlarged to the full registry population + native multibrot t_good adopted → tier-0.5 workflow (drive-sync exchange folder; CLAUDE.md owns the standing prompt contract; prompts no longer restate it).

## THE GOAL (Matt) — unchanged
Two learned functions: **(a) find good minibrots** (screening over maneuver targets) and **(b) find the q4 within a neighbourhood** (guided descent). **Stated end-state: FULLY UNSUPERVISED / PROGRESSIVE wallpaper generation, nonstandard renders included.** Correction loop is the mechanism; per-sitting correction rate the convergence metric (first datum 43.6%, v10-era); era gate (release-sheet review) the standing human act.

## THE PLAN — Phase C → D transition
*(20) v11 retrain DONE-and-ADOPTED · (21) τ_h DONE (enlarged) · conformance item DONE (`derive_t_good` on grouped-split default) · ranker question CLOSED (deleted; emission stays unranked by design).*
**Post-checkpoint queue (Matt-approved order):** **(24) cross-run saturation memory** — visited-density discount on breadth steering, scale-aware radius knob (default calibrated from run 2's banked sat_frac curve), dive/quality legs EXEMPT; no decay. Gates the first long run. **(25) first v11 production run** — first run ever with julia:mandelbrot + phoenix served (real t_good, not 0.50); repopulates the library seed; feeds mb4's missing walk arm; fold in the phoenix:classic supply leg (`--run-phoenix` + classic supply path — classic has ZERO admitted v11 supply); its release-sheet review is the era gate that judges the knife-edge cuts. **(23) wallpaper v4b** when minibrot/maneuver material reaches stage-2 intake (that sitting MUST include maneuver views + top-slice positives; flip carries gate re-derivation + the floor-admit split). **(16) sittings recur** — phoenix:classic still needs its own bucket or a non-bucketed sitting (7 positives; bucketed cuts do NOT reserve). **(18) descent harness resumes.**

## STATUS
- **v11 LIVE** (flipped 2026-08-08); ladder **v11 → v10 only**. Corpus 12,637 labeled / 14,339 registered. Stage-2 unchanged: wallpaper v3 LIVE (v4 weights de-tracked; retrain-from-scratch at v4b) · mining v1 LIVE enforcing · pref v3-gvo LIVE.
- t_good: every partition calibrated EXCEPT phoenix:classic (0.50, stamped) — j:mandelbrot + phoenix first-ever, natives adopted 0.61/0.85/0.61. τ_h: full-registry derivation adopted, per-run truncation stamped.
- Workflow: `C:\Code\fractal-drive-sync\{prompts,reports}\` exchange live both directions; standing prompt contract lives in fractal-maker CLAUDE.md; controller CLAUDE.md carries the mirror rules; `matt-claude-workflow.md` documents the pattern for new projects.
- Suite green (default 116 s; slow lane now ~2.6 min after `decdfc2`); tree clean; artifacts store 32 GB with teardown-on-clean-close live.

## FLAGS (new this era)
- **multibrot4 τ_h is harvest-arm-only** (walk arm lost at t_good 0.85: 2/169 passers < min_n) — an upper bound with no lower bound, and the table's largest move (0.47→0.82). Remedy = walk rows from run (25); flag dies when the walk arm re-clears min_n.
- **Native multibrot τ_h trio is CONFOUNDED** (t_good + population moved together between derivations); de-confound = compute-only third derivation over the banked 3,492-row sample — available, deliberately skipped (measurement minutiae).
- **phoenix:classic: zero admitted supply under v11** (24 rows, all decode ≤2) vs release_mix asking ~12/intake — remedy in run (25).
- Knife-edge t_good plateaus on j:mandelbrot + phoenix — adopted-with-flags; run (25)'s release review is their judge.

## OPEN — recorded, not scheduled
label-run target semantics (currency vs clock/row-share) · mandelbrot price rests on 3 samples · phoenix units-weighted EMA step promoted to next allocator touch · release selection carries no mix term + deficit granularity · `emission_selector` z-plane `VIEWPORT_K`/`ZOOM_RATIO` uncalibrated · eval slice lacks parameter axes; classic viewport instrument NOT_DRAWN, fail-closed · opaque-export guard gap (verify merges by row count) · frozen-record hazard sites (6, swept, undecided) · namespace-package migration · `LS.FIELDS` at `bulk()` · `tau_h_retained_readout.py` not re-run against the enlarged base.
*(Closed this era: un-segmented pair — segmentation DEAD, 8h ledger = 3.6 MB · τ_h population deferral · ranker · v9 parity gate.)*

## PARKED — named, not half-open
color-space cool-lean (levers named) · two dead strange modes (27% of colorize budget) · `render_release` unbounded end-to-end · phoenix render-cost fact (6–20×/field) · pref re-collection (two triggers) · uniform draws (contingency) · mining gate_report false-cut signal · refill knobs unexercised near limits · variety measure · composition · Douady tuning · perturbation in `render-one` · probe as standing audit · Rust-kernel profiling · ∂M-distance-scaled c-floor · lever-2 · deep-render tier · native-τ_h de-confound (above) · wider-than-68 palette draw (68-palette draw is live; "wider set" now means beyond it).

## ROSTER — soft size targets (unchanged; targets move only with Matt)
operating 13k · state 6k · engine 11k · storage 6k · orchestration 4k · models 8k · thresholds 5k · corpus 8k · discovery 13k · emission 6k
