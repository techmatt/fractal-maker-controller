# fractal-state — ckpt 24, 2026-08-01

**Rewritten in full at EVERY distillation — the only doc guaranteed to be.** Holds NO FACTS: status, plan, flags, open/parked, manifest. A fact that needs recording forces its owner doc onto the touched list (fractal-operating).

**This checkpoint = the restructure.** The 4-doc set (ckpt 23) is retired into this 10-doc set; CC-facing practice paged into the repo (`verification_practice.md`, `measurement_practice.md`, `retired.md` + patches — commits `cee8f97`, `72c7ffe`).

## THE GOAL (Matt, stated plainly)
Two learned functions: **(a) find good minibrots** — a SCREENING problem over maneuver targets, not a search for a source — and **(b) find the q4 within a neighbourhood**, the GUIDED-DESCENT function, learning how Matt defines a beautiful descent location ("nothing specific to do with minibrots"). Full automation stays the target; manual isolation of q4s is scaffolding to collect examples, not the product.

## THE PLAN
**(1) ~~v8~~ · (2) ~~re-render + retrain~~ v9 SHELVED · (3) ~~maneuvers built + shaken down~~ · (4) ~~maneuver improvements + per-degree probe~~ · (5) THE 4 h MANEUVER SUPPLY RUN ← next · (6) label its output; retrain (v10) — THE FLIP · (7) evaluate the maneuvers · (8) THE HUNT · (9) guided descent (harness resumes) · (10) one production campaign.**
- Campaign stays last (a new generation type enters as a partition; a campaign now spends its eye-hours twice). Nothing is urgent — no early deliverables. The harness is SHELVED until step 9 (Matt, explicit).

## STATUS
- **EMISSION IS DARK** — every ledger row went non-current at the v8 flip; the hunt relights it. Library 1387 admitted / 1268 clusters, six ledgers stale-decode.
- Discovery last ran: campaign 2 + julia parent probe + maneuver shakedown + per-degree probe. Emission last ran: first release (FINE) + q4-harvest probe.
- Suite 860 Python + 73 Rust, green. Repo 30,236 files / 7.93 GB.
- `main` is ahead of `origin/main`, unpushed (SSH auth fails on this machine).

## STALENESS FLAGS
- **thresholds:** everything derived pre-cap-raise sits on a moved distribution — `t_good` + keeper cuts + τ_h re-derive TOGETHER at step 6 (`deferred_recalibration.md`).
- **discovery:** economics EMA stale until a v8-era run refreshes it; ring scores pre-2026-07-31 on the old maxiter scale.
- **orchestration:** library seed unavailable in principle until the next discovery run's admissions — scheduler-off meanwhile.

## OPEN ITEMS — recorded, not scheduled
Sheet 3 produced only 22 atoms while rating very highly — supply limit or budget cap decides source vs curiosity · the ~285 MiB v8/v9 deletion — approved, blocked on preconditions (→ `storage_classes.md`) · `coevo/`'s retirement verdict in `tools/README.md` — Matt's call · `scratch/maneuver_degree_report.md` Part 3 content has no owner yet (its §2.6 half is stale against the tree; extract-or-delete pending).

## PARKED — named, not half-open
The variety measure (within-source AND within-release — one answer with emission diversity; span-vs-oscillation the standing candidate) · composition (no instrument sees interior fraction, placement, balance) · Douady tuning (unblocked, unbuilt) · perturbation in `render-one` (the gate on any deep location being a candidate) · probe as a standing audit · the recolor-batching executor (next cache rebuild) · the wall display's `id_map` rewiring (only if Matt scans the wall) · the deferred-recalibration cluster (`deferred_recalibration.md`) · wider aug palette set (32–64, next rebuild).

## MANIFEST — replace only the files listed as touched at each distillation
| doc | last touched | wc -c | ceiling |
|---|---|---|---|
| fractal-operating | ckpt 24 | 12,871 | 13,000 |
| fractal-state | ckpt 24 | (this file) | 6,000 |
| fractal-engine | ckpt 24 | 10,513 | 11,000 |
| fractal-storage | ckpt 24 | 5,759 | 6,000 |
| fractal-orchestration | ckpt 24 | 3,335 | 4,000 |
| fractal-models | ckpt 24 | 7,355 | 8,000 |
| fractal-thresholds | ckpt 24 | 4,716 | 5,000 |
| fractal-corpus | ckpt 24 | 7,318 | 8,000 |
| fractal-discovery | ckpt 24 | 12,718 | 13,000 |
| fractal-emission | ckpt 24 | 5,598 | 6,000 |

Total ceiling 80,000 B (vs 116.9 KB at ckpt 23). Ceilings never increase without Matt. fractal-discovery is the largest and the hottest — the first candidate for a split if it presses its ceiling.
