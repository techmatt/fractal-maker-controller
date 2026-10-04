# fractal-state — checkpoint 160 (2026-10-03/04: structured deep-dive pilots run, then closed and parked; a page of about 500 dives and their Julia sets published and linked from Deep zoom; a forum image of the walk; both repos' `scratch/` wiped whole)

## Where we are
Three phases, each depending strictly on the one before (→ fractal-discovery). Matt iterates from pictures, not counts. Phase 3 is his eye on the final seating, and **every planned collection has a viewer at its official size.**

**★ MINING IS CLOSED (Matt, 2026-09-21) UNTIL HE REOPENS IT.**
- The pool as merged on 2026-09-21 is the population, and the `final139_*` solves (§RECORDS) are the published galleries.
- On a reopen, read `preserve\mining_laws.md` whole, then wallpapers `curation/LEGS.md §Mining is CLOSED (2026-09-21) — reopen inventory`. State carries none of it.
- ⚠ A reopened mine reads most pool pictures from the E: mirror (§RETENTION AND STORAGE).
- ⚠ Before 2026-09-26, `headroom.population` never passed spiral scores to the solve, so every `curate headroom` census and `pool_draw` reading taken before then counted spiral places as uncapped. Production solves were never affected. Retake any such census before relying on it.

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

**★ THE HUMAN VETO IS SHIPPED** (→ `curation/README.md`): Matt marks ONLY `1`s; an unmarked tile is not a label.

**★ A THEMED PASS RELAXES THE BAR INSIDE ITS OWN CELL** (`solve.themed_fine_bar`). ⚠ `--themed CELL` names a codebook cell; the family pass is `--collection <family>`.

**★ FAMILY PASSES FLOOR AT `mode_policy.seat_floors(n)`; A MODE PASS FLOORS AT 0.** ⚠ The floor is not monotone.

**★ COLOUR:** a hue family is not the union of its four cells (→ `palettes/README.md`). Curation constrains the 48 coloured cells only. The palette group cap is `0.075·n` themed and `0.025·n` general. K is Matt's; Claude never proposes reopening K.

**★ A GALLERY PAGE IS PRESENTED STRATIFIED** (`curation/page_order.py`). **★ GUARD RULINGS: loosening only, nothing loosened.** **★ `pool_scores.jsonl` IS ONE-SHOT: mine → merge → `gallery-grade score-pool` → solve.**

## MODES, PHASE, PALETTE
- **★ Seven targeted-gallery modes.** `curvature` is `UNMINED`.
- **★ The explorer's render-mode roster is thirteen** (`listedModes()`). **★ It shows ENGINE NAMES** for modes and families, and the article teaches the same names.
- **★ Exponential smoothing reads as "smooth" on the site**; recipes keep `exp_smoothing`.
- **★ Texture weight, rotation and phase are CLOSED; palette replication is PARKED.** `data/palettes/palettes_for_random_choice.csv` (232 maps) is the approved-for-random list.
- **★ The palette modes `scale`, `lambda`, `period` and `knee` are EXPLORER-ONLY** (→ fractal-engine).
- **★ STRAIGHTEN ITER (`knee`):** on by default for new absolute work in the explorer; a link without `knee` is off, so every older link draws as before.
- ⚠ A seat's `mode` in `gallery.jsonl` is ROUTED; render at `recipe["mode"]`.

## TONE CURVES AND LINKS
- **★ Every gallery seat's tone curve is recorded** (`artifacts/curation/autolevel_backfill.jsonl`).
- **★ THE LINK CONTRACT** (owner: website `explorer/README.md`) spells `curve` and `knee`. Wallpapers `explorer_link.query_of` writes links byte for byte like the site. The engine's `link.rs` reads `curve` and a stated `scale=leveled`.
- **★ A Phoenix recipe that omits `c` or `p` means the classic constants, never zero.** The website's `links.py` spells `phoenix_m` as `phoenix_plane` with its constants.
- **★ A LINK IS A PICTURE**, proven across every tab, mode and family by `explorer/bench/link-fidelity.mjs` (a browser harness, not in `builder check`).
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
- **★ PACK PREVIEWS:** Best 30, 100 and 200 and the main gallery show Matt's hand picks; the colour packs use the voted-only walk (nothing shown elsewhere on the site, at most two per hue family), so a change to what the site shows moves them and `builder packs --import` re-runs the walk; the deep gallery's five are a seeded draw.
- **★ The wallpapers are licensed CC BY 4.0, credit Matt Fisher.** Both repos' code stays MIT.
- **★ FRIEND VOTES:**
  - **The store** is `C:\Code\fractal-drive-sync\votes\events.jsonl`: append-only, never in a repo, and losing it is a major failure.
  - **Ingest:** Matt says "ingest NAME <links or files>" to CC in fractal-website; `builder votes browse` regenerates the browser.
  - **★ The votes are sufficient for now (Matt, ckpt 159).** A pack rebuild (stage → plan → zips → upload) happens only when Matt decides enough new votes have arrived; never proposed.

## ZOOM VIDEOS
- **★ Four videos, all PUBLIC on YouTube (Matt, 2026-10-01):** Double Descent (`MgmOF7Q-YIA`), the seahorse descent (`N_041iZNHvQ`), the julia3 descent (`GcJnRBlqSHw`) and the multibrot3 descent (`zYHpYwFDQbM`, section "A degree-3 Mandelbrot set spiral"). All four are embedded on Deep zoom videos.
- **★ KNEE IS THE CODE DEFAULT FOR VIDEOS:** `zoom.py` takes knee when no `--mapping` is given; an explicit mapping still wins. Owner: website `builder/README.md`. The knee has one home, the engine's `coloring.rs`.
- **★ Every video gets Midway and Final frame links** through its own `go/` redirects, and new videos are prototyped on the `preview` variant before the 4K render.
- `builder descent --direct` takes a single Multibrot link as one stage; without it, a single Multibrot link is read as a twin chain.

## THE SHOWCASE VIDEO (DRAFT)
- **★ A silent ~30-second 1920×1080 30 fps MP4 of the explorer's real UI**, for Reddit, HN and Mastodon. Shallow renders show at real speed (previews included); only Deep-tab waits are cut, and deep views are cuts (Matt, ckpt 159).
- **Demo mode** (`demo=1`: drawn cursor with click pulses, a fixed Dive landing hook, hidden Deep progress, a caption bar) and the tour script `explorer/bench/showcase.mjs` are committed; owner website `explorer/README.md §Demo mode`. One take is one command, about 3 minutes.
- The path (gallery → lime chip → hero D → zoom → palettes → modes on 5B → Julia → Atlas → Dive → deep cuts → caption "Mandelnaut Explorer · techmatt.github.io/fractals/explorer") is in the committed tour script. The draft take (32.3 s) and its planning sheet were wiped with `scratch/` at ckpt 160; a retake regenerates it.

## THE PAGE OF DIVES AND THEIR JULIA SETS (ckpt 160)
- **★ Published at `deep-zoom/dives-and-julia-sets/`** and linked by one sentence at the end of Deep zoom's Random dives passage. It stays out of the rail and the header and has no text beyond section headings and two controls (Fixed / Random coloring; Show Julia twin).
- **What it holds:** about 500 existing random dives that land on a gallery view placed inside a minibrot, the location judge's top picks per degree (200 / 100 / 100 / 50 / 50 for degrees 2–6), plus the Deep zoom figure's panels and the deep gallery forced in. Each has a Julia twin at its centre.
- **★ "Carried" is internal shorthand for that landing kind and never appears in reader-facing text** (the folder and title were renamed for it).
- **★ The twin's rules (Matt):** a twin with a central black disk is zoomed out until the disk is about 5% of the frame's width, never to the whole Julia set; every twin is coloured by a fresh absolute fit on its own field, palette kept.
- **★ Its images are tracked (Matt's ruling; about 100 MB)** so the page loads fast.
- **It rebuilds from the record alone:** `builder/data/julia-dives-picks.jsonl` and `python -m builder.julia_dives page`. Owner: website `builder/README.md §The page of dives and their Julia sets`. The saved fields were wiped with `scratch/`, so a recolour is a re-render.

## START HERE AND OTHER FIGURES
- **★ The pink picks are Matt's daughter's twelve**, placed at seed 20260930 from her full list (`article/pink-gallery.jsonl`); a re-pick is a new `chosen` line.
- **★ Start here's gallery figure is a seeded draw from the voted leftovers** (seed 1): voted pictures from any collection, minus everything shown elsewhere on the site, at most two per hue family, no touching tiles sharing a family. `builder start start-gallery --replace --gallery-seed N` redraws it; a new vote never moves it.
- **★ A figure panel may show another artist's work** under a CC license that allows non-commercial sharing, credited and linked (panel `credit`, source kind `external`; the rule is in website `CLAUDE.md`). Other artistic techniques opens with the hand-directed art section and two such panels.
- **★ On phones, the twelve `modes-*` sheets swap to a 640-wide version below 30rem**, and repeated taps on overlapping atlas marks step through the pile (ckpt 159).

## LAWS STATE STILL CARRIES
- **★ The degree-6 plane is never labelled** (`partitions.NEVER_LABELLED`).
- **★ Parabolic Julia sets are CLOSED (ckpt 147); Douady–Hubbard tuning is PARKED (ckpt 148); BLA stays removed (ckpt 149).**
- **★ Structured deep dives are CLOSED AND PARKED (Matt, ckpt 160):** copy-in-copy chains and minibrots framed at a fixed screen size (→ `preserve\parked.md`, fractal-engine §Deep render).

## RETENTION AND STORAGE
- **★ Everything fractal on E: lives under `E:\Fractals\`:** `FractalStorage\` (the ARCHIVE tier), `FractalWallpapers\` and `history_undo_ckpt157\`. Every older `E:\FractalStorage` or `E:\FractalWallpapers` spelling is dead.
- **★ The keep is five per `(place, mode)` plus one family allowance** (→ `curation/README.md`). Pinned rows and every published record's seats are prune-proof via `tentative.kept()`.
- **★ THE POOL PICTURES LIVE ON THE E: MIRROR (ckpt 158).** A pool picture name resolves from C: first, then from the archive's `pool_pictures/` mirror, and raises `ArchiveUnreachable` when E: is configured but absent. Wallpapers `paths.Tiers` and the website's `builder/renders.py` `Tiers` both follow the rule (→ `picture_mirror.py`, `storage pictures`, website `builder/README.md`).
  - Kept seats and protected rows stayed on C:, as did 56 pictures behind website figures.
  - ⚠ Retraining `gallery_grade` needs its pictures restored to C: first (`require_hot`); most of its corpus is on E:.
- **Behind junctions to E::** `C:\Code\fractal-maker` and the website's video trees (`deep-zoom`, `double-descent`, `julia3-descent`, `multibrot3-descent`).

## RECORDS: THE PUBLISHED SET
- **★ The store is exactly the twenty-one published records:** the twenty `final139_*` and `final140_general2000`, tracked whole.
- `portable.GENERAL_CHECK` = `final139_general`; `portable.REFERENCE` = `final139_green`. Nothing is re-cut while the pool is closed.
- **★ BACKUPS ARE MATT'S.** `storage export` runs only at his direction and is never proposed.
- **★ `git grep <stamp>` before calling any record stray.**

## THE REPO AS A CLONE SEES IT
- **★ BOTH HISTORIES WERE REWRITTEN (ckpt 157).** Tags were re-pointed ONCE, to tree-equivalent commits; the never-move rule holds again, and a tag is never deleted and recreated, because that drops its release to a draft. `E:\Fractals\history_undo_ckpt157\` holds the undo mirrors, the commit maps, and the only copy of the first location judge's weights. Matt keeps it.
- **★ The website's CI checks out wallpapers at `explorer/engine.manifest.json`'s pin.**
- **★ A fresh box continues every stage from a `storage export` alone** (→ `preserve\fresh_box.md`).
- **★ CUDA is opt-in.** ⚠ This box syncs `--extra cuda`. **★ Both repos build and run on Windows, Linux and macOS, and CI proves it.**
- ⚠ Drive the makers through `.venv/Scripts/fractal-wallpapers.exe`. Concurrent prompts in one checkout commit by pathspec and stage by hunk.
- ⚠ `perturb.wasm` builds on rustc 1.96.0 (`RUSTUP_TOOLCHAIN=1.96.0`).
- **`engine.wasm` carries no local paths since ckpt 159** (`--remap-path-prefix`); builds from different checkout paths still differ through cargo's path-dependency metadata, a known gap left open (→ `explorer/README.md`).

## WEBSITE
**★ The site is LIVE AND ADVERTISED since 2026-10-01** at `techmatt.github.io/fractals/` (repo `techmatt/fractals`; the local folder stays `C:\Code\fractal-website`). Whether it must now be kept in sync is Matt's to rule. Every fact about the site is owned by the website repo:

| Topic | Owner |
|---|---|
| Explorer: tabs, Deep, phones, the link contract, Straighten iter, demo mode, the link-fidelity harness, native-vs-Wasm numbers (`§Measured`) | `explorer/README.md` |
| Deep kernel, `nuclei::classify`, the twin, the chain cap rule, the low-period catalogue, the count a framed minibrot needs | `explorer/perturb-wasm/README.md` |
| Builder: figures (incl. credited external panels), packs (staging, ranking, previews, the deep pack, uploads), `votes`, zoom videos, Random dives (generator, survival, judge scores), the page of dives and their Julia sets, the resolver, head tags, every `builder check` check | `builder/README.md` |
| Traps, the rail rule, pathspec and hunk staging, the external-image license rule | `CLAUDE.md` |
| Style and voice | `prose\writing-guidance.md` · website `CLAUDE.md` |
| Per-page status | `docs/page-review.md` |

- **★ THE EXPLORER IS NAMED MANDELNAUT (Matt, ckpt 159).** On every page, the first mention of the explorer reads "Mandelnaut Explorer" and later mentions stay "the explorer"; the explorer's `<title>` is "Mandelnaut Explorer — Making Fractal Wallpapers" and its H1 "Mandelnaut"; the rail and `go/` titles read "Mandelnaut Explorer". Start here's heading stays "Fractal explorer" (its `#fractal-explorer` fragment). The site manifest keeps the site's name. The "open in fractal explorer" figure mark is unchanged.
- **★ NAVIGATION:** the rail reads in three groups: Start here | Wallpaper packs, Tools and data, Deep zoom videos | Contents. The site header carries the same links.
- **★ PHONES: reasonable, not overboard.**
- **★ PALETTE CREDIT:** pages may say "palettes I made" as long as they link to Make your own palettes, which credits Claude writing them from three checked-in prompts.
- **★ Head tags** come from each page's own first sentence (`builder/heads.py`); a series is never cut at a list comma. A page with no prose carries an authored description.
- **★ A LINK IS A PICTURE. The site never tells a reader a view is "not exact." No figure reuses a picture unless the reuse is intentional. Figures are never changed because they drifted. Figure recipes are never lost.**
- **★ The site reads as its final form; the Oxford comma; American spelling; THE VOICE** (`prose\writing-guidance.md` §Voice).

**★ PROSE: MATT REOPENS IT PIECEMEAL, ONE PASSAGE AT A TIME.** This era's only prose edit was one sentence added to Deep zoom, linking the page of dives, made in its master in place.

**★ THE EXPLORER'S BAR (Matt):** complexity is a cost; text is for the artist; the left panel changes the view, the right manipulates it; the shallow view and Deep are one tool; Deep auto-renders. Wasm threads are out. ⚠ This box drifts about 30% between identical runs.

## IN FLIGHT ACROSS THIS BOUNDARY
Nothing.

## QUEUED IN DRIVE `prompts\`
Nothing.

## OPEN (ordered): Matt raises each
Items 2, 3, 6, 7, 8, 9, 10, 11, 12, 14, 15, 16 and 17 are closed; the numbering is kept.
1. **Mining is CLOSED; he reopens it.**
4. **Prose reopens piecemeal (Matt).**
5. **Deploy.** **Matt tracks where the site is posted himself (ckpt 160); the docs carry no posting list.** Left: more deep zoom videos for the videos page, in the knee style.
13. **Small follow-ups (all optional):**
    - the atlas rebuild for the nine replayable tone dots (skip unless Matt notices one);
    - the Period slider's one-decade minimum travel on deep frames (Matt looks first);
    - `palette-moods`' provenance rule would draw 29 strips if re-run.
18. **The showcase video is a draft (Matt, ckpt 159).** Beat 3's zoom into the spiral's eye reads as rotation, not travel: re-aim it toward something that changes as it approaches. The last take ran 32.3 s against a ~30 s target. A retake is one command (§THE SHOWCASE VIDEO).

Parked → `preserve\parked.md`.

## STATUS / KNOWN REDS
- `builder check`: green at `carried_dives_publish_ckpt160`.
- ⚠ A website `builder check` beside a wallpapers merge can throw a transient ledger red; retry.
- ⚠ A report just copied to Drive `reports\` can read back empty for minutes; retry once, then ask Matt to paste it.

## RULINGS THIS ERA
ckpt 160 (2026-10-03/04). Reported prompts, all website:
- `dive_chain_audit_pilot`, `minibrot_size_pilot`, `dive_candidate_sheet`, `random_dives_audit`;
- `carried_dives_500`, `carried_dives_twins`, `carried_dives_twin_fit`, `carried_dives_publish`;
- `walk_descent_image` (a one-off forum image; nothing tracked).

Delivered as a micro-task, assumed handled: `pre_closeout_ckpt160` (the page's `noindex` removed; the parked entry written).

Matt's rulings:
- **Structured deep dives are closed and parked.**
- **A view placed inside a minibrot is the landing kind worth showing others;** the published page is built from those.
- **The page's images are tracked,** and the page is indexed.
- **The Julia twin's framing and colouring rules** (§THE PAGE OF DIVES AND THEIR JULIA SETS).
- **A forum image may show rescaled judge scores;** that ruling covered that one image only.
- **Matt tracks the site's postings himself.**
- **Both repos' `scratch/` are wiped whole at this closeout;** nothing in either is kept.

## KEEP LIST
**Drive `prompts\`:** nothing to keep. Matt wipes it himself.

**Drive `reports\`:** wipe everything.

**Drive `votes\`: DURABLE, never wiped.**

**Drive `prose\`:** the live masters are unchanged in name (all edits this era were made in place):
- `Start here v2.md`, `Deep zoom v4.md`, `Wallpaper packs v1.md`, `Tools and data v1.md`, `Deep zoom videos v1.md`;
- `Overview v2.md`, `Escape-time fractals v1.md`, `Rendering fundamentals v1.md`;
- `Color palettes v7.md`, `Make your own palettes v4.md`, `Rendering modes v5.md`;
- `Training judges v7.md`, `Finding good locations v8.md`, `Finding good wallpapers v3.md`;
- `Gallery curation v2.md`, `Full pipeline v6.md`, `Fractal atlases v2.md`;
- `Other artistic techniques v1.md`, `Fractal math v2.md`;
- `writing-guidance.md`.

**Wallpapers `scratch/` and website `scratch/`:** wiped whole at ckpt 160 (Matt). Nothing is kept in either.

**Website `artifacts/`:**
- KEEP `deep-zoom/`, `double-descent/`, `julia3-descent/` and `multibrot3-descent/` (with their E: junctions), `mathjax/`, `pool-study/`, `dive-reference/` and `deep-pack/`.
- `packs-stage/` and `votes/` regenerate.
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
