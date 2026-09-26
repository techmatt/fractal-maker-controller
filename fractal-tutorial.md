# fractal-tutorial — the active repo (fractal-wallpapers) & the website

Changes when: fractal-wallpapers or website work. This doc owns DECISIONS, CAVEATS and POINTERS only. **Every mechanic has a README home: grep the repo with `git grep` (never `grep -r`, because `artifacts/` is 400k files) rather than asking.** Rewritten wholesale at ckpt 142: §Mode policy, §The mining loop and §Caveats moved verbatim to `preserve\mining_laws.md`, which is read before any mining prompt; history narration was cut.

Homes:
- Selection → `preserve\solver_design.md`, `preserve\selection_design.md`.
- Curation → `curation/README.md` (stores) · `GALLERY.md` (solve, augment, records, ceilings, the colour rule, mode policy, kit costs) · `LEGS.md` (legs, rosters, the reopen inventory) · `MEASUREMENTS.md` (every rate).
- Tests → `CLAUDE.md` + `tests/README.md`.
- Closed rulings → `preserve\rulings_*.md`. Parked → `preserve\parked.md`.
- Render truths → fractal-engine.

## THE REPO — `fractal-wallpapers` (PUBLIC on Matt's GitHub)
- **What it is:** one "make me N wallpapers" pipeline (source → score → colorize → select → full-res), plus render/explore entry points, pretrained judges, training scripts and flat labels. Rust+Python, and the tree is LOCKED [`test_cli.py`; `test_history_purity.py`]. **Rust makes every pixel; Python never renders.**
- **Four heads ship in-repo:** location · **render** (the one judge) · palette · **`gallery_grade`** (`p_fine`, a k=3 fp16 ensemble), plus the `spiral` probe. **On the site they are the location, wallpaper, palette, and gallery judges (Matt, ckpt 148):** `render` is the wallpaper judge and `gallery_grade` the gallery judge; "render judge" no longer appears in reader-facing prose.
  - **★ One dated release tag holds all four (`weights-2026-09-14`), and a published tag is never moved.** A change cuts a new dated tag. `roster.TAG` is the one spelling.
- **★ `CLAUDE.md` IS THE STANDING CONTRACT AND IS RULES ONLY (Matt).** It covers report shape (tests appear only for an unfixed red), README promotion, the lanes, one pool-holding process per box, the artifacts policy, backgrounding and the commit gate. Prompts never restate any of it.
- **Every nested verb is a real argparse subparser,** so a misplaced flag exits 2 rather than being silently dropped. The CLI is six modules under `cli/`.
- **Storage tiers:** C: = HOT, `E:\FractalStorage` = ARCHIVE. `paths.Tiers.resolve` is the one resolver, and the unit of tiering is a top-level name. `renders/` is ARCHIVED.
- **Ten Durables** (→ `src/fractal_wallpapers/README.md`). Only three are `durables.guarded()`. `hunt/frames.jsonl` has no rebuild.
- **A picture without a ledger row is garbage:** `curate candidate-ledger orphans`.
- **★ The binary `ALLOWLIST` is Matt's to grant.** `examples/` holds the README's thumbnail strip; each entry is tracked, an image, and under 128 KiB (→ `examples/README.md`). ⚠ There is no `docs/` tree, and the README says so.
- **★ Training is deterministic or it says so.** The shipped gallery-grade corpus is tracked at `data/gallery_grade/corpus/twelve_sheets/`. ⚠ JPEG floor trap → `models/README.md`.

## Selection — the solve
- **★ THREE PHASES, STRICTLY ORDERED (Matt); THE LAST GATE IS THE SOLVE.** `curate solve run` is the one selection leg at every n: seed → 1-swap → augmenting chains → 1-swap → record. Read `preserve\solver_design.md` before touching `view.py`, `rules.py`, `solve.py` or `augment.py`.
- **★ Mining owns scoring; selection reads scores off rows and never re-scores.**
  - The recipe key derives through `renders.spec_of` (minus `output` and `colormap_dir`) plus the autolevel band's sha. `candidate_ledger` is a package.
  - **★ A judge flip empties the pool.** Adoption, floor refit and a full rescore are ONE act (→ `preserve\judge_training.md`).
- **★ One spelling per rule, one objective, one `Demand` type.** The strict tier order is: filled → floor shortfall → worst seated → sum. Read `mode_floors` off the record, never a weight.
- **★ Set constraints are counted against seats filled, so they bind DURING the walk:** the spiral cap, the per-mode ceilings (`threads`) and the palette group cap. Values and flags → `GALLERY.md`, fractal-state. ⚠ A record predating a field cannot say whether it ran under it; never mix such groups.
- **★ The view may narrow alternates, never reach.**
- **Diversity is two rules:** neutral pre-selection distinctness, and the pixel-cloud twin test at `TAU` (→ fractal-discovery §What binds). **★ There is no colour term in the rank key (Matt).**
  - The colour ceiling and floor are one arithmetic, Matt's, and the one colour constraint (→ `GALLERY.md`, `ceiling.py`).
  - The allowance counts MEMBERSHIPS, not seats.
  - Nothing in the tree answers *which colours is the collection short of*.
- **★ Locations are cumulative, candidates per-pass. ★ One seat per location is permanent.**
- **Verbs:** `curate solve run · record · browse · resolve · list · viewers · recipes` and `curate pins resolve`.
  - `--themed CELL` names a codebook cell; the family pass is `--collection`.
  - Records, recipes, the keep list and publishing → `GALLERY.md`, `tentative.py`, fractal-state §RECORDS.
  - `index.html` is never tracked.
  - The pool-view door (`solve.solve(candidates=…, explain=…)`) is how "what did leg X buy" is asked.
  - ⚠ `data/curation/release/gallery1…4` is LIVE; every pool reader reads it.

## Gates and geometry
- **★ Two stacked gates.** `headroom.bars` gates the POOL per mode (`P(≥4) ≥ 0.50`, falling back to `P(≥3)`). The solve's `fine_bar` then acts over the whole pool (→ fractal-state §THE BAR).
  - Bars derive at read time.
  - Unfilled beats padded, and the bar outranks the guarantee.
  - `--explain-seats-of NAME` writes per-key refusal reasons.
- **Geometry:** the design phase is 1280×720 ss2, and phase 3 is 2560×1440 ss4. A tentative record never renders. The votes kit → fractal-corpus.

## Caveats that would cause a misread
- **No head ever scores the wallpaper that ships.** Judges read the 640×360 candidate, while a release row is a cold render with autolevel inside it.
- **⚠ A seat's `mode` in `gallery.jsonl` is ROUTED; render at `recipe["mode"]`.** Seats count routed, recipes count drawn.
- **⚠ The rank key reads `flatness`,** so every seating is busier than the pool. This is intentional.
- **⚠ Box memory is commit charge and leaks** (`tests/README.md`). There is one pool per box across repos. A prompt that stops a leg kills its own workers by pid.

## THE ARTICLE & SITE — `C:\Code\fractal-website`
The repo owns its own rules: website `CLAUDE.md`, `builder/README.md`, `docs/page-review.md`, `explorer/README.md` and `explorer/perturb-wasm/README.md`. **Cite them; never restate them here, and keep no per-page list of any kind.**
- **★ Editorial authority is `prose\writing-guidance.md`** (with website `CLAUDE.md`). It sits outside the repo on purpose.
- **Prose path:** Claude drafts a wholesale master → `prose\` → a PLACE prompt places it verbatim. A superseded master is trashed.
- **★ The site is LIVE BUT UNADVERTISED (ckpt 152)** at `techmatt.github.io/fractals/` (repo `techmatt/fractals`; the local folder stays `C:\Code\fractal-website`). Until Matt advertises it, it never needs preserving or keeping in sync. He reviews from the site. Outdated figures and prose are not refreshed until "ready for publishing".
- The wasm lock and the pool-adjacent `builder check` → fractal-operating §ONE COMMIT AT A TIME.

## WORKFLOW
- Prompts go to Drive `prompts\` (→ fractal-operating) with a TARGET-REPO guard.
- `C:\Code\fractal-maker` is the read-only archive.
- State the NEW names for whatever a prompt moves, and verify from source over these docs.
- A line number is never a citation anchor.
