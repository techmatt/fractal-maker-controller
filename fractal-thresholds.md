# fractal-thresholds — live cuts & the decode predicate

Changes when: a flip, a re-derivation. **⚠ STANDING CAVEAT: every threshold and score derived before the ckpt-22 cap raise sits on a moved distribution** (scores moved ~2× on the cap change alone) — express cuts RELATIVE TO A REFERENCE, never as absolutes, and re-derive `t_good` + keeper cuts + τ_h **together, not piecemeal** (register → `docs/design/deferred_recalibration.md`).

## t_good — ADOPTED on v8's scale, per-family objective
q3 = `p_good ≥ t_good AND p_notbad ≥ 0.5`.

| partition | objective | t_good | prec | rec | F | F_OOF | status |
|---|---|---|---|---|---|---|---|
| mandelbrot | **F0.5** | **0.85** | 0.571 | 0.154 | 0.370 | 0.300 | derived |
| julia:multibrot3 | **F2** | **0.39** | 0.513 | 1.000 | 0.841 | 0.804 | derived |
| julia:multibrot4 | **F2** | **0.14** | 0.545 | 1.000 | 0.857 | 0.797 | derived |
| julia:multibrot5 | **F2** | **0.20** | 0.677 | 0.955 | 0.882 | 0.813 | derived |
| julia:mandelbrot · multibrot3/4/5 · phoenix | — | 0.50 | — | — | — | — | **UNCALIBRATED** |

- **★★ The objective principle (`classifier_retrain_protocol.md` §4): weight RECALL where supply is scarce, PRECISION where supply is abundant** — a false admit costs the same everywhere; the cost of a MISS differs by family.
- **★ UNCALIBRATED IS STAMPED, NOT IMPLIED** (`t_good_status → DERIVED | UNCALIBRATED | UNKNOWN`) — in a config file a baseline 0.50 and a derived 0.50 are indistinguishable.
- **⚠ Mandelbrot's operating point rests on SEVEN admits** (4 tp / 3 fp; 7 of 526 = 1.3% admit rate on the family that is 55% of the corpus); optimum spans [0.79, 0.85], one-step cliff at 0.86. **Nobody has compared this rate to v7's — check explicitly on the first post-flip run.** The failure mode looks like the library quietly stopping growth.
- **⚠ All three julia:multibrot cuts are threshold-overfit at small n** (OOF is the honest column; mb4/mb5 sit on 1–2-step plateaus). **Re-derive on more labels; never hand-nudge.**

## τ_h — re-derived under v8, no longer fatal
`data/atlas/tau_h_base_v8.json`, from 3,492 rows; all 8 partitions cut on their own population (n_pass 39–285), none pooled.

| partition | v7 (retired) | **v8** | | partition | v7 | **v8** |
|---|---|---|---|---|---|---|
| mandelbrot | 0.201 | **0.704** | | julia:mandelbrot | 0.184 | **0.349** |
| multibrot3 | 0.201 | **0.417** | | julia:multibrot3 | 0.311 | **0.381** |
| multibrot4 | 0.774 | **0.550** | | julia:multibrot4 | 0.207 | **0.200** |
| multibrot5 | 0.201 | **0.437** | | julia:multibrot5 | 0.186 | **0.199** |

The values move enormously and that is the point — v8's `t_good` is a stricter bar, so frames clearing it sit far higher on the cheap axis. **A float says nothing about which model it describes — exactly how a vendored constant survives a flip still looking authoritative.**
- **★ The harvest log is LEFT-TRUNCATED by construction** (holds only checks that cleared the previous head's τ_h ⇒ its quantile is an upper bound). Committed value = per-partition MINIMUM of harvest-log and untruncated walk-outcome derivations — a too-high cut sheds admissions.
- **`TAU_H_CAMPAIGN_FLOOR` retired, not carried** — a v7 floor on a v8 base is the category error the version stamp exists to stop; table emptied with its own stamp, mechanism still tested via an injected floor. Not re-derivable until a v8-era run produces admissions.

## Keeper cuts (`data/atlas/keeper_cuts.json`)
REPORT-ONLY floor; ranker orders within eligible; recut against the durable v8 eval slice, stamped `model: "v8"`; **a keeper is `label >= 3`, not `== 3`**. ⚠ On mandelbrot the keeper bar and discovery bar are now the SAME number (0.85) — safe because nothing gates on it; **any stricter mandelbrot keeper bar is guesswork until the family has class-4 eval labels.**

## Decode-version predicate — version-general (HIGH-touch)
`corpus_common`: `is_decoded_by`, `is_current_decoded`, `current_rows_only`, `require_current`, `StaleDecodeError`. **Mixed-decode readouts are poison.** Admissible pool = current-decoded ledgers; a t_good flip retro-re-decodes by arithmetic on stored raw probabilities — stale rows die by the predicate, nothing hand-deleted. **Also a load-bearing FIREWALL:** `load_admitted` requires current-decode; that gate alone contained a total resolver bug on walk-era julia rows.
- **★ What it CANNOT catch: freshly-written rows that are wrong** — smoke/test rows are current-decode and admissible, which is why sink isolation (fractal-orchestration) is a hard requirement, not hygiene. ⚠ Its cost: the flip made the library seed unreconstructable (fractal-orchestration).
