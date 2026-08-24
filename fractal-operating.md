# fractal-operating — the method

**Amended by diff, never rewritten in full** (full rewrites only when Matt sanctions one; ckpt 50, 65 and 71 were). Read first, every session. Ownership test: *would this still be true if the project weren't fractals at all?*

---

## THE DOCUMENT SET

**Author & audience.** Claude writes these; sole consumer = a future fresh Claude. Write for yourself minus this session.

**★★ THREE READERS, THREE HOMES (ckpt 65, Matt-ratified).** CC reads each repo's `CLAUDE.md` + module READMEs + whatever a prompt cites; future claude.ai reads these six docs + `preserve\` on demand; Matt reads none of it routinely. So: **a mechanic of a repo lives in that repo's README/CLAUDE.md, never here** — these docs carry a pointer (`→ <module>/README.md §…`); a design spec or plan for unbuilt work lives in `preserve\`; these docs keep ONLY what changes a future session's decision. Tutorial grew to 2× target by carrying code facts for a reader (CC) that never sees it — the failure this rule prevents.

**★ NEVER ENTER THE CODE REPO (Matt, firm).** Docs live in their own git-init'd folder (`C:\Code\fractal-maker-controller`) with a dedicated applier CC; a copy inside a code repo desyncs. **★ THE DOCS CHANGE ONLY VIA THE APPLY-PROMPT** — Matt never edits them; an uploaded copy is byte-identical to what Claude last authored; any doc-vs-memory discrepancy is Claude's error. Docs persist at `/mnt/user-data/uploads/` all conversation — re-read from disk.

**The roster — one doc per subject:** operating (method) · state (plan/status/flags/roster — EVERY distillation) · tutorial (fractal-wallpapers + website/article, decisions and caveats only) · corpus (labels, sampling, judge method, accumulator) · discovery (sourcing truths) · engine (archive stub: anchors · cross-repo render truths · maker-archive status) — **six docs**. Retired docs' recovery = controller git history.

**★★ SELECTIVE DISTILLATION (Matt).** At a distillation claude.ai emits ONLY the docs the era touched or invalidated, plus state — default a SMALL SUBSET; emitting everything needs a stated reason; an untouched doc cannot grow. The `DISTILL_ckptXX_apply.md` prompt (guard: working dir holds the six `fractal-*.md` at root, no Cargo.toml/src/tools — else STOP) carries exact hunks (verbatim unique match or STOP), verifies untouched files untouched, spot-greps single-home, sanity-checks sizes, one commit. **Wholesale replacements travel as individual presented files that Matt places himself** (never inside the prompt or through Drive); the prompt verifies they are present and differ from HEAD.
- Walk the full manifest once per distillation — TOUCHED / INVALIDATED (truth changed without an edit — flag in state, never silence) / CLEAN.
- State the scratch-preservation notice at every distillation — what under `scratch/` MUST survive; default nothing.
- Distill only from a SETTLED state — never mid-session, never with a prompt outstanding; its job is to CLOSE threads. Do NOT write the distillation until the era's FINAL report is in.
- **The claude.ai session AUTHORS all doc content; the apply prompt is mechanical** — it never asks CC to compose or condense prose.
- **Hunk authoring rules (ckpt 70's failure):** within a file, no hunk's OLD text may overlap text a prior step of the same prompt deletes or moves — edits to moved content target the DESTINATION file; MOVE steps sort last within their file.

**★★ SIZE TARGETS, NOT HARD CAPS (Matt).** Soft targets in state's roster; the deletion test is the real control; targets move only with Matt. state holds NO FACTS — status/plan/flags/roster only.

**★★ THE DELETION TEST (Matt, firm).** *"These docs are the ACTIVE WAVEFRONT, not a history."* A line survives only if it would change a FUTURE decision AND cannot be encoded in code. Passes: decisions not yet made · measurement-validity caveats that would cause a future result to be MISREAD · true-but-unenforceable facts. Compression rules: a number in a tracked repo file never appears here (verdict + path) · a `[code:]` fact with a guard = one line + pointer, the guard is the memory · a closed arc ≤3 lines: verdict · what changed · record path · run facts live in run records. **The failure mode is Claude's: treating a CC report as material to CARRY rather than evidence a line can be CUT.**

**★★ SINGLE-HOME.** One doc per subject; grep each bolded numeral across emitted docs and assert single occurrence; other docs NAME a fact and cross-reference, never restate.

**★★ TAG CLAIMS ABOUT CODE.** A line asserting what the tree does carries `[code: path]` or `[unverified]`; a claim of AUTOMATIC FUTURE BEHAVIOR names the enforcing mechanism or is not written. Every checkpoint that checked has falsified some untagged claim (ckpt 65: five at once).

**Compression.** Telegraphic; rewording ≠ compressing — delete whole blocks. **Repo practice docs:** fractal-wallpapers has NONE by decision (Matt, 2026-08-18) — conventions live in CLAUDE.md; seed one only from a demonstrated incident.

**Self-perpetuation.** Carry this document forward, amended or preserved, never eroded.

---

## TIER 0.5 — THE EXCHANGE FOLDER

**`C:\Code\fractal-drive-sync\{prompts,reports,prose,preserve}\`** — Drive-synced, outside all repos. `preserve\` is DURABLE (Matt never deletes; use sparingly; cite by path; claude.ai may also edit it Drive-side — trash + recreate, never a same-named duplicate). Everything else is SCRATCH — Matt deletes freely. One writer per subfolder; `scratch/` stays a report's canonical home. `matt-claude-workflow.md` (exchange root) documents the pattern for a NEW project; each repo's `CLAUDE.md` owns the standing prompt contract (report shape/path/delivery, runtime discipline, commit gate) — prompts never restate it.
- **★ ALL PROMPTS GO THROUGH `prompts\`** — code-work, addenda, and checkpoint prompts alike. **DELIVERY = a confirmed Drive create into `prompts\` in the same turn the prompt is authored; presenting a file is NOT delivery** (missed twice). Re-resolve each session by PARENT CHAIN: find `fractal-drive-sync` (title + folder mimeType), then the `prompts` folder whose parentId equals that id — never by title alone, a sibling-filename check, or a parentId lifted from a file search (misdelivered to the other `prompts` three times). Same for `prose\`, `reports\`, `preserve\`. **Drive files cannot be edited in place — a correction to a delivered prompt, run or not, is an ADDENDUM file** (`<prompt>_addendumN.md`, "paste with the original").
- Every prompt opens with a TARGET-REPO guard (`fractal-wallpapers` / `fractal-website` / `fractal-maker` / `fractal-maker-controller`) with STOP-on-mismatch, and ends with an explicit "Commit when done." unless it states its reason not to.
- **★★ CHECKPOINT NAMING (Matt):** `DISTILL_ckptXX_apply.md` = the controller-CC apply prompt; `continuation_ckptXX.md` = a hand-off WITHOUT distilling, against unchanged docs. **A checkpoint produces exactly ONE hand-off artifact** — session context a fresh session needs is written INTO state, never a side file.
- CC MAY be pointed at the controller folder — READ-ONLY to code-work CC (Matt, 2026-08-11).
- **★★ CONTEXT STEWARDSHIP IS PART OF THE SESSION CONTRACT.** Track the session's own budget against a **~150k soft ceiling**; on reaching it, call "checkpoint now" instead of proposing another prompt; report an estimate at the checkpoint.
- **★ DRIVE FETCH: `read_file_content` returns plain text at 1× — use it for ALL text fetches.** `download_file_content` is base64 (~3×) — binary only.

**PRESERVE INDEX** (audited ckpt 71; near-frozen — cite by path, never restate; claude.ai self-fetches via Drive; update whenever preserve changes):
- `gallery_pass_design.md` 8.6k — the ruled two-phase design: steps, floors, embed spec, radius calibration, audit reuse map. §6 build order stale — the code is the record.
- `sourcing_measurements.md` 7.7k — retired-head verdicts + run-era numbers, PRIORS only: family character, plane depth, deep-descent ruling, interior cliff, run10, julia ∂M, twin slice, mandelbrot offer, proven first serving, novelty smoke.
- `audit_deep_descent_report.md` 17k — two-repo deep-surface audit: maker perturbation tier + S1/S2 anchors, `min_width` provenance, f64 sites, costs, head validity, 5 contradictions. Line refs = 2026-08-20; the maker's stay valid, the wallpapers' rot.
- `deep_kernel_plan.md` 2.8k — the ruled perturbation arc, UNBUILT.
- `visitor_explorer_design.md` 1.8k — explorer design record; BUILT ckpt 70 — live mechanics = `explorer/README.md`.
- `parked.md` 1.5k — deliberately unscheduled items; re-enter only from a demonstrated repo need.
- `maker_transfer_cautions.md` 1.9k — maker archive-read cautions + the old→new rename table.

---

## STANDING POSITIONS (Matt, firm)

- **★★ RUNS ARE PRODUCT; LABELING IS AN EVAL ACTIVITY (2026-08-13).** Runs are on Matt's schedule with no verification homework attached. **A LONG RUN (100 h+) MUST NEVER REQUIRE LABELING IN THE LOOP.** Labeling re-anchors the books when it happens; high-value sources ACCUMULATE (fractal-corpus). **Retrain when a decision needs it, NEVER preemptively.** A design that makes a run's allocation depend on fresh human labels is refused.
- **★★ THE DISTILLED-REPO MODEL (2026-08-14).** Fresh repo = everything pulled in cleanly, CONTEXT-FREE; labels FLAT; NO byte-identity requirement — cleanliness over byte-identicalness; shipped weights trained WITHIN the repo. Editorial line: *"this is about fractals, not ML."*
- **★★ NO ARCHAEOLOGY; DELETION IS NORMAL.** Don't resurrect artifacts that don't match how things work now; Matt holds retention outside the repo. **★★ USEFULNESS BEFORE RECOVERABILITY** — if nothing will want it back, delete the regeneration machinery with the data; regenerability is not per-file when builds are chained.
- **★★ NOTHING LOAD-BEARING LIVES IN `scratch/`, both ways** — evidence leaves it when it justifies a decision; a proposal computed there never leaves as a fact. Exceptions declared in an enforced allowlist; Matt wipes scratch between checkpoints.
- **★★ A DURABLE RECORD WRITTEN AFTER A FALLIBLE STEP IS NOT DURABLE** — irreplaceable record first. **★★ LOSING HAND-LABELED DATA IS A MAJOR FAILURE** — nothing rewrites, deletes, or re-keys stored label rows; re-attribution is reader-side; verify exports BY ROW COUNT. **A tracked RECORD is never edited in place** — the check that reads it gets its semantics fixed, or an amendment the reader prefers is added beside it (ckpt 65: the concurrent-writer check was the bug; `segments` added, `wall_seconds` never redefined).
- **★ REPO-DOC ADMISSION:** something in the code owns it and it stays true as the code changes; a transient measurement lives in scratch, survivors extracted, source deleted — **an extraction that does not delete its source is the failure; a rule nothing enforces is not a rule — name the guard.**
- **★ FRACTAL TYPES ARE PERMANENT DESIGN CONSTRAINTS** (phoenix and phoenix:classic included).
- **★★ ENFORCING FROZEN THRESHOLDS WERE THE ROOT CAUSE OF THE IMPOSSIBLE-STATE FAILURES.** Prefer read-time rank + coarse semantic floors; a threshold change is a READ-TIME CHOICE, never an event that invalidates populations. Kept guards: sink isolation · dedup · label-carries-its-join · seeded determinism.
- **★★ THE 10,000-HOUR FRAME (Matt, 2026-08-22).** Judge every design decision by "what makes the best-framed, highest-quality, most beautiful, most diverse collection given 10,000 hours." Anything that discards and never revisits is generally wrong; err toward over-admitting whatever could be good and let the embedding + gallery pass reject near-duplicates. Lineage caps, saturation discount, spacing floors = PACING (new ground first), never rejection — a future session must not tighten them into gates. Don't over-think trivially small counts. **★ A DANGLING REFERENCE IS NOT A TASK** — "explore-the-set" and "phoenix seed-pool coverage" each survived two checkpoints with no referent in any repo; a line that sounds like a task but names nothing fails the deletion test (ckpt 69, twice).
- **★ A RULE'S PURPOSE BOUNDS ITS SCOPE (ckpt 65).** Before refusing or redesigning on a rule, name what the rule protects; if that thing is not in play, the rule is not either. (The judges-figure lock-up: a figure-exemplar rule and a split rule were applied to a results grid neither governs.)
- **★ TWO SPELLINGS OF ONE FACT IS A SILENT NULL (ckpt 70).** One adapter, one key, and the reader asserts the spelling it expects — same law as label-carries-its-join (ckpt 70: two spellings of a ledger key read as "nothing" for 1,120 rows; a witness on the wrong axis understated a gap).
- **★ WRONG-GEOMETRY ESTIMATES (ckpt 70):** cost tracks what the pixels do — pilot on the target population before sizing any leg (a 13 h projection was 56 min real: the prior was a deploy-view cost on gate survivors; labeling form → fractal-corpus).

---

## REASONING & MEASUREMENT

**Confidence convention.** Every verdict carries **basis** (`[human n=X]`·`[machine-decode]`·`[measured]`·`[inferred]`·`[by-eye]`), **population**, **overturned-by**. No falsifier = a belief; `[machine-decode]` is evidence about the MODEL, not the world.
- **★ Cuts and floors are RELATIVE TO A REFERENCE, never absolutes.** Every precision in a lock or anchored rate is a CEILING.
- **★★ TWO RESTATEMENT MODES when a cut must survive a head flip:** VOLUME-MATCHED (same fraction of a fixed reference pool; CORN scales are train-prior-calibrated) · HUMAN-DERIVED CROSSOVER (isotonic P(≥boundary)=0.5 on a labeled sheet; the volume change can BE the finding).
- **★★ NEVER POOL ACROSS AN ESTIMAND CHANGE. A REGENERATION MOVES EVERY MEASURED ROW** (partial adoption = hand-splice). **A DEFAULTED SEED IS A BAND**, not a neutral prior.
- **★ BUDGET A LEG OFF AN OBSERVED LEG, never off a rate** — rate extrapolations understate ~2× (bulk small-file moves: ~3× — see fractal-tutorial §THE REPO); stage anomalies rank by ratio to the unit's OWN median.
- **★ A reproducibility test re-runs the writer the artifact came from. ★ NEVER CONSTRUCT A TEST'S EXPECTED VALUE WITH THE TRANSFORM UNDER TEST**; a planted red proves the guard bites. **★ A PRE-DECLARED BAR MUST OUT-RESOLVE ITS INSTRUMENT**; a teacher's self-agreement is a ceiling, never a bar. **★★ A "BYTE-IDENTICAL" CLAIM IS PROVEN BY RUNNING THE REAL COMMANDS** — and scoped to the module that was compared (the wasm spike measured one export; the explorer's banding was argued until `bands.test.mjs` measured it, ckpt 69).
- **★ Early reads of a slow-starting run:** mechanism valid immediately; yield is warm-up. **★★ A STAGE THAT CAN TRUNCATE ITS OWN INPUT ON THE WAY TO FAILING HIDES ITS OWN FAILURE** — refuse to write when draw and ledger share zero rows. An append-only log is a SUPERSET of checkpointed counters after a kill — dedup before quoting. **A clock started after a resume block under-reports every relaunched run** — a wall-vs-history inequality is not a concurrency tell.
- Judge-method and split rules are OWNED by fractal-corpus — point, don't restate.

---

## WORKING STYLE

One CC prompt at a time PER REPO — different repos concurrent by default; same-repo parallelism only when verified (overnight wait-gate PROVEN). **★★ A website prompt that may touch the engine LOCKS BOTH repos (Matt, 2026-08-21)** — check in-flight state across both before handing off, and say so in the prompt header; read-only audits may run beside anything (explicit no-write, no-commit). Engine carve-out for wasm consumers → fractal-tutorial §WORKFLOW. Progress-through-delivery over methodological minutiae; scope narrow; diagnosis-first NOT a standing policy. **★ MATT'S N-HOUR BUDGET COVERS EVERYTHING** — build + run + post ≤N wall-clock; run cap ~N−2. **One run per budget — a follow-up of ANY length is a NEW budget question.** **★ EXPLORATORY ~8 h RUNS: ONE PROMPT COVERS LAUNCH AND POSTMORTEM** — CC stays running across the run and writes the readout at the end; separate readout prompts only as follow-ups; not for ~100 h runs (Matt, 2026-08-22). **★ THE 100-HOUR POSTURE:** bounded by disk and unmeasured saturation convergence — never by a labeling cadence. **★ LAUNCHES TREND TO ONE COMMAND** — pre-flight facts and refusals fold into the run command; prep prompts tolerated meanwhile.

- Prompts = short `.md`, presented AND delivered; scale length to risk; trust CC on mechanics; for steps >~30 s instruct CC to estimate and background. **★ CC's honest spec-deviations with stated reasons are consistently right — read before overriding** (ckpt 65: every deviation taken was correct). Supply claims to be CHECKED, not transcribed; ask for the corrections list back. **★ AFTER A REPORT, DO NOT SUMMARIZE IT BACK** — say what it CHANGES, what Claude got WRONG, what's next; **trivial outcomes get ≤2 sentences (Matt, 2026-08-23)**. **★ NO "UNREVIEWED BY MATT" TRACKING** — assume CC's calls and the rendered state are fine until Matt says otherwise; flag only decisions that BLOCK upcoming work. Everything on the site is DRAFT — argue toward the right FINAL PRODUCT, never from churn.
- **★ NEVER EDIT A PROMPT ALREADY HANDED OVER** — addendums. Matt does NOT hand-edit JSON/config — he dictates, the prompt applies. Acceptance BY EYE except classifier evals. Git — commits, push, remotes — is his entirely: never flag or mention its state. **★ CC commits to `main` ONLY. ★★ NO COMMIT ≥20 MB WITHOUT MATT'S EXPLICIT PRIOR CONFIRMATION** (in repo CLAUDE.md; stop and ask).
- **★ A FIX WITH A SHAPE NEEDS THE PROMPT, NOT A "YES."** **★★ AUDIT-FIRST:** when a task needs technically-important knowledge the session lacks, STOP and ask Matt whether to send a facts-only audit prompt — never scaffold load-bearing content around CC-fill spots; audits report facts, the session authors prose. **★ A POLICY FLIP ASKS "WHO ELSE APPLIES THIS DECISION?"** — grep for private copies (bit twice). **★ BUILD ≠ FLIP** — staged in one prompt, adopted in another against a pre-registered bar; exceptions bought by disasters: pre-registered eval bars · blind human reads of any model-selected population · reject autopsy + identity round-trips. **Reject autopsy — standing habit:** every readout emits numbers AND a visual sample of admissions + rejects.
- **★ Name full paths in any delete/move instruction** — "delete v7" is a version, not a path.

**Labeling.** **★★ AFFORDABLE WHEN WE NEED IT** — size for power; renders, not labeling, price a batch (~6.3 rows/min). **★★ LABELS MUST SERVE OBJECTIVES THE NEXT RETRAIN CANNOT DEPRECATE** — eval instruments, design reads, correction sittings pass; training volume fails by default. **★★ NEVER add calibration duplicates, drift probes, or repeat rows** — "noise is expected at all boundaries" (Matt), never re-raise. **★★ THE CORRECTION LOOP IS THE LABELING METHOD** (mechanics → fractal-corpus); assume proper randomization — a distribution concern is ≤1 line of prose. **★ Don't editorialize on a sheet about to be labeled blind.** A prompt running while Matt labels conflicts on GIT, not CPU — commit only its own files by explicit path.
