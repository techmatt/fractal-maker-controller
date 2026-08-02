# fractal-operating — the method

**Amended by diff, never rewritten in full.** Read first, every session. The rules for how this document set and this collaboration work. Ownership test: *would this still be true if the project weren't fractals at all?*

---

## THE DOCUMENT SET

**Author & audience.** Claude (claude.ai) writes these; sole consumer is a future Claude, fresh, reconstructing state. Write for yourself minus this session. CC never sees them; CC prompts never mention them.

**★ NEVER ENTER THE REPO (Matt, firm).** claude.ai working memory only — a repo copy desyncs the moment CC edits it. Durable in-repo knowledge = `docs/design/*.md`.

**★ MATT NEVER MODIFIES THESE DOCS** ⇒ an uploaded copy is byte-identical to what Claude last emitted; any doc-vs-memory discrepancy is Claude's error, never drift. They persist at `/mnt/user-data/uploads/` all conversation — if uploaded earlier in the SAME session, re-read from disk rather than asking again.

**The roster — one doc per subject, grouped by what changes together:**

| doc | owns | changes when |
|---|---|---|
| **operating** | this method | Matt changes how we work |
| **state** | plan, status, flags, manifest, open/parked | EVERY distillation |
| **engine** | renderer, render canon, families, identity, anchors, machine guards | renderer/family/render-axis work |
| **storage** | repo, durability contract, tracked-bulk policy | storage/repo work |
| **orchestration** | production loop, run safety, concurrency | orchestrator work |
| **models** | v8, ranker, screens, aug recipe | retrains |
| **thresholds** | t_good, τ_h, keeper cuts, decode predicate | flips / re-derivations |
| **corpus** | labels, sampling regime, rig, coverage | labeling |
| **discovery** | stage 1, sourcing, maneuvers, hunt, harness | discovery work |
| **emission** | stage 2 | emission work |

**★★ SELECTIVE DISTILLATION — the core rule of this regime (Matt).** At a distillation, **claude.ai itself decides which docs the era touched or invalidated, and emits ONLY those plus state.md.** The default output is a SMALL SUBSET — state + 1–3 docs; emitting everything requires a stated reason. **An untouched doc is not re-emitted at all** — Matt's copy stays canonical, and a doc that isn't rewritten cannot grow. state.md's manifest tells Matt which files to replace.
- **Walk the full manifest once per distillation** — verdict per doc: TOUCHED (amend) / INVALIDATED (era changed its truth without editing it — e.g. a flip invalidates thresholds) / CLEAN. Invalidated-but-not-rewritten gets a staleness flag in state.md, never silence.
- **Stable docs are amended by diff.** A full rewrite of any one doc happens only when its subject was heavily reworked, or Matt asks.
- Distillation still only from a SETTLED state — never mid-session, never with a CC prompt outstanding; its job is to CLOSE threads, not open them.

**★★ CEILINGS.** Per-doc, recorded in state.md's manifest, checked with `wc -c` at every touch. An amendment may not push a doc over its ceiling — to add, delete within that doc first. **Ceilings never increase without Matt.** state.md holds NO FACTS — status, plan, flags, manifest only; a fact that needs recording forces its owner doc onto the touched list (amending a small doc is cheap).

**★★ WHAT GOES IN — THE DELETION TEST (Matt, firm).** *"These docs are the ACTIVE WAVEFRONT, not a history of what has happened to the project."* A line survives only if it would change a FUTURE decision AND cannot be encoded in code. Three things pass: decisions not yet made · measurement-validity caveats that would cause a future result to be MISREAD · true-but-unenforceable facts. Everything else goes — inventories superseded by their own guard, rules now fail-closed in the tree, incident histories, "we fixed X." Durable anchors (coords, thresholds, version pins, formulas) stay verbatim. Reconstructable from code/git → pointer. Spec in `docs/design/*.md` → point by exact path, never restate.
- **⚠ The failure mode is Claude's:** treating a CC report as material to CARRY rather than as evidence a doc line can be CUT. Findings feel like additions; usually they are subtractions.
- **A closed arc collapses to three lines:** verdict · what it changed · record path.

**★★ SINGLE-HOME.** One doc per subject makes this structural, but values still leak: at a distillation, grep each bolded numeral across the emitted docs and assert single occurrence. Other docs may NAME a fact and cross-reference its doc; never restate its value or mechanism.

**★★ TAG CLAIMS ABOUT CODE.** A line asserting what the tree does carries `[code: path]` or `[unverified]`. Untagged lines are decisions or measurements. Every checkpoint that checked has falsified some of these — all stated more strongly than their evidence supported.

**Compression.** Telegraphic, fragments, no scaffolding. **Rewording ≠ compressing — check `wc -c` old vs new**; when a reword pass stops paying, delete whole blocks.

**★ THE REPO PRACTICE DOCS** — `docs/design/verification_practice.md` (writing tests/guards) · `docs/design/measurement_practice.md` (designing measurements/evals/projections) · `docs/design/retired.md` (append-only register of retired approaches; a reversal is a new UN-RETIRED entry, never an edit). **CC-facing: prompts CITE them instead of transcribing rules, and this doc set never restates their content.** CLAUDE.md points CC at them; claude.ai's job is to remember they exist and to check `retired.md` before proposing an approach.

**Self-perpetuation.** Each future Claude knows only what these docs contain → carry this document forward, amended or preserved, never eroded.

---

## STANDING POSITIONS (Matt, firm)

- **★★ NO ARCHAEOLOGY; DELETION IS NORMAL.** Don't resurrect artifacts that don't match how things work now — repeat fresh rather than recover. Only the latest model matters; superseded manifests, plans, eval slices are gone and stay gone. Matt holds retention outside the repo; in a genuine last-resort case ask once, otherwise move on.
- **★★ USEFULNESS BEFORE RECOVERABILITY.** First question: will anything ever want it back? If nothing will, delete the regeneration machinery with the data. **Regenerability is not per-file when builds are chained** — each `vN` gate compares against `vN−1`; rebuilding needs the ORDER, which nothing in code states.
- **★★ NOTHING LOAD-BEARING LIVES IN `scratch/`, both ways.** Evidence leaves it the moment it justifies a durable decision; a proposal computed there never leaves it as a fact. Its absence is never written up as a loss.
- **★★ A DURABLE RECORD WRITTEN AFTER A FALLIBLE STEP IS NOT DURABLE IN PRACTICE.** Write the irreplaceable record first, then the work that can fail; derive the rest at read time.
- **★ `docs/design/` ADMISSION:** something in the code owns it and it stays true as the code changes. A maintained index passes; a transient measurement doesn't — it lives in scratch, survivors extracted into the owning doc, then deleted. **An extraction that does not delete its source is the failure; a rule nothing enforces is not a rule — name the guard when you write the rule.** A surviving measurement carries date + command, and the command is re-derived at commit time.
- **★ FRACTAL TYPES ARE PERMANENT DESIGN CONSTRAINTS** — phoenix and the 2% classic-phoenix case included. Retiring a generation METHOD is legitimate only when emission for that type is uncompromised.

---

## REASONING

**Confidence convention.** Every verdict carries **basis** (`[human n=X]`·`[machine-decode]`·`[measured]`·`[inferred]`·`[by-eye]`), **population** (what it's true OF — most falsified verdicts were population errors wearing a number), and **overturned-by** (the observation that would kill it). A verdict with no falsifier is a belief; `[machine-decode]` is evidence about the MODEL, not the world.

General measurement method (range restriction, confounder matching, run projection, truncated output, null instruments, fail-closed defaults, …) = **`docs/design/measurement_practice.md`** — cite it in prompts, don't transcribe. Verification practice (how guards fail, absence-tolerance, vacuity, parity) = **`docs/design/verification_practice.md`** — same.

---

## WORKING STYLE

One CC prompt at a time; wait for results. Progress through delivery over methodological minutiae (Matt); scope narrow. Diagnosis-first is NOT a standing policy — case by case.

- Prompts = short `.md` in `/mnt/user-data/outputs/`, presented, **never inline**. Scale length to risk; trust CC on mechanics. Prompts touching tests, guards, or measurements cite the repo practice docs by path.
- **★ CC's honest spec-deviations with stated reasons are consistently right — read before overriding.** Supply claims to be CHECKED, not text to transcribe, and ask for the corrections list back.
- **★★ SPECIFY THE REPORT, OR IT ARRIVES AS AN ESSAY (Matt, firm). Paste into every prompt:** (1) per item — outcome, commit, 1–3 sentences; (2) EVERY correction, one line each, unfiltered — the proof CC checked rather than transcribed; (3) anything CC decided that the prompt didn't specify; (4) suite counts before/after, pre-existing vs newly red; (5) what was NOT done and what a new test does NOT cover. **Not wanted:** line numbers, importer tables, inventories, reproduction transcripts, restatements of the prompt, mechanisms of already-tested fixes. Target one screen; detail that must persist goes in the REPO, not the report.
- **★ AFTER A REPORT, DO NOT SUMMARIZE IT BACK.** Say only what it CHANGES, what Claude got WRONG, and what's next.
- **★ CC WRITES ITS REPORT TO A `.md` UNDER `scratch/`, NEVER THE TERMINAL** — TUI copy-out mangles at wrap boundaries, fluently. Screenshot = fine fallback; paste = not.
- **★ NEVER EDIT A PROMPT ALREADY HANDED OVER** — addendums as separate paste-able files are welcome. Not-yet-run → edit. If an outputs file diverges from what ran, restore it.
- Matt does NOT hand-edit JSON/config — he dictates values, the prompt applies them. Acceptance BY EYE except classifier/ranker evals. He commits his own work — never flag his uncommitted state. **★ CC commits to `main` ONLY.**
- **★ A FIX WITH A SHAPE NEEDS THE PROMPT, NOT A "YES"** (derive-from-data vs hardcode, relational vs literal).
- **★ BUILD ≠ FLIP.** Built and staged in one prompt, adopted in another against a pre-registered bar. Standing exceptions bought by disasters: pre-registered eval bars · blind human reads as adjudicator of any model-selected population · reject autopsy + identity round-trips.
- **★ A SHAKEDOWN BEFORE A LONG UNATTENDED RUN PAYS FOR ITSELF.** Its report is "what broke, what to change." A cap that never fired is untested, not working.
- **★ NEVER DRAFT A `docs/design/` FILE BLIND** — CC reads the tree first. Name design files after CODE ARTIFACTS where possible; index at creation. An analysis worth keeping is written and committed in the SAME prompt that produces it, BEFORE the execution it describes.

**Labeling.**
- **★★ LABELING IS FAST — ~10 min per ~290-row batch.** Never argue a batch is too expensive; size for statistical power, not Matt's time.
- **★★ NEVER add calibration duplicates, drift probes, repeat rows, or ANY calibration aid to a labeling batch (firm)** — including anchor/exemplar panels beside the rig, explicitly dropped by Matt; do not re-propose. **"Noise is expected at all boundaries" (Matt)** — never re-raise adjacent-category disagreement or bar drift. Trust the labels as written.
- **★ Don't editorialize on a sheet the human is about to label blind.** Pre-labeling sheets get design commentary only. An INSPECTION sheet inverts one rule — auditing the model's own inputs shows literal cached bytes, parameters captioned, no vivid substitution.
- **★ A prompt running while Matt labels conflicts on GIT, not CPU** — in-progress exports sit unstaged under `labels/`; commit only your own files by explicit path.

**Runs.** Detached; cap = accumulated ACTIVE time, never wall-clock; check at the finest safe boundary AND don't start a unit that can't finish; hard-kill backstop clamped to remaining budget; idempotent resume via state file. An external reaper kills long Python/GPU processes at random → per-unit checkpoint + exact resume. Halt on invariant violations; isolate+record operational failures; rate-threshold the flaky.
- **★★ AN INTERRUPTIBLE WRITE MUST BE ATOMIC OR RESUME-BY-SKIP POISONS THE OUTPUT** — `.tmp` sibling + rename, byte-identity verified. Any long resumable producer needs this shape.
- **★ AN APPEND-ONLY LOG IS A SUPERSET OF THE CHECKPOINTED COUNTERS AFTER A KILL** — deliberate; dedup before quoting any log-derived rate.
