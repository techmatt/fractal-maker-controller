# fractal-state — checkpoint 164 (2026-10-15: Find minibrots always finds a copy, with progressive previews and dives that widen; Deep zoom v5 prose)

## Where we are
Three phases, each depending strictly on the one before (→ fractal-discovery). Matt iterates from pictures, not counts. Phase 3 is his eye on the final seating, and **every planned collection has a viewer at its official size.**

**★ MINING IS CLOSED (Matt, 2026-09-21) UNTIL HE REOPENS IT.**
- The pool as merged on 2026-09-21 is the population, and the `final139_*` solves (§RECORDS) are the published galleries.
- On a reopen, read `preserve\mining_laws.md` whole, then wallpapers `curation/LEGS.md §Mining is CLOSED (2026-09-21) — reopen inventory`. State carries none of it.
- ⚠ A reopened mine reads most pool pictures from the E: mirror (§RETENTION AND STORAGE).
- ⚠ Before 2026-09-26, `headroom.population` never passed spiral scores to the solve, so every `curate headroom` census and `pool_draw` reading taken before then counted spiral places as uncapped. Production solves were never affected. Retake any such census before relying on it.
- ⚠ Since ckpt 161 a mixed `harvest` behaves differently on degree 6: it draws viewport-sampler roots by default, and the degree-6 pair is capped at a tenth of the walk (→ `curation/LEGS.md`). A reader's toy run in a fresh clone is not a reopen.
- ⚠ **740 graded rows lost their `.leveled/` colormaps in the tier move to E:** (a local-only wallpapers red that CI skips). Left alone while mining is closed (Matt, ckpt 163).

**★ EVERY COLLECTION HAS A TARGET, IN `curation/targets.py`: NINETEEN COLLECTIONS, TWELVE FAMILIES AND SEVEN MODES.**
- Reached by `curate solve run --collection NAME`; `--n` overrides; a collection with no target REFUSES.
- ⚠ The general gallery's size is `tentative.RECORDED_SEATS` (1,000), not a `targets.py` entry.
- The website's `builder/seats.py` hand-lists the collections.

**★ ⚠ GALLERY SIZE IS MATT'S DECISION ALONE.** Never raise it, queue it, or reason about shrinking `n`. `final140_general2000` (n=2000) is offered on the site beside the n=1000 default.

**★ "TRULY FINALIZED" IS COMPLETE (ckpt 157).** The twenty-one records are tracked and published, and both repos' histories were rewritten (§THE REPO AS A CLONE SEES IT). Any further publishing is Matt's to raise.

**★ PINNED SEATS.** `data/curation/pins.txt` → `curate pins resolve` → `pins.json`: ten pins, seated before the seed and prune-proof (→ `curation/GALLERY.md §Pinned seats`).

**★ THE BAR: `DEFAULT_FINE_BAR = 0.030242` ON THE FINE COLUMN**, under `fine_head = twelve_sheets_drop_high_asymmetric_auc_ge4_more_k3`.
- ⚠ A bar is unreadable without its head.
- ⚠ 0.50 is NOT the seating bar: `solve.Q4_BAR = 0.50` is the render judge's constant on `p_ge4`.
- `p_fine` is the fine head's column, where the bar lives: THE quality reading. On the site: the location, wallpaper, palette and gallery judges.
- **`p_fine`, `p_coarse` and the bars are closed (Matt, 2026-09-12).**
- **A forced fill exists for early pools (ckpt 161):** it seats past the pool gate and the fine bar, it is stamped on its record, and a forced record can never be published (→ `curation/GALLERY.md`, wallpapers `README.md`).

**★ THE HUMAN VETO IS SHIPPED** (→ `curation/README.md`): Matt marks ONLY `1`s; an unmarked tile is not a label.

**★ A THEMED PASS RELAXES THE BAR INSIDE ITS OWN CELL** (`solve.themed_fine_bar`). ⚠ `--themed CELL` names a codebook cell; the family pass is `--collection <family>`.

**★ FAMILY PASSES FLOOR AT `mode_policy.seat_floors(n)`; A MODE PASS FLOORS AT 0.** ⚠ The floor is not monotone.

**★ COLOUR:** a hue family is not the union of its four cells (→ `palettes/README.md`). Curation constrains the 48 coloured cells only. The palette group cap is `0.075·n` themed and `0.025·n` general. K is Matt's; Claude never proposes reopening K.

**★ A GALLERY PAGE IS PRESENTED STRATIFIED** (`curation/page_order.py`). **★ GUARD RULINGS: loosening only; one loosened, accepted by Matt at ckpt 161** — the website's `builder check` `endings` check now flags only a file whose committed line endings differ from its endings on disk. **★ `pool_scores.jsonl` IS ONE-SHOT: mine → merge → `gallery-grade score-pool` → solve.**

## THE READER PATH (ckpt 161)
- **★ A new reader can clone, install with or without CUDA, and walk the whole chain** — render, install check, walk, mine, gallery — from the top wallpapers `README.md` alone. This was proven by fresh clones on this box in both installs, and at ckpt 163 on a second Windows laptop. Linux and macOS are left to CI.
- **★ Windows builds use MSVC** (README since ckpt 163): a GNU-toolchain engine passes `judges check` but runs up to 17× slower.
- **★ EVERY LOOK AT INTERMEDIATE STATE IS A WALLPAPERS COMMAND (Matt):** each writes a parseable file and a plain page drawn from it, and one `walkthrough` command exports them all as a small self-contained folder. The website hosts those pages unchanged and builds no visualization of its own.
- **Homes:** the path and the cost table → wallpapers `README.md`; every file a reader inspects → `FORMATS.md`; the hosted page → website `builder/README.md`. The cost table lives in the README only (Matt).
- **The page** is "Run the pipeline yourself" at `tools-and-data/run-it-yourself/`. It sits out of the rail and the header and is linked by one sentence from Tools and data. Its text was authored in the placing prompts and lives in the website builder, with no prose master.
- **The sample it shows** is a ten-minute walk and a ten-minute mine, with a forced twelve-seat gallery recorded after a further five-minute mine. Its imported files are tracked, so the page rebuilds without any clone.

## THE DEEP TAB (ckpts 162–164)
Render truths, the kernel's home and the rulings → fractal-engine §Deep render. Numbers and mechanics → website `explorer/README.md`.
- **★ ONE CPU PICTURE KERNEL, IN WALLPAPERS `perturbation/` (ckpt 163).** `render-link` draws Deep links through it, and the website's `perturb-wasm` wraps it. Every core-kernel edit locks both repos and rebakes.
- **★ THE GPU BOX IS OPT-IN AND OFF BY DEFAULT (Matt, ckpt 163),** remembered per browser and never written into a link.
  - With it ticked, the final frame and downloads draw on the GPU where the self-test passes.
  - Pictures may differ slightly between machines, never between arrival paths on one machine.
- **The second GPU (Intel Arc 140V iGPU, ckpt 163):** every agreement and recovery gate passed, with zero driver resets. It was slower than the CPU on the 159-frame sample and on downloads, and faster only on very deep, heavy frames. Its cold GPU-ready took about 22 s, against the 30 s settle bound.
- **The main box's 22 display-driver resets are [inferred] specific to its card or driver; the question is CLOSED (Matt, ckpt 163).**
- **★ FIND MINIBROTS ALWAYS FINDS A COPY (ckpt 164; owner `explorer/README.md`, code `explorer/deep.js`).**
  - It searches inside the view first, up to a period budget. When the view's atom domain belongs to a larger copy and nothing else is found, it widens ×4 a step around the centre, and the status line says the result is outside the view.
  - Previews draw one at a time, largest first, each with the whole pool. Each shows its own progress and time left, and a "Previews: n of m" count runs beside the list.
  - A tile whose cap holds fewer than 6 periods of its copy (`PREVIEW_PERIODS`, set from pictures) is not drawn: it reads "too deep to preview" and stays clickable.
  - A FRESH dive press that `dive::pick` refuses for every listed copy widens outward to the nearest copy it can land on. A press continuing a chain keeps its refusal.
  - At deep, heavy views that landing can be wider than the view: the centre landing needs 32 periods under the 2M ceiling. That limit is the parked-chains wall, not a bug.
  - **A per-place cache for Keep diving retries is DECLINED (Matt, ckpt 164).**
- **Behaviour from ckpts 162–163, owned by `explorer/README.md`:**
  - Double-single BLA on the GPU path, with exact orbit points.
  - The quarter pass on the GPU by an iteration census.
  - A frame waits for the self-test outcome.
  - A lost device recovers without ever mixing kernels in one frame.
  - Background kernel compiles.
  - `retire()` as the one eviction path.
  - Leaving a page releases the device, so those pages leave the back/forward cache.
  - SIMD with a scalar fallback for old Safari.
- **The shallow tab** stopped re-laying-out its 1,000 gallery tiles on every frame (`.tiles` and `.browse-tiles` use `flex: 1 1 0`).

## MODES, PHASE, PALETTE
- **★ Seven targeted-gallery modes.** `curvature` is `UNMINED`.
- **★ The explorer's render-mode roster is thirteen** (`listedModes()`). **★ It shows ENGINE NAMES** for modes and families, and the article teaches the same names.
- **★ Exponential smoothing reads as "smooth" on the site**; recipes keep `exp_smoothing`.
- **★ Texture weight, rotation and phase are CLOSED; palette replication is PARKED.** `data/palettes/palettes_for_random_choice.csv` (232 maps) is the approved-for-random list.
- **★ The palette modes `scale`, `lambda`, `period` and `knee` are EXPLORER-ONLY** (→ fractal-engine).
- **★ STRAIGHTEN ITER (`knee`):** on by default for new absolute work in the explorer. A link without `knee` is off, so every older link draws as before.
- ⚠ A seat's `mode` in `gallery.jsonl` is ROUTED; render at `recipe["mode"]`.

## TONE CURVES AND LINKS
- **★ Every gallery seat's tone curve is recorded** (`artifacts/curation/autolevel_backfill.jsonl`).
- **★ THE LINK CONTRACT** (owner: website `explorer/README.md`) spells `curve` and `knee`. Wallpapers `explorer_link.query_of` writes links byte for byte like the site. The engine's `link.rs` reads `curve` and a stated `scale=leveled`.
- **★ A DEEP COORDINATE MAY BE 128 CHARACTERS (ckpt 162);** shallow links keep 64 (→ fractal-engine).
- **★ A Phoenix recipe that omits `c` or `p` means the classic constants, never zero.** The website's `links.py` spells `phoenix_m` as `phoenix_plane` with its constants.
- **★ A LINK IS A PICTURE**, proven across every tab, mode and family by `explorer/bench/link-fidelity.mjs` (a browser harness, not in `builder check`), with a depth tab at 1e-60 to 1e-110. It proves the CPU path; GPU-versus-CPU agreement is `bench/deep-gpu-agree.mjs`.
- **★ Filigree's gallery link states its colour (Matt, ckpt 163)**, so its tile and its click draw the same picture.
- **★ Seat-addressed figure panels carry the cap** whenever it differs from the policy; `builder check`'s `caps` check holds them.

## FULL-RESOLUTION WALLPAPERS AND PACKS
- **★ THE FULL SET:** 6,299 pictures at 2560×1440 ss3, JPEG q95 4:4:4, in `E:\Fractals\FractalWallpapers\full\` with `membership.jsonl`. `curation/full_set.REGIME` is the one spelling. Every file carries its explorer link.
- **★ THE PACKS: 19 zips in release `wallpapers-2026-09-29`** on `techmatt/fractals`, all digest-verified against the local zips on 2026-10-01. The site downloads through `releases/latest/download/<file>`. The upload procedure (one asset at a time, verify by digest) is owned by website `builder/README.md`. The next full rebuild may cut a new dated release with all 19.
  - **Best 30, 100 and 200:** the staged vote ranking, plus Matt's preview picks forced in even from outside the thousand (`wallpaper-packs/preview-picks.json`). They nest, and Best 200 sits in part 1.
  - **The main gallery, three parts:** the thousand plus every hand-pick from outside it, in rank order. The explorer's gallery stays exactly the thousand.
  - **Twelve colour packs,** each in its own staged order.
  - **The deep gallery:** hand-picked deep views rendered site-side by the native deep renderer. Recipes: `builder/data/deep-pack.jsonl`. Deep pictures never enter the pipeline.
  - **Not shipped:** n=2000 and the mode collections.
- **★ THE RANKING:** summed votes, one per voter per seat; ties fall to the seeded plan's order (→ website `builder/README.md`).
- **★ PACK PREVIEWS:**
  - **Best 30, 100 and 200 and the main gallery** show Matt's hand picks.
  - **The colour packs** use the voted-only walk: nothing shown elsewhere on the site, at most two per hue family. A change to what the site shows therefore moves them, and `builder packs --import` re-runs the walk.
  - **The deep gallery's five** are a seeded draw.
- **★ The wallpapers are licensed CC BY 4.0, credit Matt Fisher.** Both repos' code stays MIT.
- **★ An iteration cap was checked on a shipped picture (ckpt 162) and is not the problem:** general #71 drew identically at 64× its cap; what looked off was colouring. No re-render of the set is owed.
- **★ FRIEND VOTES:**
  - **The store** is `C:\Code\fractal-drive-sync\votes\events.jsonl`: append-only, never in a repo, and losing it is a major failure.
  - **Ingest:** Matt says "ingest NAME <links or files>" to CC in fractal-website; `builder votes browse` regenerates the browser.
  - **★ The votes are sufficient for now (Matt, ckpt 159).** A pack rebuild (stage → plan → zips → upload) happens only when Matt decides enough new votes have arrived; it is never proposed.

## ZOOM VIDEOS
- **★ Four videos, all PUBLIC on YouTube (Matt, 2026-10-01), all embedded on Deep zoom videos:**
  - Double Descent (`MgmOF7Q-YIA`).
  - The seahorse descent (`N_041iZNHvQ`).
  - The julia3 descent (`GcJnRBlqSHw`).
  - The multibrot3 descent (`zYHpYwFDQbM`, section "A degree-3 Mandelbrot set spiral").
- **★ KNEE IS THE CODE DEFAULT FOR VIDEOS:** `zoom.py` takes knee when no `--mapping` is given; an explicit mapping still wins. Owner: website `builder/README.md`. The knee has one home, the engine's `coloring.rs`.
- **★ Every video gets Midway and Final frame links** through its own `go/` redirects, and new videos are prototyped on the `preview` variant before the 4K render.
- `builder descent --direct` takes a single Multibrot link as one stage; without it, a single Multibrot link is read as a twin chain.

## THE SHOWCASE VIDEO
Parked by Matt at ckpt 162 as not relevant now. Demo mode and the tour script `explorer/bench/showcase.mjs` stay committed (owner website `explorer/README.md §Demo mode`); a take is one command.

## THE PAGE OF DIVES AND THEIR JULIA SETS (ckpt 160)
- **★ Published at `deep-zoom/dives-and-julia-sets/`** and linked by one sentence at the end of Deep zoom's Random dives passage. It stays out of the rail and the header and has no text beyond section headings and two controls (Fixed / Random coloring; Show Julia twin).
- **What it holds:**
  - About 500 existing random dives that land on a gallery view placed inside a minibrot: the location judge's top picks per degree (200 / 100 / 100 / 50 / 50 for degrees 2–6).
  - The Deep zoom figure's panels and the deep gallery, forced in.
  - Each has a Julia twin at its centre.
- **★ "Carried" is internal shorthand for that landing kind and never appears in reader-facing text.**
- **★ The twin's rules (Matt):** a twin with a central black disk is zoomed out until the disk is about 5% of the frame's width, never to the whole Julia set. Every twin is coloured by a fresh absolute fit on its own field, palette kept.
- **★ Its images are tracked (Matt's ruling; about 100 MB)** so the page loads fast.
- **It rebuilds from the record alone:** `builder/data/julia-dives-picks.jsonl` and `python -m builder.julia_dives page` (→ website `builder/README.md`). A recolour is a re-render.

## START HERE AND OTHER FIGURES
- **★ The pink picks are Matt's daughter's twelve**, placed at seed 20260930 from her full list (`article/pink-gallery.jsonl`); a re-pick is a new `chosen` line.
- **★ Start here's gallery figure is a seeded draw from the voted leftovers** (seed 1). `builder start start-gallery --replace --gallery-seed N` redraws it; a new vote never moves it.
- **★ A figure panel may show another artist's work** under a CC license that allows non-commercial sharing, credited and linked (the rule is in website `CLAUDE.md`).
- **★ On phones (ckpt 159):** the twelve `modes-*` sheets swap to a 640-wide version below 30rem, and repeated taps on overlapping atlas marks step through the pile.

## LAWS STATE STILL CARRIES
- **★ The degree-6 plane is never labelled** (`partitions.NEVER_LABELLED`).
- **★ Parabolic Julia sets are CLOSED (ckpt 147); Douady–Hubbard tuning is PARKED (ckpt 148).**
- **★ Structured deep dives are CLOSED AND PARKED (Matt, ckpt 160)** (→ `preserve\parked.md`, fractal-engine §Deep render).

## RETENTION AND STORAGE
- **★ Everything fractal on E: lives under `E:\Fractals\`:** `FractalStorage\` (the ARCHIVE tier), `FractalWallpapers\` and `history_undo_ckpt157\`. Every older `E:\FractalStorage` or `E:\FractalWallpapers` spelling is dead.
- **★ The keep is five per `(place, mode)` plus one family allowance** (→ `curation/README.md`). Pinned rows and every kept record's seats are prune-proof via `tentative.kept()`.
- **★ THE POOL PICTURES LIVE ON THE E: MIRROR (ckpt 158).** A pool picture name resolves from C: first, then from the archive's `pool_pictures/` mirror. It raises `ArchiveUnreachable` when E: is configured but absent (→ `picture_mirror.py`, `storage pictures`, website `builder/README.md`).
  - Kept seats and protected rows stayed on C:, as did 56 pictures behind website figures.
  - ⚠ Retraining `gallery_grade` needs its pictures restored to C: first (`require_hot`); most of its corpus is on E:.
- **Behind junctions to E::** `C:\Code\fractal-maker` and the website's video trees (`deep-zoom`, `double-descent`, `julia3-descent`, `multibrot3-descent`).

## RECORDS: THE PUBLISHED SET
- **★ The published store is exactly twenty-one records:** the twenty `final139_*` and `final140_general2000`, tracked whole.
- **★ `curate solve record` KEEPS BY DEFAULT since ckpt 161 (Matt):** kept records are data (`tentative/keep.jsonl`), released with `curate solve release`; a measurement solve records with `--no-keep`.
- `portable.GENERAL_CHECK` = `final139_general`; `portable.REFERENCE` = `final139_green`. Nothing is re-cut while the pool is closed.
- **★ BACKUPS ARE MATT'S.** `storage export` runs only at his direction and is never proposed.
- **★ `git grep <stamp>` before calling any record stray.**

## THE REPO AS A CLONE SEES IT
- **★ BOTH HISTORIES WERE REWRITTEN (ckpt 157).**
  - Tags were re-pointed ONCE, to tree-equivalent commits; the never-move rule holds again.
  - A tag is never deleted and recreated, because that drops its release to a draft.
  - `E:\Fractals\history_undo_ckpt157\` holds the undo mirrors, the commit maps, and the only copy of the first location judge's weights. Matt keeps it.
- **★ ONE PIN: the website's `explorer/engine.manifest.json` `wallpapers_commit` pins engine.wasm AND both perturb modules (perturb manifest schema 3, ckpt 163).** Website CI checks out wallpapers at it.
  - **★ The pin follows the bytes:** `builder explorer` moves it only when engine.wasm's bytes or `perturbation/` changed (→ website `explorer/README.md`).
  - The bake sets `RUSTUP_TOOLCHAIN=1.96.0` itself and refuses any other toolchain; stable rustc no longer reproduces the committed modules.
  - ⚠ The perturb modules reproduce only at the same checkout paths, and a rebake through a junction moves the bytes. Rebake from a real path.
  - ⚠ `--perturb`, `deep-gallery-native` and `deep-gpu-model` need the sibling wallpapers checkout.
  - ⚠ The `build.rs` files in the wasm wrapper crates are empty stubs: deleting them moves all three modules' bytes.
- **★ A fresh box continues every stage from a `storage export` alone** (→ `preserve\fresh_box.md`). **A fresh clone with no export starts from empty by the README's path** (§THE READER PATH); a configured `builder check` on one skips the artifact-dependent checks as `NO_ARTIFACTS`.
- **★ CUDA is opt-in.** ⚠ This box syncs `--extra cuda`. **★ Both repos build and run on Windows, Linux and macOS, and CI proves it.**
- ⚠ Drive the makers through `.venv/Scripts/fractal-wallpapers.exe`. Concurrent prompts in one checkout commit by pathspec and stage by hunk.
- **`engine.wasm` carries no local paths since ckpt 159** (`--remap-path-prefix`). Builds from different checkout paths still differ through cargo's path-dependency metadata; that is a known gap, left open (→ `explorer/README.md`).

## WEBSITE
**★ The site is LIVE AND ADVERTISED since 2026-10-01** at `techmatt.github.io/fractals/` (repo `techmatt/fractals`; the local folder stays `C:\Code\fractal-website`). **★ It need not be kept in sync (Matt, ckpt 164).** Every fact about the site is owned by the website repo:

| Topic | Owner |
|---|---|
| Explorer: tabs, Deep, Find minibrots and the dive, the GPU kernel and its box, phones, the link contract, Straighten iter, demo mode, the harnesses, the pin and the bake, measured numbers (`§Measured`) | `explorer/README.md` |
| The GPU kernel's native model and oracle, and the f32 verdicts | `explorer/deep-gpu-model/README.md` |
| The wasm wrapper, `nuclei::classify`, the twin, the chain cap rule, the low-period catalogue | `explorer/perturb-wasm/README.md` |
| The CPU picture kernel, the interior proof | wallpapers `perturbation/README.md` |
| Builder: figures (incl. credited external panels), packs, `votes`, zoom videos, Random dives, the page of dives and their Julia sets, Run the pipeline yourself, the resolver, head tags, every `builder check` check | `builder/README.md` |
| Traps, the rail rule, pathspec and hunk staging, the external-image license rule, the two-repo kernel order | `CLAUDE.md` |
| Style and voice | `prose\writing-guidance.md` · website `CLAUDE.md` |
| Per-page status | `docs/page-review.md` |

- **★ THE EXPLORER IS NAMED MANDELNAUT (Matt, ckpt 159).** On every page, the first mention of the explorer reads "Mandelnaut Explorer"; later mentions stay "the explorer".
  - The explorer's `<title>` is "Mandelnaut Explorer — Making Fractal Wallpapers" and its H1 is "Mandelnaut".
  - The rail and `go/` titles read "Mandelnaut Explorer".
  - Start here's heading stays "Fractal explorer" (its `#fractal-explorer` fragment).
  - The site manifest keeps the site's name. The "open in fractal explorer" figure mark is unchanged.
- **★ NAVIGATION:** the rail reads in three groups: Start here | Wallpaper packs, Tools and data, Deep zoom videos | Contents. The site header carries the same links.
- **★ PHONES: reasonable, not overboard.**
- **★ PALETTE CREDIT:** pages may say "palettes I made" as long as they link to Make your own palettes, which credits Claude writing them from three checked-in prompts.
- **★ Head tags** come from each page's own first sentence (`builder/heads.py`); a series is never cut at a list comma. A page with no prose carries an authored description.
- **★ A LINK IS A PICTURE. The site never tells a reader a view is "not exact." No figure reuses a picture unless the reuse is intentional. Figures are never changed because they drifted. Figure recipes are never lost.**
- **★ The site reads as its final form; the Oxford comma; American spelling; THE VOICE** (`prose\writing-guidance.md` §Voice).
- **★ Any colouring control recolours what is on screen, immediately, from the retained field (ckpt 162).**

**★ PROSE: MATT REOPENS IT PIECEMEAL, ONE PASSAGE AT A TIME.** At ckpt 164, Deep zoom's §How a deep frame is computed (second paragraph) and §Rendering speed were rewritten and placed (`Deep zoom v5.md`), with figures verified from source. The video's final frame is about 6 s on the CPU, about eighteen times Fraktaler 3's like-for-like rate; it is recorded in `explorer/README.md §Measured`.

**★ THE EXPLORER'S BAR (Matt):** complexity is a cost; text is for the artist; the left panel changes the view, the right manipulates it; the shallow view and Deep are one tool; Deep auto-renders. Wasm threads are out. ⚠ This box drifts about 30% between identical runs. ⚠ A heap reading against time measures the back/forward cache, not the page.

## IN FLIGHT ACROSS THIS BOUNDARY
Nothing.

## QUEUED IN DRIVE `prompts\`
Nothing.

## PARKED SMALL EDIT: rides the very next wallpapers prompt that regenerates `engine/fixtures/deep-cases.json`
- The embedded generator's `what` text still says a gallery link without `scale` records `rgb: null`. None does now: the refusal case is the test's own `DEEP_LINK_WITHOUT_A_SCALE` constant. Correct the sentence.

## OPEN (ordered): Matt raises each
Items 2, 3 and 6–19 are closed; the numbering is kept.
1. **Mining is CLOSED; he reopens it.**
4. **Prose reopens piecemeal (Matt).**
5. **Deploy.** **Matt tracks where the site is posted himself (ckpt 160); the docs carry no posting list.** Left: more deep zoom videos for the videos page, in the knee style.

Parked → `preserve\parked.md`.

## STATUS / KNOWN REDS
- Website `builder check`: green at ckpt 164. Both repos' CI: green on the tree as committed at ckpt 163; ckpt 164 touched only website explorer JS, CSS and READMEs.
- ⚠ Wallpapers local-only red: the 740 rows missing `.leveled/` colormaps (§Where we are; left alone).
- ⚠ A website `builder check` beside a wallpapers merge can throw a transient ledger red; retry.
- ⚠ A report just copied to Drive `reports\` can read back empty for minutes; retry once, then ask Matt to paste it.

## RULINGS THIS ERA
ckpt 164 (2026-10-15). Reported prompts, all website and all explorer JS:
- `minibrot_nearby_ckpt164`
- `place_deep_zoom_v5_ckpt164`
- `minibrot_preview_progress_ckpt164`
- `minibrot_drawable_ckpt164`
- `dive_widen_on_refusal_ckpt164`

Matt's rulings:
- **Find minibrots searches inside the view, then widens** until it finds a copy.
- **Previews are skipped below a picture-set period threshold** (6), and dives widen on refusal.
- **The live site need not be kept in sync.**
- **No per-place cache** for Keep diving retries.
- **The Deep zoom v5 rewrite is approved and placed.**

## KEEP LIST
**Drive `prompts\`:** nothing to keep. Matt wipes it himself.

**Drive `reports\`:** wipe everything.

**Drive `votes\`: DURABLE, never wiped.**

**Drive `prose\`:** the live masters:
- `Start here v2.md`, `Deep zoom v5.md`, `Wallpaper packs v1.md`, `Tools and data v1.md`, `Deep zoom videos v1.md`;
- `Overview v2.md`, `Escape-time fractals v1.md`, `Rendering fundamentals v1.md`;
- `Color palettes v7.md`, `Make your own palettes v4.md`, `Rendering modes v5.md`;
- `Training judges v7.md`, `Finding good locations v8.md`, `Finding good wallpapers v3.md`;
- `Gallery curation v2.md`, `Full pipeline v6.md`, `Fractal atlases v2.md`;
- `Other artistic techniques v1.md`, `Fractal math v2.md`;
- `writing-guidance.md`.

**Wallpapers `scratch/` and website `scratch/`:** nothing is kept in either.

**Website `artifacts/`:**
- KEEP `deep-zoom/`, `double-descent/`, `julia3-descent/` and `multibrot3-descent/` (with their E: junctions), `mathjax/`, `pool-study/`, `dive-reference/` and `deep-pack/`.
- `packs-stage/`, `votes/` and `explorer/` regenerate.
- `explorer-bench/` is sweepable.
- `cap-split/`, `random-dives/` and `pink-picker/` are sweepable.
- `temp-pics/` is Matt's.

**`E:\Fractals\`:** KEEP everything.

**Outside both repos:** `C:\Tools\fraktaler-3\` stays until Matt removes it. The rustc 1.96.0 toolchain stays.

## OWED
Nothing.

## SCRATCH/ARTIFACT FLAGS
- **★ The standing keep roster lives in the repo:** `src/fractal_wallpapers/README.md §The standing keep roster`.
- ⚠ CRLF drift is real; check with `git ls-files --eol`.

## PARKED / SETTLED
→ `preserve\INDEX.md`, which lists every file. Never re-list them here.
