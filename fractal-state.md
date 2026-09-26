# fractal-state — checkpoint 151 (2026-09-26: four section cuts placed (Finding good locations v8, Training judges v7, Color palettes v7, Rendering modes v5); the double-descent 4K60 master finished and its settings became the video baseline; engine-wasm imports the engine's levelling code)

## Where we are
Three phases, each depending strictly on the one before (→ fractal-discovery). Matt iterates from pictures, not counts. Phase 3 is his eye on the final seating, and **every planned collection has a viewer at its official size.**

**★ MINING IS CLOSED (Matt, 2026-09-21) UNTIL HE REOPENS IT.**
- The pool as merged on 2026-09-21 is the population, and the `final139_*` solves (§RECORDS) are the semi-final galleries.
- On a reopen, read `preserve\mining_laws.md` whole, then wallpapers `curation/LEGS.md §Mining is CLOSED (2026-09-21) — reopen inventory`, which lists the open arms and prices, every line citing `MEASUREMENTS.md`. State carries none of it.
- ⚠ **Before 2026-09-26, `headroom.population` never passed spiral scores to the solve**, so every `curate headroom` census and `pool_draw` reading taken before then counted spiral places as uncapped. Production solves read the ledger themselves and were never affected. On a reopen, retake any such census before relying on it.
- Nothing is committed until Matt says "truly finalized". Nothing is published.

**★ EVERY COLLECTION HAS A TARGET, AND THE TARGETS LIVE IN `curation/targets.py` — NINETEEN COLLECTIONS: TWELVE FAMILIES, SEVEN MODES.**
- Reached by `curate solve run --collection NAME`; `--n` overrides; a collection with no target REFUSES. A change is a one-line edit there, never a number retyped into a prompt.
- **⚠ The GENERAL gallery's size is NOT a `targets.py` entry.** It is `tentative.RECORDED_SEATS` (1,000).
- There is no per-partition collection: every partition, d=6 included, enters the general gallery.
- Matt has said the sizes are essentially final.
- The website's `builder/seats.py` hand-lists the collections (→ website `builder/README.md`).

**★ ⚠ GALLERY SIZE IS MATT'S DECISION ALONE.**
- Never raise it, never queue it, never reason about shrinking `n`.
- "Final gallery quality" is his judgement, not a median.
- **Re-solving at a larger `n` reshuffles, and that is expected.**
- `final140_general2000` (n=2000) is offered on the site beside the n=1000 default. Its viewer is `artifacts/curation/viewer/general_n2000/index.html`; `viewer/index.html` stays the n=1000 page and `viewer/all.html` lists all 21.

**★ NOTHING IS PUBLISHED.**
- `tentative.PUBLISHED` is empty, so `tentative.latest()` refuses and every unstamped read names a stamp.
- Matt raises publishing himself; never ask, never list it.
- Viewers: `curate solve viewers` with no stamp builds every kept record and a complete `viewer/all.html`; named stamps still work.

**★ PINNED SEATS.** `data/curation/pins.txt` → `curate pins resolve` → `pins.json`. Ten pins, seated before the seed and prune-proof; `--no-pins` for comparisons (→ `curation/GALLERY.md §Pinned seats`). `pins.query_of` writes gallery links; they are never hand-spelled.

**★ THE SUMMARY METRICS ARE SETTLED AT THIS HORIZON.** The 10,000-hour frame stays as the way to JUDGE a product choice (→ fractal-operating).

**★ THE BAR: `DEFAULT_FINE_BAR = 0.030242` ON THE FINE COLUMN**, under `fine_head = twelve_sheets_drop_high_asymmetric_auc_ge4_more_k3`, a k=3 seed ensemble averaged on the probability scale.
- **⚠ A bar is unreadable without its head.**
- **⚠ 0.50 is NOT the seating bar.** `solve.Q4_BAR = 0.50` is the RENDER judge's constant on `p_ge4`.
- **⚠ There are two quality columns.** `p_ge4` is the render judge's GATE reading. `p_fine` is the fine head's own column, where the bar lives, and it is THE quality reading. Its scale is compressed: read q1 and the fraction above a mark, not the bare median.
- **Reader names:** on the site the render judge is **the wallpaper judge** and the fine head is **the gallery judge**; with the location and palette judges the site counts four (→ fractal-tutorial).
- ⚠ One seed of the fine head is not the mean. ⚠ `--fine-bar 0` still excludes unread rows. Provenance → `models/gallery_grade/README.md`.
- **★ `p_fine`, `p_coarse` and the bars are all operating well; every task that would alter them is CLOSED (Matt, 2026-09-12).**
- ⚠ The palette relabel-and-retrain touched the WALLPAPER judge only; the gallery judge was fitted later from its own sheets.

**★ THE HUMAN VETO IS SHIPPED** (→ `curation/README.md`). The rejection pass is a labeling mode: Matt marks ONLY `1`s, and an unmarked tile is NOT a label.

**★ A THEMED PASS RELAXES THE BAR INSIDE ITS OWN CELL.** `solve.themed_fine_bar` = the lower of the shipped bar and the `p_fine` of the 4n-th best dominant row, floored at 0.01. Mining moves a family's bar. **⚠ `--themed CELL` names a codebook colour cell, not the family bar; the family pass is `--collection <family>`.**

**★ FAMILY PASSES FLOOR AT `mode_policy.seat_floors(n)`; A MODE PASS FLOORS AT 0.** `--flat-floor` is the door back. ⚠ The floor is NOT monotone. The recurring family holes are `itinerary`, `curvature` and `direct_trap_lines`, and they are supply, not rule.

**★ COLOUR:**
- ⚠ A hue family is NOT the union of its four cells (→ `palettes/README.md`).
- Curation constrains the 48 coloured cells only; the four neutrals of the 52-colour codebook get no ceiling or floor (`ceiling.py` `CELL_SHARE = 1/48`).
- The palette group cap is `0.075·n` themed and `0.025·n` general.
- ⚠ The colour allowance is proportional to `n`.
- K is Matt's; Claude never proposes reopening K.
- Measured at ckpt 150 (website `builder/pool_study.py`): lime clears the bar least often of any hue, and all five of the worst shades are limes or light green; dark vivid reds and roses clear most often.

**★ A GALLERY PAGE IS PRESENTED STRATIFIED** (`curation/page_order.py`).

**★ GUARD RULINGS: loosening only, and nothing was loosened.** The solver is not at its optimum, and Matt says that is not a concern. There is no honest score column over the seated population; Matt's eye is the only independent read. Every other standing fact of the solve → `curation/GALLERY.md`.

**★ `pool_scores.jsonl` IS ONE-SHOT: mine → merge → `gallery-grade score-pool` → solve.**

**`curate growth`** records the seated and eligible `p_fine` spreads and counts the pool inside the fine bar; it agrees with the website's pool study seat for seat. The site's `pipeline-growth` figure bakes from the website's own `builder/pool_study.py`.

## MODES, PHASE, PALETTE
- **★ The targeted-gallery modes are seven.** Smooth is special and special-cased. `curvature` is `UNMINED`. A stored `smooth` score does not order a `tia` yield.
- **★ The explorer's render-mode roster is thirteen** (`listedModes()`), and the Walk's roster is that list. `gaussian_int`, `trap_circle`, `smooth_trap_circle` and `direct_trap_ring` are pipeline-only.
- **★ Texture weight is a drawn recipe parameter, [0.2, 0.9], on by default. Closed.**
- **★ Rotation and phase are CLOSED:** one random phase per candidate, `--phase-draw`, OFF by default (→ `curation/LEGS.md`, `preserve\rotation_phase_economics.md`).
- **★ Palette replication is PARKED (Matt, 2026-09-12).** `data/palettes/palettes_for_random_choice.csv` (232 maps) feeds the explorer's Random palette and the Walk's "All palettes".
- **★ The explorer's palette modes are EXPLORER-ONLY.** `scale` (leveled | absolute), `lambda` and `period` are omitted at default, and the pipeline's key whitelist never emits them. Leveled stays the pipeline's default and the shallow view's (→ `engine/README.md`, `explorer/README.md`).
- ⚠ A seat's `mode` in `gallery.jsonl` is ROUTED; render at `recipe["mode"]` (→ fractal-tutorial). A seat recorded `smooth` whose recipe draws another mode is routing, not a record bug.

## FULL-RESOLUTION WALLPAPERS
- **★ The shipped setting is 2560×1440 at ss3 (a 3×3 grid per pixel), saved as JPEG q95 with 4:4:4 chroma (Matt, ckpt 148).** ss2 was nearly indistinguishable; ss3 costs about 2.2× ss2. WebP is out because Windows 10 does not open it natively. Every file carries its explorer link as metadata.
- **The population is 6,299 distinct recipes** across the 21 kept records. Measured on ten seats: ss4 costs 3.64× ss2, and the production pool buys only about 5% at this size. The ss3 run is projected at about 46 wall hours and roughly 13–14 GB.
- **`fulls_ss3_ckpt148` is QUEUED; Matt launches it at the start of the next checkpoint** (§QUEUED). It is resumable: the same prompt is the resume prompt, Matt may pause it by telling CC, and the whole CC instance may be killed and resumed. It first checks ss3 against the ss4 renders in `E:\FractalWallpapers\ss_test_ckpt148\` and warns (without stopping) if any picture is not closer to ss4 than ss2 was. Output: `E:\FractalWallpapers\full\`, with `membership.jsonl` for pack assembly.
- ⚠ **The native production binary is a rustc 1.98.1 build, and its timing against the 1.96.0 build was never measured.** Rust 1.97's correctly rounded `hypot` made the WASM `tia` and lattice modes up to 3.5× slower; native `hypot` comes from the MSVC runtime and is expected to be unaffected, but that is untested. The check is `fulls_ss3`'s own early rate against the 46-hour projection, not a separate measurement. The fingerprint is unmoved, so pixels are not in question.
- Until that prompt promotes it, the tree's phase-3 default is still ss4; fractal-tutorial's geometry line follows the code, not this decision.
- **★ Pack hosting (Matt, ckpt 149):** GitHub Releases for the smaller packs; Matt's Google Drive for general-2000 and anything else too large. Most people will take the best 100–200.

## LAWS STATE STILL CARRIES
- **★ The degree-6 plane is never labelled** (`partitions.NEVER_LABELLED`).
- **★ Inside a minibrot copy is a named phenomenon** → `preserve\minibrot_copies.md`. It is a §Deep zoom source, with `preserve\deep_zoom_section.md` (OPEN 9).
- **★ Parabolic Julia sets are CLOSED (Matt, ckpt 147):** judged by eye on a sheet. The few that work sit just outside a root, at about ε = 1e-4; the rest fill with interior. They are reachable by hand in the explorer and are not included as a tool or in the pipeline. §13 points to Wikibooks and Chéritat.
- **★ Douady–Hubbard tuning in a Julia set is PARKED (Matt, ckpt 148)** (→ `preserve\parked.md`): the effect is real but the pictures are not artistic enough to earn a §14 figure.
- **★ BLA stays removed (ruling reaffirmed ckpt 149):** it ranged from about 20% slower to about 2.6× faster on frames with structure, and it moved escape counts at every tolerance tried. The site says so (Deep zoom); never re-argue it from the speedup alone.

## RETENTION
**★ The keep is five per `(place, mode)` plus one family allowance.** Forward-only and colour-blind (→ `curation/README.md`). Pinned rows and every kept record's seats are prune-proof via `tentative.kept()`.

## RECORDS — THE SEMI-FINAL SET
- **★ The store is exactly the twenty-one records on the keep list (`tentative.KEPT_UNPUBLISHED`):** the twenty `final139_*` (general n=1000 plus the nineteen collections, 9,000 seats) and `final140_general2000` (n=2000, same pool and config apart from `n`).
- **Every kept record carries its `recipes.jsonl`, and all are untracked.** ★ Tracking a recipe file IS publishing its stamp.
- **Check records are kept records:** `portable.GENERAL_CHECK` = `final139_general`, and `portable.REFERENCE` = `final139_green`. Nothing is re-cut while the pool is closed.
- **★ BACKUPS ARE MATT'S.** `storage export` runs only at his direction and is never proposed. He holds the copies off-box and deletes the local instance at once, so nothing expects one on disk. Restore → wallpapers `src/fractal_wallpapers/README.md §Continuing on a fresh box`.
- **★ ⚠ A record is discarded by default; preservation derives from the keep list alone.**
  - ⚠ A record is two directories.
  - `solve.write_record` refuses to overwrite. `record` never renders.
  - `git grep <stamp>` before calling any record stray.
  - `backfill.DEFAULT_RECORD` → `final139_general`.
  - The `final139_*` set is the PRE baseline until something merges.
- **★ A record carries its prose whole, and the source carries one copy** (`SCHEMA_NOTES`).

## THE REPO AS A CLONE SEES IT
- **★ A fresh box continues every stage from a `storage export` alone** (→ `preserve\fresh_box.md`).
- **★ CUDA is opt-in (Matt, ckpt 148): nothing heavy installs unless asked for.** The `models` extra is CPU torch on every platform; the conflicting `cuda` extra is cu124 on Windows and Linux x86_64 (→ wallpapers README §Install). ⚠ **This box syncs `--extra cuda`**; a plain `uv sync --extra models` here would swap its torch to CPU.
- **★ People should be able to run both repos on Windows, Linux and macOS (Matt, ckpt 148).** Wallpapers CI runs one job on `ubuntu-latest`, `macos-latest` (arm64) and `windows-latest`; its first run comes on Matt's next git step. ⚠ The watch item is the exact-pixel digest checks on arm64 macOS: a red there is the first real platform difference, and the choice is per-platform digests or a tolerance, never a skip. Intel Macs get no `models` extra. The website's CI matrix is OPEN 13.
- **★ The Rust-only renderer SHIPPED (ckpt 149):** `fractal-engine render-link` (→ fractal-engine). A render-only user needs no Python.
- ⚠ `p_fine` rows are stamped with a weights sha, and a clone's rows differ by design.
- ⚠ Drive the makers through `.venv/Scripts/fractal-wallpapers.exe`.
- **Concurrent prompts in one checkout commit with a pathspec** (`git commit -- <paths>`); both repos' `CLAUDE.md` own the rule (ckpt 151, after a bare commit swept in another prompt's staged deletions).

## WEBSITE — THE EXPLORER STUDIO AND THE ARTICLE
**Nothing is live; the site never needs preserving or keeping in sync.** Every fact about the site is owned by the website repo, and state keeps no copy:

| Topic | Owner |
|---|---|
| Explorer: tabs, keys, Deep/Cancel/undo/recolour, Deep auto-render and its switch, palette modes, Fit (f) and the arrival refit, Hold look, the fade table, Find minibrots, zoom-out stop, screensaver, Walk, Phoenix, the two iteration ceilings, `panel=` and `collection=` links, link round-trips and orbit reuse, measured timings, the WASM toolchain pin (rustc 1.96.0, because of 1.97's slow `hypot`), the operator being the engine's | `explorer/README.md` |
| Deep kernel, oracle, calibration, closed verdicts (BLA included), `sameOrbit` | `explorer/perturb-wasm/README.md` |
| Atlas, and the live `atlas-live` figure with its miniatures | `atlas/README.md` |
| Builder, figures, the split rule, `seats.py`, the staged set, site size, the zoom-video tooling (`zoom.py`) and its defaults, the deep-figure maker (`builder deep`), automatic minibrot descents (`builder descent`), the `start-*` maker (`builder/start.py`), display formulas (`builder formulas`), the pool study (`builder/pool_study.py`), every `builder check` check, the rail groups, the site's icon | `builder/README.md` |
| The recolour-race harness (`explorer/bench/recolour-race.mjs`, about an hour, outside `builder check`) | `explorer/README.md` |
| Explorer links embedded in downloaded and released files | `stamp.js` · wallpapers `explorer_link`; the `stamps` check |
| The Deep tab's gallery: its register (`explorer/deep-gallery.jsonl`), maker (`builder/deep_gallery.py`) and method | `builder/README.md §How the first set was found` |
| Traps: native exe rebuild, perturb rebake, repo links, the no-`<video>` rule, the one script kind an article page may carry, the rail, pathspec commits | `CLAUDE.md` |
| Style and voice: no italics, no em-dashes, the Oxford comma, American spelling, vocabulary, §Voice | `prose\writing-guidance.md` · website `CLAUDE.md` |
| Per-page status, and deliberate simplifications (the pool gate's per-mode fallback is left off Training judges on purpose) | `docs/page-review.md` |

- **★ STAGING RULE (Matt):** no gallery-sized or library-sized commits until he says deploy.
- **Hosting:** the site deploys to GitHub Pages at `techmatt.github.io/fractal-website` (`pages.yml`), about 156 MiB, every asset by relative path. Pages is its CDN. The packs' host is decided (§FULL-RESOLUTION WALLPAPERS).
- Shallow contract **v4** (an optional `n`, omitted at the width rule); deep contract **v3**. `n` runs 50 to 2e6 in both. **Deep links always write `scale`, `scale=leveled` included (Matt, ckpt 150)**; a deep link with no `scale` still means the Absolute fit on arrival, so no older link changed.
- **★ A LINK IS A PICTURE (ckpt 150):** the same link draws the same picture whatever the explorer did before, and an idle canvas equals a fresh render of the address-bar URL.
- **★ No figure reuses a picture shown elsewhere on the site unless the reuse is intentional (Matt).** An intentional reuse carries a `reuse_reason` that names the figure it repeats.
- **★ The site reads as its final form (Matt, ckpt 147):** no "under construction" wording. Matt's own "yet"s are his to keep.
- **★ The Oxford comma everywhere (Matt, ckpt 148). Site prose uses American spelling.**
- **★ THE VOICE (Matt, ckpt 149; `prose\writing-guidance.md` §Voice):** first person, plain, conversational; what Matt did and why. No spec or essay register, no punchlines, no coined rules. **The article describes the design as intended: a rule that never had to bind (a floor or cap never hit) is written as existing, and is never flagged or "verified" as untrue. A semi-idealized description is preferred where the real detail is a distraction (Matt, ckpt 151).** New prose is written to this standard; a green that paraphrases must keep every fact.
- **★ Display formulas are typeset (ckpt 149):** a master writes `$$ … $$` on its own line; the builder renders it to inline SVG with MathJax, fetched and never committed. Inline math stays HTML. The `formulas` check holds each SVG to a fresh typesetting.
- **★ The judges' reader names (Matt, ckpt 148):** the location judge, the wallpaper judge, the palette judge, and the gallery judge. "Render judge" no longer appears in reader-facing prose; code keeps its names.
- **★ Links (ckpt 148):** each thing a reader can go and use is linked once per page, at its first natural mention. `?panel=<tab>` opens a tab and `?panel=gallery&collection=<name>` opens one collection.
- **The article runs to fourteen sections plus Start here.**
  - The rail shows START HERE, then **WALLPAPER PACKS** (a peer group), then CONTENTS.
  - Start here (`start-here.html`, master `Start here v2.md`) has h1 "Start here" and four h2 parts: Fractal wallpapers, Fractal explorer, Deep zoom rendering, Future work.
  - §9 Gallery curation is v2 (`article/gallery-curation.html`, master `Gallery curation v2.md`). Its figures are `gallery-top-scored` (the gallery judge's strict top 24), `gallery-twins` and `gallery-output`.
  - **Full pipeline is v6 (`Full pipeline v6.md`):** the three parts, then "How I ran it" in Matt's words. Figures: `pipeline-overview`, `pipeline-hue-shares`, `pipeline-hue-extremes`, and `pipeline-growth`. All four bake from `builder/pool_study.py`, whose measurement lives in `artifacts/pool-study/` (kept).
  - **Finding good locations is v8, Training judges v7, Color palettes v7, and Rendering modes v5 (ckpt 151)**; each kept every figure in order. Finding good locations writes multibrot and twin degrees as 3 to 6 (Matt).
  - §12 is "Deep zoom rendering" (`article/deep-zoom.html`, master `Deep zoom v3.md`). Minibrot descents holds what was "Automatic minibrot descents" (Matt: descents are an artistic composition, automation optional).
  - §14 is "Fractal math" (`article/fractal-math.html`, master `Fractal math v2.md`); its Pi section is two displayed limits.
  - The front page carries hand-written intro and Contents blurbs, with no master and no ✓ marks; the voice pass did not reach them.
  - `escape-families` has 18 panels: five planes (degree 2 to 6), each with two of Matt's Julia picks, then Phoenix.
- **★ The download page is "Wallpaper packs" (`wallpaper-packs/`),** distinct from the explorer's Gallery tab. Its icon-source figure carries no caption. The Gallery tab's staged images stay under `assets/images/galleries/`; where the packs' own images live is decided when packs exist.

**★ THE SECTION-CUT TEMPLATE (Matt, ckpt 148). Done: Gallery curation (v2), Full pipeline (v6), Finding good locations (v8), Training judges (v7), Color palettes (v7), Rendering modes (v5, a prose pass only: Matt had reviewed it by hand). Next: other sections as Matt names them.**
- **The test for every passage:** would a reasonably intelligent CS undergrad think of this unprompted? If so, it collapses to a sentence or goes.
- **What stays:** the non-obvious insight that motivates the section, shown with a figure; Matt's own judgement calls; facts invisible from outside; honest notes on what was considered and turned out unnecessary.
- **What collapses:** each rule becomes one bullet with its number in it, and the algorithm becomes two sentences plus links to the code files.
- **What goes:** mechanism detail; plumbing another section covers; figures that illustrate a mechanism rather than a result.
- **Default when Matt says "keep the figures, tighten the text":** every figure and its caption stay, in order; headings may merge.
- **Process:** Claude reads the live master from Drive `prose\`, drafts the cut in chat with a list of what was cut and the facts to confirm; Matt corrects; Claude trashes the old master, creates the new one in `prose\` (these are small enough), and writes a placement prompt with a verify list at its foot. The placing CC checks the list from source and corrects the prose, reporting each change.
- **A sentence-level review uses a coloured docx:** numbered blocks of black context, red current text, green proposed text, and black context. Matt deletes the blocks he rejects and edits the greens; an apply prompt swaps by red text, found exactly once or skipped.

**★ THE SITE IS RE-BASED ON `final139_*` + `final140_general2000` — DATA ONLY. Prose and captions wait for "ready for publishing".**

**★ Figure recipes are never lost.** `article/figure-recipes.jsonl` is site-owned and tracked; a `spec` panel's recipe is its registry row. A panel whose run kept no tone curve may carry a re-measured one in an optional `tone` field (one row does: `4438b8c4`). ★ Every composite figure that can be split is split (Matt).

**★ THE EXPLORER'S BAR (Matt):**
- Complexity is a cost to the person using a tool; only clear wins are added (→ `preserve\rulings_website.md §2026-09-20`).
- Its text is for the artist, and every keyed button wears its key. "Render mode" is the term everywhere.
- Left panel changes the view; right panel manipulates this view.
- **The shallow view and the Deep tab are one tool at two depths (Matt, ckpt 144):** the same control grid, the same button in the same place wherever both have it, one Save, one Root (r), and Find minibrots in both. Details → `explorer/README.md`.
- **The Deep tab renders by itself, on by default and expected to stay on (Matt, ckpt 146),** with one per-viewer off switch that never enters a link.
- **★ Entering Deep switches to Absolute and fits (Matt, ckpt 147),** unless already Absolute or the link states `scale`. Leaving Deep keeps the scale. Fit (f) targets `PASSES = 7` (`explorer/fit.js`), which is Matt's to tune.
- It targets the desktop.
- Explorer-only fast paths are allowed only where the pixel difference from the pipeline is easy to bound. Wasm threads are out.
- ⚠ This box drifts ~30% between identical runs; alternate before/after.

**★ Deep (perturbation) is explorer-only; nothing deep enters the pipeline (Matt)** (→ fractal-engine §Deep render). The Inflection tab is paged out (`explorer/paged-inflection/`); §13 mentions it. **★ The Walk is a short demonstration of how the galleries were made.** Parked → `preserve\parked.md`.

**★ ZOOM VIDEOS (Matt, ckpt 151):** the double-descent 4K60 master's settings are the baseline for every new video (owned by `builder/README.md`): 7680×4320 fields for 3840×2160 at 60 fps, CRF 12 slow film yuv420p with full BT.709 tags, and the monotone undercap rule (a 480×270 probe at the 2M ceiling, cap = 2×need at 1e-5 black-but-exterior, never falling down a descent). Every new record also gets a 960×540 `preview` variant at a sixteenth of the cost. Speed and path stay per video.

## IN FLIGHT ACROSS THIS BOUNDARY
None.

## QUEUED IN DRIVE `prompts\`
- **`fulls_ss3_ckpt148` (wallpapers):** Matt launches it at the start of the next checkpoint. The engine is settled (the engine-wasm import left `engine/` and the fingerprint untouched). The box crashed and rebooted during the video render on 2026-09-25/26, so its uptime is short; reboot only if it has been up past a week.

## NEXT CHECKPOINT GOAL
Matt raises it at the top of the checkpoint.

## OPEN (ordered) — Matt raises each
Items 3, 6, 8, 10 and 11 are closed; the numbering is kept.
1. **Mining is CLOSED; he reopens it.** Read `preserve\mining_laws.md`, then the reopen inventory in wallpapers `curation/LEGS.md`. The `final139_*` set is the PRE baseline, and `gallery-grade score-pool` runs before any solve. Retake any headroom census taken before 2026-09-26 (§Where we are).
2. **"Truly finalized": the commits (Matt raises it).** What waits on it: the twenty-one kept records and their recipes (tracking = publishing), the staged website assets, and the pre-final history rewrite.
4. **Website: the section-by-section review pass** (Matt brings a section's review doc, or asks for a direct cut; → OPEN 12).
5. **Deploy preparation (preparing, not deploying).**
   - Done: the favicon (F08); explorer links embedded in every download and release render; the two repo READMEs' funnels; the packs' host decided; Wallpaper packs in the rail; the double-descent 4K60 master (ckpt 151).
   - **Left:**
     - building the packs from `fulls_ss3`'s output and `membership.jsonl`, and uploading them (Releases for the smaller packs, Drive for the large);
     - a history rewrite before the final commit;
     - **cross-platform support:** both repos build and run on Linux and macOS as well as Windows, proven by a CI OS matrix (wallpapers done, first run pending; website → OPEN 13);
     - the zoom videos' YouTube uploads (Matt is trying the double-descent master's encode on YouTube), then final deployment.
   - **After deployment:** post the site to fractalforums.org.
7. **The Deep tab's follow-ups.**
   - **The gallery (33 frames, Matt's picks).** Matt adds frames over time, including frames centred away from any minibrot. He sends links, and a one-line prompt appends each row, pins `n` from the width rule, and bakes its thumbnail (→ `builder/README.md`). Julia frames are supported. One Filigree place appears twice, in two colourings, as asked.
9. **THE WRITEUP (Matt raises it; the session authors a prose master plus a placement prompt).**
   - **§Deep zoom rendering (`article/deep-zoom.html`, master `prose\Deep zoom v3.md`).**
     - **Placed figures:** `deep-f64-and-perturbation` (Porcelain Field, phase 0.41, absolute, period 0.295); `deep-shallow-and-deep` (its two panels do NOT share a colouring, on purpose); `deep-final-colorings` (a 2×2 of Matt's four links on the video's final frame: Final frame, Leveled, Higher period, Palette switch); `deep-descent-rungs` (Chalcedony, absolute, λ 0, period 0.5); `deep-descent-pairs` (seats `afdb47c0`, `9c6a3d87`, glowdon; caption "Two frames, A and B (top), and the four ways to nest one inside the other (bottom)."); `deep-misiurewicz-pairs`: three rows (a shallow degree-2 point, then tuned degree-3 and degree-4 points deep) by three columns (whole Julia set, Julia at c, that row's Mandelbrot or multibrot set at c), caption final. Its per-row palettes are placeholders for Matt.
     - **Placeholders:** `deep-zoom-video` (first cut exists, paused on Matt's colour and ending; on the page a poster WebP linking out, never a `<video>` embed); `deep-descent-video`; `deep-multibrots` (Matt writes the multibrots section).
     - **The double-descent movie is FINAL (Matt, ckpt 151):** the favicon seat `double-descent_power_L0.38_a0.15_along-the-starry-way-25`, `smooth`, 4K60, 85 s, at `artifacts/double-descent/4k60/video/` (linked to `E:\FractalStorage\fractal-website\double-descent-4k60`). Under the monotone cap rule its ending opens M₂ at about 61 periods, not 32; Matt accepted that. It is not supersampled; supersampling k25–k29 would cost about 38 hours.
     - **When the figure round finishes,** delete `preserve\minibrot_copies.md` and `preserve\deep_zoom_section.md`.
   - **Start here:** `start-video` waits on Matt's new video. `start-pink-gallery` (six magenta, six rose) is a placeholder for his daughter's final picks. `start-modes` is two Mandelbrot rows Matt picked. The other `start-*` figures are placeholders Matt adjusts. The "darker pink gallery" link opens `magenta`; `rose` is the other honest choice (Matt's call).
   - **After `fulls_ss3` reports:** finalize Rendering modes' mode table. The wallpaper-render column is a placeholder scaled from candidate time; fill it from real ss3 times (`E:\FractalWallpapers\full\progress.jsonl`), change the text's "supersampled 4×" to 3×, and drop the placeholder note under the table. **Rendering fundamentals' "The production setting is s = 4, so sixteen orbits" becomes s = 3 and nine, in the same prompt.**
12. **The section-cut pass:** other sections as Matt names them. Not yet cut: Overview, Escape-time fractals, Rendering fundamentals, Make your own palettes, Finding good wallpapers, Fractal atlases, Deep zoom rendering, Other artistic techniques, Fractal math, and Start here.
13. **Small follow-ups, each a short prompt (website):** the `stamps` check may add render-link as a third embedder; the website CI and OS matrix.

Parked → `preserve\parked.md`.

## STATUS / KNOWN REDS
- ⚠ A website `builder check` beside a wallpapers merge can throw a transient "not in the candidate ledger" red; retry.
- ⚠ A report just copied to Drive `reports\` can read back EMPTY, or not appear in search, for minutes; retry once, then ask Matt to paste it.
- `builder check` was all green at the end of ckpt 151; its only note is the one figure still to make (`start-video`).

## RULINGS THIS ERA
ckpt 151 (2026-09-26). Reported prompts: `double_descent_4k_ckpt148`, `place_finding_locations_v8_ckpt151`, `video_defaults_ckpt151`, `place_training_judges_v7_ckpt151`, `place_color_palettes_v7_ckpt151`, `place_rendering_modes_v5_ckpt151`, `engine_wasm_import_ckpt151`, `preclose_ckpt151`.

- **Four section cuts (Matt):** Finding good locations, Training judges, and Color palettes cut to about half, keeping every figure; Rendering modes given a prose pass only.
- **Degrees up to 6 (Matt):** Finding good locations writes the multibrot planes and the twin channel as degree 3 to 6.
- **Semi-idealized over exact (Matt):** Training judges writes the pool gate as even odds of a 4 with no per-mode fallback, and prints no score constant.
- **The double-descent master is final at about 61 periods, and its settings are the video baseline (Matt).**
- **Engine-wasm imports the engine's levelling code** in the gap before `fulls_ss3` (Matt); the engine did not move.

## KEEP LIST
**Drive `prompts\`:** keep `fulls_ss3_ckpt148.md`; wipe everything else.

**Drive `reports\`:** wipe everything. (`interesting_rust_change.md` beside the engine-wasm report goes too; its finding lives in `explorer/README.md`.)

**Drive `prose\`:** unchanged by the closeout. The live masters are `Start here v2.md`, `Overview v2.md`, `Escape-time fractals v1.md`, `Rendering fundamentals v1.md`, `Color palettes v7.md`, `Make your own palettes v4.md`, `Rendering modes v5.md`, `Training judges v7.md`, `Finding good locations v8.md`, `Finding good wallpapers v3.md`, `Gallery curation v2.md`, `Full pipeline v6.md`, `Fractal atlases v2.md`, `Deep zoom v3.md`, `Other artistic techniques v1.md` and `Fractal math v2.md`, plus `writing-guidance.md`.

The review docs' canonical copies are website `review\deep-zoom.docx` and `review\gallery-curation.docx`; the applied voice pass is archived in Drive `review\applied\voice-pass-2026-09-25.docx`.

**Wallpapers `scratch/`:**
- KEEP `place_radius_sheet/`, `retired_tentative/`, `preclose_ckpt125/off_list_stamps.txt`, `tuning_test/`, `leg_numbers.py` and `mbc140/` (§Deep zoom's picking sheets).
- WIPE everything else (`cpu_default_and_rust_audit_ckpt148_findings.md` goes: the engine-wasm switch landed).

**Website:**
- `scratch/`: wipe all except `deep_gallery_sheet/` (the 65-tile sheets, for further picks). The untracked staged set is NOT cleaned; it also holds `explorer/deep-gallery/` (33 thumbnails) and the atlas slot pictures.
- **KEEP `artifacts/deep-zoom/`** (fields, coloured keyframes, MP4s), **`artifacts/double-descent/`** (the movie's fields, stills and cuts, including the final 4K60 master and its untagged original), **`artifacts/mathjax/`** (the fetched typesetter) and **`artifacts/pool-study/`** (the measurement behind the four Full pipeline figures, kept until "ready for publishing"). All are untracked.
- `artifacts/deep-gallery/` and `artifacts/cap-split/` are sweepable.

**`E:\FractalWallpapers\`:** KEEP `ss_test_ckpt148\` (the ss4 references `fulls_ss3`'s check compares against). `full\` is `fulls_ss3`'s output.

**`preserve\`:** `deep_zoom_section.md` and `minibrot_copies.md` stay until the figure round finishes. `art_techniques_links.md` stays until Matt rules.

**Outside both repos:** `C:\Tools\fraktaler-3\` stays until Matt removes it. The rustc 1.96.0 toolchain installed beside stable stays: WASM bakes need it.

**Wallpapers records:** the twenty-one kept records are the whole store, and their `recipes.jsonl` stay.

**Hot artifacts:**
- Stay: `artifacts/discovery/minibrot_examples.jsonl`, `artifacts/tuned129x_*`, the d=6 harvest and depth directories, every 2026-09-18/19/21 leg's directories, and `artifacts/curation/growth/` (three 2026-09-02 runs).
- Sweepable when Matt sweeps: the parabolic pilot's legs, superseded `gallery_grade_head/pool_scores_*`, `curation_backup/`, `tiles/` manifests and `render_dose/*.pt`.

## OWED
Nothing.

## SCRATCH/ARTIFACT FLAGS
- **★ The standing keep roster lives in the repo:** `src/fractal_wallpapers/README.md §The standing keep roster`.
- ⚠ `.leveled/` directories are sweepable (→ `preserve\leveled_identity.md`).
- `artifacts/atlas/<plane>/thumbs/` stays while the atlas may be re-ingested.
- ⚠ CRLF drift is real; check with `git ls-files --eol`.
- ARCHIVED (restore before reuse): unchanged from ckpt 106.

## PARKED / SETTLED
→ `preserve\INDEX.md`, which lists every file. Never re-list them here.
