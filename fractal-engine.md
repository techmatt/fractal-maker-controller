# fractal-engine — render truths that outlive any renderer

The live engine is the `fractal-engine` crate in fractal-wallpapers.
- **Its canon is `engine/README.md`**: per-family behaviour, symmetry, `fractional_multibrot`, mirror-fold, specialization and perf, the wasm build and the palette bake.
- The crate's own docs (`mode.rs`) own the modulate mechanics.
- fractal-maker is a closed archive, and porting is over.
- Every ★ below is enforced, and the guard is the memory: grep the cited test, don't re-argue.
- Rewritten wholesale at ckpt 142 as verdicts and pointers. The f64 precision audit moved to `preserve\deep_shelf.md`.

## Rules a future session must not get wrong
- **★ Never gate on clip share; use in-mask chroma** (→ `engine/README.md §The direct traps`). UF shape names do not transfer by name.
- **★ Every renderer draws the same picture for the same recipe.** There is one builder (`release.task_for`, `engine_spec.spec_of`), guarded by `tests/test_renderer_agreement.py`. A new spec site goes through the builder, never through a longer keyword list.
- **★ A coloring field spelled flat on a manifest row is legitimate** (→ wallpapers `README.md §One shape for a place`).
- **★ Identity:**
  - Any new field-side render axis must enter the field-cache/replay identity key; a variant through `mode_params` needs none.
  - New serialized fields `skip_serializing_if` their default, or every cached picture renames.
  - Every `KEYED` member reaches the digest (`recipes._KEYED_THROUGH`).
  - ⚠ `renders.job_name` is NOT a durable identity: it digests the checkout path. Never pin it in a test.
- **★ Levelling is decided once and replayed upward.** Nothing entered identity except the band sha in `recipes.KEYED`. Re-derivation is faithful.
  - The replay and derivation halves live in the website's `explorer/engine-wasm/src/level.rs`.
  - ⚠ The engine's `coloring::percentile` is nearest-rank, while the operator uses numpy linear interpolation; they cannot be swapped.
  - Owner → wallpapers `curation/README.md §Levelling is decided once and replayed upward`. `.leveled/` → `preserve\leveled_identity.md`.
- **★ The field is dumpable, and a recolour is byte-identical to a render.** Composites, direct traps and the angle modes cannot dump. `colorize.render` refuses a curve override together with a fields directory, and that refusal is correct.
- **★ The engine build is the fifth pin** (`identity.enforce`, `drawn_by.jsonl`, `test_engine_fingerprint.py`).
  - A new mode is invisible to the identity digest; `mode_policy.check` is what trips.
  - Scores overlay `score_amendments.jsonl` via `intake.read_scores`; never open the sidecar directly.
- **★ The home view is a Rust constant:** `Family::home_view()`.
  - Python's one door is `engine.home_view(family)`. The explorer asks `engine.wasm` `plan().home`, and there is no JS table.
  - `Multibrot { degree }` covers degrees 3–6.
  - Adding a degree means one engine cap, one box, and one-line lists in both repos. Enumerate them from source; never from this doc.
- **★ There are two shipped modulates.** The catalogue has 20 modes, 19 of them production; standings live in `MODE_POLICY`.
- **★ The palette is a render axis:** `Palette.phase` and `cycles`, both keyed.
  - `mirror` is a bake and `cycles` an index, and they multiply.
  - The axis is a byte-for-byte no-op on the four direct traps.
  - Adding maps never moves an existing bake.
  - `scale` (leveled | absolute), `lambda` (Box–Cox, before the stretch) and `period` (ckpt 143) are EXPLORER-ONLY keys, omitted at default and never emitted by the pipeline's key whitelist (→ `engine/README.md`).
- **★ A flat texture is smooth-with-rank** (`mode_policy.routed_mode`). `data/coloring/texture_flat.jsonl` is a tracked register with geometry in the key.
- **★ The direct traps:**
  - `direct_trap_multiply` whitewashes because it is read through sRGB. Fixes are mode-param variants, never engine edits (→ `engine/README.md`).
  - `threshold` is an absolute iterate-plane distance, unnormalised against `maxiter`.
  - In the angle modes, `weight` is an AMPLITUDE mix, drawn per candidate since 2026-09-18 (the default is 0.85).
- **★ An explicit iteration cap is keyed end to end, EXCEPT at `expand.rs`'s `Node` and the shallow link.** That is why parabolic aiming below ε ≈ 3e-3 is untested (fractal-state OPEN 8).
  - `maxiter::for_width` reads the width only. Above the cap a sample is painted interior, so two caps are two pictures.
  - `pins.query_of` is the recipe→link writer.
- **★ `Family::PhoenixM` (`phoenix_m`; explorer name `phoenix_plane`).** At p = 0 it is the Mandelbrot set. It is not mined. ⚠ The classic Ushiki c = 0.5667 lies just OUTSIDE the p = −0.5 filled set.
- **★ Zero-behaviour is not bytes alone:** time the three anchors as well as hashing them. An enum arm once pushed `Family::step` past LLVM's inline threshold and doubled the Mandelbrot anchor.
- **Heuristics:**
  - Production mirrors non-cyclic maps; treat that as a suspect, but check before assuming.
  - Genericity, not multiplicity, is the perf trap, and family spread dwarfs mode spread (live numbers → website `explorer/README.md §Measured`).
  - Compare maps by sampling through the bake; `data/palettes` never stores the table size.
  - `release.Task` carries `mode_params`, `curve` and `palette`. Time a render pilot in seat order.
- **The f64 floor is relative** (`RESOLUTION_ULPS` 4), and failure is clean-then-refused. The full audit → `preserve\deep_shelf.md`.
- **★ A spec render may opt out of the f64 refusal** with `"allow_unresolvable_in_f64": true` (ckpt 144). This applies to spec renders only: the pipeline never emits it, it enters no identity, and the tile path keeps its refusal. It exists for §Deep zoom's f64-versus-perturbation figure (→ `engine/README.md`).

## Deep render — the single home for deep/depth
- **DEEP (perturbation) is EXPLORER-ONLY:** the website's `explorer/perturb-wasm` crate plus the Deep tab. Nothing deep enters the pipeline (Matt).
  - Its kernel, oracle, per-degree speeds, calibration, minibrots at degree d, link v3 and the closed verdicts (fractional degrees; Phoenix at depth) are owned by `explorer/perturb-wasm/README.md` and `explorer/README.md`.
  - Its traps (rebuild the native exe; any `perturb-wasm` edit is a rebake) are in website `CLAUDE.md`.
  - **★ BLA was built, measured and removed; do not rebuild it.**
  - **★ `cap::CEILING` = 1,000,000 binds on degree-6 near-parabolic frames; RULED keep.**
- **DEPTH (the f64 pipeline) stays SHELVED.** ⚠ In wallpapers, `deep/` and `cli/deep_commands.py` are DEPTH; the perturbation kernel is named `perturb`.
- **Un-shelving DEPTH, or any entry of deep pictures into the pipeline,** reads:
  - `preserve\deep_shelf.md`
  - `preserve\perturb_seam_audit.md`
  - `preserve\sourcing_measurements.md`
  - wallpapers `deep/README.md`
