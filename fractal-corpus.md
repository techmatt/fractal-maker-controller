# fractal-corpus — labels, sampling, the rig

Changes when: labeling happens, a batch is registered, coverage moves. Spec + the 1–4 rubric itself = `CORPUS_SCHEMA.md`.

## The label corpus — read before counting anything
**Canonical reader = `label_store.resolve_score` — never write another, never infer labeling state from `images.jsonl`.** Labels live in three registered places (in-store `images.jsonl` + repo-root `labels/*.json` sidecars + the amendment overlay). Labels never-delete, committed; `decoded_class` ≠ human label; location label = max over crops. **8,467 pairs / 7,151 locations at ckpt 25; +730 crawl (81 = rule `interior_gt30_v1`) +580 harvest +870 combined harvest sitting (2026-08-03: 237/285/313/35 across classes; 35 fours in one sitting).**
- **★★ The scale is 1–4. Class 4 = "exceptional wallpaper emission"** — preferred where available, NOT a new floor. **Class 4 is JUST A CLASS (Matt, firm)**: no special case, no separate threshold, no per-family class-4 calibration; if there isn't enough to train well, harvest and label more. A written class-4 rubric is RETIRED (`retired.md`) — the anchor sheets are the bar.
- **★★ The amendment overlay.** `resolve_score(row, labels, amendments=None)` prefers a revision; without amendments returns the original, so the pre-revision boundary reconstructs as a one-liner. Revisions → per-source `amend_<batch>.json`; originals never modified. **The split is MANDATORY** (filling in-row would double-count each source against its anchor twin in the version-blind trainer). A revision batch shows null in its own `images.jsonl` — expected, do not "fix". **Every training consumer routes through the overlay — enforced** [code: `corpus_reader.iter_labeled` choke-point + build_manifest GATE 9; verified 2026-08-02].
- Two corpora share `labels/`, separation KEYED by registration — the window corpus carries 3-way STRING classes, never pooled with location rows. `image_id` collides across scale batches — `resolve_score` joins on `join_key` (canonical location identity incl. `fw`, plus palette/composition).
- ⚠ The corpus holds three render regimes (flat-8000 / old-auto / new-auto from 2026-07-31). **Matt's direction: the labels hold; not to be raised as a concern.**
- **★★ `loc_id` stability is a silent-failure seam** — the aug cache maps `loc_id` → coordinates (~171k tiles); a manifest rebuild that renumbers points every tile at the wrong location and training still completes with plausible numbers. **Any rebuild asserts tile↔location agreement in BOTH directions first.**

## Sampling regime — the whole ball game
| batch | usable as |
|---|---|
| `loose0_v3` (mandelbrot, 526) | unbiased base rate (3.4%) AND v8's forced mandelbrot EVAL floor |
| census `prospect_run1_baserate_*` (144) | the PINNED primary eval instrument; never train |
| `gather_v6` / band batches / `julia_ladder_j0` | train (rank/band-biased) |
| `blindspot_v6reject_v1` | never in q3-vs-rest eval (negative by construction) |
| steered_run2 blind (60) + dive blind (21) · `campaign1_blind` (298) | ranker train/eval; keeper calib |
| `phoenix_grid` (500) · `native_multibrot_band_v1` (300) | train-side only; never base-rate |
| `anchor_class4_v1` (60) | cross-family class-4 anchor; 52 rows are revisions |
| `minibrot_roster_v2` (487) | WINDOW corpus — 3-way string classes |
| `interior_band_v1` (80) | uniform-sampled high-interior; train-side hard negatives |
| supply-crawl `…_uniform_v1` (90) | PROMOTED TO EVAL (2026-08-02, v10 build) — the only score-unconditioned maneuver-view draw; 0/90 ≥3 bounds that supply ≤~3.3% |
| supply-crawl `…_strat_a/b_v1` (290+290) | train; spans every bin — the negative footing; labeled 2026-08-01 |
| `2026-08-02_label_seeded_v2_{a,b}` (291+289) | train (label/fit-selected, never eval); results → fractal-discovery |
| harvest sitting `2026-08-03_q4_combined_label_v1` = 3 registered batches (290×3) | ranked-harvest + near-minibrot ladder: train · uniform eval leg: EVAL (score-unconditioned) — labels merged 2026-08-03, route-merge live-proven |
| supply-crawl `…_exemplar_v1` (60) | train; similarity RETIRED after two null reads (fractal-discovery) |

- **★★ The disqualifying bias for an EVAL set is MODEL-DRIVEN SELECTION, not non-randomness** — a systematic grid, ladder or base-rate draw is eval-eligible; candidates kept because a model scored them well are not.
- **★ `assign_split` is FAIL-CLOSED** — an unregistered batch classifies as biased/train; a contradiction against the `label_store` registration hard-aborts. ⇒ **register a new generation method BEFORE its batch is built, or it silently lands train-side.** Split-group unioning includes SHARED MINIBROT ATOM as a seed (2026-08-02, protocol seed rule) — k-variant views of one atom are invisible to the spatial 1.5×-fw union.
- **★ Nominal splits are not realized splits** (a nominal 70/30 realized 17.2% eval) — check realized shares before quoting a CI. A forced-eval batch drops its biased neighbours (census-100%-eval + zero-biased-in-eval + zero-group-straddle can't all hold).

## What the corpus cannot tell you
Unbiased pool = 3 batches / **692 locations**: ~76% mandelbrot, ~21% julia:mb, ~3% native-mb, **0% phoenix, 0% julia:mandelbrot** — those two have NEVER been sampled unbiasedly; no draw size fixes it retroactively.
- **★★ The eval gap is PAID: `data/label_corpus/eval_instruments/q4_uniform_eval_v1.json`** (uniform leg, n=290, score-unconditioned, eval-registered) — unscreened base rates: julia:mandelbrot ≥3 **16.7%** [8.7–29.6] · phoenix ≥3 6.1% (zero fours in the leg) · **native mb3/4/5 0/144 at ≥2 — a verdict on the unscreened ∂M-shell draw, not a family ceiling.** Consumed at the next version's t_good. Phoenix remains the calibration priority (class 4 outnumbers class 3 in training, astride the cutpoint).
- Class-4 counts as of 2026-08-03: mb3 **9** · mb4 **8** · mb5 **16** (the earlier "mb3 zero anywhere" is dead). Mandelbrot: 0 class-4 in 526 unbiased ⇒ an unbiased draw there is mostly overhead.
- Base rate ≥3 [location-level]: julia:mb 0.451, mandelbrot 0.049, pooled 0.139. P(4|≥3): census julia:mb 22/65 = 0.338 [0.235–0.460]. **Class-4 eval today: 22 locations, all julia:multibrot.**
- (Rejected and stays rejected: a stratified holdout over the corpus — most of it is model-selected. Fresh per-family uniform draws are the paired instrument; the first set exists, above.)
- **★ Class-4 supply channel = biased harvesting of candidates for Matt to label** — the re-judge-the-old-top-bin seam is SPENT. ⚠ The revisit's 338 class-4s are a biased population (`mining_v3guided` + `julia_ladder_j0` heavy, train-side).

## The labeling rig — reuse, don't rebuild
`tools/viz/corpus_label.html?batch=…` (+ `?manifest=` for a blinded manifest), served by `tools/viz/serve.py`, which resolves relocated crops transparently.
- **Seeded shuffle per batch — never draw order.** Blind by default: hides score/verdict/arm, degree/period/band, `image_id` (encodes fate), prior labels. `r` reveals; reveal state recorded and exported [0 reveals across ~1800 labels].
- Canonical label-crop + VIVID `blue_orange` companion together — canonical is what the model sees, vivid is what Matt judges from. Export = ONE `labels.json`; revisions → `merge_amendments.py --apply`; fresh rows → `merge_scores.py --max-score 4`.
- **Anchor first, bulk second** for a fresh scale — but an anchor batch is CURATED: it calibrates a bar, it does not estimate a population. Calibration aids: never (fractal-operating, firm).
- **★ The batch-design template (amended 2026-08-03, Matt):** ONE combined sitting ≤1000 rows, single manifest + single export (`?manifest=…&order=file` — the page reshuffles client-side otherwise), **apportionment-sequenced to ±1 across (source_batch × family)** (the natural stride fails at ≥15 cells). Blindness: opaque ids post-shuffle; leak keys DROPPED, not nulled; the sheet dir holds NO `images.jsonl` (glob discovery would double-count) — guarded. **Non-optional builder stages, each injection-proven: interior>0.30 auto-1 `interior_gt30_v1`, NEVER shown to Matt (firm) · presentation morph-dedup at 0.974 · per-partition machine-1 discard (fractal-models owns the table; OFF for julia:mandelbrot).** Yields from any sitting are quoted raw AND one-per-cluster.

## Label noise — what it forbids
A ceiling effect localized to the old top category — resolved by the class-3 revisit; disagreement is adjacent-category only: a real ordinal scale with a fuzzy boundary, not a learnability ceiling. **Forbids: reading small AUC differences on the ≥3 boundary.** Pre-register bars before computing; verify the instrument's inputs actually change (`measurement_practice.md`). **Matt: "noise is expected at all boundaries" — do not re-raise.**
