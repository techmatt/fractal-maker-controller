# fractal-models — the instruments

Changes when: retrains, ranker/screen work, aug-recipe changes. Thresholds live in fractal-thresholds; label corpus in fractal-corpus; the view-fit sourcing screen in fractal-discovery.

## Division of labor
| model | judges | scope |
|---|---|---|
| **v10** location head | location potential, pre-color, classes 1–4 | within-family STEER + FLOOR + decode-admission; NEVER ranks, NEVER allocates cross-family |
| **`pref_loc_v1`** ranker | ranking of admitted locations | ORDERS (keeper / emission-intake / dive-result); never steers, never allocates |
| **`view_fit_v1.1`** | maneuver-candidate sourcing order | fractal-discovery owns it |

The steer/rank/select split is load-bearing — winner's curse recurs at instance, family AND selection level (`measurement_practice.md`). **"q4" names the artist-quality look = class 4 on the label scale; there is no separate q4 network and will not be one.**

## v10 — the deployed location head (flipped 2026-08-02)
MobileNetV4 (`mobilenetv4_conv_medium`, 1280-D penultimate), CORN ordinal, multi-family, K=4 — K is per-version, read off the checkpoint's own `config`, never hardcoded. Deploy: 384×224 stretch from 640×360 ss2 `twilight_shifted`, via the pins module; transform pinned bit-for-bit. Method = `classifier_retrain_protocol.md`; role/reading = `aesthetic_scoring.md`. Trained on the v9-cache extension (201,168 tiles) + 1,310 new labels (730 crawl incl. 81 rule-provenance / 580 harvest); uniform-90 held out of training AND of model selection.

- **Certification [pre-registered]:** census-144 **0.742 vs v8 re-scored 0.751, p=0.79 ⇒ NON-INFERIOR** · floor-526 0.872 vs 0.867 NON-INFERIOR · uniform-90 (NEW instrument: the only score-unconditioned maneuver-view draw; ≥2 boundary; non-gating first use) both heads separate, v10 0.828 / v8 0.848. Palette invariance ρ̄ 0.845, inside the 0.10 band.
- **★★ THE GAIN WAS ZERO** (p 0.69–0.84 everywhere): 1,310 labels bought non-regression. Structural reason, not mystery: appended labels are 100% native-plane while the primary instrument and ALL class-4 eval power are julia:multibrot — the instruments could not price the intervention. **Corpus-mix consequence PAID (2026-08-03): the uniform eval leg bought per-family instruments** (recorded, fractal-corpus) — consumed at the next retrain's calibration. The ≥3 boundary in the maneuver-view population remains instrument-less.
- **★★ THE MODEL-SELECTION OBJECTIVE IS A CONTROLLED VARIABLE.** Attempt 1 was INFERIOR because promoting uniform-90 to eval silently moved the split the checkpoint pick selects on; `model_last` beat `model_best` on the census (+0.104, p=0.002). Fix: freeze selection to the baseline-comparable population; amendment committed BEFORE the re-run. Generalizable to every future retrain.
- **★ CORRECTED CLAIM (was a population error):** "v8 non-separating on maneuver views" was `[machine-decode]` evidence at the ≥3 boundary, where the uniform leg has ZERO positives. At ≥2, v8 separates that population at 0.848. **The ≥3 boundary has no eval instrument anywhere — that, not v8-blindness, is the open measurement gap.**
- **Class-4 WATCH (no gate):** descriptive AUC 0.813 → 0.728 [n=22, all julia:multibrot, inside label noise] — rides `cloud_diagnostic`, keyed on scorer version, self-retiring. First v10-era run gets a qualitative eye on q4 yield.
- **Inherited role limits** [human n=81+298+500]: on selected output `p_good` is a badness filter; NEVER allocate across families (family-mean Spearman −0.57); over-separates seed fertility (machine ICC 0.90–0.965 vs human 0.72–0.82).
- **★★ Machine-1 trust is PARTITION-DEPENDENT [human n=870, blind, 2026-08-03]:** P(human=1 | decode=1) — native multibrot 94–100% and phoenix 72% with 0/82 ≥3 ⇒ auto-discard safe there; **julia:mandelbrot 30.9%, with 16.5% of its machine-1s human-≥3** ⇒ never auto-discard. The pooled 68.9% is composition, not a decision. Matt's cross-degree coupling of "badness" holds on the c-plane and stops at julia.
- **Rollback ladder v10 → v8 → v7 → v6 → v5** (recorded with the revert-together set beside the pin). **★ A rollback to v8 must RE-DERIVE its t_good table, not copy it** — fractal-thresholds owns why; the hazard is also written at the pins module.
- **★★ Flip-era lesson kept: when checking whether a flip moves a frozen artifact, check the sites that BUILD its inputs, not just the loader** (the v8 flip nearly corrupted the ranker's frozen v7 features silently; now pinned via `tools/ranker/scorer.PENULTIMATE_CKPT`, raises rather than falls back).

## v9 — shelved (closed)
Never deployed; its cache was the forward asset and v10 extended it byte-identically (170,760/170,760 prefix plan rows). `keeper_cuts_v9.json` deleted. Its lesson survives in the aug-recipe rules below.

## The augmentation recipe
**24 crops/location: 4 palettes × 3 geometric samples × 2 AA levels.** Palettes per LOCATION with a per-location seed: `twilight_shifted` always (deploy-matched) · `blue_orange` always (the map Matt's labels are formed on) · 2 from the 76 curated, **with 8 held out of training entirely as the invariance instrument.** Geometry: one identity framing + 2 jittered (shift ≤ 0.11 fw, scale ∈ [0.90,1.10]). AA: `ss1 box` + `ss2 lanczos3`. `data_v4.Loc.palette_renders()` derives the expected count from `aug_roster.json` — a recipe change is data, not code.
- **★★ Never augment in a way that destroys the evidence the label was based on** (off-structure crops inheriting the location's label corrupted the positive classes for every model v4→v7).
- **⚠ Wider palette set (32–64/location): wanted, now parked TWO consecutive builds** — genuinely next rebuild.
- **Costs for sizing [measured, v10 extend]:** 30,408 tiles in 7.52 h (estimate missed 1.49× even sampled in run order) — **appended maneuver material runs ~9× v9's per-tile cost, driven by interior mass, not the cap.** Full rebuild at 8,382 locations ≈ 11–13 h; the recolor-batching executor (fractal-engine) would cut the appended half ~4×.

## `pref_loc_v1` — the ranker (`tools/ranker/`)
Frozen **v7**-penultimate + colored-CLIP, logistic good-vs-rest. Certified [3-batch LOBO n=379]: pooled Spearman +0.279 CI[+0.185,+0.371] vs canon p_good +0.115, positive every family; phoenix transfer adds nothing. **HARD SCOPE: never wired into frontier priority, dive-start, scheduling, or any discovery decision.** Not refit onto v8 or v10 — pinned.

## q4 stage-1 screen (G) — superseded at sourcing (kept for its invariants)
**★★ G is a weak gate and a dead ranker** [human n=487, blind]: AUC 0.605 pooled, 0.511 within its own accepts. Use to discard junk only; the interior clause is inert as a quality filter but **KEEP as a 5.3× COMPUTE filter** [160/160 atoms]. Invariants any successor inherits: OOD-mask permanent · p NOT calibrated — gate from LABELED precision · deterministic seed before any weight-stability claim · referee = minibrot-DISJOINT LOMO. ⚠ Neither G nor any ring measure sees within-source VARIETY or COMPOSITION — open; no scalar settles a composition call.
