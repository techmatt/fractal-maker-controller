# fractal-corpus — labels, sampling, judge method, the accumulator

Changes when: labeling happens, a batch is registered, judge method moves. The label corpus MIGRATES with the project (state §OPEN 6); these rules govern it wherever it lives. Spec + the 1–4 rubric = `CORPUS_SCHEMA.md` (maker tree until migrated); per-batch roles → `docs/design/corpus_batches.md`.

## Laws
- **★★★ A LABEL ROW CARRIES ITS JOIN.** Label + complete render block/params in the SAME tracked row; a label keyed on an id whose meaning lives in a separate untracked file is orphaned when that file dies (proven twice: stage-2 joins, the 379 orphaned ranker labels). Wallpapers ships labels FLAT: label + complete join + batch id + registration flags; eligibility DERIVED, never stored per-row.
- **Canonical reader = the label store's resolver — never write another, never infer labeling state from raw image lists.** Originals never modified; revisions live in a per-source amendment overlay that the resolver prefers; the split is MANDATORY (in-row filling double-counts each source against its anchor twin); every training consumer routes through the overlay choke-point.
- **★★ The scale is 1–4. Class 4 = "exceptional wallpaper emission"** — preferred where available, NOT a new floor. **Class 4 is JUST A CLASS (Matt, firm):** no special case, no separate threshold, no per-family calibration; short of training data → harvest and label more. Anchor sheets are the bar, not a written rubric.
- ⚠ Multiple render regimes coexist in the corpus — **Matt: the labels hold; not to be raised.** Location label = max over crops; `decoded_class` ≠ human label.

## Sampling regime
- **★★ The disqualifying bias for an EVAL set is MODEL-DRIVEN SELECTION, not non-randomness** — a systematic grid or base-rate draw is eval-eligible; candidates a model scored well are not.
- **★★ Split registry is the SINGLE owner, FAIL-CLOSED:** unregistered ⇒ biased/train; contradiction ⇒ hard abort ⇒ **register a new generation method BEFORE its batch is built.** A new generation type is a NEW partition — register before building.
- **★★ Score-unconditioned eval instruments are EXEMPT from the forced-eval group cascade (Matt)** — biased group-mates stay TRAIN; model reads on those legs are mildly optimistic — fine for base rates, NEVER for fine AUC.
- **★ Nominal splits are not realized splits** — check realized shares before quoting a CI. (Wallpapers realized eval 8.86%; thin sides julia:mandelbrot 48 / julia:multibrot5 39; strict no-exemption rule RATIFIED — a thin eval side buys more score-unconditioned rows, never exemption machinery.)
- **★★ Location-grouped randomized splits are the default everywhere; group by the EXACT non-`c` axes, never by seed-`c` alone** — seed-c-alone once made a whole plane grid ONE spatial group; any family swept at a fixed parameter point has this failure available.
- **★★ §2a — CONTRADICTING STAMPED SPLITS FORCE A GLOBAL RE-DERIVATION** (or a frozen authority protecting an incumbent's eval). **§2b — anchored correction-sheet labels are TRAIN-SIDE ONLY, per-head.**
- **★★ THE EVAL-ONLY PIN — a split constraint OUTRANKING §2a's fixes**, wired at UNIT granularity; trainers assert on the c-INCLUSIVE coordinate, never `image_id` — a re-render under a fresh id cannot spend an instrument.
- **★★ A BLIND SHEET INFORMS EXACTLY ONE BOUNDARY, AND ITS DRAW'S QUALITY CONDITIONING CHOOSES WHICH** — design the conditioning for the boundary you intend to referee. Blind sheets are eval-only forever — never train, never re-drawn, never re-spent. Anchored sheets measure AGREEMENT with the incumbent, and a measured anchoring gap never transfers across heads; a rate off any prefilled sheet is a CEILING.
- Standing eval instruments (migrated as data): blind_minibrot (197, ≥4 boundary; drawn behind the good floor — its 97.0% ≥3 is the GATED intake's base rate) · blind_modes (150, ≥2). OPEN instruments owed: smooth_render ≥3 blind · a phoenix:classic score-unconditioned draw (single-point parameter space needs a VIEWPORT instrument).

## Judge method (folded from the retired models doc — governs every retrain)
- **★★ THE WINNER RULE:** a staged head becomes candidate only if (a) no overall pre-declared metric significantly worse (95% paired bootstrap) AND (b) the motivating slice significantly better, none worse; declare slices before numbers.
- **★★ CROSS-SEED COMPARISONS SCORE THE BAND, NEVER THE STAGED PICK ALONE** — a staged pick has sat bottom of its own band on the first held-out population it saw. A pick that spends a selection set leaves the BAND as the honest read.
- **★★ THE MODEL-SELECTION OBJECTIVE IS A CONTROLLED VARIABLE** — freeze selection to the baseline-comparable population; amendment before the re-run.
- **★★ CORN scale is train-prior-calibrated** — a retrain moves the whole probability scale; restatement modes → fractal-operating. Conditional-sigmoid caution → fractal-tutorial §CAUTIONS.
- **Never finetune** (small-data damage, proven). **★★ Never augment in a way that destroys the evidence the label was based on.**
- **Division of labor (semantics, transfers to any head roster):** the location head STEERS within-family and NEVER ranks or allocates cross-family (family-mean correlation was strongly negative) · render heads judge FINISHED renders of their own kind, never each other's · the palette head picks palettes within a location, never quality · winner's curse recurs at every selection level — steer/rank/select stay split.
- Correction-loop mechanics: relevant head pre-labels; presentation **SORTED good→bad by the head's score**, suggestion prefilled, accept-all-below sweep behind confirm; unreviewed suggestions never leave the page as labels; no blind rows or calibration aids in a correction sitting (firm). One manifest + one export per sitting (`order=file`); ≤1000 rows; anchor first, bulk second for a fresh scale.

## ★★ THE ACCUMULATOR — things Matt needs to label (merge into one sitting; don't over-label)
Spent by the ~500-row sitting (state §OPEN 5), correction-sheet mechanics, labeled through the wallpapers rig into its flat store; a human label takes per-location PRECEDENCE over machine stock, so a sitting re-anchors the allocation for free. By value-per-label:
1. **mandelbrot floor-passers** — 13 rows + a near-floor slice; prices the run-3 mix-ratio call; re-anchors the thinnest partition.
2. **Plane-channel deep admissions** — stratified by rung/width over run2's 474; the head starts agreeing a DECADE below the labeled band, and no label has ever seen 1e-6..1e-8 widths; feeds the N=6 call.
3. **Twin top slices** — julia:multibrot3's standing demand is retired by machine rows nobody has looked at (~30× machine/label currency), jm4/jm5 similar; twins were 61% of run2 admissions.
4. **Strange renders over new-channel material** — checks the acting bar's KEEP direction (the reject direction is eyeball-validated); also feeds the future labels-derived bar restatement.
5. **Released-row 3-vs-4** — released smooth rows saturate P(≥3); the P(≥4) column is the advisory doing real work; calibrate it.
6. **Carried maker-era items** (lower priority): phoenix machine-4s · human_q3plus floor-vein · maneuver-view ≥3 boundary · unclassed q4_harvest rows.
Merge opportunity: the deferred **niche draw** (~500 renders of threads/itinerary/de against Matt's wallpaper bar) rides the same sitting day as a separate sheet.

## Label noise — what it forbids
Disagreement is adjacent-category only: a real ordinal scale with a fuzzy boundary, not a learnability ceiling. **Forbids reading small AUC differences on the ≥3 boundary.** Pre-register bars before computing; verify the instrument's inputs actually change. **Matt: "noise is expected at all boundaries" — do not re-raise.**
