# fractal-state — checkpoint 78 (2026-08-25)

## Where we are
**Both repos FREE; nothing in flight.** gallery3 CLOSED — 150/150 seated, no `below_bar`, full-size leg ran on the live floors; its findings are absorbed into discovery/tutorial/engine and the record is in Drive `reports\`. sweep_row specialization LANDED in both repos. FIX (picture-identity dedupe · pass-id launch lock · seed probe) LANDED. Two read-only audits closed. **The next arc is COLOUR SELECTION + DIVERSITY, then gallery4.** Running at scale v2 still awaits Matt's review — deferred here by decision, not by dependency.

## OPEN (ordered)
1. **Colour selection + diversity design — the next thing.** Floor shape ruled: **`1/cells`**, not `1/N` (Matt, ckpt 78) — write the constant as `1/cells` (49 today, after the three near-dup codebook pairs collapse), never the literal. Sizing blocker before any quota value: **strange clears the release floor at 14%, smooth at 74%** — a quota removing candidates from a strange neighbourhood removes them from an already-thin pool. Stage diagnosis (capable → drawn → won → expressed) is useful but NOT critical; Matt's prior is the DRAW stage. Working notes below.
2. **Seeded point draw — BUILD BEFORE gallery4** (Matt, ckpt 78). Shape and constraints → fractal-tutorial.
3. **Per-pass candidates — BUILD** (ruled ckpt 78) → fractal-tutorial. One predicate; make it in `pool_rows`/`pool_candidates` and NOT at the `below_floor_sheet` call site — that sheet keeps the standing rows, it is the reach-problem-vs-supply-fact evidence. Full observer list → `reports\AUDIT_gallery_seating_candidate_set_report.md`. `curation/README.md`'s "a later pass reads both stores" moves with it.
4. **gallery4** — after 1–3.
5. **Running at scale — Matt reviews v2 → website placement prompt** (website only, runs beside anything): verbatim placement; the editorial block at the draft's head carries the verification list and the three `pending` figure rows (`scale-budget-plan` · `scale-yield-decay` · `scale-yield-by-channel`, all from `artifacts/harvest_run10/`, proven channel OFF); the channel-ON TODO stays an HTML comment; **the placement prompt adds the reader-facing clock-framing ban to `writing-guidance.md` and the guidance check**. The first-person "mix is my preference" sentence is Matt's to keep or reword.
6. **Sidecar engine-age fix** — pin the engine build into the identity chain, then **RE-RENDER** cached node views and rescore into an amendment artifact; never edit ledger rows. Rescoring alone reads the same stale picture. Open sub-question: at quality weight 1.0, did optimistic scores on the four disagreeing ledgers bias which locations won entry? Law → fractal-discovery.
7. **Post-gallery3 figure + prose round, one wallpapers rig prompt + one website prompt:** gallery-* figures · `gallery-output` **UNHELD** (gallery3 rendered full-size on live floors) + closer sentence · `palette-neighborhood`/`palette-moods` "seven hundred" (STALE-WHEN; the pool is now 900 of 901) · 7 `pending` From-locations rows · the three scale-* makers · **the two framing-refinement sentences must be RE-DRAFTED, not placed** — they carry the dead site asymmetry · "all three sizes" wording in Training judges.
8. **`palettes.js` drift** — a palette prompt's call → fractal-tutorial.
9. Matt's call, no urgency: framing window (3 widths × 4 recentres) and k=3 unswept · the ×1.0 rung free at harvest · seeded-draw top-K (the probe used 25).

## WORKING NOTES — colour cap mechanism (TEMPORARY; delete once OPEN 1 is designed)
Not a design, not a ruling — the live options from the ckpt-78 conversation, carried so they are not re-derived.
- **Matt's proposal:** achromatic exceptions (black, white, maybe gray — present by geometry, not chosen); every other cell gets a quota, in isolation (only X% of pictures ≥25% of one cell) and jointly (only Y% ≥25% of two named cells); over-quota candidates cannot be drawn, so the palette head must pick from what is not over-drawn.
- **Cap and floor do different jobs.** A cap flattens the top but creates whatever is *second* most preferred — it will not move the seven zero cells. Six of the seven are green or lime, 59–120 maps can reach each, and admitting 200 rare-colour maps (including `dark-vivid-green`) moved rose and magenta onto shipped pixels and green not at all. Both mechanisms, two jobs.
- **Hard quota vs soft discount.** A hard cap makes "no more than X% of this gallery is blue-dominant" a statable property but introduces a cliff and needs a stated fallback when a whole neighbourhood is over quota. The saturation discount already built for lineage novelty — `max(f, 1/(1+k·n))`, n = seats already expressing the cell — has no cliff and reuses understood machinery, but guarantees nothing. Claude's lean: discount for the cap side, a real floor for the green side.
- **Instrument, unvalidated.** Expression is measured on the release PNG (a share vector is not scale-free). A draw-time or candidate-time quota would have to read the 640×360 candidate JPEG instead, and candidate↔release agreement has never been checked — this is the shape of the ramp-share error. Both exist for all 150 gallery3 rows; check before building.
- Two thresholds now in play — census presence at 10%, proposed dominance at 25%. Name them distinctly from the start.
- Quota consumption is path-dependent (seating runs top-down per partition per kind), so it needs a seeded deterministic order and a record of which seats were displaced and what they would otherwise have taken — record-and-rank, so a bad quota is visible.
- Blue+red is a claim about a PAIR; everything measured so far is marginal. A co-occurrence matrix over the cells against an independence baseline is the cheap read. Test the mirror fold first: production mirrors non-cyclic colormaps and a folded diverging map puts both ends on the page by construction (gallery3 shipped 41 folded / 109 unfolded) — that would be a recipe cause, not a taste cause.

## PARKED (Matt, ckpt 78 — do not raise until he does)
- **Explorer performance and module size.** Includes the two remaining slow modes, the `smooth` interior-count escape hatch, and the retired `x generic` column.
- **Cross-partition radius.** ⚠ If it ever re-enters: `closest_pairs` shows SEATED wallpapers, whose palette *and* mode differ, while the distance is computed on NEUTRAL palette-free, mode-free renders — the sheet makes pairs look more distinct than the embedding measures and biases toward loosening. The design record's "fine at N≈1000" is untested; all 8 nearest seated pairs at N=150 are cross-partition, closest 0.0304.

## RULINGS THIS ERA
Appended to `preserve\settled_rulings.md` (ckpt 78 block) by the apply prompt.

## CLOSED (records = Drive `reports\`)
gallery3 · sweep_row_specialization · FIX_gallery_ids_lock_seed · AUDIT_gallery_seating_candidate_set · AUDIT_sweep_row_archaeology.

## SCRATCH/ARTIFACT FLAGS
KEEP: `artifacts/curation/` (backs the figure round) · `artifacts/node_views/` (input to the OPEN-6 re-render) · the census artifact. DISPOSABLE: everything ckpt 77 marked disposable. gallery3's five scratch HTML sheets — Matt keeps them for now and deletes them himself; **not preserved, no flag, no tracking**.

## ROSTER — sizes at ckpt 78
operating ~20.0k · state ~6.5k · tutorial ~16k · corpus 10.0k (UNTOUCHED) · discovery ~11.5k · engine ~5.1k. This distillation: **state WHOLESALE** (presented file, Matt places) · tutorial/discovery/engine/operating **by exact hunk** · corpus UNTOUCHED · preserve by APPEND ONLY (`settled_rulings.md`). Five of six emitted, by stated reason: the era changed engine (public API + an 18-mode identity chain), discovery (three falsified laws), tutorial (one ruling + four caveats), operating (one new rule). **`gallery_pass_design.md` and `color_coverage_floor_design.md` are session-side Drive edits, NOT the apply prompt's job** — pending at authoring.
