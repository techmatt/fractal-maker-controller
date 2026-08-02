# fractal-operating — the method

**Amended by diff, never rewritten in full** (ckpt-25 rewrite sanctioned: the mechanism changed). Read first, every session. Ownership test: *would this still be true if the project weren't fractals at all?*

---

## THE DOCUMENT SET

**Author & audience.** Claude (claude.ai) writes these; sole consumer is a future Claude, fresh, reconstructing state. Write for yourself minus this session. Code-work CC prompts never mention them; the ONLY CC contact is the distillation apply-prompt (below), which edits mechanically, never editorially.

**★ NEVER ENTER THE CODE REPO (Matt, firm).** The docs live in their own git-init'd folder with a dedicated CC instance (its CLAUDE.md encodes the applier role); a copy inside fractal-maker desyncs the moment code-work CC touches it. Durable in-repo knowledge = `docs/design/*.md`.

**★ THE DOCS CHANGE ONLY VIA THE APPLY-PROMPT** — Matt never edits them; the doc-folder CC applies Claude's exact hunks + wholesale replacements, mechanically (verbatim unique match or stop — no typo fixes, no normalization) ⇒ an uploaded copy is byte-identical to what Claude last authored; any doc-vs-memory discrepancy is Claude's error, never drift. Docs persist at `/mnt/user-data/uploads/` all conversation — re-read from disk rather than asking again.

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
| **discovery** | stage 1, sourcing, maneuvers, screen, hunt, harness | discovery work |
| **emission** | stage 2 | emission work |

**★★ SELECTIVE DISTILLATION — the core rule (Matt).** At a distillation, claude.ai decides which docs the era touched or invalidated and emits ONLY those plus state.md — default a SMALL SUBSET; emitting everything needs a stated reason. An untouched doc is not re-emitted and cannot grow. **The apply-prompt does the applying:** a `DISTILL_`-prefixed prompt (content guard: working dir must hold the 10 fractal-*.md at root, no Cargo.toml/src/tools — else STOP) carries wholesale replacements + exact hunks, sanity-checks touched files against their soft targets (small justified overage = apply and note; dramatic overage or padding = stop and report), spot-greps single-home, verifies untouched files untouched, one git commit per distillation.
- **Walk the full manifest once per distillation** — verdict per doc: TOUCHED / INVALIDATED (era changed its truth without editing it — staleness flag in state.md, never silence) / CLEAN.
- Stable docs amended by diff; a full rewrite only when the subject was heavily reworked, or Matt asks. To add substantially to a doc, prefer deleting within it first.
- Distillation only from a SETTLED state — never mid-session, never with a CC prompt outstanding; its job is to CLOSE threads, not open them.

**★★ SIZE TARGETS, NOT HARD CAPS (Matt, 2026-08-02).** Per-doc soft targets in state.md's roster; the deletion test is the real control. A small overage with a good reason is fine — apply and note it. DRAMATIC overage, or growth that is padding rather than content, = stop and report. Targets move only with Matt. No size bookkeeping beyond this: no measured-size columns, no touched-line counts. state.md holds NO FACTS — status, plan, flags, roster only; a fact that needs recording forces its owner doc onto the touched list.

**★★ WHAT GOES IN — THE DELETION TEST (Matt, firm).** *"These docs are the ACTIVE WAVEFRONT, not a history of what has happened to the project."* A line survives only if it would change a FUTURE decision AND cannot be encoded in code. Three things pass: decisions not yet made · measurement-validity caveats that would cause a future result to be MISREAD · true-but-unenforceable facts. Everything else goes. Durable anchors (coords, thresholds, version pins, formulas) stay verbatim. Reconstructable from code/git → pointer. Spec in `docs/design/*.md` → point by exact path, never restate.
- **⚠ The failure mode is Claude's:** treating a CC report as material to CARRY rather than evidence a doc line can be CUT.
- **A closed arc collapses to three lines:** verdict · what it changed · record path.

**★★ SINGLE-HOME.** One doc per subject; at a distillation, grep each bolded numeral across the emitted docs and assert single occurrence. Other docs may NAME a fact and cross-reference; never restate its value or mechanism.

**★★ TAG CLAIMS ABOUT CODE.** A line asserting what the tree does carries `[code: path]` or `[unverified]`. Untagged lines are decisions or measurements. Every checkpoint that checked has falsified some of these.

**Compression.** Telegraphic, fragments, no scaffolding. **Rewording ≠ compressing**; when a reword pass stops paying, delete whole blocks.

**★ THE REPO PRACTICE DOCS** — `docs/design/verification_practice.md` · `measurement_practice.md` · `retired.md` (append-only; a reversal is a new UN-RETIRED entry, never an edit; **a reused or re-scoped retired policy needs a new dated entry**). CC-facing: prompts CITE them, this doc set never restates them; check `retired.md` before proposing an approach.

**Self-perpetuation.** Each future Claude knows only what these docs contain → carry this document forward, amended or preserved, never eroded.

---

## STANDING POSITIONS (Matt, firm)

- **★★ NO ARCHAEOLOGY; DELETION IS NORMAL.** Don't resurrect artifacts that don't match how things work now. Only the latest model matters. Matt holds retention outside the repo; in a genuine last-resort case ask once, otherwise move on.
- **★★ USEFULNESS BEFORE RECOVERABILITY.** First question: will anything ever want it back? If nothing will, delete the regeneration machinery with the data. **Regenerability is not per-file when builds are chained** — rebuilding needs the ORDER, which nothing in code states.
- **★★ NOTHING LOAD-BEARING LIVES IN `scratch/`, both ways.** Evidence leaves it the moment it justifies a durable decision; a proposal computed there never leaves it as a fact.
- **★★ A DURABLE RECORD WRITTEN AFTER A FALLIBLE STEP IS NOT DURABLE IN PRACTICE.** Write the irreplaceable record first, then the work that can fail.
- **★ `docs/design/` ADMISSION:** something in the code owns it and it stays true as the code changes. A transient measurement lives in scratch, survivors extracted into the owning doc, then deleted — **an extraction that does not delete its source is the failure; a rule nothing enforces is not a rule — name the guard.** A surviving measurement carries date + command, re-derived at commit time.
- **★ FRACTAL TYPES ARE PERMANENT DESIGN CONSTRAINTS** — phoenix and the 2% classic-phoenix case included. Retiring a generation METHOD is legitimate only when emission for that type is uncompromised.

---

## REASONING

**Confidence convention.** Every verdict carries **basis** (`[human n=X]`·`[machine-decode]`·`[measured]`·`[inferred]`·`[by-eye]`), **population** (most falsified verdicts were population errors wearing a number), and **overturned-by**. A verdict with no falsifier is a belief; `[machine-decode]` is evidence about the MODEL, not the world.

Measurement method → `measurement_practice.md`; verification → `verification_practice.md` — cite in prompts, don't transcribe.

---

## WORKING STYLE

One CC prompt at a time; wait for results. Progress through delivery over methodological minutiae (Matt); scope narrow. Diagnosis-first is NOT a standing policy — case by case. **★ MATT'S N-HOUR BUDGET COVERS EVERYTHING** — build + shakedown + run + post done ≤N wall-clock; the run's own cap ~N−2, shaved further when build/post estimates grow; overlapping build/post with a running crawl is legitimate.

- Prompts = short `.md` in `/mnt/user-data/outputs/`, presented, **never inline**. Scale length to risk; trust CC on mechanics. Prompts touching tests, guards, or measurements cite the repo practice docs by path.
- **★ CC's honest spec-deviations with stated reasons are consistently right — read before overriding.** Supply claims to be CHECKED, not text to transcribe, and ask for the corrections list back.
- **★★ SPECIFY THE REPORT (Matt, firm). Paste into every prompt:** *Report (HARD CAP ~60 lines, `scratch/`). Filter for every line: does it change what claude.ai decides next? If not, it goes in the repo (commit message or design doc), pointed to by path. (1) per item: outcome + commit, ≤1 line — no mechanism, no rationale for settled decisions; (2) corrections to the prompt: every one, ONE line each; (3) unrequested decisions needing attention: one line each; settled implementation choices: names/paths only; (4) results that move decisions: each number once, with population + basis; confounds; costs that change future sizing; (5) suite: two lines max — counts, newly-red vs pre-existing, "N proved red by injection, M test defects fixed"; (6) NOT done / not covered: one line each. Over the cap: cut content, never compress wording.*
- **★ AFTER A REPORT, DO NOT SUMMARIZE IT BACK.** Say only what it CHANGES, what Claude got WRONG, and what's next.
- **★ CC WRITES ITS REPORT TO A `.md` UNDER `scratch/`, NEVER THE TERMINAL** — TUI copy-out mangles at wrap boundaries. Screenshot = fine fallback.
- **★ NEVER EDIT A PROMPT ALREADY HANDED OVER** — addendums as separate paste-able files. Not-yet-run → edit. If an outputs file diverges from what ran, restore it.
- Matt does NOT hand-edit JSON/config — he dictates values, the prompt applies them. Acceptance BY EYE except classifier/ranker evals. He commits his own work; git — commits, push, remotes, auth — is his entirely: never flag, track, or mention its state. **★ CC commits to `main` ONLY.**
- **★ A FIX WITH A SHAPE NEEDS THE PROMPT, NOT A "YES"** (derive-from-data vs hardcode, relational vs literal).
- **★ BUILD ≠ FLIP.** Built and staged in one prompt, adopted in another against a pre-registered bar. Standing exceptions bought by disasters: pre-registered eval bars · blind human reads as adjudicator of any model-selected population · reject autopsy + identity round-trips.
- **★ A SHAKEDOWN BEFORE A LONG UNATTENDED RUN PAYS FOR ITSELF.** A cap that never fired is untested, not working.
- **★ NEVER DRAFT A `docs/design/` FILE BLIND** — CC reads the tree first. Name design files after CODE ARTIFACTS; index at creation. An analysis worth keeping is committed in the SAME prompt that produces it, BEFORE the execution it describes.

**Labeling.**
- **★★ LABELING IS FAST — ~10 min per ~290-row batch.** Never argue a batch is too expensive; size for statistical power, not Matt's time. **Renders, not labeling, price a batch build** [measured]: ~6.3 rows/min at label fidelity (two crops/row), decelerating on deep tails — budget construction around render time and bound it.
- **★★ NEVER add calibration duplicates, drift probes, repeat rows, or ANY calibration aid to a labeling batch (firm)** **"Noise is expected at all boundaries" (Matt)** — never re-raise adjacent-category disagreement or bar drift.
- **★ Don't editorialize on a sheet the human is about to label blind.** Pre-labeling sheets get design commentary only; an INSPECTION sheet inverts one rule — literal cached bytes, parameters captioned, no vivid substitution.
- **★ A prompt running while Matt labels conflicts on GIT, not CPU** — commit only your own files by explicit path.

**Runs.** Detached; cap = accumulated ACTIVE time, never wall-clock; check at the finest safe boundary AND don't start a unit that can't finish; hard-kill backstop clamped to remaining budget; idempotent resume via state file. An external reaper kills long Python/GPU processes at random → per-unit checkpoint + exact resume. Halt on invariant violations; isolate+record operational failures; rate-threshold the flaky.
- **★★ AN INTERRUPTIBLE WRITE MUST BE ATOMIC OR RESUME-BY-SKIP POISONS THE OUTPUT** — `.tmp` sibling + rename, byte-identity verified. Legitimate alternative when rename-per-record is prohibitive (multi-hundred-MB stores): append-only + fsync'd index + self-healing recovery — record lands first, one index line names it, the next open recomputes position from the VALID index.
- **★ AN APPEND-ONLY LOG IS A SUPERSET OF THE CHECKPOINTED COUNTERS AFTER A KILL** — dedup before quoting any log-derived rate.
