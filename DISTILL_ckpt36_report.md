# DISTILL_ckpt36 — apply report

## Per-doc deltas (lines +/−, bytes before → after)

| doc | lines | bytes | note |
|---|---|---|---|
| state | +20 / −14 | 5,594 → 6,093 | (A) wholesale replacement, verbatim |
| engine | +2 / −2 | 11,633 → 12,358 | all 3 edits |
| models | +17 / −16 | 9,828 → 10,023 | all 5 edits |
| thresholds | +35 / −28 | 9,267 → 11,217 | all 5 edits; see gap (2) |
| corpus | +3 / −1 | 15,167 → 16,105 | all 3 edits |
| storage | +8 / −4 | 11,203 → 13,400 | all 6 edits |
| orchestration | +4 / −1 | 6,374 → 7,112 | all 4 edits |
| discovery | +3 / −1 | 17,534 → 18,450 | all 3 edits |
| emission | +1 / −1 | 8,541 → 8,923 | edit 1; edit 2 was "no edit" |
| operating | +10 / −1 | 17,211 → 18,814 | both edits |

Roster check: every doc was already ~1.5–2× its soft target before this era; nothing changed
that. Largest growth this pass = storage +19.6% and thresholds +21%, which carry the era's two
biggest edit lists (6 and 5 items). Both got a compression pass over the newly-written prose
after a first draft ran higher. Judged small-justified-overage → applied and noted, not stopped.

## Source gaps — three named sources are ABSENT

`C:\Code\fractal-drive-sync\reports\` does not contain, and neither does anywhere else in the
exchange folder:

- `v11_crop_executor_report.md` (named for the engine edits)
- `v11_cache_render_report.md` (named for the engine edits)
- `v11_train_cert_report.md` (named for the models edits)

Present and used: `v11_adoption_report.md`, `tau_h_enlargement_report.md`,
`tau_h_enlargement_rederive.log`, `storage_cleanup_report.md`, `claude_md_absorption_report.md`.

Consequence:

1. **Engine — no loss.** Every number the engine edits ask for is stated inline in the prompt
   (containment inequality, `field_ss 2`, 0/30 flips, ~3% maxiter policy change,
   0.531 s/location + 0.0104 s/tile, legacy 0.1577). Applied from the prompt.
2. **Models — partial.** "cert results verbatim from the cert report's bar table" could not be
   transcribed; no bar table was available. The certification bullet is written from what the
   prompt itself states (arms non-inferior, q4-uniform separates, cutpoint tightened onto the
   0.4713 base, ECE .162→.130, ordering not damaged, tile-path |Δ|≤0.02). **No per-arm numbers
   were invented.**
3. **Models / state cache facts** (361,696 tiles, 22.57 GiB, 3.09 h, q60..95, 65.4 KiB/tile,
   4.8–7.3×) taken from the prompt text, unverified against a source.

## Not applied / applied partially

- **thresholds edit 4 — "keeper cuts: v11 recut values from the adoption report."** The adoption
  report carries **no numeric keeper-cut table**; it records only that the recut ran on the
  discovery table's own population, with the two populations that changed (j:mandelbrot 302 =
  254+48, phoenix 211 = 113+98). Applied the qualitative content and the population fix. The
  stale v10 values (mandelbrot 0.03 / j:mb3 0.47 / j:mb4 0.55 / j:mb5 0.55) were **removed
  rather than left stamped as current** — the section now points at `keeper_cuts.json`. If those
  four v11 numbers matter, they need a source.
- **emission edit 2** — followed as written ("no edit"). Note that the intake line still reads
  **"751 admitted @v10"**; the adoption report's post-rescore census is **1,657 current / 779
  admitted** under v11. Left stale by instruction.

## Contradictions found in the sources

None that contradicts an edit. Two sequencing points worth stating, both resolved in favour of
the prompt:

- `v11_adoption_report.md` says native multibrot t_good was **WITHHELD** (0.61/0.85/0.61,
  fork-scheduled). `tau_h_enlargement_report.md` item 2 records it **ADOPTED** later the same
  day (`8d5e5e8`), byte-for-byte the withheld numbers. The prompt's "natives adopted" is correct;
  the withhold is now history and is recorded as such in the t_good table.
- The τ_h numbers in `v11_adoption_report.md` are the 3,492-row adoption-era derivation, since
  superseded. The table applied is the **enlarged** one, read off the final block of
  `tau_h_enlargement_rederive.log` (which is the only place the full 8-partition table appears —
  the report itself gives deltas plus two values).

## Adjustments beyond the literal edit list

Made because the edits directly falsify a neighbouring line, all in docs the prompt was
already editing:

- **models / storage — "v5–v7 rungs carry NO `config.json`"** deleted. The storage report
  records those three `config.json` extracted and tracked before the weights left; the claim is
  now false at both sites.
- **storage — `data/classifier/v7/` "IS LOAD-BEARING BEYOND ROLLBACK"** rewritten to past tense
  (the ranker that pinned it is deleted). The name-full-paths lesson is kept.
- **storage — "Tree holds v5–v10 weights"** → active + previous, per the new retention policy;
  the "v8/v9 plan+manifest set" dropped from the over-policy keeps list (both pairs de-tracked).
- **models — the flip-era lesson's dead example** (`tools/ranker/scorer.PENULTIMATE_CKPT`)
  swapped for the era's live one (a study importing `V6_CKPT_ROLLBACK`).
- **thresholds — "A ROLLBACK TO v8..."** → "A ROLLBACK..." (the ladder is v11 → v10 only, so
  naming v8 would have been the only surviving claim that v8 is a rung).

## Checks

- Working tree was clean before applying; no `fractal-*.md` created, deleted, or renamed.
- Nothing written anywhere under `C:\Code\fractal-drive-sync\` (read-only, per CLAUDE.md).
- All 10 docs were on the prompt's touched list; no untouched-file check applies.
- Single-home spot-greps: values that appear twice all do so because the (A) wholesale
  replacement of state carries them in its era summary — 361,696 / 3.09 h / 43.6% /
  0.61-0.85-0.61 / 3.6 MB. That is claude.ai's own authored text and was applied verbatim.
  One prose overlap in the emitted docs: the 379 orphaned ranker labels appear in both
  models' one-line closure and storage's pre-existing "Ranker durability arc" bullet.
