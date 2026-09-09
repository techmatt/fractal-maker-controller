# fractal-state — checkpoint 117 (2026-09-08)

## Where we are
THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE: (1) the LOCATION hunt · (2) the WALLPAPER hunt · (3) the final curation SOLVE + release render. `MODE_POLICY` is the one place a mode carries a standing; Matt iterates from pictures, not counts. Phase 3 is Matt's eye on the final seating. **NO PUBLISHING OF ANY KIND until Matt raises it — never ask, never list it.**

**★ THE FINAL GALLERY SHIPS AT n=1000 (Matt, ckpt 117), and THEMED COLLECTIONS OF n=200 ARE PART OF THE PRODUCT.** Nothing has touched themed since he said so. n=2000 is not the direction; making n=1000 better is. "Better" means true quality, NOT maximizing `p_fine` — maximizing it would restrict the gallery to a tiny subset.

**★ THE BAR: `p_fine(≥4) ≥ 0.50`, `DEFAULT_FINE_BAR = 0.50`, fill n=1000.** Ratified ckpt 115 and **CLOSED**. ⚠ There is no CLI spelling for the unbarred population: `--fine-bar 0` is a bar of zero and still excludes every unread row; `fine_bar=None` in process is the only way back. ⚠ `curate growth` and `curate solve k-sweep` inherit the bar.

**★ NEVER PROPOSE REOPENING K.** Not as a question, not as a closeout item, however strong the measurement pointing at it. Matt has had to say this repeatedly. The colour-cell allowance is assumed good; he raises it himself if he ever wants to. The ckpt-117 measurement below does NOT reopen it.

**★ THE `p_fine` SEATING IS THE WAY; `rank_key` IS DEPRECATED AS AN OFFER AND NOTHING MORE.** `--key` offers `{cascade, p_ge4}` through `solve.OFFERED_KEYS`; `solve.KEYS` still holds all three. **`rank_key` IS NOT RETIRABLE**: `cascade_order` is built on `ranking_for`'s mapping and lays the fine head over its top, so the cascade IS the rank key below the bar. Reopening it means proposing a replacement below-bar order, never deleting a key.

**★ THE LABEL CORPUS IS IN THE POOL, AND THE OLD JOIN REGIME IS OVER.** `label_migration merge` put **5,329 scored rows** (human classes 3 and 4, derived at candidate geometry from both finished stores) into the ledger — 2,314 already there, **3,015 new** — under their own merge stamp. Ledger 337,960 → 340,972. **Every one of Matt's 2,107 graded-4 wallpapers is now a ledger row BY KEY.** The derivation is an identity claim, not a resemblance: re-rendered keys came back byte-identical. ⚠ The old ruling that the label stores and the ledger overlap by PLACE and not by key describes a regime that no longer holds — it is history, not a constraint. Retention pruned only 3 of 5,329 because `a_label_row_joins_to_it` protected 252.

**★ THE FINE BAR REJECTS SEVEN IN TEN OF MATT'S OWN 4s, AND THAT IS THE CENTRAL OPEN QUESTION ABOUT n=1000.** Exact fates of all 2,107 in `20260908T211552Z`: **117 off the roster** (weight-0 modes, no bar ever read them, no rule ever refused them) · **502 below the coarse bar** (never reach the fine head, since `score-pool` runs on coarse-clears only) · **832 below the fine bar** (`p_fine` median 0.056) · **524 refused** (`p_fine` median 0.903) · **132 seated**. The render judge separates Matt's 3s from his 4s cleanly; the fine head barely does at the median and does at p90. Whether the head is right or is selecting on an axis that is not Matt's taste is unresolved and is an eye question. Pages → `scratch/label4_fate_0908/`.

**★ THERE IS NO HONEST SCORE COLUMN OVER THAT POPULATION.** 1,271 of the 1,824 finished-store rows are inside the shipped render judge's own train side, so `p_ge4` is largely recognition for them (60.3% over the whole page; the migration's 70.3% was over its own 5,329). And **all 312 gallery-grade rows are inside the fine head's 1,000-row corpus** — 245 fitted, 67 stopping — so `p_fine` is recognition for those too. `p_fine` is honest for the two finished stores (1.1% overlap) and for nothing else. On a gallery-grade card the human grade is the only independent thing.

**★ `cell_allowance` IS THE TOP REFUSAL AND THE ROW THAT TOOK THE SEAT IS USUALLY WORSE.** Of the 524 refused: `cell_allowance` 348, `location` 102, `another_place_is_the_same_place` 71, `twin` 3. Pairing each refusal with the row whose departure its rule would accept: **326 of 453 paired cards have a NEGATIVE gap, median −0.1638.** That is what *marginal* means — the seat a cell would give up is the weakest in that cell — so **"beat it" means took the seat, not scored better**. 348 cell-allowance refusals land on just **28** distinct pictures. Definition and its guard → `curation/` (`competitors` reproduces 450 of 450 recorded refusals or refuses outright). ⚠ This is a measurement, NOT an argument to reopen K.

**★ 81.6% OF THE GRADED 4s SIT WHERE THE GALLERY HOLDS NOTHING.** 1,719 of 2,107; only 388 places are held at all, 132 by the graded row itself, so just **256** lost their place to a different picture. The dominant fate is not "the head chose something else", it is "nothing was chosen there" — a thousand seats over 5,318 places in the view.

**★ LEVELLING IS DECIDE-ONCE, REPLAY-UPWARD (adopted ckpt 117).** The curve is derived at candidate geometry and higher-resolution renders inherit it. **Nothing entered identity** — `key_of` is byte-identical over 20,000 live rows. `measured` still means this render's own base statistics; provenance names where the curve came from; `levelling_of` needs no fourth word and the website's three are untouched. A release now inherits rather than measures: the curve changes, the act-or-not verdict did not (12 of 12). ⚠ The release comparison was taken at 1280×720 ss2, not at release geometry, so the magnitude at 2560×1440 ss4 is unmeasured.

**★ `mine.make` DREW EVERY VARIED CANDIDATE BARE, AND THE SAME CLASS OF BUG WAS FOUND IN FOUR RENDERERS.** `mine.make` never passed `mode_params`, so a leg naming a variant recorded it, keyed it and drew the bare mode — **10,664 rows across 13 legs**, the damage route being `depth.Shot`. `candidate_ledger.rerender` had it twice (one arm accidentally protective). Fixed, with a guard written as *every renderer draws the same picture for the same recipe*, byte-compared, plus a must-differ-from-bare arm. **Still unfixed:** `solve.render_seats` does not pass `curve`/`palette`; `shrinkage._render_one` drops `mode_params` and re-measures levelling at label geometry; `manufacture` drops `mode_params`. Twelve seats were exposed, seven rewritten, and **six of 1,000 seats had been held on a picture the pool would not have chosen**.

**★ THE `both` SETTINGS CORNER IS RETIRED BY MATT'S EYE (ckpt 117), OVERRIDING THE ckpt-104 RULE.** A cell was to leave only at zero clears; `both` clears 4 of 40 and the rule would have kept it. Matt's reading of the by-place sheet: the right-most column is too dark, consistently and heavily negative on `P(≥3)`. The other three cells are genuinely mixed and stay. **★ AND THE FRAME IS A PARAMETER SWEEP, NOT A ROSTER VERDICT** (Matt): the goal is to exclude always-bad ranges and sweep the rest. Opacity and threshold are currently a hand-enumerated roster of five cells while the palette side samples gamma across a continuum, which is the wrong shape for a knob that should be swept.

**★ THE WHITEWASH FIX WORKS AND IS SMALL.** Near-white goes from 3.8% of the mask to 0.000 at every cell, but chroma only moves 0.021 → 0.027 against 0.067–0.138 for every other mode's seats. **Losing white is not gaining colour** — pushed harder the multiply goes through darkness, not through colour. The mode is pastel by construction. ⚠ The ckpt-116 reading that this mode cannot make a vivid picture was taken on BARE candidate renders and is retired as evidence. The ckpt-104 roster ruling itself stands: the 188 variants of `dtm_variants_20260902` were really drawn and judged, at LABEL geometry through the sheet, whose renderer passed the settings. What never happened is a variant reaching the POOL.

**★ EXPRESSIBILITY IS CLOSED.** The candidate path hard-codes `colorize.CURVE` and the plain palette recipe, so 6,420 of 11,849 derived recipes are outside what mining can draw — gamma alone is 98.5% of that and is a sampled continuum (4,178 distinct values), `log` alone is zero, mirror never moves. But the inexpressible half scores **lower** on median and p90 in both label-4 classes, so widening the palette draw buys nothing. ⚠ That verdict is the fine head's; by Matt's own labels the two halves are comparable. 1,000 of 1,000 seats are expressible.

**★ `p_fine` COVERAGE IS EXACT BY ARITHMETIC, NOT BY LUCK.** Of 297,321 unscored ledger rows, **exactly zero** clear their own mode's render-judge bar; per mode `with_p_fine == q4_rows` in all thirteen accepted modes, because `score-pool` runs on coarse-clears at the same height `headroom.bars` uses. ⚠ **`pool_scores.jsonl` is a one-shot file**: above-bar rows merged after the last `score-pool` are unread and therefore unseatable. **Mine → merge → score-pool → solve.** Nothing enforces that ordering. Second reopening route: a mode under `FALLBACK_LOCATIONS` clears on `p_ge3`, which the fine head does not read at all.

**★ THE SOLVE DOES APPLY A BAR OF ITS OWN.** `solve.solve` carries `fine_bar`, `DEFAULT_FINE_BAR = 0.50`, applied to the WHOLE POOL before the per-mode bars, on the gallery-grade head. The per-mode `headroom.bars` gate is separate and is on the render judge's `p_ge4`. Two stacked gates. `solve.Q4_BAR = floors.RELEASE_ADVISORY = 0.50`; `headroom.FALLBACK_BAR` is the **same** constant on `p_ge3` under `FALLBACK_LOCATIONS = 25`. The bar's height is one number; only the cutpoint moves per mode.

**★ ALL THIRTEEN ACCEPTED MODES SEAT AT n=1000.** The six absent ones are weight-0 and refused at pool construction, never reaching a bar. `ceiling.TAU = 0.034281`, `TWINS = 2`. The colour cell allowance is binding — roughly 40 of 48 cells at their 42-seat allowance.

**⚠ SEATS-CHANGED IS NOT A MEASURE OF POOL CHANGE.** 96 seats and 73 places moved for **six** rows leaving the pool — 16× amplification. The greedy seed plus swap plus augment settles into a different local optimum under a tiny perturbation. Never read a seat-for-seat diff as a finding.

**⚠ ESTIMATES ARE MEASURED ON AN IDLE BOX.** A render estimate taken beside the fast lane was 6× wrong (5.5/min against 26.7/min). The `CLAUDE.md` rule about idle-box measurement applies to estimates as much as to lanes.

**This era (ckpt 116→117, one day).** The label corpus was derived at candidate geometry, scored, merged and solved; levelling became replay; four renderer holes were found and one class of bug closed with a general guard; the exact fate of every graded 4 was computed and paged; the whitewash fix was drawn for the first time and its `both` corner retired.

**Records.** 66. `20260908T144844Z` (first cascade record) · `20260908T201911Z` · `20260908T211552Z` (current). ⚠ **`211552Z` is honestly WORSE than `201911Z` on `solve.Objective.order`** — shortfall 6 → 12, which outranks worst seat (identical, 1.50391) and sum (1881.561 → 1885.675). Cause: the direct-trap repair removed six collapsed rows from the view; `direct_trap_multiply` went 31 → 25 clearing against a floor of 16 and 15 → 11 seated, `itinerary` 27 → 25 as collateral. **The old record's better shortfall was met by pictures that do not exist.** ⚠ `211552Z` is itself stale once PRECLOSEOUT's repair lands. Nothing is deleted — Matt has no reason to delete any record. The four the site stands on are unchanged: `20260902T161757Z` · `20260902T164622Z` · `20260904T023748Z` · `20260904T233233Z`. `20260906T133236Z`'s hold is still undecided.

## IN FLIGHT ACROSS THIS BOUNDARY
**`PRECLOSEOUT_ckpt116_renderer_holes_and_repair_0908`** — four parts: the three remaining renderer holes plus a guard generalised over every renderer in the tree; `mine.make` recording its autolevel stamp; re-render and re-score of the 10,652 varied rows; `curate autolevel backfill` over the full `protected_keys()` set. It does NOT re-solve, by instruction. Read its report cold and file it.

## QUEUED IN DRIVE `prompts\` — none.

## NEXT CHECKPOINT GOAL — NOT SET. Matt raises it.

## OPEN (ordered) — Matt raises each
1. **The 70%, and what to do about the head.** Retrain, a labeling sitting, or nothing — Matt's answer at ckpt 117 was "nothing until you've read v2; this is an open topic for next checkpoint".
2. **Themed collections at n=200.** Part of the product, untouched. Every themed pass to date ended in near-zero pictures at the tail; which cells the themed collections are FOR is undecided.
3. **The parameter sweep for `direct_trap_multiply`.** Opacity and threshold as swept ranges rather than a five-cell roster, with the `both` corner excluded.
4. **`pictures/` in the ten `runs` legs.** 5.37 GiB, held three independent ways, replayability total.
5. **The augment inner clock — a proposal, not applied.** `chain_at` has no clock check inside its walk; a pass overran a 300 s budget by 74%. The gate failed: two n=2000 tentative records exist under a bound stage.
6. **Records-only picture retention.** Direction → `preserve\retention_design.md`. Regeneration determinism is now much better than it was — see the levelling change.
7. **`carriers.jsonl`** at 65.9% of the 1 MiB history guard. A cross-repo seam with the website's `builder/palettes.py:carriers()`.
8. **`itinerary.jsonl`'s guard** at 62% of 786,432; roughly nine drops of horizon.
9. **Website — CLOSED.** Matt closed it 2026-09-08 and had to say so twice. **Do not write website prompts, do not iterate on site details, do not raise site defects until he says resume.** His own editing of the text is what matters there. Per-page status lives in `docs/page-review.md`. The front page's Gallery curation blurb is known wrong — it omits the fine bar and welds a false causal chain onto a true clause — and stays wrong until he reopens.
10. **The reframe channel's cadence.** Running dry: `g10` converted 384 fires into 2 productive with 376 unresolved.
11. **`20260906T133236Z`'s hold** — held tentative, appears nowhere in the website repo.

Parked → `preserve\parked.md`: augment at n=2000; the rung-frame overwrite; medium refactors; the `tia` bound question; the `groups.jsonl` re-cut; `BOUND_BLOCKS` 8; the K re-sweep (**never propose it**); the desire list as an explicit instrument; the `inventory.feasibility` colour-allowance formula on paper.

## STATUS / KNOWN REDS
**NO KNOWN REDS.** The direct-trap reproduction red is diagnosed and the mechanism fixed; the 10,652 rows carrying readings of the wrong pictures are PRECLOSEOUT's job.

Fast lane **4,060 passed / 129 deselected, ~130 s**, green on an idle box. The slow lane ran once this era at 4,136 passed with nothing skipped. ⚠ Run BESIDE a render leg the fast lane read 219 s with `test_twins.py`'s wall-clock refill guard red, green in 1.96 s alone — the documented load failure behaving as documented. `ruff` clean. The crate is untouched this era.

## RULINGS THIS ERA
→ `preserve\rulings_method.md §ckpt 117`, and the domain rulings in the docs themselves.

## KEEP LIST
Drive `prompts\`: KEEP `PRECLOSEOUT_ckpt116_renderer_holes_and_repair_0908`; **wipe everything else**, including the superseded `SHOW_ckpt116_labeled_q4_fate_0908` and its addendum, which were never run. `reports\`: **wipe everything** — all were read. Wallpapers `scratch/`: KEEP `label4_fate_0908/`, `label_migration_0908/`, `dtm_whitewash_0908/`; **WIPE everything else**, including `show_n1000_0908/` and `general_mine_0908/`. Website `scratch/`: unchanged from ckpt 116.

## OWED
Nothing.

## SCRATCH/ARTIFACT FLAGS
**★ THE STANDING KEEP ROSTER LIVES IN THE REPO — `src/fractal_wallpapers/README.md §The standing keep roster`.** Read it there; this doc keeps no copy. ⚠ Nothing on it is protected by `orphans`' reference set; it is a set of rulings rather than a mechanism.

⚠ **`artifacts/render_folds/` DOES NOT EXIST on either tier.** `read_assignment` refuses, so `renders dose`, `renders grade` and `renders deploy` refuse.

⚠ **`.leveled/` DIRECTORIES ARE SWEEPABLE** — `orphans` reaches them by the name each JPEG would have. What cannot be written is a BOUNDED sweep of the rest: 1.6% of directories, 1.3% of bytes. → `preserve\leveled_identity.md`, and ⚠ that file may still carry the old wrong wording.

Per-checkpoint: three new records are prune-protected like every record. `artifacts/curation/depth/*/fields` keeps growing at roughly 226 MB a leg and the sweep cannot reach it. ⚠ **Two `label_migration` rows are the only pool rows the plain render path cannot reproduce** — authored-palette recipes; `re_render` correctly refuses them and nothing else in the tree says so. ARCHIVED (RESTORE before reuse): unchanged from ckpt 106.

## PARKED / SETTLED
→ `preserve\parked.md`, `preserve\rulings_corpus.md`, `preserve\rulings_curation.md`, `preserve\rulings_sourcing.md`, `preserve\rulings_engine.md`, `preserve\rulings_website.md`, `preserve\rulings_method.md`, `preserve\sourcing_channel_laws.md`, `preserve\retention_design.md`, `preserve\solver_design.md`, `preserve\leveled_identity.md`, `preserve\deep_shelf.md`. The old `settled_rulings.md` is a stub index.
