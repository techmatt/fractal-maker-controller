# fractal-operating — the method

**Amended by diff, never rewritten in full** (full rewrites only when Matt sanctions one; ckpt-39's compression pass was one). Read first, every session. Ownership test: *would this still be true if the project weren't fractals at all?*

---

## THE DOCUMENT SET

**Author & audience.** Claude writes these; sole consumer = a future fresh Claude. Write for yourself minus this session. Code-work CC prompts never mention them; the ONLY CC contact is the distillation apply-prompt (mechanical, never editorial).

**★ NEVER ENTER THE CODE REPO (Matt, firm).** The docs live in their own git-init'd folder (`C:\Code\fractal-maker-controller`) with a dedicated applier CC; a copy inside fractal-maker desyncs. Durable in-repo knowledge = `docs/design/*.md`.

**★ THE DOCS CHANGE ONLY VIA THE APPLY-PROMPT** — Matt never edits them; the doc-folder CC applies exact hunks + wholesale replacements (verbatim unique match or stop) ⇒ an uploaded copy is byte-identical to what Claude last authored; any doc-vs-memory discrepancy is Claude's error, never drift. Docs persist at `/mnt/user-data/uploads/` all conversation — re-read from disk.

**The roster — one doc per subject, grouped by what changes together:** operating (this method) · state (plan/status/flags/manifest — EVERY distillation) · engine (renderer, render canon, families, identity, anchors, machine guards) · storage (repo, durability contract, tracked-bulk policy) · orchestration (production loop, run safety, concurrency) · models (v11, stage-2 heads, screens, aug recipe) · thresholds (floors, τ_h, live cuts) · corpus (labels, sampling, rig, coverage) · discovery (stage 1: sourcing, maneuvers, hunt, harness) · emission (stage 2).

**★★ SELECTIVE DISTILLATION — the core rule (Matt).** At a distillation, claude.ai decides which docs the era touched or invalidated and emits ONLY those plus state.md — default a SMALL SUBSET; emitting everything needs a stated reason; an untouched doc cannot grow. **The apply-prompt does the applying:** a `DISTILL_`-prefixed prompt (content guard: working dir must hold the 10 fractal-*.md at root, no Cargo.toml/src/tools — else STOP) carries wholesale replacements + exact hunks, sanity-checks touched files against soft targets, spot-greps single-home, verifies untouched files untouched, one git commit.
- **Walk the full manifest once per distillation** — verdict per doc: TOUCHED / INVALIDATED (era changed its truth without editing it — staleness flag in state.md, never silence) / CLEAN.
- **State the scratch-preservation notice to Matt at every distillation** — what under `scratch/` MUST survive (read off the enforced allowlist) AND useful-to-keep candidates; default nothing necessary.
- Diffs by default; full rewrite only when heavily reworked or Matt asks; to add substantially, delete within the doc first. Distillation only from a SETTLED state — never mid-session, never with a CC prompt outstanding; its job is to CLOSE threads.
- **Delivery (Matt, 2026-08-11):** WHOLESALE replacement docs are emitted as INDIVIDUAL files and presented — Matt uploads them himself; the apply-prompt shrinks to guard + file list + hunks + spot-grep + one commit, and wholesale content never travels inside the prompt or through Drive. Exact-hunk distillations keep the in-prompt carrier.
- **Do NOT write the distillation prompt until the era's FINAL report is in** — it always changes it. Corrections to a handed-off prompt go as ADDENDUM files, never a rewrite (Matt, 2026-08-11).

**★★ SIZE TARGETS, NOT HARD CAPS (Matt).** Soft targets in state.md's roster; the deletion test is the real control; small justified overage fine, dramatic overage/padding = stop and report; targets move only with Matt; no size bookkeeping beyond this. state.md holds NO FACTS — status/plan/flags/roster only; a fact that needs recording forces its owner doc onto the touched list.

**★★ WHAT GOES IN — THE DELETION TEST (Matt, firm).** *"These docs are the ACTIVE WAVEFRONT, not a history of what has happened to the project."* A line survives only if it would change a FUTURE decision AND cannot be encoded in code. Three things pass: decisions not yet made · measurement-validity caveats that would cause a future result to be MISREAD · true-but-unenforceable facts. Everything else goes. Durable anchors (coords, thresholds, pins, formulas) stay verbatim; reconstructable from code/git → pointer; spec in `docs/design/*.md` → exact path, never restate.
- **The four compression rules (standing, 2026-08-11):** 1. a number that lives in a tracked repo file never appears in a handoff doc — verdict + exact path · 2. a `[code:]`-tagged fact with a guard behind it is one line + pointer; the guard is the memory · 3. a closed arc is ≤3 lines: verdict · what it changed · record path · 4. run facts live in run records; a handoff doc keeps only the transferable lesson.
- **⚠ The failure mode is Claude's:** treating a CC report as material to CARRY rather than evidence a doc line can be CUT.

**★★ SINGLE-HOME.** One doc per subject; at a distillation, grep each bolded numeral across the emitted docs and assert single occurrence. Other docs may NAME a fact and cross-reference; never restate its value or mechanism.

**★★ TAG CLAIMS ABOUT CODE.** A line asserting what the tree does carries `[code: path]` or `[unverified]`. Untagged = decisions or measurements; every checkpoint that checked has falsified some of these. **A claim of AUTOMATIC FUTURE BEHAVIOR requires `[code: path]` naming the enforcing mechanism — else it is not written (Matt).**

**Compression.** Telegraphic, fragments, no scaffolding. **Rewording ≠ compressing**; when a reword pass stops paying, delete whole blocks.

**★ THE REPO PRACTICE DOCS** — `docs/design/verification_practice.md` · `measurement_practice.md` · `retired.md` (append-only; a reversal is a new UN-RETIRED entry, never an edit; a reused or re-scoped retired policy needs a new dated entry). Prompts CITE them, this doc set never restates them; check `retired.md` before proposing an approach.

**Self-perpetuation.** Each future Claude knows only what these docs contain → carry this document forward, amended or preserved, never eroded.

---

## TIER 0.5 — THE EXCHANGE FOLDER

**`C:\Code\fractal-drive-sync\{prompts,reports}\`** — Drive-synced, outside both repos: claude.ai writes prompts into `prompts\`; CC copies reports into `reports\`. **SCRATCH — Matt deletes freely**; empty/absent is normal. One writer per subfolder; `scratch/` stays a report's canonical home.
- **★★ THE STANDING PROMPT CONTRACT LIVES IN fractal-maker's `CLAUDE.md`** (`## Standing prompt contract`, `6634410`) — report shape/path/delivery, runtime discipline, engine-subprocess helpers, commit gate. **Prompts no longer restate any of it** — including the ≤10-line VERDICT block at report top (absorbed 2026-08-12); absorb by cross-reference, never by copy.
- **★ ALL PROMPTS GO THROUGH `prompts\`** — code-work and session/distillation prompts alike; one channel, no exceptions.
- The controller repo's `CLAUDE.md` carries the mirror rules. **CC MAY be pointed at `C:\Code\fractal-maker-controller` directly, even from fractal-maker prompts — READ-ONLY to code-work CC (Matt, 2026-08-11).** `matt-claude-workflow.md` (exchange-folder root) documents the pattern for a NEW project.
- **★★ CONTEXT STEWARDSHIP IS PART OF THE SESSION CONTRACT.** Claude tracks its OWN context budget against a **~150k soft ceiling (raised 2026-08-11 from 100k — a session should span multiple prompt/report cycles)**; on reaching it, **call "checkpoint now" instead of proposing a further prompt**; report a token estimate at the checkpoint.
- **★ DRIVE FETCH: `Google Drive:read_file_content` returns PLAIN TEXT at 1× — use it for ALL text/report fetches.** `download_file_content` base64-encodes (~3× with decode) — binary only. (Supersedes the "decode once" lesson, which had tested only the download path.)

---

## STANDING POSITIONS (Matt, firm)

- **★★ RUNS ARE PRODUCT; LABELING IS AN EVAL ACTIVITY (Matt, 2026-08-13).** The required-run chain ended at run 27 — future runs are product, on Matt's schedule, with no verification homework attached. **A LONG RUN (100 hr+) MUST NEVER REQUIRE LABELING IN THE LOOP.** Labeling happens as its own act and RE-ANCHORS the books when it does; high-value sources ACCUMULATE between sittings (fractal-corpus) rather than standing as obligations. **Retrain when a decision needs it, NEVER preemptively.** Corollary, and the test to apply to any proposed mechanism: **a design that makes a run's allocation depend on fresh human labels is refused** — that is what the self-updating deficit bought (fractal-discovery).
- **★★ NO ARCHAEOLOGY; DELETION IS NORMAL.** Don't resurrect artifacts that don't match how things work now; only the latest model matters. Matt holds retention outside the repo; last-resort → ask once, then move on.
- **★★ USEFULNESS BEFORE RECOVERABILITY.** Will anything ever want it back? If not, delete the regeneration machinery with the data. **Regenerability is not per-file when builds are chained** — rebuilding needs the ORDER, which nothing in code states.
- **★★ NOTHING LOAD-BEARING LIVES IN `scratch/`, both ways.** Evidence leaves it the moment it justifies a durable decision; a proposal computed there never leaves it as a fact. Exceptions DECLARED in the enforced allowlist (fractal-storage) with owner + lifetime; Matt wipes scratch between checkpoints.
- **★★ A DURABLE RECORD WRITTEN AFTER A FALLIBLE STEP IS NOT DURABLE IN PRACTICE.** Write the irreplaceable record first, then the work that can fail.
- **★★ LOSING HAND-LABELED DATA IS A MAJOR FAILURE (Matt, firm).** Nothing rewrites, deletes, or re-keys stored label rows; re-attribution is reader-side only; verify every export merged BY ROW COUNT.
- **★ `docs/design/` ADMISSION:** something in the code owns it and it stays true as the code changes. A transient measurement lives in scratch, survivors extracted into the owning doc, then deleted — **an extraction that does not delete its source is the failure; a rule nothing enforces is not a rule — name the guard.**
- **★ FRACTAL TYPES ARE PERMANENT DESIGN CONSTRAINTS** — phoenix and the 2% classic-phoenix case included. Retiring a generation METHOD is legitimate only when emission for that type is uncompromised.
- **★★ ENFORCING FROZEN THRESHOLDS WERE THE ROOT CAUSE OF THE IMPOSSIBLE-STATE FAILURES (Matt).** Derived per-partition cuts held as frozen state produced the recurring "zero supply / impossible by construction" pattern. **Prefer read-time rank + coarse semantic floors; a threshold change should be a READ-TIME CHOICE, never an event that invalidates populations.** Kept guards: sink isolation · dedup · label-carries-its-join · seeded determinism.

---

## REASONING

**Confidence convention.** Every verdict carries **basis** (`[human n=X]`·`[machine-decode]`·`[measured]`·`[inferred]`·`[by-eye]`), **population** (most falsified verdicts were population errors wearing a number), **overturned-by**. No falsifier = a belief; `[machine-decode]` is evidence about the MODEL, not the world.
- **★ A reproducibility test must re-run the writer the artifact came from**, not a plausible neighbour; a prompt making classification mechanical PINS the writer.
- **★★ A "BYTE-IDENTICAL REBUILD" CLAIM IS PROVEN BY RUNNING THE REAL COMMANDS, FIRST** — before anything is de-tracked, with the dependencies already gone. It is also the step that finds what does NOT reproduce (a live disk probe frozen into a record has no guard and will differ).
- **★ Early reads of a slow-starting run:** mechanism (mix conformance, queue states) valid immediately; yield/funnel is warm-up, not the run.
- **★★ A STAGE THAT CAN TRUNCATE ITS OWN INPUT ON THE WAY TO FAILING HIDES ITS OWN FAILURE** — refuse to write when the draw and the ledger share zero rows, BEFORE opening the output; fix any self-exclusion separately so the guard is not the only wall.

---

## WORKING STYLE

One CC prompt at a time; wait for results. Progress-through-delivery over methodological minutiae (Matt); scope narrow; diagnosis-first is NOT a standing policy. **★ MATT'S N-HOUR BUDGET COVERS EVERYTHING** — build + shakedown + run + post done ≤N wall-clock; the run's own cap ~N−2, shaved further when build/post estimates grow; overlapping build/post with a running crawl is legitimate. Deadline form = same semantics at launch: reserve for post, wall-budget = remaining − reserve, active = wall/1.15; the pre-loop draw is OUTSIDE the wall cap — subtract its bound too (fractal-orchestration). **One run per budget: a follow-up run of ANY length is a NEW budget question for Matt — never launch back-to-back on inference.** **★ THE 100-HOUR POSTURE:** a run at that scale is bounded by disk and by unmeasured saturation convergence — never by a labeling cadence. The in-run pruner removed the disk blocker (fractal-orchestration); the convergence unknown is open (state).

- Prompts = short `.md` in `/mnt/user-data/outputs/`, presented, never inline; scale length to risk; trust CC on mechanics; prompts touching tests/guards/measurements cite the practice docs by path.
- **★ CC's honest spec-deviations with stated reasons are consistently right — read before overriding.** Supply claims to be CHECKED, not text to transcribe; ask for the corrections list back. **★ AFTER A REPORT, DO NOT SUMMARIZE IT BACK** — say only what it CHANGES, what Claude got WRONG, and what's next.
- **★ NEVER EDIT A PROMPT ALREADY HANDED OVER** — addendums as separate paste-able files. Not-yet-run → edit. If an outputs file diverges from what ran, restore it.
- Matt does NOT hand-edit JSON/config — he dictates, the prompt applies. Acceptance BY EYE except classifier evals. Git — commits, push, remotes, auth — is his entirely: never flag, track, or mention its state. **★ CC commits to `main` ONLY.** **★★ NO COMMIT ≥20 MB — single blob or aggregate, LFS counted — WITHOUT MATT'S EXPLICIT PRIOR CONFIRMATION (firm):** binds claude.ai prompts and CC alike; encoded in repo CLAUDE.md; stop and ask.
- **★ A FIX WITH A SHAPE NEEDS THE PROMPT, NOT A "YES"** (derive-from-data vs hardcode, relational vs literal).
- **★ A POLICY FLIP ASKS "WHO ELSE APPLIES THIS DECISION?"** — an owner only decides for the sites that ask it; grep for private copies before declaring a flip done (bit twice).
- **★ BUILD ≠ FLIP.** Built and staged in one prompt, adopted in another against a pre-registered bar. Standing exceptions bought by disasters: pre-registered eval bars · blind human reads as adjudicator of any model-selected population · reject autopsy + identity round-trips.
- **★★ THE RETRAIN PROTOCOL IS THE OWNER — POINT, DON'T RESTATE** (`docs/design/classifier_retrain_protocol.md`): **§2a** contradicting stamped splits → global re-derivation (or a frozen authority) · **§2b** anchored correction-sheet labels are train-side only, per-head · **§5a** volume-matching · **§5-0** the pin-marker class. Corpus owns §2a/§2b's populations; thresholds owns the cuts.
- **★★ A STAGE-2 FLIP IS NOT A STAGE-1 FLIP** — §5's ledger-rescore and τ_h steps are LOCATION-HEAD-SPECIFIC; a stage-2 pin move touches no ledger `p_good`. Stage-2 score carriers (`release_records`, `mining_gate_reports`) are RECORDS OF DECISIONS TAKEN, never rewritten: the `floor` column says what each was judged against; loss stated as `known_flip_cost` in the adoption records.
- **★ A `--limit` RUN STAMPS `incomplete` AND THE LOCK REFUSES IT** — a partial measurement must not become a calibration.
- **Run safety is owned by `verification_practice.md` §11** (detached launches · liveness · up-front input validation · atomic/resumable writes · reaper survival · a-running-trainer-pins-every-module · shakedown-before-a-long-unattended-run · cap semantics); **red-test-nobody-runs → §4**. Prompts cite; this doc no longer restates the mechanics. Two corollaries stay: an append-only log is a SUPERSET of checkpointed counters after a kill — dedup before quoting a log-derived rate · cap = accumulated ACTIVE time, checked at the finest safe boundary, don't start a unit that can't finish.

**Labeling.**
- **★★ LABELING IS AFFORDABLE WHEN WE NEED IT (Matt)** — size for statistical power, spend deliberately; **renders, not labeling, price a batch build** [~6.3 rows/min at label fidelity] — budget around render time and bound it.
- **★★ LABELS MUST SERVE OBJECTIVES THE NEXT RETRAIN CANNOT DEPRECATE (Matt, firm).** Passes: eval instruments, design reads, correction sittings; score-unconditioned draws = one-time purchase, DEMOTED to contingency; fails by default: training volume for the current head.
- **★★ NEVER add calibration duplicates, drift probes, repeat rows, or ANY calibration aid to a labeling batch (firm).** "Noise is expected at all boundaries" (Matt) — never re-raise adjacent-category disagreement or bar drift.
- **★★ THE CORRECTION LOOP IS THE LABELING METHOD (Matt):** heads pre-label, Matt corrects (mechanics → fractal-corpus); assume proper randomization — a real distribution concern gets ≤1 line of prose, never a design; per-sitting correction rate = the head's report card and the convergence metric; reads off corrected labels are CEILINGS (anchoring) — state it, it blocks nothing.
- **★ Don't editorialize on a sheet about to be labeled blind** (design commentary only; an INSPECTION sheet inverts one rule: literal cached bytes, parameters captioned, no vivid substitution). **★ A prompt running while Matt labels conflicts on GIT, not CPU** — commit only your own files by explicit path.
