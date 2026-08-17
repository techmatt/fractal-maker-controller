# fractal-operating — the method

**Amended by diff, never rewritten in full** (full rewrites only when Matt sanctions one; the ckpt-50 cut pass was one). Read first, every session. Ownership test: *would this still be true if the project weren't fractals at all?*

---

## THE DOCUMENT SET

**Author & audience.** Claude writes these; sole consumer = a future fresh Claude. Write for yourself minus this session. Code-work CC prompts never mention them; the ONLY CC contact is the distillation apply-prompt (mechanical, never editorial).

**★ NEVER ENTER THE CODE REPO (Matt, firm).** The docs live in their own git-init'd folder (`C:\Code\fractal-maker-controller`) with a dedicated applier CC; a copy inside a code repo desyncs. Durable in-repo knowledge = each repo's `docs/`.

**★ THE DOCS CHANGE ONLY VIA THE APPLY-PROMPT** — Matt never edits them; the doc-folder CC applies exact hunks + wholesale replacements (verbatim unique match or stop) ⇒ an uploaded copy is byte-identical to what Claude last authored; any doc-vs-memory discrepancy is Claude's error, never drift. Docs persist at `/mnt/user-data/uploads/` all conversation — re-read from disk.

**The roster — one doc per subject, grouped by what changes together:** operating (this method) · state (plan/status/flags/roster — EVERY distillation) · tutorial (the active repo fractal-wallpapers + the website/article) · corpus (labels, sampling, judge method, the accumulator) · discovery (sourcing truths) · engine (archive stub: anchors + cross-repo render truths) · storage (archive stub) — **seven docs** since ckpt 50. Retired at ckpt 50: emission, orchestration, models, thresholds — survivors folded; recovery = controller git history.

**★★ SELECTIVE DISTILLATION — the core rule (Matt).** At a distillation, claude.ai decides which docs the era touched or invalidated and emits ONLY those plus state.md — default a SMALL SUBSET; emitting everything needs a stated reason; an untouched doc cannot grow. **The apply-prompt does the applying:** a `DISTILL_`-prefixed prompt (content guard: working dir must hold the seven `fractal-*.md` at root, no Cargo.toml/src/tools — else STOP) carries wholesale replacements + exact hunks, sanity-checks touched files against soft targets, spot-greps single-home, verifies untouched files untouched, one git commit.
- **Walk the full manifest once per distillation** — verdict per doc: TOUCHED / INVALIDATED (era changed its truth without editing it — staleness flag in state.md, never silence) / CLEAN.
- **State the scratch-preservation notice to Matt at every distillation** — what under `scratch/` MUST survive AND useful-to-keep candidates; default nothing necessary.
- Diffs by default; full rewrite only when heavily reworked or Matt asks; to add substantially, delete within the doc first. Distillation only from a SETTLED state — never mid-session, never with a CC prompt outstanding; its job is to CLOSE threads.
- **Delivery (Matt, 2026-08-11):** WHOLESALE replacement docs are emitted as INDIVIDUAL files and presented — Matt places them himself; the apply-prompt shrinks to guard + file list + hunks + spot-grep + one commit, and wholesale content never travels inside the prompt or through Drive. Exact-hunk distillations keep the in-prompt carrier.
- **Do NOT write the distillation prompt until the era's FINAL report is in** — it always changes it. Corrections to a handed-off prompt go as ADDENDUM files, never a rewrite (Matt, 2026-08-11).

**★★ SIZE TARGETS, NOT HARD CAPS (Matt).** Soft targets in state.md's roster; the deletion test is the real control; small justified overage fine, dramatic overage/padding = stop and report; targets move only with Matt; no size bookkeeping beyond this. state.md holds NO FACTS — status/plan/flags/roster only; a fact that needs recording forces its owner doc onto the touched list.

**★★ WHAT GOES IN — THE DELETION TEST (Matt, firm).** *"These docs are the ACTIVE WAVEFRONT, not a history of what has happened to the project."* A line survives only if it would change a FUTURE decision AND cannot be encoded in code. Three things pass: decisions not yet made · measurement-validity caveats that would cause a future result to be MISREAD · true-but-unenforceable facts. Everything else goes. Durable anchors (coords, thresholds, pins, formulas) stay verbatim; reconstructable from code/git → pointer; spec in a repo doc → exact path, never restate.
- **The four compression rules (standing, 2026-08-11):** 1. a number that lives in a tracked repo file never appears in a handoff doc — verdict + exact path · 2. a `[code:]`-tagged fact with a guard behind it is one line + pointer; the guard is the memory · 3. a closed arc is ≤3 lines: verdict · what it changed · record path · 4. run facts live in run records; a handoff doc keeps only the transferable lesson.
- **⚠ The failure mode is Claude's:** treating a CC report as material to CARRY rather than evidence a doc line can be CUT.

**★★ SINGLE-HOME.** One doc per subject; at a distillation, grep each bolded numeral across the emitted docs and assert single occurrence. Other docs may NAME a fact and cross-reference; never restate its value or mechanism.

**★★ TAG CLAIMS ABOUT CODE.** A line asserting what the tree does carries `[code: path]` or `[unverified]`. Untagged = decisions or measurements; every checkpoint that checked has falsified some of these. **A claim of AUTOMATIC FUTURE BEHAVIOR requires `[code: path]` naming the enforcing mechanism — else it is not written (Matt).**

**Compression.** Telegraphic, fragments, no scaffolding. **Rewording ≠ compressing**; when a reword pass stops paying, delete whole blocks.

**★ THE REPO PRACTICE DOCS** — each repo's `verification_practice.md` / `measurement_practice.md` / `retired.md` equivalents (append-only; a reversal is a new UN-RETIRED entry, never an edit). Prompts CITE them, this doc set never restates them; check the retired record before proposing an approach.

**Self-perpetuation.** Each future Claude knows only what these docs contain → carry this document forward, amended or preserved, never eroded.

---

## TIER 0.5 — THE EXCHANGE FOLDER

**`C:\Code\fractal-drive-sync\{prompts,reports,prose}\`** — Drive-synced, outside all repos: claude.ai writes prompts into `prompts\` and article drafts into `prose\`; CC copies reports into `reports\`. **SCRATCH — Matt deletes freely**; empty/absent is normal. One writer per subfolder; `scratch/` stays a report's canonical home.
- **★★ THE STANDING PROMPT CONTRACT LIVES IN EACH REPO'S `CLAUDE.md`** — report shape/path/delivery, runtime discipline, commit gate. **Prompts no longer restate any of it** — absorb by cross-reference, never by copy. Every CC prompt still carries an explicit "Commit when done." line unless the prompt states its specific reason not to.
- **★ ALL PROMPTS GO THROUGH `prompts\`** — code-work and session/distillation prompts alike; one channel, no exceptions.
- **Every prompt opens with a TARGET-REPO guard** naming its repo (`fractal-wallpapers` / `fractal-website` / `fractal-maker` / `fractal-maker-controller`) with STOP-on-mismatch.
- **★★ CHECKPOINT PROMPT NAMING (Matt, 2026-08-14): `DISTILL_ckptXX_apply.md` is ALWAYS the controller-CC apply prompt (mechanical); `continuation_ckptXX.md` is what a fresh claude.ai session receives alongside the docs.** **A checkpoint produces exactly ONE hand-off artifact.** If the checkpoint distills: author the apply prompt alone — the updated doc set, especially state's status/OPEN/Queue, IS the fresh session's hand-in; session-specific context a fresh session needs is written INTO state, never into a side file. If a session hands off WITHOUT distilling: author `continuation_ckptXX.md` alone, against the unchanged docs. Never both.
- The controller repo's `CLAUDE.md` carries the mirror rules. **CC MAY be pointed at `C:\Code\fractal-maker-controller` directly — READ-ONLY to code-work CC (Matt, 2026-08-11).** `matt-claude-workflow.md` (exchange-folder root) documents the pattern for a NEW project.
- **★★ CONTEXT STEWARDSHIP IS PART OF THE SESSION CONTRACT.** Claude tracks its OWN context budget against a **~150k soft ceiling**; on reaching it, **call "checkpoint now" instead of proposing a further prompt**; report a token estimate at the checkpoint.
- **★ DRIVE FETCH: `Google Drive:read_file_content` returns PLAIN TEXT at 1× — use it for ALL text/report fetches.** `download_file_content` base64-encodes (~3× with decode) — binary only.

---

## STANDING POSITIONS (Matt, firm)

- **★★ RUNS ARE PRODUCT; LABELING IS AN EVAL ACTIVITY (Matt, 2026-08-13).** Runs are on Matt's schedule with no verification homework attached. **A LONG RUN (100 hr+) MUST NEVER REQUIRE LABELING IN THE LOOP.** Labeling happens as its own act and RE-ANCHORS the books when it does; high-value sources ACCUMULATE between sittings (fractal-corpus) rather than standing as obligations. **Retrain when a decision needs it, NEVER preemptively.** Corollary, and the test for any proposed mechanism: **a design that makes a run's allocation depend on fresh human labels is refused.**
- **★★ THE DISTILLED-REPO MODEL (Matt, 2026-08-14).** Fresh repo = everything pulled in cleanly, CONTEXT-FREE — no version baggage, no side-script ecology. Labels move FLAT: resolved one-row, split PROVIDED as data, iteration history ≈ a few sentences. NO byte-identity requirement — cleanliness over byte-identicalness; the bar = a head trained INSIDE the clean repo lands ~within new-seed variance. Shipped weights are trained WITHIN the small repo, never copied. Editorial line: *"this is about fractals, not ML."* Per-transfer: Matt+Claude jointly pick the minimal clean form.
- **★★ NO ARCHAEOLOGY; DELETION IS NORMAL.** Don't resurrect artifacts that don't match how things work now; only the latest model matters. Matt holds retention outside the repo; last-resort → ask once, then move on.
- **★★ USEFULNESS BEFORE RECOVERABILITY.** Will anything ever want it back? If not, delete the regeneration machinery with the data. **Regenerability is not per-file when builds are chained** — rebuilding needs the ORDER, which nothing in code states.
- **★★ NOTHING LOAD-BEARING LIVES IN `scratch/`, both ways.** Evidence leaves it the moment it justifies a durable decision; a proposal computed there never leaves it as a fact. Exceptions DECLARED in an enforced allowlist with owner + lifetime; Matt wipes scratch between checkpoints.
- **★★ A DURABLE RECORD WRITTEN AFTER A FALLIBLE STEP IS NOT DURABLE IN PRACTICE.** Write the irreplaceable record first, then the work that can fail.
- **★★ LOSING HAND-LABELED DATA IS A MAJOR FAILURE (Matt, firm).** Nothing rewrites, deletes, or re-keys stored label rows; re-attribution is reader-side only; verify every export merged BY ROW COUNT.
- **★ A repo-doc ADMISSION test:** something in the code owns it and it stays true as the code changes. A transient measurement lives in scratch, survivors extracted into the owning doc, then deleted — **an extraction that does not delete its source is the failure; a rule nothing enforces is not a rule — name the guard.**
- **★ FRACTAL TYPES ARE PERMANENT DESIGN CONSTRAINTS** — phoenix and the ~1.5% classic-phoenix case included. Retiring a generation METHOD is legitimate only when release for that type is uncompromised.
- **★★ ENFORCING FROZEN THRESHOLDS WERE THE ROOT CAUSE OF THE IMPOSSIBLE-STATE FAILURES (Matt).** Derived per-partition cuts held as frozen state produced the recurring "zero supply / impossible by construction" pattern. **Prefer read-time rank + coarse semantic floors; a threshold change should be a READ-TIME CHOICE, never an event that invalidates populations.** Kept guards: sink isolation · dedup · label-carries-its-join · seeded determinism.

---

## REASONING & MEASUREMENT

**Confidence convention.** Every verdict carries **basis** (`[human n=X]`·`[machine-decode]`·`[measured]`·`[inferred]`·`[by-eye]`), **population** (most falsified verdicts were population errors wearing a number), **overturned-by**. No falsifier = a belief; `[machine-decode]` is evidence about the MODEL, not the world.
- **★ Cuts and floors are expressed RELATIVE TO A REFERENCE, never as absolutes** — a float says nothing about which model it describes; an annotation on the wrong probability scale is as unreadable as a gate on one. **Every precision in any lock or anchored rate is a CEILING.**
- **★★ TWO RESTATEMENT MODES when a cut must survive a head flip, choose by evidence class:** (1) VOLUME-MATCHED — restate a floor as the score passing the SAME FRACTION of a fixed reference pool (CORN scales are train-prior-calibrated; a retrain moves the whole scale) · (2) HUMAN-DERIVED CROSSOVER — isotonic P(≥boundary)=0.5 on a labeled sheet; the midpoint convention is reusable, its volume invariant is NOT — the volume change can BE the finding.
- **★★ NEVER POOL ACROSS AN ESTIMAND CHANGE** — single-source is the rule, not a convenience. **A REGENERATION MOVES EVERY MEASURED ROW** — holding some rows at old values while taking others from a new run is a hand-splice. **A DEFAULTED SEED IS NOT A NEUTRAL PRIOR — IT IS A BAND** a converged estimator may never escape.
- **★ BUDGET A LEG OFF AN OBSERVED LEG, never off a rate** — file-rate extrapolations have understated legs ~2×; stage anomalies rank by ratio to the unit's OWN stage median, never by raw seconds.
- **★ A reproducibility test must re-run the writer the artifact came from**, not a plausible neighbour; a prompt making classification mechanical PINS the writer.
- **★ NEVER CONSTRUCT A TEST'S EXPECTED VALUE WITH THE TRANSFORM UNDER TEST** — a guard that folds/normalizes its own reference encodes the bug as the expectation; expectations come from an independent route, and a planted red proves the guard bites.
- **★ A PRE-DECLARED BAR MUST OUT-RESOLVE ITS OWN INSTRUMENT** — a floor inside the instrument's margin returns a FAIL the sheet cannot confirm; a control that is the teacher's SELF-AGREEMENT is a ceiling reference, never a bar.
- **★★ A "BYTE-IDENTICAL REBUILD" CLAIM IS PROVEN BY RUNNING THE REAL COMMANDS, FIRST** — before anything is de-tracked, with the dependencies already gone.
- **★ Early reads of a slow-starting run:** mechanism (mix conformance, queue states) valid immediately; yield/funnel is warm-up, not the run.
- **★★ A STAGE THAT CAN TRUNCATE ITS OWN INPUT ON THE WAY TO FAILING HIDES ITS OWN FAILURE** — refuse to write when the draw and the ledger share zero rows, BEFORE opening the output.
- An append-only log is a SUPERSET of checkpointed counters after a kill — dedup before quoting a log-derived rate. Cap = accumulated ACTIVE time, checked at the finest safe boundary; don't start a unit that can't finish.

---

## WORKING STYLE

One CC prompt at a time; wait for results. Progress-through-delivery over methodological minutiae (Matt); scope narrow; diagnosis-first is NOT a standing policy. **★ MATT'S N-HOUR BUDGET COVERS EVERYTHING** — build + shakedown + run + post done ≤N wall-clock; the run's own cap ~N−2, shaved further when build/post estimates grow; overlapping build/post with a running crawl is legitimate. **One run per budget: a follow-up run of ANY length is a NEW budget question for Matt — never launch back-to-back on inference.** **★ THE 100-HOUR POSTURE:** a run at that scale is bounded by disk and by unmeasured saturation convergence — never by a labeling cadence.

- Prompts = short `.md` in `/mnt/user-data/outputs/`, presented, never inline; scale length to risk; trust CC on mechanics; prompts touching tests/guards/measurements cite the repo practice docs by path.
- **★ CC's honest spec-deviations with stated reasons are consistently right — read before overriding.** Supply claims to be CHECKED, not text to transcribe; ask for the corrections list back. **★ AFTER A REPORT, DO NOT SUMMARIZE IT BACK** — say only what it CHANGES, what Claude got WRONG, and what's next.
- **★ NEVER EDIT A PROMPT ALREADY HANDED OVER** — addendums as separate paste-able files. Not-yet-run → edit. If an outputs file diverges from what ran, restore it.
- Matt does NOT hand-edit JSON/config — he dictates, the prompt applies. Acceptance BY EYE except classifier evals. Git — commits, push, remotes, auth — is his entirely: never flag, track, or mention its state. **★ CC commits to `main` ONLY.** **★★ NO COMMIT ≥20 MB — single blob or aggregate, LFS counted — WITHOUT MATT'S EXPLICIT PRIOR CONFIRMATION (firm):** encoded in repo CLAUDE.md; stop and ask.
- **★ A FIX WITH A SHAPE NEEDS THE PROMPT, NOT A "YES"** (derive-from-data vs hardcode, relational vs literal).
- **★ A POLICY FLIP ASKS "WHO ELSE APPLIES THIS DECISION?"** — an owner only decides for the sites that ask it; grep for private copies before declaring a flip done (bit twice).
- **★ BUILD ≠ FLIP.** Built and staged in one prompt, adopted in another against a pre-registered bar. Standing exceptions bought by disasters: pre-registered eval bars · blind human reads as adjudicator of any model-selected population · reject autopsy + identity round-trips. **Reject autopsy — standing habit:** every readout emits numbers AND a visual sample of admissions + rejects.
- Judge-method and split rules (winner rule, §2a/§2b analogues, anchored-vs-blind) are OWNED by fractal-corpus — point, don't restate.

**Labeling.**
- **★★ LABELING IS AFFORDABLE WHEN WE NEED IT (Matt)** — size for statistical power, spend deliberately; **renders, not labeling, price a batch build** [~6.3 rows/min at label fidelity] — budget around render time and bound it.
- **★★ LABELS MUST SERVE OBJECTIVES THE NEXT RETRAIN CANNOT DEPRECATE (Matt, firm).** Passes: eval instruments, design reads, correction sittings; score-unconditioned draws = one-time purchase, demoted to contingency; fails by default: training volume for the current head.
- **★★ NEVER add calibration duplicates, drift probes, repeat rows, or ANY calibration aid to a labeling batch (firm).** "Noise is expected at all boundaries" (Matt) — never re-raise adjacent-category disagreement or bar drift.
- **★★ THE CORRECTION LOOP IS THE LABELING METHOD (Matt):** heads pre-label, Matt corrects (mechanics → fractal-corpus); assume proper randomization — a real distribution concern gets ≤1 line of prose, never a design; per-sitting correction rate = the head's report card; reads off corrected labels are CEILINGS — state it, it blocks nothing.
- **★ Don't editorialize on a sheet about to be labeled blind** (an INSPECTION sheet inverts one rule: literal cached bytes, parameters captioned, no vivid substitution). **★ A prompt running while Matt labels conflicts on GIT, not CPU** — commit only your own files by explicit path.
