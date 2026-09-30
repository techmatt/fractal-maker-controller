# fractal-corpus — STUB: the label laws a non-labeling session can break

Changes when: labeling returns. **The whole method — sampling regime, judge-reading caveats, sitting design, the closed sittings — moved to `preserve\corpus_method.md` at ckpt 134** (no sitting is foreseeable in the remaining horizon; Matt). **Read that file, and `preserve\judge_training.md` for a retrain, BEFORE specifying any sheet, sitting, split or retrain.** Mechanics live in the wallpapers repo (`labeling/README.md`, `models/README.md`, `data/batch_caveats.md`). Nothing is accumulated for Matt to label.

## Laws
- **★ NO DEGREE-6 ROW IS EVER LABELLED (Matt, 2026-09-16)** — `partitions.NEVER_LABELLED` refuses at every label door; a sheet naming one is refused whole.
- **★ LOSING HAND-LABELED DATA IS A MAJOR FAILURE** — nothing rewrites, deletes or re-keys a label row; a revision is a later row, LATEST-WINS; the canonical readers are `store.resolved()` / `finished.resolved()`, never write another. A label row carries its join (label + complete render block in one tracked, flat row).
- **★ `labeler:null` = MATT'S LABELS, except rows cast by a rule (e.g. `rule:interior_gt30_v1`): a reader of "Matt's ratings" filters on human origin. Matt is the ONLY human labeler.** Origin rules protect exactly eval-split integrity and taste attribution; otherwise a label is a label.
- **★ THE SCALE IS 1–4 FOR EVERY HEAD.** `friend_votes` and `spiral` are ATTRIBUTE stores — never the 1–4 scale, never pooled with a quality store. Friend votes arrive as Saved links through the website's `builder votes ingest` into the append-only `C:\Code\fractal-drive-sync\votes\events.jsonl` (never in a repo); `votes export-order` writes the packs `--order` file (→ website `builder/README.md`).
- **★ THE REJECTION PASS MARKS ONLY `1`s AND AN UNMARKED TILE IS NOT A LABEL** (the human veto → fractal-state).
- **★ LABELING IS AN EVAL ACTIVITY, AFFORDABLE WHEN NEEDED** — labels serve objectives the next retrain cannot deprecate; no eval instrument is built for a retrain (Matt, ckpt 103: he is the instrument). Sheets are pre-labeled and sorted good→bad.

## Judge reading — what every session still needs
- **★ THE RENDER JUDGE IS A GATE, NOT A TOP-END RANKER**: no order inside its own top on any kind. `P(≥4) ≥ 0.5` is a TRUSTED quality gate (Matt) and reads as a well-calibrated ≥3 screen. The top end is Matt's eye on the final seating.
- **★ THE FINE HEAD'S LEVEL IS TRUSTED, NOT ONLY ITS ORDER (Matt, 2026-09-07)**; `p_fine`, `p_coarse` and the bars are closed (→ fractal-state). **The hue-bias worry is CLOSED (Matt, ckpt 115).**
- **★ A JUDGE FLIP IS ONE ACT** — adoption + floor refit + FULL rescore (→ `preserve\judge_training.md`). The render judge is NOT regime-robust: fit and read on the label-geometry column.
- **★ A q3+ VERDICT IN ANY STORE IS A PROVEN ROOT** (`supply.proven.derive`; → `preserve\mining_laws.md`).
- **At depth (ckpt 156; 817 dive candidates; [human n=15/57]): the location judge transfers** (AUC 0.88 on Matt's top 15; twelve of fifteen in its top fifth). **The wallpaper and gallery judges do not**, under absolute or leveled colouring alike: they sit near a less-interior baseline, and their rank correlation across the two colourings is about 0.3, so they read colouring more than place. Published as Deep zoom's judges fold (`builder/deep_judges.py`; scores in `builder/data/deep-judges-scores.jsonl`). The location judge's input recipe is owned by wallpapers `models/location_view.py`.
