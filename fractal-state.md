# fractal-state — checkpoint 42 (2026-08-12)

## Where we are
Ckpt 42 closes the RUN-27 era, and **the required-run chain ENDS HERE (Matt, explicit): run 27 was the last DEVELOPMENT-OBLIGATION run — future runs are PRODUCT, on Matt's schedule, with no verification homework attached.** Both ckpt-41 §OPEN items closed and run 27 ran clean. The price lockout is FIXED and production-verified — **the counterfactual inverted** (mandelbrot admissions 5.4% → 12.5% early→late against run 26's 11.9% → 0; 9/9 partitions `samples == pops`; the price converged off the 10×-wrong seed to 0.345 against a realized ~0.31 INSIDE ONE RUN; the mid-run b53 floor-fire prediction was made at b52 and verified at b53). `deploy_tail`'s driver is RETIRED (recon → Matt's call → `d73a6c6`) and the mining gate is now annotation-only EVERYWHERE — a deliberate demotion, not a cleanup's side effect. Stage-level profiling is live with a run-26 baseline. Era gate: NONE needed (no flip); Matt reviewed via the close report.
Era commits: `efdb5dd` estimator rebase · `d73a6c6` deploy_tail retire · `007b2c7` table regen · `25ab4e9` shakedown + profiling · `97d2e8c` run 27 · `a61b0b5` readouts promoted.

## OPEN (ordered)
1. **Seed-table reseed — the run-28 PREREQUISITE, and a TABLE REGENERATION, not a run.** The two `source_defaulted` entries (`mandelbrot`, `julia:mandelbrot`, flat 3.0, ~10× measured) reseed off run 27's own realized min/unit with run-27 provenance — run 27 is the first run to have MEASURED them, which is exactly what `source_defaulted` waits for. The snap-on-first-measurement class rule is OPTIONAL hardening: convergence-in-one-run is now demonstrated, so decide it on appetite, not necessity.
2. **Emission-side `stage_times` durability class** — still scratch, wipes with `rm -r scratch/*`; the discovery side is committed. NOBODY HAS A MANDATE (run-27 launch §NOT-done) → fractal-storage.
3. **Gate-passer readers stay pinned to the v3 universe** — repointing at v4b is a CORPUS decision with its own sheet (fractal-corpus).

## CLOSED this era (verdict · record)
- Price lockout FIXED, production-verified; the mechanism was CARRIED minutes, not dropped · `efdb5dd` + price_lockout_fix report + run-27 launch §price health.
- Seed table regenerated at `price_ema` 0.15 — one variable, 9/9 seeds byte-identical · `007b2c7` + regen report.
- `deploy_tail` driver + `tail_alloc` RETIRED, library half kept; the mining gate's demotion booked at the source · recon + retire reports, `d73a6c6`.
- Stage-level profiling shipped, run-26 baseline backfilled · `25ab4e9` + shakedown report.
- Run 27 clean end to end — three legs rc=0, 12/12 released, ledgers registered 12→14 (the standing step run 26 missed) · `97d2e8c` + launch report.
- The three standing readouts promoted out of scratch; validating them against run 26's published figures surfaced two run-26 errata · `a61b0b5`.

## Queue
Seed-table reseed → convergence sitting (run 27's output IS the material) → tutorial turn.

## ROSTER — soft size targets (re-ratified at ckpt 41)
operating 17k · state 6k · engine 10.5k · storage 6.5k · orchestration 5.5k · models 7k · thresholds 6k · corpus 8k · discovery 11k · emission 6.5k
