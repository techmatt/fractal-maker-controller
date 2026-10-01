# fractal-state — checkpoint 157 (2026-09-30: phone support; the history rewrite of both repos; disk cleanup; the `knee` colour mapping (zoom videos, then the explorer's Straighten iter); the seahorse video on YouTube; the votes store and browser; vote-ranked packs with hand-picked previews and the deep gallery, all 19 zips rebuilt and re-uploaded; link fidelity; release audit and polish; `julia3_video_4k_ckpt157` still rendering)

## Where we are
Three phases, each depending strictly on the one before (→ fractal-discovery). Matt iterates from pictures, not counts. Phase 3 is his eye on the final seating, and **every planned collection has a viewer at its official size.**

**★ MINING IS CLOSED (Matt, 2026-09-21) UNTIL HE REOPENS IT.**
- The pool as merged on 2026-09-21 is the population, and the `final139_*` solves (§RECORDS) are the published galleries.
- On a reopen, read `preserve\mining_laws.md` whole, then wallpapers `curation/LEGS.md §Mining is CLOSED (2026-09-21) — reopen inventory`. State carries none of it.
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
- **★ STRAIGHTEN ITER (`knee`, ckpt 157):** on by default for new absolute work (knee 5000, λ 0.1); a link without `knee` is off, so every older link draws as before. The Period slider still moves in cycles across the frame.
- ⚠ A seat's `mode` in `gallery.jsonl` is ROUTED; render at `recipe["mode"]`.

## TONE CURVES AND LINKS
- **★ Every gallery seat's tone curve is recorded** (`artifacts/curation/autolevel_backfill.jsonl`).
- **★ THE LINK CONTRACT** (owner: website `explorer/README.md`) spells `curve` and `knee`. Wallpapers `explorer_link.query_of` writes links byte for byte like the site. The engine's `link.rs` reads `curve` and a stated `scale=leveled` (ckpt 157).
- **★ A Phoenix recipe that omits `c` or `p` means the classic constants, never zero** (ckpt 157). Both link writers once wrote zeros, which sent 17 Phoenix seats (50 links) to a plain disk; the 50 links are re-derived and the 17 full-size files re-stamped.
- **★ A LINK IS A PICTURE**, proven across every tab, mode and family by `explorer/bench/link-fidelity.mjs` (a 13-minute browser harness, not in `builder check`).
- **★ Seat-addressed figure panels carry the cap** whenever it differs from the policy; `builder check`'s `caps` check holds all 107.

## FULL-RESOLUTION WALLPAPERS AND PACKS
- **★ THE FULL SET:** 6,299 pictures at 2560×1440 ss3, JPEG q95 4:4:4, in `E:\FractalWallpapers\full\` with `membership.jsonl`. `curation/full_set.REGIME` is the one spelling. Every file carries its explorer link, and all 6,299 match.
- **★ THE PACKS (19 zips, rebuilt 2026-09-30) ARE IN RELEASE `wallpapers-2026-09-29`** on `techmatt/fractals`, replaced in place with `gh release upload … --clobber`. That was a one-time exception to "a rebuild is a new dated release", taken because the site is unadvertised; the next full rebuild may cut a new dated release with all 19. The site downloads through `releases/latest/download/<file>`.
  - **Best 30, 100 and 200:** the staged vote ranking, plus Matt's preview picks forced in even from outside the thousand (`wallpaper-packs/preview-picks.json`; four such seats today). They nest, and Best 200 sits in part 1.
  - **The main gallery, three parts:** the thousand plus every hand-pick from outside it, 1,008 in rank order (336 each). The explorer's gallery stays exactly the thousand.
  - **Twelve colour packs,** each in its own staged order.
  - **The deep gallery:** 28 hand-picked deep views (Matt's 15 plus `deep-random-dives`, deduplicated), rendered site-side by the native deep renderer at the full-set regime. Recipes: `builder/data/deep-pack.jsonl`. Deep pictures never enter the pipeline.
  - **Not shipped:** n=2000 and the mode collections.
- **★ THE RANKING:** summed votes, one per voter per seat; ties fall to the seeded plan's order. `builder packs stage` writes the staging page (`artifacts/packs-stage/`) and the plan inputs (`order.txt`, `forced.json`, one order per colour pack); the wallpapers pack plan takes `--forced` and `--orders` and refuses packs that don't nest or don't match.
- **★ PACK PREVIEWS (the packs page, live):**
  - Best 30, 100 and 200 and the main gallery show Matt's hand picks from `preview-picks.json`, chosen in the votes browser's pick mode.
  - The colour packs use the walk: voted members only, nothing shown elsewhere on the site, nothing used earlier on the page, at most two per hue family. A slot nothing fills shows "needs votes".
  - The deep gallery's five are a seeded draw across hues.
- **★ The wallpapers are licensed CC BY 4.0, credit Matt Fisher.** Both repos' code stays MIT.
- **★ FRIEND VOTES:**
  - **The store** is `C:\Code\fractal-drive-sync\votes\events.jsonl`: append-only, never in a repo, and losing it is a major failure.
  - **Voters:** matt (189 picks), jason, and website (Matt's flags on the site's own showcase pictures).
  - **Ingest:** Matt says "ingest NAME <links or files>" to CC in fractal-website. Ingest is idempotent, a trailing list letter is dropped ("MattB" adds to matt), and `builder votes browse` regenerates `artifacts/votes/index.html` (by person; by summed score).
  - **The final pack rebuild** comes after the last votes: stage → plan → zips → upload.

## ZOOM VIDEOS
- **★ VIDEOS USE THE `knee` MAPPING BY DEFAULT (Matt, ckpt 157):** one fixed curve of ν, so colour never flows over structure already on screen; a depth schedule does flow. Owner: website `builder/README.md`. The knee has one home, the engine's `coloring.rs`, which `zoom.py` calls.
- **★ Every video gets Midway and Final frame links** through its own `go/` redirects, and new videos are prototyped on the `preview` variant before the 4K render.
- **Double Descent** (`youtu.be/MgmOF7Q-YIA`) and **the seahorse descent** (`youtu.be/N_041iZNHvQ`, embedded on Deep zoom and the videos page) are UNLISTED. Matt flips them public at deployment.
- **The julia3 descent** (knee 5000, λ 0.157, period 1870, phase 0.091) is rendering at 4K60; its prompt places `go/julia3-mid`, the knee form of `go/julia3-end`, and the videos page's Midway cell.

## LAWS STATE STILL CARRIES
- **★ The degree-6 plane is never labelled** (`partitions.NEVER_LABELLED`).
- **★ Parabolic Julia sets are CLOSED (ckpt 147); Douady–Hubbard tuning is PARKED (ckpt 148); BLA stays removed (ckpt 149).**

## RETENTION AND STORAGE
- **★ The keep is five per `(place, mode)` plus one family allowance** (→ `curation/README.md`). Pinned rows and every published record's seats are prune-proof via `tentative.kept()`.
- **The ckpt-157 cleanup** freed 155 GiB on C: (246 GiB free).
  - **Gone:** every `fields/` dump (the roster's depth, rotation and repetition fields were released), the neutral JPEGs, and every `.leveled/` except the 2,035 beside kept seats. The sweep is licensed in `curation/README.md`.
  - **Archived to E::** `sheet`, `render_grade` and 14 closed walk legs.
  - **Behind junctions to E:** `C:\Code\fractal-maker` (now at `E:\FractalStorage\fractal-maker`) and the website's deep-zoom and double-descent `video/`, `fields/` and `colour/` trees.
  - **Backups:** the July `fractal-generator` backup moved from D: to `E:\FractalStorage\backups\`.
  - **Still on C::** the ~82 GiB of pool pictures. Moving them is an optional future prompt of about 25 files, needing one picture-path lookup that fails loudly when E: is absent.
- ⚠ **`e_drive_consolidate_ckpt157` is QUEUED** to move everything fractal on E: under `E:\Fractals\` (`FractalStorage`, `FractalWallpapers`, `history_undo_ckpt157`). After it reports, every `E:\…` path in these docs is INVALIDATED. The report lists the doc mentions to update at the next closeout.

## RECORDS: THE PUBLISHED SET
- **★ The store is exactly the twenty-one published records:** the twenty `final139_*` and `final140_general2000`, tracked whole.
- `portable.GENERAL_CHECK` = `final139_general`; `portable.REFERENCE` = `final139_green`. Nothing is re-cut while the pool is closed.
- **★ BACKUPS ARE MATT'S.** `storage export` runs only at his direction and is never proposed.
- **★ `git grep <stamp>` before calling any record stray.**

## THE REPO AS A CLONE SEES IT
- **★ BOTH HISTORIES WERE REWRITTEN (ckpt 157).**
  - History-only non-code blobs were stripped, keeping every code commit. The website clone went from 270 to 156 MiB, and wallpapers from 31 to 22 MiB.
  - Tags were re-pointed ONCE, to tree-equivalent commits: `weights-2026-09-14` and `wallpapers-2026-09-29`. The never-move rule holds again, and a tag is never deleted and recreated, because that drops its release to a draft.
  - The `weights-v1` release and tag are gone.
  - `E:\history_undo_ckpt157\` holds the undo mirrors, the commit maps, and the only copy of the first location judge's weights. Matt keeps it.
  - Both remotes are https through `gh`.
- **★ The website's CI checks out wallpapers at `explorer/engine.manifest.json`'s pin.**
- **★ A fresh box continues every stage from a `storage export` alone** (→ `preserve\fresh_box.md`).
- **★ CUDA is opt-in.** ⚠ This box syncs `--extra cuda`. **★ Both repos build and run on Windows, Linux and macOS, and CI proves it.**
- ⚠ Drive the makers through `.venv/Scripts/fractal-wallpapers.exe`. Concurrent prompts in one checkout commit by pathspec and stage by hunk.
- ⚠ `perturb.wasm` builds on rustc 1.96.0 (`RUSTUP_TOOLCHAIN=1.96.0`).
- ⚠ `dive_candidates.below_normal()` was a silent no-op on 64-bit Windows until ckpt 157.

## WEBSITE
**★ The site is LIVE BUT UNADVERTISED** at `techmatt.github.io/fractals/` (repo `techmatt/fractals`; the local folder stays `C:\Code\fractal-website`). Until Matt advertises it, it never needs preserving or keeping in sync. Every fact about the site is owned by the website repo:

| Topic | Owner |
|---|---|
| Explorer: tabs, Deep, phones (the Pictures \| Controls switch, pinch, `pointers.js`), the link contract, Straighten iter, the link-fidelity harness | `explorer/README.md` |
| Deep kernel, `nuclei::classify`, the twin | `explorer/perturb-wasm/README.md` |
| Builder: figures, packs (staging, the ranking, previews, the deep pack), `votes` (ingest, browse), zoom videos, head tags, `404.html`, every `builder check` check (31, incl. `caps` and `heads`) | `builder/README.md` |
| Traps, the rail rule, pathspec and hunk staging | `CLAUDE.md` |
| Style and voice | `prose\writing-guidance.md` · website `CLAUDE.md` |
| Per-page status | `docs/page-review.md` |

- **★ NAVIGATION:** the rail reads in three groups: Start here | Wallpaper packs, Tools and data, Deep zoom videos | Contents. The site header carries the same links.
- **★ PHONES (ckpt 157): reasonable, not overboard.** Every page fits at 375 px, and Make your own palettes fits at 360 px.
- **★ PALETTE CREDIT:** pages may say "palettes I made" as long as they link to Make your own palettes, which credits Claude writing them from three checked-in prompts, with the caveat that hand-tailored palettes are more beautiful.
- **★ Head tags** come from each page's own first sentence (`builder/heads.py`), with absolute `og:` URLs as the one exception to relative links.
- **★ A LINK IS A PICTURE. The site never tells a reader a view is "not exact." No figure reuses a picture unless the reuse is intentional. Figures are never changed because they drifted. Figure recipes are never lost.**
- **★ The site reads as its final form; the Oxford comma; American spelling; THE VOICE** (`prose\writing-guidance.md` §Voice).

**★ PROSE: MATT REOPENS IT PIECEMEAL, ONE PASSAGE AT A TIME.** This era's prose edits were made in their masters in place: Fractal atlases, Wallpaper packs (the deep gallery and its opening sentence), Make your own palettes, Color palettes, Training judges, Rendering modes and Gallery curation.

**★ THE EXPLORER'S BAR (Matt):** complexity is a cost; text is for the artist; the left panel changes the view, the right manipulates it; the shallow view and Deep are one tool; Deep auto-renders. Wasm threads are out. ⚠ This box drifts about 30% between identical runs.

## IN FLIGHT ACROSS THIS BOUNDARY
- **`julia3_video_4k_ckpt157` (+ addendum 1), website, RUNNING.**
  - It renders the julia3 descent at 4K60 in the knee style to `E:\FractalStorage\fractal-website\julia3-descent-4k60\`, places `go/julia3-mid`, the knee form of `go/julia3-end` and the videos page's Midway cell, and commits the record.
  - Addendum 1 makes votes on the 17 pre-fix Phoenix link spellings count, reader-side.
  - Its report arrives next era; then Matt uploads the video and sends the YouTube id.

## QUEUED IN DRIVE `prompts\`
- **`e_drive_consolidate_ckpt157`** (wallpapers; locks both repos). Run it only when nothing writes to E:, meaning after the julia3 render.

## OPEN (ordered): Matt raises each
Items 2, 3, 6, 7, 8, 10, 11, 12, 14, 15 and 16 are closed; the numbering is kept.
1. **Mining is CLOSED; he reopens it.**
4. **Prose reopens piecemeal (Matt).**
5. **Deploy preparation (preparing, not deploying).** Left:
   - more friends' votes, then the final pack rebuild and upload;
   - the julia3 video: render (in flight) → YouTube → its id into the pending row;
   - more deep zoom videos for the videos page, in the knee style;
   - flip the videos public, advertise the site, then post to fractalforums.org and other fractal forums.
9. **Figures that are Matt's to supply:**
   - the `start-gallery` and `pipeline-overview` seeded stand-ins;
   - Start here's other `start-*` placeholders;
   - the pink picks' two placeholders, which make "my daughter picked these" untrue until she picks two more.
13. **Small follow-ups (all optional):**
    - `--remap-path-prefix` for a byte-reproducible `engine.wasm` (a rebake);
    - the atlas rebuild for the nine replayable tone dots (skip unless Matt notices one);
    - the Period slider's one-decade minimum travel on deep frames (Matt looks first);
    - `links.py` maps `phoenix_m` records to the wrong name and gives them no constants (latent; a record using it would fail loudly when the site is built);
    - **page descriptions:** the clause rule cuts at a list comma, so the home page's description names one of "two things" and Make your own palettes' names two of three prompts. Exclude a comma before "and"/"or", or shorten those first sentences;
    - Color palettes says "The prompt ships with the repository" right after "prompts I wrote";
    - `palette-moods`' provenance rule would draw 29 strips if re-run;
    - on phones, the atlas marks overlap (a tap opens the top one), and 12 composite figures draw their labels at about 3–4 px;
    - `zoom.py --mapping` is still required, so "knee by default" is a convention, not code.
17. **Moving the pool pictures to E:** optional; about 25 files (§RETENTION AND STORAGE).

Parked → `preserve\parked.md`.

## STATUS / KNOWN REDS
- `builder check`: 31 checks green at `release_polish_ckpt157`. `preclose_website_ckpt157` skipped the run at Matt's word.
- ⚠ A website `builder check` beside a wallpapers merge can throw a transient ledger red; retry.
- ⚠ A report just copied to Drive `reports\` can read back empty for minutes; retry once, then ask Matt to paste it.

## RULINGS THIS ERA
ckpt 157 (2026-09-29/30). Reported prompts:
- **wallpapers:** `history_audit`, `history_rewrite`, `disk_audit`, `disk_cleanup` (+ addendum 1), `e_drive` (queued).
- **website:**
  - phones, menus and fixes: `phone_support` (+ addendum 1), `mobile_followups` (+ addendum 1), `website_micro`, `link_fidelity` (+ addendum 1);
  - colour and video: `julia3_palette`, `julia3_curve`, `explorer_knee`;
  - votes and packs: `flag_sheet`, `votes_ingest_browse`, `votes_ingest_mattB`, `packs_stage`, `packs_stage_voted` (+ addendum 1), `packs_forced_members`, `packs_best_rebuild` (+ addendum 1), `deep_pack`;
  - the release: `release_audit`, `release_polish`, `preclose_website`;
  - plus `deep_zoom_video_ckpt156`'s final report.

Matt's rulings:
- **The history rewrite:** option (a) on both repos, pushed over https through `gh`, and the tags re-pointed once.
- **Zoom videos use the knee mapping by default.** The explorer's Straighten iter is on for new absolute work and off for links that don't name it.
- **Packs:**
  - summed votes rank everything;
  - Matt hand-picks the previews for Best 30, 100 and 200 and the main gallery, and the best packs absorb picks from outside the thousand;
  - the main gallery's zips grow past a thousand instead of re-solving it;
  - the colour packs' previews follow the voted-only walk;
  - the live page shows the staged picks ahead of the zips.
- **The deep gallery is a pack** of 28 hand-picked deep views.
- **The palette judge was trained on Matt's ratings,** and the site says so.
- **"Degree-N" only where the extra precision helps;** "degree-3 Mandelbrot set" is fine in captions.
- **Disk:** C: freed as listed, and everything fractal on E: goes under `E:\Fractals\` (queued).

## KEEP LIST
**Drive `prompts\`:** keep `julia3_video_4k_ckpt157.md` and its `_addendum1.md` (in flight), and `e_drive_consolidate_ckpt157.md` (queued). Matt wipes the rest himself.

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

**Wallpapers `scratch/`:** KEEP whichever of the old keep list still exists (`place_radius_sheet/`, `retired_tentative/`, `preclose_ckpt125/off_list_stamps.txt`, `tuning_test/`, `leg_numbers.py`; the disk audit found most of them already gone). WIPE everything else.

**Website:**
- `scratch/`: KEEP `julia3_palette_ckpt157/` and `julia3_curve_ckpt157/` until the julia3 video reports, and `deep_gallery_sheet/` and `deep_minibrot_candidates/` if present. WIPE the rest.
- `artifacts/`:
  - KEEP `deep-zoom/`, `double-descent/` and `julia3-descent/` (with their E: junctions), `mathjax/`, `pool-study/`, `dive-reference/` and `deep-pack/`.
  - `packs-stage/` and `votes/` regenerate.
  - `cap-split/`, `dive-candidates/` and `random-dives/` are sweepable.
- `temp-pics/` is Matt's.

**`E:\`:** KEEP everything (`FractalStorage\`, `FractalWallpapers\`, `history_undo_ckpt157\`) until the consolidation moves it under `E:\Fractals\`.

**`preserve\`:** `art_techniques_links.md` stays until Matt rules.

**Outside both repos:** `C:\Tools\fraktaler-3\` stays until Matt removes it. The rustc 1.96.0 toolchain stays.

## OWED
Nothing.

## SCRATCH/ARTIFACT FLAGS
- **★ The standing keep roster lives in the repo:** `src/fractal_wallpapers/README.md §The standing keep roster`.
- ⚠ CRLF drift is real; check with `git ls-files --eol`.

## PARKED / SETTLED
→ `preserve\INDEX.md`, which lists every file. Never re-list them here.
