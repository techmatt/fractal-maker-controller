# fractal-state — checkpoint 116 (2026-09-08)

## Where we are
THREE PHASES, EACH DEPENDING STRICTLY ON THE ONE BEFORE: (1) the LOCATION hunt · (2) the WALLPAPER hunt · (3) the final curation SOLVE + release render. `MODE_POLICY` is the one place a mode carries a standing; Matt iterates from pictures, not counts. Phase 3 is Matt's eye on the final seating. **NO PUBLISHING OF ANY KIND until Matt raises it — never ask, never list it.**

**★ THE BAR IS THE DEFAULT NOW: `p_fine(≥4) ≥ 0.50`, `DEFAULT_FINE_BAR = 0.50`, fill n=1000.** Ratified ckpt 115 and **CLOSED** — going past 0.50 reduces diversity, which was evaluated, discussed and concluded; Matt reopens it himself if he ever wants to. Where-the-bar-breaks is dropped from OPEN and is not a measurement anyone should take. ⚠ **There is no CLI spelling for the unbarred population any more**: `--fine-bar 0` is a bar of zero and still excludes every unread row; `fine_bar=None` in process is the only way back. ⚠ **`curate growth` and `curate solve k-sweep` inherit the bar**, so a sweep taken from 2026-09-08 on is not comparable with one taken before.

**★ THE `p_fine` SEATING IS THE WAY; `rank_key` IS DEPRECATED AS AN OFFER AND NOTHING MORE (Matt, ckpt 116).** `--key` offers `{cascade, p_ge4}` through `solve.OFFERED_KEYS`; `solve.KEYS` still holds all three. **`rank_key` IS NOT RETIRABLE**: `cascade_order` is built on `ranking_for`'s mapping and lays the fine head over its top, so **the cascade IS the rank key below the bar** — retiring the code would retire the cascade's below-bar half. `_prune_ranks` still ranks retention on it and the 62 older records still replay. Reopening it means proposing a replacement below-bar order, never deleting a key.

**★ THE FIRST CASCADE RECORD EXISTS: `20260908T144844Z`** — cascade key, `fine_bar 0.50` both recorded, page at `artifacts/curation/tentative/20260908T144844Z/index.html`. Seat for seat and bit-identical to the night's `full` counterfactual. 63 records, 7 published; **this one is NOT published** and is in neither `.gitignore` nor `tentative.PUBLISHED`. `protected_keys()` 6,000 → **6,673**, of which 673 are named by no other record.

**★ AT n=1000 THE GALLERY IS SATURATED (measured, ckpt 116).** A full unaimed night bought **33 rendered seats plus 105 that changed hands**, for objective 1876.602 → 1877.205 — **+0.03%** — with the worst seat unmoved. The pool it enriched grew 10,974 → 11,120 rows over 6,297 places and the greedy seed went 792 → 803. So mining now buys option value for a later re-solve, and quality inside themes and conditional galleries, rather than visible movement at this n. The ckpt-113 saturation reading reproduced exactly.

**★ THE GENERAL-LEG GALLERY-GRADE RATE IS 29.0% — never measured before ckpt 116.** 146 of 504 clears reach 0.50, 99 reach 0.75, 58 reach 0.90. **★ AND AIMING IS CLOSED AS A POLICY.** The instrument works — 3.15× lift into the target union, up to 8.18× a cell — and buys nothing: the conditioned arm cleared **zero** in all four quarters, its aimed map supply exhausted in seven minutes, and `direct_trap_multiply` cannot make a vivid picture at all (0 `light_vivid_cyan` in 13,938 unaimed rows, every one of its top 18 realized cells muted). An unaimed leg already lands 27% of its rows in that coordinate, so the ceiling on aiming was 3.7×. An unaimed leg on the full `mined()` roster is not a marginal source of gallery-grade material; it is the source.

**★ GROUPS ARE PALETTE GROUPS AND MINING CANNOT MOVE THEM.** `groups.group_of` is total — a map in the cut takes its cluster id, a map outside it is its own group — so **a new group needs a new MAP**. 942 before last night's four merges and 942 after, from 750 new locations and 146 gallery-grade rows. The last thing to move it was the `classic-pairs-2026-09` drop, 822 → 942. ⚠ The count depends entirely on where it is read: **942** seatable pool · **934** rows the fine head has scored · **762** the ≥0.50 view · **477** across the seated thousand. `group_cap` refuses **zero** and no group sits at its cap; ⚠ `map:river-of-light-25` takes **24 of 25**, one off for the first time.

**★ ARM B IS THE BEST BUY AND THERE IS ALMOST NONE OF IT.** 39.7 gallery-grade rows an engine-hour against breadth's 13.3 and 6.1 and the floor arm's 3.6; its band exhausted in seven minutes; **breadth refills that band at 16.2% of the places it opens**, a fourth reading agreeing with the three in `LEGS.md`. So the next general leg alternates breadth → merge → band rather than standing one band unit at the front. **★ AND A FLOOR ARM SHOULD NOT RUN unless a mode is actually short** — none is (thinnest is `direct_trap_lines`, 146 seats against a floor of 16), and the one that did cost 1,001 engine-seconds a gallery-grade row against arm B's 91, with `phoenix:classic` taking 60.3% of its seconds for 9.3% of its candidates because a proven-places draw runs with no partition weights.

**This era (ckpt 115→116, one day).** Three ownership audits moved the docs' own claims into the repos that own them, 26 of the last 30 already owned; the two big mining questions were answered and both closed; the first cascade record was written and the bar's default flipped with it; the contact-sheet builder became tracked code; `inventory.feasibility` stopped pricing a cap retired on 2026-08-28; the website took Matt's rendering-modes round and `page-review.md`'s round column was redefined to admit a round that arrives as notes.

**Records.** 63. The four the site stands on are unchanged: `20260902T161757Z` · `20260902T164622Z` · `20260904T023748Z` · `20260904T233233Z`. ⚠ **`20260906T133236Z` is still held as a tentative KEEP but appears NOWHERE in the website repo** — the site's own mapping is `article/figures.jsonl` — so why it is held needs re-deciding rather than re-asserting.

## IN FLIGHT ACROSS THIS BOUNDARY — none.

## QUEUED IN DRIVE `prompts\` — none.

## NEXT CHECKPOINT GOAL — NOT SET. Matt raises it.

## OPEN (ordered) — Matt raises each
1. **`pictures/` in the ten `runs` legs.** 5.37 GiB. Held three independent ways, any one sufficient; replayability is total and is not the obstacle. `orphans` last read **0 pictures named by no store**, and listed the ten unmerged legs holding 15,022 pictures and left them, as the rule says.
2. **The augment inner clock — a proposal, not applied.** `chain_at` has no clock check inside its walk, so `--augment-seconds` is tested only between seats and a pass overran a 300 s budget by 74%. The gate failed: two n=2000 tentative records exist under a bound stage, so the change would re-seat records that exist.
3. **Records-only picture retention.** The sweep premise is dead; the cost is one-off at build. What survives is regeneration determinism. Direction → `preserve\retention_design.md`.
4. **`carriers.jsonl`** sits at 65.9% of the 1 MiB history guard, 4.3 drops away. **A cross-repo seam**: the website's `builder/palettes.py:carriers()` derives the same two columns.
5. **`itinerary.jsonl`'s guard** was raised to 786,432 and sits at 62%. The real horizon is roughly nine drops, a design question rather than a constant.
6. **Website** (Matt's pace). **Per-page status, masters, sweep state, figure holds and review rounds live in `docs/page-review.md` — cite it, never restate it here.** **Color palettes is the next page for critic review**; Training judges v6 was placed 2026-09-07 and nothing is outstanding on it. Still open there: **the front page's Gallery curation blurb still makes two claims the adopted bar retracts** — quality-first-then-constraints, and every rendering mode represented, the second of which the bar makes definitely false; `palettes/all-palettes.html`'s 13 em-dashes, generated, so `builder/palettes.py`'s to rule on; `locations-walk-lengths` lettering a run identifier into its own picture; and the re-base onto a newer record, named and unscheduled. Stale figures and prose are NOT tracked or refreshed until "ready for publishing".
7. **The reframe channel's cadence.** Label-bound rather than clock-bound, and ⚠ the channel is running dry — `g10` converted 384 fires into 2 productive with 376 unresolved. Sizing → `curation/MEASUREMENTS.md`.
8. **`20260906T133236Z`'s hold** — see Records above.

Parked → `preserve\parked.md`: augment at n=2000; the rung-frame overwrite; the `mine` leg's autolevel stamp gap; medium refactors; the `tia` bound question; **the `groups.jsonl` re-cut**, which is now the only thing that could ever change the gallery's group breadth; `BOUND_BLOCKS` 8; the K re-sweep under the cascade; the desire list as an explicit instrument; the `inventory.feasibility` colour-allowance formula computed on paper where `ceiling.Rule.allowed` is the derived function (live constants, agreeing exactly at the shipped k=2, so nothing has been misreported — a two-line fix, not urgent).

## STATUS / KNOWN REDS
**NO KNOWN REDS.**

Fast lane **3,935 passed / 128 deselected, ~121 s**. ⚠ **The slow lane's expected 4,063 is a DERIVATION from the fast lane's collected total, not a reading** — it was skipped on Matt's call mid-prompt, so the next slow lane confirms it rather than being checked against it. `ruff` clean both repos. Website `builder check` **18** green with nothing skipped and the wallpapers checkout configured, so `library`, `bake`, `seats` and the source-key half of `figures` all ran; 47 JS tests. ⚠ **`seats` skips whole on a bare clone and that is fine by construction** — CI answers four fewer questions than the docs used to claim, not three.

## RULINGS THIS ERA
→ `preserve\rulings_method.md §ckpt 116`, and the domain rulings in the docs themselves.

## KEEP LIST
Drive `prompts\`: **wipe everything** — nothing is queued. `reports\`: **wipe everything** — all nine were read. Wallpapers `scratch/`: KEEP `show_n1000_0908/` and `general_mine_0908/`; **WIPE everything else**, including `filtered_view_p_fine_0907/`, `gallery_by_p_fine_0907/`, `eye_check_calibration_0907/` and `dtm_lime_cyan_smoke_0908/` — the sheet builder those were kept for is now tracked code at `curation.sheet.score_sheet`. Website `scratch/`: KEEP `_modes_render_times.py`, the walk-descent figure rig, and `three_bands/pick_seats.py`.

## OWED
Nothing.

## SCRATCH/ARTIFACT FLAGS
**★ THE STANDING KEEP ROSTER LIVES IN THE REPO — `src/fractal_wallpapers/README.md §The standing keep roster`, 19 entries.** Read it there; this doc keeps no copy.

⚠ **NOTHING ON THAT ROSTER IS PROTECTED BY `orphans`' REFERENCE SET.** `picture_dirs` walks `<tier>/curation/<subtree>/<leg>/pictures` for six pool subtrees and nothing else, so 18 of 19 entries are structurally out of the sweep's reach and the roster is a set of rulings rather than a mechanism anything could violate.

⚠ **`artifacts/render_folds/` DOES NOT EXIST on either tier** and has not for some time. `read_assignment` refuses, so `renders dose`, `renders grade` and `renders deploy` refuse until the fold deal is re-derived, which `sides_for` would demand anyway. What is lost is the record of which fold each row was in. Low consequence under the ckpt-103 ruling that no eval instrument is built for a retrain.

⚠ **`.leveled/` DIRECTORIES ARE SWEEPABLE** — the old "not sweepable" wording was wrong; `orphans` reaches them by the name each JPEG would have. What cannot be written is a BOUNDED sweep of the rest: 1.6% of directories, 1.3% of bytes. Identity and the prune argument → `preserve\leveled_identity.md`, and ⚠ that file may still carry the old wording — check it before citing it.

Per-checkpoint: the new record `20260908T144844Z` is prune-protected like every record. `artifacts/curation/depth/*/fields` keeps growing at roughly 226 MB a leg and the sweep is structurally unable to reach it. ARCHIVED (RESTORE before reuse): unchanged from ckpt 106.

## CLOSED (records wiped — verdicts in the docs and the rulings parts)
AUDIT_ckpt115_website_ownership_0908 · AUDIT_ckpt115_wallpapers_ownership_0908 · EDIT_ckpt115_writing_guidance_additions_0908 · EDIT_ckpt115_rendering_modes_matt_round_0908 · MINE_ckpt115_dtm_lime_cyan_smoke_0908 · MINE_ckpt115_general_breadth_overnight_0908 · SHOW_ckpt115_n1000_page_and_groups_0908 · PRECLOSEOUT_ckpt115_docs_ownership_0908 · FIX_ckpt115_feasibility_group_cap_0908 · FIX_ckpt115_page_review_column_0908.

## PARKED / SETTLED
→ `preserve\parked.md`, `preserve\rulings_corpus.md`, `preserve\rulings_curation.md`, `preserve\rulings_sourcing.md`, `preserve\rulings_engine.md`, `preserve\rulings_website.md`, `preserve\rulings_method.md`, `preserve\sourcing_channel_laws.md`, `preserve\retention_design.md`, `preserve\solver_design.md`, `preserve\leveled_identity.md`. The old `settled_rulings.md` is a stub index.
