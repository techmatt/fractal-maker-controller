# fractal-operating — the method

**Amended by diff, never rewritten in full** (full rewrites only when Matt sanctions one; ckpt 50, 65, 71 and 77 were). Read first, every session. Ownership test: *would this still be true if the project weren't fractals at all?*

---

## THE DOCUMENT SET

**Author & audience.** Claude writes these for a future fresh Claude — write for yourself minus this session.

**★★ THREE READERS, THREE HOMES (ckpt 65, Matt-ratified).** CC reads each repo's `CLAUDE.md` + READMEs + what a prompt cites; claude.ai reads these six docs + `preserve\` on demand; Matt reads none routinely. So: **a mechanic of a repo lives in that repo's README/CLAUDE.md, never here** — these docs carry a pointer (`→ <module>/README.md §…`); a design spec or plan for unbuilt work lives in `preserve\`; these docs keep ONLY what changes a future session's decision.

**★ NEVER ENTER THE CODE REPO (Matt, firm).** Docs live in their own git folder (`C:\Code\fractal-maker-controller`) with a dedicated applier CC; a copy inside a code repo desyncs. **★ THE DOCS CHANGE ONLY VIA THE APPLY-PROMPT** — Matt never edits them; an uploaded copy is byte-identical to what Claude last authored — any doc-vs-memory discrepancy is Claude's error. Docs persist at `/mnt/user-data/uploads/` all conversation; re-read from disk.

**The roster — one doc per subject, six docs:** operating (method) · state (plan/status/flags/roster — EVERY distillation) · tutorial (wallpapers repo + website, decisions and caveats only) · corpus (labels, sampling, judge method, accumulator) · discovery (sourcing truths) · engine (cross-repo render truths, maker-archive status). Retired docs' recovery = controller git history.

**★★ SELECTIVE DISTILLATION (Matt).** Emit ONLY the docs the era touched or invalidated, plus state — a SMALL SUBSET by default; emitting everything needs a stated reason; an untouched doc cannot grow. The `DISTILL_ckptXX_apply.md` prompt (guard: six `fractal-*.md` at root, no Cargo.toml/src/tools — else STOP) carries exact hunks (verbatim unique match or STOP), verifies untouched files untouched, spot-greps single-home, sanity-checks sizes, one commit. **Wholesale replacements travel as individual presented files that Matt places himself** (never inside the prompt or through Drive); the prompt verifies they are present and differ from HEAD.
- Walk the full manifest once per distillation — TOUCHED / INVALIDATED (truth changed without an edit — flag in state, never silence) / CLEAN.
- State the scratch-preservation notice at every distillation — what under `scratch/` MUST survive; default nothing.
- Distill only from a SETTLED state — never mid-session, never with a prompt outstanding, never before the era's FINAL report; its job is to CLOSE threads.
- **The claude.ai session AUTHORS all doc content; the apply prompt is mechanical** — it never asks CC to compose or condense prose.
- **Hunk authoring rules:** within a file, no hunk's OLD text may overlap text a prior step of the same prompt deletes or moves — edits to moved content target the DESTINATION file; MOVE steps sort last within their file.

**★★ SIZE TARGETS, NOT HARD CAPS (Matt).** Soft targets in state's roster; the deletion test is the real control; targets move only with Matt. state holds NO FACTS — status/plan/flags/roster only.

**★★ THE DELETION TEST (Matt, firm).** *"These docs are the ACTIVE WAVEFRONT, not a history."* A line survives only if it would change a FUTURE decision AND cannot be encoded in code. Passes: decisions not yet made · measurement-validity caveats that would cause a future result to be MISREAD · true-but-unenforceable facts. Compression: a number in a tracked repo file never appears here (verdict + path) · a guarded `[code:]` fact = one line + pointer, the guard is the memory · a closed arc ≤3 lines (verdict · what changed · record path) · run facts live in run records · **★ AN OPEN QUEUE ITEM'S RECORD POINTER IS THE LAST THING TO DROP, NEVER THE FIRST (ckpt 78)** — ckpt 77 compressed the `sweep_row/compute_lanes` line past its `shape → <report>` pointer and the item became unrecoverable from the docs alone; a queue line naming no record is a dangling reference. **The failure mode is Claude's: treating a CC report as material to CARRY rather than evidence a line can be CUT.**

**★★ SINGLE-HOME.** Grep each bolded numeral across emitted docs and assert single occurrence; other docs NAME a fact and cross-reference, never restate.

**★★ TAG CLAIMS ABOUT CODE.** A line asserting what the tree does carries `[code: path]` or `[unverified]`; a claim of AUTOMATIC FUTURE BEHAVIOR names the enforcing mechanism or is not written. Every checkpoint that checked has falsified some untagged claim.

**Compression.** Telegraphic; rewording ≠ compressing — delete whole blocks. **Repo practice docs:** fractal-wallpapers has NONE by decision (Matt, 2026-08-18) — conventions live in CLAUDE.md; seed one only from a demonstrated incident.

**Self-perpetuation.** Carry this document forward, amended or preserved, never eroded.

---

## TIER 0.5 — THE EXCHANGE FOLDER

**`C:\Code\fractal-drive-sync\{prompts,reports,prose,preserve}\`** — Drive-synced, outside all repos. `preserve\` is DURABLE (Matt never deletes; use sparingly; cite by path; claude.ai edits Drive-side by trash + recreate, never a same-named duplicate). Everything else is SCRATCH — Matt deletes freely. One writer per subfolder; `scratch/` stays a report's canonical home. `matt-claude-workflow.md` (exchange root) = the pattern for a NEW project; each repo's `CLAUDE.md` owns the standing prompt contract (report shape/path/delivery, runtime discipline, commit gate) — prompts never restate it.
- **★ ALL PROMPTS GO THROUGH `prompts\`** — code-work, addenda, and checkpoint prompts alike. **DELIVERY = a confirmed Drive create into `prompts\` in the same turn the prompt is authored; presenting a file is NOT delivery.** Re-resolve each session by PARENT CHAIN: find `fractal-drive-sync` (title + folder mimeType), then the `prompts` folder whose parentId equals that id — never by title alone, a sibling-filename check, or a parentId lifted from a file search (a same-named `prompts` exists under another project). Same for `prose\`, `reports\`, `preserve\`. **Drive files cannot be edited in place — a correction to a delivered prompt, run or not, is an ADDENDUM file** (`<prompt>_addendumN.md`, "paste with the original").
- Every prompt opens with a TARGET-REPO guard (`fractal-wallpapers` / `fractal-website` / `fractal-maker` / `fractal-maker-controller`) with STOP-on-mismatch, and ends with an explicit "Commit when done." unless it states its reason not to.
- **★★ CHECKPOINT NAMING (Matt):** `DISTILL_ckptXX_apply.md` = the controller-CC apply prompt; `continuation_ckptXX.md` = a hand-off WITHOUT distilling, against unchanged docs. **A checkpoint produces exactly ONE hand-off artifact** — session context a fresh session needs is written INTO state, never a side file.
- CC MAY be pointed at the controller folder — READ-ONLY to code-work CC (Matt, 2026-08-11).
- **★★ CONTEXT STEWARDSHIP IS PART OF THE SESSION CONTRACT.** Track the session; **~150k is the WARN point, not a hard limit** — on reaching it, say so clearly with the estimate. **Matt ALWAYS decides when to distill**, weighing the live discussion context himself (ruled ckpt 79); never stop proposing work on the count alone.
- **★ Session-side Drive edits VERIFY FROM SOURCE exactly as prompts do:** a number carried in state is a pointer, not a fact — ckpt 79 wrote "49 cells" into the floor doc from state's word and the next audit found 52. Recreate method for a preserve doc: create → verify size → trash the old; never leave a same-named duplicate.
- **★ DRIVE FETCH: `read_file_content` returns plain text at 1× — use it for ALL text fetches.** `download_file_content` is base64 (~3×) — binary only.

**★ BEFORE PROPOSING TO REOPEN, REVISIT, OR REDESIGN ANYTHING, GREP `preserve\settled_rulings.md`** — closed questions live there, not in these docs; re-entry is a question to Matt from a demonstrated repo need.

**PRESERVE INDEX** (near-frozen — cite by path, never restate; claude.ai self-fetches via Drive; update whenever preserve changes):
- `settled_rulings.md` ~13k — every "never re-raise / firm" ruling, one line each, by area. The docs drop their tombstones into it.
- `gallery_pass_design.md` ~17k — the gallery pass as BUILT (steps 0–7, verified from source ckpt 75; ckpt-76 amendment: step 5a framing refinement, fifth sheet `refined_pairs`, its smoke truths SUPERSEDED in place; ckpt-78 amendment: per-pass candidates, seeded draw, picture identity, the node-view cache law, pricing off pass rows) + the truths its runs bought + decisions and why. Step 7 still says 2560 ss4 — session-side chore (fractal-state).
- `color_coverage_floor_design.md` 12.1k — the ruled coverage-floor spec (cells, pixel laws, three enforcement mechanisms, recolor pool, precedence fold, build order), UNBUILT; ckpt-78 amendment + ckpt-79 corrections (`1/cells`; 52 cells, collapse UNBUILT; the measured candidate↔release law; nine zero cells; pairs are a RECIPE fact). Build gate open; the ceiling is listed as under discussion, not in the spec.
- `sourcing_measurements.md` 12.5k — retired-head verdicts + run-era numbers (families, plane depth, deep descent, run10, julia/phoenix/twin math, motif saturation, deep_run1), PRIORS only.
- `audit_deep_descent_report.md` 17k — two-repo deep-surface audit (perturbation tier, S1/S2 anchors, `min_width` provenance, f64 sites, 5 contradictions); wallpapers line refs rot, the maker's hold.
- `deep_kernel_plan.md` 2.8k — the ruled perturbation arc, UNBUILT.
- `visitor_explorer_design.md` 1.8k — explorer design record; BUILT ckpt 70 — live mechanics = `explorer/README.md`.
- `parked.md` ~1.8k — deliberately unscheduled items; re-enter only from a demonstrated repo need.
- `maker_transfer_cautions.md` 1.9k — maker archive-read cautions + the old→new rename table.

---

## STANDING POSITIONS (Matt, firm)

- **★★ RUNS ARE PRODUCT; LABELING IS AN EVAL ACTIVITY (2026-08-13).** Runs are on Matt's schedule with no verification homework. **A LONG RUN (100 h+) MUST NEVER REQUIRE LABELING IN THE LOOP.** Labeling re-anchors the books when it happens; high-value sources ACCUMULATE (fractal-corpus). **Retrain when a decision needs it, NEVER preemptively.** A design that makes a run's allocation depend on fresh human labels is refused.
- **★★ THE DISTILLED-REPO MODEL (2026-08-14).** Fresh repo = everything pulled in cleanly, CONTEXT-FREE; labels FLAT; NO byte-identity requirement — cleanliness over byte-identicalness; shipped weights trained WITHIN the repo. Editorial line: *"this is about fractals, not ML."*
- **★★ NO ARCHAEOLOGY; DELETION IS NORMAL.** Don't resurrect artifacts that don't match how things work now; retention is Matt's, outside the repo. **★★ USEFULNESS BEFORE RECOVERABILITY** — if nothing will want it back, delete the regeneration machinery with the data; regenerability is not per-file when builds are chained.
- **★★ NOTHING LOAD-BEARING LIVES IN `scratch/`, both ways** — evidence leaves it when it justifies a decision; a proposal computed there never leaves as a fact. Exceptions in an enforced allowlist; Matt wipes scratch between checkpoints.
- **★★ A DURABLE RECORD WRITTEN AFTER A FALLIBLE STEP IS NOT DURABLE** — irreplaceable record first. **★★ LOSING HAND-LABELED DATA IS A MAJOR FAILURE** — nothing rewrites, deletes, or re-keys stored label rows; re-attribution is reader-side; verify exports BY ROW COUNT. **A tracked RECORD is never edited in place** — fix the reader's semantics, or add an amendment the reader prefers beside it. ONE exception (ckpt 75): a split REGISTRATION is a pre-build DECLARATION, not an event — a contradicting row is REFUSED at write and read, so a wrong registration is corrected in place [code: registry.refuse_contradiction; tests/test_label_registry.py].
- **★ REPO-DOC ADMISSION:** something in the code owns it and it stays true as the code changes; a transient measurement lives in scratch — survivors extracted, source deleted — **an extraction that does not delete its source is the failure; a rule nothing enforces is not a rule — name the guard.**
- **★★ ENFORCING FROZEN THRESHOLDS WERE THE ROOT CAUSE OF THE IMPOSSIBLE-STATE FAILURES.** Read-time rank + coarse semantic floors; a threshold change is a READ-TIME CHOICE, never an event that invalidates populations. Kept guards: sink isolation · dedup · label-carries-its-join · seeded determinism.
- **★★ THE 10,000-HOUR FRAME (Matt, 2026-08-22)** governs every product decision — in full at `preserve\gallery_pass_design.md` §1; pacing-never-rejection → settled_rulings. Don't over-think trivially small counts. **★ A DANGLING REFERENCE IS NOT A TASK** — a line that sounds like a task but names nothing in any repo fails the deletion test.
- **★ A RULE'S PURPOSE BOUNDS ITS SCOPE (ckpt 65).** Before refusing or redesigning on a rule, name what the rule protects; if that thing is not in play, the rule is not either.
- **★ TWO SPELLINGS OF ONE FACT IS A SILENT NULL (ckpt 70).** One adapter, one key, and the reader asserts the spelling it expects; a witness on the wrong axis understates a gap.
- **★ A DECLARED DESIGN THE LAUNCH DOESN'T READ IS NOT THE DESIGN (ckpt 76).** Guard two-ended — the launcher reads the declaration, the reader refuses a written config that disagrees, a planted mismatch fails; an artifact's size against its predecessor's is a free check. Explain a surprising result only after the realized recipe is verified.
- **★ WRONG-GEOMETRY ESTIMATES (ckpt 70):** cost tracks what the pixels do — pilot on the target population before sizing any leg; a prior from another population has been wrong by an order of magnitude.

---

## REASONING & MEASUREMENT

**Confidence convention.** Every verdict carries **basis** (`[human n=X]`·`[machine-decode]`·`[measured]`·`[inferred]`·`[by-eye]`), **population**, **overturned-by**. No falsifier = a belief; `[machine-decode]` is evidence about the MODEL, not the world.
- **★ Cuts and floors are RELATIVE TO A REFERENCE, never absolutes.** Every precision in a lock or anchored rate is a CEILING.
- **★★ TWO RESTATEMENT MODES when a cut must survive a head flip:** VOLUME-MATCHED (same fraction of a fixed reference pool; CORN scales are train-prior-calibrated) · HUMAN-DERIVED CROSSOVER (isotonic P(≥boundary)=0.5 on a labeled sheet; the volume change can BE the finding).
- **★★ NEVER POOL ACROSS AN ESTIMAND CHANGE. A REGENERATION MOVES EVERY MEASURED ROW** (partial adoption = hand-splice). **A DEFAULTED SEED IS A BAND**, not a neutral prior.
- **★ BUDGET A LEG OFF AN OBSERVED LEG, never off a rate** — rate extrapolations understate ~2× (bulk small-file moves: ~3×); stage anomalies rank by ratio to the unit's OWN median.
- **★ A reproducibility test re-runs the writer the artifact came from. ★ NEVER CONSTRUCT A TEST'S EXPECTED VALUE WITH THE TRANSFORM UNDER TEST**; a planted red proves the guard bites. **★ A PRE-DECLARED BAR MUST OUT-RESOLVE ITS INSTRUMENT**; a teacher's self-agreement is a ceiling, never a bar. **★★ A "BYTE-IDENTICAL" CLAIM IS PROVEN BY RUNNING THE REAL COMMANDS** — and scoped to the module that was compared.
- **★ Early reads of a slow-starting run:** mechanism valid immediately; yield is warm-up. **★★ A STAGE THAT CAN TRUNCATE ITS OWN INPUT ON THE WAY TO FAILING HIDES ITS OWN FAILURE** — refuse to write when draw and ledger share zero rows. An append-only log is a SUPERSET of checkpointed counters after a kill — dedup before quoting. **A clock started after a resume block under-reports every relaunched run** — a wall-vs-history inequality is not a concurrency tell.
- **★ A SIBLING SURFACE IS NOT A SOURCE (ckpt 74).** A cross-surface consistency claim (docs ↔ site ↔ code) is verified from CODE, never by copying a surface. Corollary: **a LIBRARY fact is not a PIPELINE fact** — a capability roster and the set a consumer actually draws diverge silently.
- **★ CHECK A VERDICT AGAINST THE DECISION'S OWN PARAMETERS BEFORE RELAYING (ckpt 74).** A feasibility verdict answers ONE parameterization.
- Judge-method and split rules are OWNED by fractal-corpus — point, don't restate.

---

## WORKING STYLE

One CC prompt at a time PER REPO — different repos concurrent by default; same-repo parallelism only when verified (proven: overnight wait-gate queueing; a second CC beside a GPU-bound wait — discipline in each repo's CLAUDE.md). **★★ A website prompt that may touch the engine LOCKS BOTH repos (Matt, 2026-08-21)** — check in-flight state across both before handing off and say so in the header; read-only audits (explicit no-write, no-commit) run beside anything. Engine carve-out for wasm consumers → fractal-tutorial §WORKFLOW. Progress-through-delivery over method minutiae; scope narrow; diagnosis-first is NOT a standing policy. **★ MATT'S N-HOUR BUDGET COVERS EVERYTHING** — build + run + post ≤N wall-clock; run cap ~N−2. **One run per budget — a follow-up of ANY length is a NEW budget question.** **★ EXPLORATORY ~8 h RUNS: ONE PROMPT COVERS LAUNCH AND POSTMORTEM** — CC stays up across the run and writes the readout at the end; separate readout prompts only as follow-ups; not for ~100 h runs (Matt, 2026-08-22). **★ THE 100-HOUR POSTURE:** bounded by disk and saturation convergence — never by a labeling cadence. **★ LAUNCHES TREND TO ONE COMMAND** — pre-flight facts and refusals fold into the run command; prep prompts tolerated meanwhile.

- Prompts = short `.md`, presented AND delivered; length scales with risk; trust CC on mechanics; steps >~30 s: CC estimates and backgrounds. **★ CC's honest spec-deviations with stated reasons are consistently right — read before overriding.** Supply claims to be CHECKED, not transcribed; ask for the corrections back. **★ AFTER A REPORT, DO NOT SUMMARIZE IT BACK** — say what it CHANGES, what Claude got WRONG, what's next; trivial outcomes ≤2 sentences (Matt). **★ NO "UNREVIEWED BY MATT" TRACKING** — assume CC's calls and the rendered state are fine until Matt says otherwise; flag only decisions that BLOCK upcoming work. The site is DRAFT — argue toward the right FINAL PRODUCT, never from churn.
- **★ NEVER EDIT A PROMPT ALREADY HANDED OVER** — addendums. Matt does NOT hand-edit JSON/config — he dictates, the prompt applies. Acceptance BY EYE except classifier evals. Git — commits, push, remotes — is his entirely; never flag or mention its state. **★ CC commits to `main` ONLY. ★★ NO COMMIT ≥20 MB WITHOUT MATT'S EXPLICIT PRIOR CONFIRMATION** (in repo CLAUDE.md; stop and ask).
- **★ A FIX WITH A SHAPE NEEDS THE PROMPT, NOT A "YES."** **★★ AUDIT-FIRST:** when a task needs technical knowledge the session lacks, STOP and ask Matt whether to send a facts-only audit prompt — never scaffold load-bearing content around CC-fill spots; audits report facts, the session authors prose. **★ A POLICY FLIP ASKS "WHO ELSE APPLIES THIS DECISION?"** — grep for private copies. **★ BUILD ≠ FLIP** — staged in one prompt, adopted in another against a pre-registered bar. Non-negotiables bought by disasters: pre-registered eval bars · blind human reads of any model-selected population · reject autopsy + identity round-trips. **Reject autopsy — standing habit:** every readout emits numbers AND a visual sample of admissions + rejects.
- **★★ QUEUE ORDER COMES FROM DEPENDENCIES, NEVER FROM WHAT IS ALREADY RULED (Matt, ckpt 76).** "X is ruled and scoped" is not a reason to run X first; ask what X needs and what needs X — a build whose benefit lands later still costs nothing to build now.
- **★ Name full paths in any delete/move instruction** — "delete v7" is a version, not a path.

**Labeling.** **★★ AFFORDABLE WHEN WE NEED IT** — size for power; renders, not labeling, price a batch (~6.3 rows/min labeled). **★★ LABELS MUST SERVE OBJECTIVES THE NEXT RETRAIN CANNOT DEPRECATE** — eval instruments, design reads, correction sittings pass; training volume fails by default. **★★ NEVER add calibration duplicates, drift probes, or repeat rows** — "noise is expected at all boundaries" (Matt), never re-raise. **★★ THE CORRECTION LOOP IS THE LABELING METHOD** (mechanics → fractal-corpus); assume proper randomization — a distribution concern is ≤1 line of prose. **★ Don't editorialize on a sheet about to be labeled blind.** A prompt running while Matt labels conflicts on GIT, not CPU — commit only its own files by explicit path.
