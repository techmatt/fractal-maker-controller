# fractal-corpus — labels, sampling, judge method, the accumulator

Changes when: labeling happens, a batch is registered, judge method moves. The label corpus MIGRATES with the project (state §OPEN 5); these rules govern it wherever it lives. Spec + rubric = `CORPUS_SCHEMA.md` (maker tree until migrated); per-batch roles → `docs/design/corpus_batches.md`.

## Laws
- **★★★ A LABEL ROW CARRIES ITS JOIN.** Label + complete render block/params in the SAME tracked row; a label keyed on an id whose meaning lives in a separate untracked file is orphaned when that file dies (proven twice). Wallpapers ships labels FLAT: label + complete join + batch id + registration flags; eligibility DERIVED, never stored per-row.
- **Export/ingest discipline (2026-08-17):** the drop is `labels\<head>.json`, untracked+gitignored — **THE INGESTED STORE IS THE COMMITTED RECORD; ritual = export → ingest in the SAME session.** ONE path (`label ingest` → intake.run), count-verified, idempotent, append/overlay-only, both stores; rig mechanics → fractal-tutorial §THE REPO.
- **Canonical reader = the label store's resolver — never write another, never infer labeling state from raw image lists.** Originals never modified; revisions live in a per-source amendment overlay the resolver prefers; every training consumer routes through the overlay choke-point.
- **★★ THE SCALE IS 1–4 FOR EVERY HEAD (Matt, 2026-08-17).** Class 4 = "exceptional wallpaper emission" — preferred where available, NOT a new floor; **class 4 is JUST A CLASS (Matt, firm)**: no special case, no per-family calibration. Anchor sheets are the bar, not a written rubric; the ckpt-51 sitting's anchors DEFINE the strange-mode 4 bar. **The PROMOTION PASS is DONE (2026-08-18)** — every pre-existing strange 3 reviewed, verdicts landed as overlay revisions, originals untouched; top-censoring cleared (record = Drive reports). **Store scale is DECOUPLED from model class count** [code: finished.SCALE · RECIPES · finished_import.SOURCE_SCALE; pin = config-vs-recipe + config-vs-checkpoint-width; a recipe that cannot express a population verdict REFUSES to train — this pin is what forced the sanctioned 4-class retrain]. strange_render is the ADOPTED 4-class head; P(≥4) is live; the config-vs-checkpoint tests assert per-run, not root-only.
- ⚠ Multiple render regimes coexist in the corpus — **Matt: the labels hold; not to be raised.** Location label = max over crops; `decoded_class` ≠ human label.

## Sampling regime
- **★★ The disqualifying bias for an EVAL set is MODEL-DRIVEN SELECTION, not non-randomness** — a systematic grid or base-rate draw is eval-eligible; candidates a model scored well are not.
- **★★ Split registry is the SINGLE owner, FAIL-CLOSED:** unregistered ⇒ biased/train; contradiction ⇒ hard abort ⇒ **register a new generation method BEFORE its batch is built.**
- **Registered 2026-08-17 (all anchored=true, train-side, score_unconditioned=false):** smooth — mandelbrot_mix_pricing 63 · released_top_end 125; strange — threads_promotion 110 · itinerary_promotion 110 · release_bar_band 55 (incl. run8h/0081, Matt's flagged keep-direction row). **DISJOINT-DRAW CAVEAT: threads_promotion and itinerary_promotion share zero locations** — independent draws over admitted stock; they support the tier promotion but cannot compare modes per-location (registry description corrected 2026-08-18).
- **★★ Score-unconditioned eval instruments are EXEMPT from the forced-eval group cascade (Matt)** — biased group-mates stay TRAIN; fine for base rates, NEVER for fine AUC.
- **★ Nominal splits are not realized splits** — check realized shares before quoting a CI (realized eval 8.86%; strict no-exemption rule RATIFIED).
- **★★ Location-grouped randomized splits are the default everywhere; group by the EXACT non-`c` axes, never by seed-`c` alone.**
- **★★ §2a — CONTRADICTING STAMPED SPLITS FORCE A GLOBAL RE-DERIVATION** (or a frozen authority protecting an incumbent's eval). **§2b — anchored correction-sheet labels are TRAIN-SIDE ONLY, per-head.**
- **★★ THE EVAL-ONLY PIN — a split constraint OUTRANKING §2a's fixes**, wired at UNIT granularity; trainers assert on the c-INCLUSIVE coordinate, never `image_id`.
- **★★ A BLIND SHEET INFORMS EXACTLY ONE BOUNDARY, AND ITS DRAW'S QUALITY CONDITIONING CHOOSES WHICH.** Blind sheets are eval-only forever. Anchored sheets measure AGREEMENT with the incumbent; a rate off any prefilled sheet is a CEILING.
- Standing eval instruments (migrated as data): blind_minibrot (197, ≥4; its 97.0% ≥3 is the GATED intake's base rate) · blind_modes (150, ≥2 — **⚠ 6 rows' labels superseded by anchored promotion-pass revisions (Matt, 2026-08-18: simplest path); 144 remain blind; the ≥2/≥3 truths are byte-unchanged; the eval side now holds four 4s. Never read blind_modes at ≥4, and never count those 6 as blind**). OPEN instruments owed: smooth_render ≥3 blind · a phoenix:classic score-unconditioned VIEWPORT instrument.

## Judge method (governs every retrain)
- **★★ THE WINNER RULE:** candidate only if (a) no overall pre-declared metric significantly worse (95% paired bootstrap) AND (b) the motivating slice significantly better, none worse; declare slices before numbers.
- **★★ CROSS-SEED COMPARISONS SCORE THE BAND, NEVER THE STAGED PICK ALONE.** A pick that spends a selection set leaves the BAND as the honest read.
- **★★ THE MODEL-SELECTION OBJECTIVE IS A CONTROLLED VARIABLE** — freeze selection to the baseline-comparable population; amendment before the re-run.
- **★★ CORN scale is train-prior-calibrated** — a retrain moves the whole probability scale; restatement modes → fractal-operating. Conditional-sigmoid caution → fractal-tutorial §CAUTIONS.
- **A head's render cache must be COMPLETE against its stored rows before it trains** — `renders plan`/`renders build` are the precondition; shortfalls → fractal-tutorial §THIS ERA.
- **Never finetune.** **★★ Never augment in a way that destroys the evidence the label was based on.**
- **Division of labor:** the location head STEERS within-family and NEVER ranks cross-family · render heads judge FINISHED renders of their own kind, never each other's · the palette head picks palettes within a location, never quality · steer/rank/select stay split.
- Correction-loop mechanics: relevant head pre-labels; SORTED good→bad by the head's score; suggestion prefilled; accept-all-below sweep behind confirm; unreviewed suggestions never leave the page as labels; no blind rows or calibration aids in a correction sitting (firm). One manifest + one export per sheet (`order=file`); ≤1000 rows; anchor first for a fresh scale. Per-sitting correction rate = the head's report card; on modes a head has never seen, agreement is NOISE, not a rate.

## ★★ THE ACCUMULATOR — things Matt needs to label (merge into one sitting; don't over-label)
Spent: the ckpt-51 sitting's four draws · the strange-3 PROMOTION PASS (ckpt 52; record = Drive reports). Remaining, by value-per-label:
1. **Plane-channel deep admissions** — stratified by rung/width over run2's 474; no label has seen 1e-6..1e-8 widths; feeds the N=6 call whenever run planning resumes.
2. **Twin top slices** — julia:multibrot3/4/5 standing demand retired by unreviewed machine rows (~30×/10×/9×); precedence leverage.
3. **Paired threads-vs-itinerary draw** — CONTINGENCY, only if per-location mode comparison ever matters (current batches disjoint).
4. **Carried maker-era items** (lower priority): phoenix machine-4s · human_q3plus floor-vein · maneuver-view ≥3 boundary · unclassed q4_harvest rows.

## Label noise — what it forbids
Disagreement is adjacent-category only: a real ordinal scale with a fuzzy boundary, not a learnability ceiling. **Forbids reading small AUC differences on the ≥3 boundary.** Pre-register bars before computing; verify the instrument's inputs actually change. **Matt: "noise is expected at all boundaries" — do not re-raise.**
