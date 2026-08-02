# fractal-models — the instruments

Changes when: retrains, ranker/screen work, aug-recipe changes. Thresholds live in fractal-thresholds; label corpus in fractal-corpus.

## Division of labor
| model | judges | scope |
|---|---|---|
| **v8** location head | location potential, pre-color, classes 1–4 | within-family STEER + FLOOR + decode-admission; NEVER ranks, NEVER allocates cross-family |
| **`pref_loc_v1`** ranker | ranking of admitted locations | ORDERS (keeper / emission-intake / dive-result); never steers, never allocates |
| **q4 stage-1 screen (G)** | window-level sourcing screen | a coarse GATE only — superseded at sourcing |

The steer/rank/select split is load-bearing — winner's curse recurs at instance, family AND selection level (`measurement_practice.md`). **"q4" names the artist-quality look = class 4 on the label scale; there is no separate q4 network and will not be one.**

## v8 — the only deployed location head
MobileNetV4 (`mobilenetv4_conv_medium`, 1280-D penultimate), CORN ordinal, multi-family, **K=4 ⇒ three cutpoint logits** — K is per-version, read off the checkpoint's own `config`, never hardcoded. Deploy: 384×224 stretch from 640×360 ss2 `twilight_shifted`, via `active_ckpt.py`; score via `score_lib.py::Scorer`; transform pinned bit-for-bit. Method = `classifier_retrain_protocol.md`; role/reading = `aesthetic_scoring.md`. v4–v7 corpora/manifests/caches are gone and stay gone.

- **Certification (unselected, within-family):** primary = julia:mb census-144 [65 pos] **0.751 CI[0.671,0.828] vs v7 re-scored 0.700, p=0.17 ⇒ NON-INFERIOR**, numerically ahead, not significant. Secondary = mandelbrot floor [n=526, 26 pos] 0.868 vs 0.885 non-inferior — and v7 trained on those rows, so its score is flattered. Class 4, descriptive only: census q4-vs-rest AUC 0.813 on 22 positives.
- **★★ v8 was a NEW MODEL, not a controlled increment** — scale, manifest, split, augmentation all changed at once; attribute no movement to the ordinal scope change.
- **Inherited role limits** [human n=81+298+500]: on selected output `p_good` is a badness filter; NEVER allocate across families (family-mean Spearman −0.57); over-separates seed fertility (machine ICC 0.90–0.965 vs human 0.72–0.82).
- **UNCERTIFIED:** deeper zoom, minibrot neighbourhoods, phoenix, julia:mandelbrot, native multibrot (zero eval rows) — **and it has never seen a maneuver-originated view**, so per-move yield is unreadable until a head is trained on that population.
- **★★ THE FLIP NEARLY BROKE THE RANKER'S FROZEN FEATURES SILENTLY** — v8 shares the backbone, so a v8 penultimate is also 1280-D: every shape check succeeds while the head returns confident nonsense from v7-fit weights. Now pinned via `tools/ranker/scorer.PENULTIMATE_CKPT`, raises rather than falls back. **Generalizable: when checking whether a flip moves a frozen artifact, check the sites that BUILD its inputs, not just the loader.**
- Kept deliberately: K=3 path byte-identical; `p_ge4` present-and-None on a K=3 trace. **The decode COUNTS thresholds met rather than chaining** — CORN cumulatives aren't guaranteed monotone; high `p_ge4` with `p_ge3` below `t_good` decodes to 3, not 4.
- **Rollback ladder v7 → v6 → v5** — must also revert `T_GOOD_OVERRIDES` + `keeper_cuts.json` (v8's scale); the keeper-provenance test makes a forgetful rollback red.

## v9 — built, measured, SHELVED (closed)
The premise was false — **the aug cache never called `auto_maxiter` at all** (`v4-render-batch` renders every plan row at one `--maxiter`, historically flat 8000). The cap raise cut v8's own train/deploy skew 10.0% → 3.3% as a side effect (deploy win strongest in the shallow deciles); the pre-registered census bar was a null instrument (all 144 tiles byte-identical — julia:multibrot converges at 8000). **Shelved; the next retrain — after the supply run, on new labels — is the flip.** v9's cache is the forward asset (170,808 tiles, byte-identical manifest; the next build EXTENDS it rather than re-rendering); `keeper_cuts_v9.json` parked. Its mandelbrot `t_good` is a knife-edge its own derivation distrusts (0.29, OOF gap +0.263).

## The augmentation recipe
**24 crops/location: 4 palettes × 3 geometric samples × 2 AA levels.** Palettes per LOCATION with a per-location seed (per-crop would defeat multi-colormap batching): `twilight_shifted` always (deploy-matched) · `blue_orange` always (the map Matt's labels are formed on) · 2 from the 76 curated, **with 8 held out of training entirely as the invariance instrument.** Geometry: one identity framing + 2 jittered (shift ≤ 0.11 fw, scale ∈ [0.90,1.10]). AA: `ss1 box` + `ss2 lanczos3`. `data_v4.Loc.palette_renders()` derives the expected count from `aug_roster.json` — the next recipe change is data, not code.
- **★★ Rule bought by the retired recipe: never augment in a way that destroys the evidence the label was based on** (off-structure crops inheriting the location's label corrupted exactly the positive classes; every model v4→v7 trained that way).
- **⚠ Wanted, NOT done: a wider palette set (32–64 per location)** — excluded from the v9 rebuild to keep it single-variable. Next rebuild.

## Palette invariance — earned, with a characterized boundary
Census-144 under `twilight_shifted` vs the 8 held-out palettes: mean Spearman **0.896**, range 0.767–0.975. The boundary is **compressed OKLab lightness range** (the two low-ρ maps are the only two with L range 0.34–0.44 vs 0.77–1.00) **[measured, n=8, suggestive not established]**; overturned by a targeted draw of more low-L-range maps failing to score low. Forward use: a compressed ramp may also make wallpapers look flat — worth more to the emission palette pool than to the classifier.

## `pref_loc_v1` — the ranker (`tools/ranker/`)
Frozen **v7**-penultimate + colored-CLIP, logistic good-vs-rest. Certified [3-batch LOBO n=379]: pooled Spearman +0.279 CI[+0.185,+0.371] vs canon p_good +0.115, positive every family; phoenix transfer [n=500] adds nothing over raw p_good. **HARD SCOPE: never wired into frontier priority, dive-start, scheduling, or any discovery decision.** Corpus prior rejected (labels distribution-bound). **Not refit onto v8 — pinned.**

## q4 stage-1 screen (G) — superseded at sourcing
The ring measures replaced G as the sourcing instrument; their validity record = `docs/design/orbital_field_metrics.md` — point, don't restate. What still matters about G:
- **★★ G is a weak gate and a dead ranker** [human n=487, blind]: pooled AUC 0.605 but 0.511 within its own accepts; within-degree at chance. **Use G to discard junk; never to order candidates; do not invest further** — the learned descent function replaces it. 11% of what it rejects is good.
- **★★ The interior clause is inert as a quality filter — KEEP it as a 5.3× COMPUTE filter** [160/160 atoms: removing it hands the ranker ×5.3 candidates and the same picks].
- **Invariants a successor inherits:** OOD-mask permanent (filter and field are one system) · p NOT calibrated — gate from LABELED precision · deterministic seed before any weight-stability claim · referee = minibrot-DISJOINT LOMO.
- **⚠ Neither G nor the ring measures see within-source VARIETY or COMPOSITION** — open; no scalar settles a composition call.
