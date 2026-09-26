# fractal-state — checkpoint 152 (2026-09-26: the site renamed to `fractals` and live but unadvertised; staged assets committed; Double Descent on YouTube and embedded in Start here; CI green on three OSes in both repos; the publishing audit applied and partly reverted by Matt; `fulls_ss3` in flight)

## Where we are
Three phases, each depending strictly on the one before (→ fractal-discovery). Matt iterates from pictures, not counts. Phase 3 is his eye on the final seating, and **every planned collection has a viewer at its official size.**

**★ MINING IS CLOSED (Matt, 2026-09-21) UNTIL HE REOPENS IT.**
- The pool as merged on 2026-09-21 is the population, and the `final139_*` solves (§RECORDS) are the semi-final galleries.
- On a reopen, read `preserve\mining_laws.md` whole, then wallpapers `curation/LEGS.md §Mining is CLOSED (2026-09-21) — reopen inventory`, which lists the open arms and prices, every line citing `MEASUREMENTS.md`. State carries none of it.
- ⚠ **Before 2026-09-26, `headroom.population` never passed spiral scores to the solve**, so every `curate headroom` census and `pool_draw` reading taken before then counted spiral places as uncapped. Production solves read the ledger themselves and were never affected. On a reopen, retake any such census before relying on it.
- Nothing in wallpapers is committed as publishing until Matt says "truly finalized". Nothing is published.

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
- **★ Exponential smoothing is not a separate mode on the site (Matt, ckpt 152):** its pictures are identical to smooth, and every reader-facing name for it says **smooth** (website `builder/picks.py` `MODE_WORDS`). Recipes keep the engine's name `exp_smoothing`.
- **★ Texture weight is a drawn recipe parameter, [0.2, 0.9], on by default. Closed.**
- **★ Rotation and phase are CLOSED:** one random phase per candidate, `--phase-draw`, OFF by default (→ `curation/LEGS.md`, `preserve\rotation_phase_economics.md`).
- **★ Palette replication is PARKED (Matt, 2026-09-12).** `data/palettes/palettes_for_random_choice.csv` (232 maps) feeds the explorer's Random palette and the Walk's "All palettes".
- **★ The explorer's palette modes are EXPLORER-ONLY.** `scale` (leveled | absolute), `lambda` and `period` are omitted at default, and the pipeline's key whitelist never emits them. Leveled stays the pipeline's default and the shallow view's (→ `engine/README.md`, `explorer/README.md`).
- ⚠ A seat's `mode` in `gallery.jsonl` is ROUTED; render at `recipe["mode"]` (→ fractal-tutorial). A seat recorded `smooth` whose recipe draws another mode is routing, not a record bug.

## FULL-RESOLUTION WALLPAPERS
- **★ The shipped setting is 2560×1440 at ss3 (a 3×3 grid per pixel), saved as JPEG q95 with 4:4:4 chroma (Matt, ckpt 148).** WebP is out because Windows 10 does not open it natively. Every file carries its explorer link as metadata, on the `techmatt.github.io/fractals/explorer/` base.
- **The ss3 check PASSED (ckpt 152):** on all ten test pictures and both measures, ss3 is closer to ss4 than ss2 was, removing about a quarter to a third of ss2's error. The q95 4:4:4 encode adds little on top.
- **The population is 6,299 distinct recipes** across the 21 kept records. **Projection: about 54–60 wall hours** (ss3 costs 0.67× ss4, not 9/16, because of fixed overhead; the live rate was about 107 pictures an hour) **and about 16 GB** (mean JPEG 2.56 MB).
- **`fulls_ss3_ckpt148` is IN FLIGHT** (§IN FLIGHT). Output: `E:\FractalWallpapers\full\`, with `membership.jsonl` for pack assembly and `progress.jsonl` for timings. The driver is `curate full-set run|status|pause` (→ wallpapers `curation/full_set.py`).
- **A stamped picture can be re-stamped in place without a render** (`embed_link` replaces its own stamp), so a link change never costs a re-render.
- Until that prompt promotes it at its end, the tree's phase-3 default is still ss4; fractal-tutorial's geometry line follows the code, not this decision.
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
- **★ Both repos build and run on Windows, Linux and macOS, and CI proves it (ckpt 152):** wallpapers `ci.yml` and website `checks.yml` are each green on `ubuntu-latest`, `macos-latest` (arm64) and `windows-latest`. The macOS red in `test_palette_train` was float32 arithmetic; those tests now compare in float64 everywhere, with no platform special case. The website's crates job checks out wallpapers at the manifest's pinned commit. Intel Macs get no `models` extra. ⚠ `engine.wasm` embeds absolute source paths, so its bytes differ per machine and CI reports hashes without asserting them (→ OPEN 13).
- **★ The Rust-only renderer SHIPPED (ckpt 149):** `fractal-engine render-link` (→ fractal-engine). It honours the explorer-only `scale`, `lambda` and `period`. A render-only user needs no Python.
- ⚠ `p_fine` rows are stamped with a weights sha, and a clone's rows differ by design.
- ⚠ Drive the makers through `.venv/Scripts/fractal-wallpapers.exe`.
- **Concurrent prompts in one checkout commit with a pathspec** (`git commit -- <paths>`); both repos' `CLAUDE.md` own the rule.
- `gh` is installed on this box and logged in as techmatt.

## WEBSITE — THE EXPLORER STUDIO AND THE ARTICLE
**★ The site is LIVE BUT UNADVERTISED (ckpt 152)** at `techmatt.github.io/fractals/`: GitHub Pages (`pages.yml`) from repo `techmatt/fractals`. The GitHub repo was renamed from `fractal-website`; **the local folder stays `C:\Code\fractal-website`**, and every guard and local path keeps that name. Every absolute URL in both repos uses the new base; the link base is spelled twice (wallpapers `explorer_link.py` and `engine/src/link.rs` `EXPLORER_URL`), held equal by the website's `stamps` check. Until Matt advertises it, the site still never needs preserving or keeping in sync. Every fact about the site is owned by the website repo, and state keeps no copy:

| Topic | Owner |
|---|---|
| Explorer: tabs, keys, Deep/Cancel/undo/recolour, Deep auto-render and its switch, palette modes, Fit (f) and the arrival refit, Hold look, the fade table, Find minibrots, zoom-out stop, screensaver, Walk, Phoenix, the two iteration ceilings, `panel=` and `collection=` links, link round-trips and orbit reuse, measured timings, the WASM toolchain pin (rustc 1.96.0, because of 1.97's slow `hypot`), the operator being the engine's | `explorer/README.md` |
| Deep kernel, oracle, calibration, closed verdicts (BLA included), `sameOrbit` | `explorer/perturb-wasm/README.md` |
| Atlas, and the live `atlas-live` figure with its miniatures | `atlas/README.md` |
| Builder, figures (the `video` row type, and linked pictures under a player), the split rule, `seats.py`, site size, the zoom-video tooling (`zoom.py`) and its defaults, the deep-figure maker (`builder deep`), automatic minibrot descents (`builder descent`), the `start-*` maker (`builder/start.py`), display formulas (`builder formulas`), the pool study (`builder/pool_study.py`), the `go/` short redirects (`go/redirects.jsonl`, `builder/go.py`, the `go` check), every `builder check` check, the rail groups, the site's icon | `builder/README.md` |
| The recolour-race harness (`explorer/bench/recolour-race.mjs`, about an hour, outside `builder check`) | `explorer/README.md` |
| Explorer links embedded in downloaded and released files | `stamp.js` · wallpapers `explorer_link`; the `stamps` check |
| The Deep tab's gallery: its register (`explorer/deep-gallery.jsonl`), maker (`builder/deep_gallery.py`) and method | `builder/README.md §How the first set was found` |
| Traps: native exe rebuild, perturb rebake, repo links, self-hosted video (a YouTube embed is the one video form), the one script kind an article page may carry, the rail, pathspec commits, the three-OS CI | `CLAUDE.md` |
| Style and voice: no italics, no em-dashes, the Oxford comma, American spelling, vocabulary, §Voice | `prose\writing-guidance.md` · website `CLAUDE.md` |
| Per-page status, and deliberate simplifications (the pool gate's per-mode fallback is left off Training judges on purpose) | `docs/page-review.md` |

- **★ The staging rule is RETIRED (Matt, ckpt 152).** Every asset the site serves is tracked: the Gallery tab's tiles, the atlas slot pictures, the Deep gallery thumbnails, the palette bake, and the judges with their ORT runtime (about 34 MB, through git by Matt's call). The tracked site is about 166 MB. A re-solve, re-ingest or rebake is a tracked diff; the pre-final history rewrite can drop superseded blobs.
- Shallow contract **v4** (an optional `n`, omitted at the width rule); deep contract **v3**. `n` runs 50 to 2e6 in both. **Deep links always write `scale`, `scale=leveled` included (Matt, ckpt 150)**; a deep link with no `scale` still means the Absolute fit on arrival, so no older link changed.
- **★ A LINK IS A PICTURE (ckpt 150):** the same link draws the same picture whatever the explorer did before, and an idle canvas equals a fresh render of the address-bar URL.
- **★ No figure reuses a picture shown elsewhere on the site unless the reuse is intentional (Matt).** An intentional reuse carries a `reuse_reason` that names the figure it repeats.
- **★ Figures are never changed because they drifted from the current records (Matt, ckpt 152)** (→ fractal-operating). `gallery-output` stays on its 2026-09-02 pass, and `wallpapers-three-bands`' bottom band is Matt's mix of two draws, by his choice.
- **★ The site reads as its final form (Matt, ckpt 147):** no "under construction" wording. Matt's own "yet"s are his to keep.
- **★ The Oxford comma everywhere (Matt, ckpt 148). Site prose uses American spelling.**
- **★ THE VOICE (Matt, ckpt 149; `prose\writing-guidance.md` §Voice):** first person, plain, conversational; what Matt did and why. No spec or essay register, no punchlines, no coined rules. **The article describes the design as intended: a rule that never had to bind (a floor or cap never hit) is written as existing, and is never flagged or "verified" as untrue. A semi-idealized description is preferred where the real detail is a distraction (Matt, ckpt 151).** New prose is written to this standard; a green that paraphrases must keep every fact.
- **★ Display formulas are typeset (ckpt 149):** a master writes `$$ … $$` on its own line; the builder renders it to inline SVG with MathJax, fetched and never committed. Inline math stays HTML. The `formulas` check holds each SVG to a fresh typesetting.
- **★ The judges' reader names (Matt, ckpt 148):** the location judge, the wallpaper judge, the palette judge, and the gallery judge. "Render judge" no longer appears in reader-facing prose; code keeps its names.
- **★ Links (ckpt 148):** each thing a reader can go and use is linked once per page, at its first natural mention. `?panel=<tab>` opens a tab and `?panel=gallery&collection=<name>` opens one collection.
- **The article runs to fourteen sections plus Start here.**
  - The rail shows START HERE, then **WALLPAPER PACKS** (a peer group), then CONTENTS.
  - Start here (`start-here.html`, master `Start here v2.md`) has h1 "Start here" and four h2 parts: Fractal wallpapers, Fractal explorer, Deep zoom rendering, Future work. **Its `start-video` is placed:** the Double Descent YouTube embed, with Midway and Final frame pictures under it linking through `go/favicon-mid` (the favicon seat's own `tia` rendering) and `go/favicon-end` (the video's final frame, deep, n = 2,000,000).
  - §9 Gallery curation is v2 (`article/gallery-curation.html`, master `Gallery curation v2.md`). Its figures are `gallery-top-scored` (the gallery judge's strict top 24), `gallery-twins` (re-picked onto `final139_general` at ckpt 152; its pair 2 is the true closest seated pair) and `gallery-output`.
  - **Full pipeline is v6 (`Full pipeline v6.md`):** the three parts, then "How I ran it" in Matt's words. Figures: `pipeline-overview`, `pipeline-hue-shares`, `pipeline-hue-extremes`, and `pipeline-growth`. All four bake from `builder/pool_study.py`, whose measurement lives in `artifacts/pool-study/` (kept).
  - **Finding good locations is v8, Training judges v7, Color palettes v7, and Rendering modes v5 (ckpt 151)**; each kept every figure in order. Finding good locations writes multibrot degrees as 3 to 6, and the twin channel as feeding the Julia families of degree 2 to 6 (ckpt 152).
  - §12 is "Deep zoom rendering" (`article/deep-zoom.html`, master `Deep zoom v3.md`). Minibrot descents holds what was "Automatic minibrot descents" (Matt: descents are an artistic composition, automation optional).
  - §14 is "Fractal math" (`article/fractal-math.html`, master `Fractal math v2.md`); its Pi section is two displayed limits.
  - The front page carries hand-written intro and Contents blurbs, with no master and no ✓ marks; the voice pass did not reach them.
  - `escape-families` has 18 panels: five planes (degree 2 to 6), each with two of Matt's Julia picks, then Phoenix. Its panel 5 was re-picked to `82bc9069` at ckpt 152 because Matt's packs picture is the old panel 5's seat.
- **★ The download page is "Wallpaper packs" (`wallpaper-packs/`),** distinct from the explorer's Gallery tab. Its figure is `packs-hero` (Matt's pick, a degree-3 Julia seat in threads, drawn by `render-link`), with no caption. Where the packs' own images live is decided when packs exist.

**★ THE SECTION-CUT TEMPLATE (Matt, ckpt 148). Done: Gallery curation (v2), Full pipeline (v6), Finding good locations (v8), Training judges (v7), Color palettes (v7), Rendering modes (v5, a prose pass only: Matt had reviewed it by hand). Next: other sections as Matt names them.**
- **The test for every passage:** would a reasonably intelligent CS undergrad think of this unprompted? If so, it collapses to a sentence or goes.
- **What stays:** the non-obvious insight that motivates the section, shown with a figure; Matt's own judgement calls; facts invisible from outside; honest notes on what was considered and turned out unnecessary.
- **What collapses:** each rule becomes one bullet with its number in it, and the algorithm becomes two sentences plus links to the code files.
- **What goes:** mechanism detail; plumbing another section covers; figures that illustrate a mechanism rather than a result.
- **Default when Matt says "keep the figures, tighten the text":** every figure and its caption stay, in order; headings may merge.
- **Process:** Claude reads the live master from Drive `prose\`, drafts the cut in chat with a list of what was cut and the facts to confirm; Matt corrects; Claude trashes the old master, creates the new one in `prose\` (these are small enough), and writes a placement prompt with a verify list at its foot. The placing CC checks the list from source and corrects the prose, reporting each change.
- **A sentence-level review uses a coloured docx:** numbered blocks of black context, red current text, green proposed text, and black context. Matt deletes the blocks he rejects and edits the greens; an apply prompt swaps by red text, found exactly once or skipped.
- **A figure-level review uses a numbered before/after HTML sheet in website `scratch/`**, and Matt answers item by item (left, right, or revert).

**★ THE SITE IS RE-BASED ON `final139_*` + `final140_general2000` — DATA ONLY.** The publishing audit (ckpt 152) found no stale URLs or retired terms and five clean pages; its text fixes are applied. What remains for "ready for publishing" is in OPEN 9.

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
- **★ Videos live on YouTube and are embedded, never self-hosted (ckpt 152).** **Double Descent** is uploaded UNLISTED at `youtu.be/MgmOF7Q-YIA` (file `mandelbrot-double-descent-4k60.mp4`). It is on the degree-3 multibrot plane, not degree 2. YouTube serves it as AV1 with BT.709 read correctly, and Matt checked the 4K. Its description is Matt's; it links the site, the two `go/` redirects and both repos, and its palette is Violet Bluebell (`along-the-starry-way-25`). Matt flips it to public at deployment.

## IN FLIGHT ACROSS THIS BOUNDARY
- **`fulls_ss3_ckpt148` (wallpapers), running between checkpoints.** Phases 1 and 2 are done; phase 3 renders 6,299 pictures into `E:\FractalWallpapers\full\` (about 107 an hour). **To resume after any stop:** paste the same prompt into a fresh session, or say "resume fulls_ss3 phase 3"; it skips finished pictures, and the OS lock makes a second `run` refuse and name the live pid. **To pause:** `fractal-wallpapers curate full-set pause --out E:\FractalWallpapers\full` (finishes the pictures in flight), or `pause --now`. `curate full-set status` reads progress. **While it runs, no prompt may touch the render path** (`colorize`, `release`, `explorer_link`, `embed_link`, `full_set`, or anything under `engine/`) **or run `cargo build --release` in wallpapers**, and the fast lane stays off. Other wallpapers edits are safe but commit with a pathspec. Its final report and README pool correction come at the end of the run.

## QUEUED IN DRIVE `prompts\`
None.

## NEXT CHECKPOINT GOAL
Matt raises it at the top of the checkpoint.

## OPEN (ordered) — Matt raises each
Items 3, 6, 8, 10 and 11 are closed; the numbering is kept.
1. **Mining is CLOSED; he reopens it.** Read `preserve\mining_laws.md`, then the reopen inventory in wallpapers `curation/LEGS.md`. The `final139_*` set is the PRE baseline, and `gallery-grade score-pool` runs before any solve. Retake any headroom census taken before 2026-09-26 (§Where we are).
2. **"Truly finalized": the commits (Matt raises it).** What waits on it: the twenty-one kept records and their recipes (tracking = publishing), and the pre-final history rewrite (which can also drop superseded website asset blobs).
4. **Website: the section-by-section review pass** (Matt brings a section's review doc, or asks for a direct cut; → OPEN 12).
5. **Deploy preparation (preparing, not deploying).**
   - Done: the favicon (F08); explorer links embedded in every download and release render; the two repo READMEs' funnels; the packs' host decided; Wallpaper packs in the rail; the double-descent 4K60 master (ckpt 151); **ckpt 152:** the repo rename to `fractals`, the staged assets committed and the site live but unadvertised, cross-platform CI green in both repos, the `go/` redirects, and Double Descent uploaded (unlisted) and embedded.
   - **Left:**
     - building the packs from `fulls_ss3`'s output and `membership.jsonl`, and uploading them (Releases for the smaller packs, Drive for the large);
     - a history rewrite before the final commit;
     - the remaining zoom videos: `deep-zoom-video` (first cut exists, paused on Matt's colour and ending) and `deep-descent-video` (a different descent video, not Double Descent), each uploaded to YouTube and embedded as a `video` row;
     - flipping the videos to public, then advertising the site.
   - **After that:** post the site to fractalforums.org.
7. **The Deep tab's follow-ups.**
   - **The gallery (33 frames, Matt's picks).** Matt adds frames over time, including frames centred away from any minibrot. He sends links, and a one-line prompt appends each row, pins `n` from the width rule, and bakes its thumbnail (→ `builder/README.md`). Julia frames are supported. One Filigree place appears twice, in two colourings, as asked.
9. **THE WRITEUP (Matt raises it; the session authors a prose master plus a placement prompt).**
   - **§Deep zoom rendering (`article/deep-zoom.html`, master `prose\Deep zoom v3.md`).**
     - **Placed figures:** `deep-f64-and-perturbation` (Porcelain Field, phase 0.41, absolute, period 0.295); `deep-shallow-and-deep` (its two panels do NOT share a colouring, on purpose); `deep-final-colorings` (a 2×2 of Matt's four links on the final frame of the glowdon `deep-zoom-descent` video, not Double Descent: Final frame, Leveled, Higher period, Palette switch); `deep-descent-rungs` (Chalcedony, absolute, λ 0, period 0.5); `deep-descent-pairs` (seats `afdb47c0`, `9c6a3d87`, glowdon; caption "Two frames, A and B (top), and the four ways to nest one inside the other (bottom)."); `deep-misiurewicz-pairs` (done, palettes included); the multibrots part (done).
     - **Placeholders:** `deep-zoom-video` and `deep-descent-video` (OPEN 5; each becomes a YouTube `video` row).
     - **Double Descent is FINAL (Matt, ckpt 151):** the favicon seat `double-descent_power_L0.38_a0.15_along-the-starry-way-25`, `smooth`, 4K60, at `artifacts/double-descent/4k60/video/` (linked to `E:\FractalStorage\fractal-website\double-descent-4k60`). Under the monotone cap rule its ending opens M₂ at about 61 periods, not 32; Matt accepted that. It is not supersampled.
     - **When the figure round finishes,** delete `preserve\minibrot_copies.md` and `preserve\deep_zoom_section.md`.
   - **Start here:** `start-pink-gallery` (six magenta, six rose) is a placeholder for his daughter's final picks. `start-modes` is two Mandelbrot rows Matt picked. The other `start-*` figures are placeholders Matt adjusts. The "darker pink gallery" link opens `magenta`; `rose` is the other honest choice (Matt's call). **The `start-video` caption is owed a fix:** it says "rendered in the explorer's Deep tab", but `zoom.py` made the video; it should read "A deep zoom into the degree-3 Mandelbrot set, rendered with the same perturbation code as the explorer's Deep tab." (→ OPEN 13).
   - **"Ready for publishing" — what the ckpt 152 audit left, all waiting on `fulls_ss3` or an idle box:**
     - Rendering fundamentals: "s = 4, so sixteen orbits" becomes s = 3 and nine, and `render-supersample`'s caption, alt text and right panel move to ss3.
     - Rendering modes: "supersampled 4×" becomes 3×; the wallpaper-render column is filled from real ss3 times (`E:\FractalWallpapers\full\progress.jsonl`, or a measurement on an idle box) and its placeholder note dropped; the candidate counts and shares are recomputed on an idle box.
     - Overview's release-render sentence, and every download promise (the index lead, Start here's zip, Overview's foot, the packs page), become true when the packs ship; no edit is planned.
     - Deep zoom's speed sentence ("about 15 seconds", "about seven times") is remeasured on an idle box.
12. **The section-cut pass:** other sections as Matt names them. Not yet cut: Overview, Escape-time fractals, Rendering fundamentals, Make your own palettes, Finding good wallpapers, Fractal atlases, Deep zoom rendering, Other artistic techniques, Fractal math, and Start here.
13. **Small follow-ups, each a short prompt (website unless named):**
    - the `start-video` caption fix (OPEN 9);
    - the stale "untracked" wording in code comments left by the asset commit (`stops.js`, `gallery.js`, `explorer.js`, `judges.js`, `checks.py`, `atlas.py`, `agreement.py`, and the `walk --help` string);
    - the `stamps` check may add render-link as a third embedder;
    - optional: `--remap-path-prefix` for byte-reproducible `engine.wasm` across machines (a rebake and a manifest line; then CI can assert the bytes).

Parked → `preserve\parked.md`.

## STATUS / KNOWN REDS
- ⚠ A website `builder check` beside a wallpapers merge can throw a transient "not in the candidate ledger" red; retry.
- ⚠ A report just copied to Drive `reports\` can read back EMPTY, or not appear in search, for minutes; retry once, then ask Matt to paste it.
- `builder check` was all green (24 checks) at the end of ckpt 152, with nothing skipped.

## RULINGS THIS ERA
ckpt 152 (2026-09-26). Reported prompts: `url_rename_wallpapers_ckpt152`, `url_rename_website_ckpt152`, `go_redirects_ckpt152`, `deploy_staged_assets_ckpt152`, `start_video_embed_ckpt152`, `start_video_links_ckpt152`, `ci_matrix_ckpt152`, `macos_palette_test_ckpt152`, `publishing_audit_ckpt152`, `publishing_fixes_ckpt152`, `packs_image_and_mid_ckpt152`, `publishing_revert_ckpt152`; `fulls_ss3_ckpt148` interim (phases 1 and 2).

- **The site is `fractals` (Matt):** repo and Pages path renamed; the local folder keeps its name.
- **Deploy (Matt):** the staging rule is lifted and the galleries are final enough to commit; the judges go through git.
- **Videos are YouTube embeds (Matt).** `deep-descent-video` will be a different descent video.
- **Figure drift is never a reason to change a figure (Matt).** He reverted most of the audit's re-picks item by item.
- **Exponential smoothing reads as smooth (Matt).**
- **Wallpapers CI failures get the best-practice fix without asking (Matt):** exact tests in float64 rather than a platform tolerance.

## KEEP LIST
**Drive `prompts\`:** keep `fulls_ss3_ckpt148.md` (in flight); wipe everything else.

**Drive `reports\`:** wipe everything. The final `fulls_ss3_ckpt148` report arrives later, in the next era.

**Drive `prose\`:** unchanged by the closeout. `Full pipeline v2 Matt` was trashed at ckpt 152. The live masters are `Start here v2.md`, `Overview v2.md`, `Escape-time fractals v1.md`, `Rendering fundamentals v1.md`, `Color palettes v7.md`, `Make your own palettes v4.md`, `Rendering modes v5.md`, `Training judges v7.md`, `Finding good locations v8.md`, `Finding good wallpapers v3.md`, `Gallery curation v2.md`, `Full pipeline v6.md`, `Fractal atlases v2.md`, `Deep zoom v3.md`, `Other artistic techniques v1.md` and `Fractal math v2.md`, plus `writing-guidance.md`. Four were edited in place at ckpt 152 (Deep zoom, Finding good locations, Make your own palettes, Overview) and keep their names.

The review docs' canonical copies are website `review\deep-zoom.docx` and `review\gallery-curation.docx`; the applied voice pass is archived in Drive `review\applied\voice-pass-2026-09-25.docx`.

**Wallpapers `scratch/`:**
- KEEP `fulls_ss3_ckpt148/` (the in-flight run's interim report, scripts and `results.json`), `place_radius_sheet/`, `retired_tentative/`, `preclose_ckpt125/off_list_stamps.txt`, `tuning_test/`, `leg_numbers.py` and `mbc140/` (§Deep zoom's picking sheets).
- WIPE everything else.

**Website:**
- `scratch/`: wipe all except `deep_gallery_sheet/` (the 65-tile sheets, for further picks). `duplicates/` and `publishing_diff/` go.
- **KEEP `artifacts/deep-zoom/`** (fields, coloured keyframes, MP4s), **`artifacts/double-descent/`** (the movie's fields, stills and cuts, including the final 4K60 master and its untagged original), **`artifacts/mathjax/`** (the fetched typesetter) and **`artifacts/pool-study/`** (the measurement behind the four Full pipeline figures, kept until "ready for publishing"). All are untracked.
- `artifacts/deep-gallery/` and `artifacts/cap-split/` are sweepable.

**`E:\FractalWallpapers\`:** KEEP `ss_test_ckpt148\` (the ss2/ss3/ss4 references; their embedded links carry the old URL, which does not matter) and `full\` (`fulls_ss3`'s output, in progress).

**`preserve\`:** `deep_zoom_section.md` and `minibrot_copies.md` stay until the figure round finishes. `art_techniques_links.md` stays until Matt rules.

**Outside both repos:** `C:\Tools\fraktaler-3\` stays until Matt removes it. The rustc 1.96.0 toolchain installed beside stable stays: WASM bakes and the website's CI pin need it.

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
