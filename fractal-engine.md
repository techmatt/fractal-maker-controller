# fractal-engine — renderer, render canon, families, identity

Changes when: renderer/kernel work, a new family, a new render axis. Owns the machine's durable anchors and identity rules.

---

## RENDER CANON (read before any render prompt)

**Two coloring recipes, different images.** Recipe 1 `render-one --palette --colormaps` — canonical for location-corpus crops, fast, takes MULTIPLE colormaps per invocation. Recipe 2 `render-one --dump-field` + `colormap.render_candidate` — arbitrary-param coloring, slower, never for location-corpus crops.

- **Field-cache reuse (load-bearing):** field invariant to colormap-tail params → one dump per (location × res × render-mode), recolor cheaply — smooth Recipe-2 only. **The field-cache key is one of only two byte-identity-critical seams** (the other: Rust↔Python LUT), pinned by frozen-literal oracles. Carries `field_mode_token` + `field_source_token` + eval-res geometry + the maxiter policy token. **★ Any new render axis must enter this key** — an absent axis collides silently with no crash while every downstream statistic shifts.
- `iterate_orbit` stays a byte-identical catch-all at `FieldNeeds::all()`; gated variant is the fast path. Mechanism → `docs/design/render_coloring_surface.md`.
- **★ Smooth is RUST-BOUND under the ×8 cap [measured 2026-08-03]:** dump median **13,072 ms** (83.4%) vs Python tail 2,232 ms (14.2%) at pool geometry — the cap raise flipped the frontier. The tail matters only ≥5.9 recolors/location (emission pool-k=7 sits just past; harvest renders Recipe-1 at zero recolors). **The tail-parity project is RETIRED; the successor attack profiles the Rust kernel (84% of wall, sized not profiled).**
- **★★ Recipe 3 `crop-batch` (`src/crop_batch.rs`) — THE CACHE-BUILD RECIPE FROM v11 ON.** ONE extended-field iteration pass per LOCATION; every tile crops out of it (`v4-render-batch` re-iterated per plan row, so a palette slot cost the same as a geometry slot). Margin is an EQUAL PLANE DISTANCE on all four sides — containment `extend ≥ 1 + 2·shift_max + max(1,H/W)·(scale_hi−1)`; the live 1.2 / [0.90,1.10] / 5% triple sits EXACTLY on it. **`field_ss 2` pinned** (grid fact: n even holds ss2's sample points and never ss1's ⇒ the antialiased arm is EXACT, the aliased arm a ≤half-subpixel point sample; 0/30 flips at deploy AA). **Canonical-frame maxiter per row** — a real ~3% policy change against v9/v10's per-slot rule, accepted. Fields stream-and-discard: NO field-cache interaction. All draws seeded `(seed_tag, loc_id, slot)`; `--replay` byte-identical. Cost **0.531 s/location + 0.0104 s/tile** vs legacy 0.1577 s/tile.
- Field-cache→recolor (~8×) = the durable fix for recurring re-colorize, LIVE library/emission work only. `render_candidate` expresses only pct/grad ⇒ **CANNOT express the morph_clip canonical transfer** (fractal-emission) — never route the canonical grayscale through it.
- **Strange modes:** monolithic `--coloring`; cached-field recolor smooth-only; composites = two-field screen blends. `specs/modes_registry.json` `tier` = deploy source of truth; 13 strange modes, smooth = spine; `direct_trap` palette-indifferent ⇒ dedup palette to one-per-location.
- **★ UF shape names do not transfer by name** — several `DirectShape` variants compute different functions from the UF shapes of the same name; per-shape `direct_threshold` defaults are coverage-anchored. Catalog → `render_coloring_surface.md` §6.
- **Palettes:** location corpus = 76 curated q3 (`score3_colormaps.json`); coloring/emission = 987 pool (`pool_colormaps.json`); `blue_orange` alone in `vivid_blue_orange.json` — in NEITHER library. `normal_map` OFF universally. **★ A plan row names a palette; something must record what that name resolved to** — `data/v8/colormaps.json` concatenates both sources verbatim for exactly this reason.

**`auto_maxiter`:** production base 500 → **4000 (×8)**, k=0.30, clamp 67000 (non-binding). The adopted cap is **median-clean, not clean** — the most decorated material stays somewhat clipped (convergent cap up to 24× legacy). Record + convergence evidence → `docs/design/auto_maxiter.md`; the "name the cap beside any field-derived number" rule is owned by `orbital_field_metrics.md` §7. Score records carry `maxiter_policy_token`; legacy rows stamped; cross-policy comparison raises; **cache tiles stamp CANONICAL-FRAME policy from v11 on** (v9/v10 paid `auto_maxiter(fw_slot)` per slot — historical note); **every orbital score committed before 2026-07-31 is on the old scale.** The enumeration (`screen_pool.jsonl`) is deliberately unstamped — nothing on that path renders a field.

## RENDER RES PINS
- **Deploy/canonical:** 640×360 ss2 16:9 Lanczos-3 (reframe, guard field, classifier → 384×224 stretch), palette `twilight_shifted` — the presentation EVERY ledger `p_good` refers to.
- **Pool/scoring geometry (pin):** 960×540 ss2 — heads res-sensitive below this; don't drop without re-deriving pool/release floors.
- **Development default = JUDGE QUALITY 1024×576 ss2** (also eval/emit). 2560×1440 ss4 Lanczos-3 wallpaper canon is HOURS — hand-picked favorites, never a batch. Full-res never as measurement; CLIP embeds at 224.
- **Steering:** 384-wide ss1 colorized field from `--expand` — steering-only, never admission.
- **Label-crop:** location corpus 1280×720 ss4 (frozen); stage-2 corpora 1280×720 ss2 Lanczos-3; blind-read/base-rate/grid 640×360 ss2 `twilight_shifted`.
- **★ Evaluation sheets and labeling companions go VIVID** — the committed `blue_orange` map, never `twilight_shifted`; a crushing palette gets good sourcing deprecated. Read the map off the committed library, never re-derive — Matt's eye is calibrated on it.

---

## FAMILY SEAM & WALKER
5 families, escape-time, all descendable; discovery/emission span **10 partitions** (base + julia twins of the c-plane degrees; phoenix varied + **`phoenix:classic`**). **`phoenix:classic` = the pinned Ushiki parameter point c=(0.5667,0) p=(−0.5,0) z₋₁=0, a DERIVED partition** [code: `partitions.partition_of_row`]: resolved row-side by EXACT family_params match (no tolerance — a float-noise miss is a STOP); absent axes resolve classic for corpus/ledger rows, but the EVAL SLICE carries no parameter axes ⇒ the resolver REFUSES its rows and slice consumers stay pooled. Degree in the name; `location.py` round-trips (decimal-string coords, lossless arbitrary precision). Descent geometry family-agnostic.

- **Julia identity = viewport AND `c`** (keyed + regression-tested; dedup seed-c-aware n-D; same-julia ε 1e-6). **★ TWO julia ledger schemas exist, keyed in `julia_ledger_schema.py`** — campaign-era and walk-era disagree which field holds `c` vs viewport; both writers stamp at birth; untagged = loud failure; `viewport_and_c` is the canonical resolver behind `descriptor.location_of`. **All new roots write CAMPAIGN schema.**
- **★ Ledger coords may be STRINGS** — normalize at the READER, never by trusting writers; the standing pattern for every identity collision, including deduping duplicate rows rather than constraining the writer.
- **Phoenix identity = the full point `(c,p,z₋₁)` AND viewport** (first-class, keyed). Absent axes → legacy Ushiki defaults, byte-identical legacy renders. Symmetry truth (measured): conjugation symmetry for all-real `(c,p,z₋₁)`, NOT 180° rotation at z₋₁=0. Reduces to quadratic julia at p=0. Phoenix+julia z-plane dedup SCALE-AWARE (`min(fw)`-radius, never flat). Block builders REFUSE a family whose extra constants weren't supplied `[code: fail-closed + non-vacuity assertion]`.
- **★ Multibrot symmetry is keyed:** z^d+c has (d−1)-fold rotational symmetry ⇒ `canonical_nucleus_c` + `nucleus_dedup_key` (d=2 an explicit identity, byte-identical key; working precision ≥ dps+15). Real-axis Newton noise fixed at READ: `snap_near_zero` + `snapped_dedup_key` + `collapse_population` at each selection consumer, first-row-wins; stored keys never move; conflicting human verdicts left uncollapsed and reported.
- `F64Backend` degree-parametric, d=2 byte-identical (SHA); fast f64 smooth path gated Smooth AND no-texture AND normal_map-Off; nucleus Newton generalizes to z^d+c.
- Per-rung machinery (Rust, reused by legacy walk + `--expand`) — constants live in code; production entry = `guided-descend --expand`: JSONL nodes → one rung each → gate survivors as candidate rows + cheap JPG; per-node RNG (seed,node_id); dead nodes emit cause tags. Julia band Rust↔Python parity 1e-12.
- **ANCHORS (verbatim):** julia known-good **c=(−0.07810228973371881, −0.6514609012382414)**; high-complexity **cx/cy=(0.4104135054546244, 0.20967482476903096), fw=0.5622541254857749**; phoenix Ushiki **c=0.5667,0 p=−0.5,0**; q4 interior-lake exemplar **julia c=(0.26103, −0.48932), center descent**. FW floor 1e-9 (not binding until ~depth 24); dive stop-margin 2e-9.

## ★★ THE `A` INSTRUMENT — atom size, orientation, precision, wall predictor
`atom_instrument(c,n,d)`, falling out of the recursion Newton already runs, ~zero cost, pure Python/mpmath, in-process. Derivation → `docs/design/atom_instrument.md` + `docs/design/minibrot_sourcing.md`.
```
z_{k+1}  = z_k^d + c
z'_{k+1} = d·z_k^(d−1)·z'_k + 1        z'_0 = 0
Lambda   = prod_k  d·z_k^(d−1)
A        = Lambda^(1/(d−1)) · P_n'(c_0)
```
⇒ window scale ≈ 1/|A| (identity locked by test, two routes), orientation ≈ −arg A (mod 2π/(d−1) — an ambiguity; pick a branch and record it), required mpmath dps from log₁₀|A| + guard digits, and an a-priori f64 pixel-spacing wall predictor.
- **★ The naïve degree-2 λ² law under-sizes the d≥3 atom by 4–2497× — do not reintroduce.** The `(d−1)`-th root damps |A| growth with period. ⚠ A statement about the FORMULA, not a measured population effect — see the degree confounds (fractal-discovery) before predicting availability.
- **★ The `A` feasibility cut is a safety rail, not a selector** — admit iff predicted f64 pixel-spacing margin ≥ 1 decade at deploy. In production walking it has NEVER bound — the walk's material sits 7.5–8.5 decades above the wall.
- **★★ Divergence abort in `dcf.newton_nucleus` [code: tools/sourcing/test_newton_divergence_abort.py]:** feasibility bound `mag(z_p) > 4·(1/ln2)·(max_steps−it)` — DERIVED (far-field Newton sheds one nat/step; measured slope −0.434 on both populations), never fitted from a capped replay. Zero lost convergers on five populations incl. the roster grid (keys via `snapped_dedup_key` — literal round-trip was never true); burners abort at ~2% of old cost. **Production `NEWTON_STEPS=600`** (60 discarded 18.8% of findable nuclei). A flat magnitude bound or a step-shrink test loses real convergers — do not reintroduce either. Precision is a non-lever (dps 60→20 = 1.22×; mpmath dispatch-bound).

## DEEP RENDER TIER — PROVEN, PARKED [spec → `docs/design/deep_zoom_sourcing.md`]
Perturbation + Zhuoran rebasing to ~3×10²⁰, deg-2 Mandelbrot only; auto-switch `PERTURB_SPACING=1e-13`; the 1e-9 search floor is POLICY, liftable. **It renders but cannot SCORE** — `--dump-field` is f64-only and emission is f64 ⇒ a deep location is not a candidate. Revive in order: floatexp delta type → deep field path → BLA/glitch. ⚠ The unparking case is a TAIL (blocks only above log₁₀|A| 11.79), not the once-claimed fifth of supply.

## MACHINE GUARDS
- **Canaries: regenerate the list with `pytest --collect-only` — don't carry it.** Only the non-obvious survive here: `test_q4_screen_parity` (synthetic field + real model, survives corpus wipe) · `field_gating_matches_ungated` (differential) · `test_the_enumeration_is_not_stamped_with_a_cap_policy` (negative-space, pins the exact key set) · `tests/occupancy.rs` (fraction-of-TILES, strict `>` at floor 0.0 vs `guided_descend`'s `<` cull).
- **Byte-identity bites in exactly two places** — the field-cache key and the Rust↔Python LUT; everywhere else, functional parity on the OUTPUT DECISION.
- **Round-trip identity:** all stamped batches rebuild byte-perfect (Guard B), incl. the full phoenix `(c,p,z₋₁)` stamp; `test_deploy_transform_parity.py` pins the deploy transform bit-for-bit.
- Suite cost record → `docs/design/pytest_suite_cost.md`.
