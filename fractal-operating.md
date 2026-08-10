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
- **State the scratch-preservation notice to Matt at every distillation** — what under `scratch/` MUST survive (read off the enforced allowlist) AND anything merely USEFUL to keep, named as candidates — preserving folders is cheap for Matt (2026-08-05). Default: nothing necessary, candidates listed.
- Stable docs amended by diff; a full rewrite only when the subject was heavily reworked, or Matt asks. To add substantially to a doc, prefer deleting within it first.
- Distillation only from a SETTLED state — never mid-session, never with a CC prompt outstanding; its job is to CLOSE threads, not open them.

**★★ SIZE TARGETS, NOT HARD CAPS (Matt, 2026-08-02).** Per-doc soft targets in state.md's roster; the deletion test is the real control. A small overage with a good reason is fine — apply and note it. DRAMATIC overage, or growth that is padding rather than content, = stop and report. Targets move only with Matt. No size bookkeeping beyond this: no measured-size columns, no touched-line counts. state.md holds NO FACTS — status, plan, flags, roster only; a fact that needs recording forces its owner doc onto the touched list.

**★★ WHAT GOES IN — THE DELETION TEST (Matt, firm).** *"These docs are the ACTIVE WAVEFRONT, not a history of what has happened to the project."* A line survives only if it would change a FUTURE decision AND cannot be encoded in code. Three things pass: decisions not yet made · measurement-validity caveats that would cause a future result to be MISREAD · true-but-unenforceable facts. Everything else goes. Durable anchors (coords, thresholds, version pins, formulas) stay verbatim. Reconstructable from code/git → pointer. Spec in `docs/design/*.md` → point by exact path, never restate.
- **⚠ The failure mode is Claude's:** treating a CC report as material to CARRY rather than evidence a doc line can be CUT.
- **A closed arc collapses to three lines:** verdict · what it changed · record path.

**★★ SINGLE-HOME.** One doc per subject; at a distillation, grep each bolded numeral across the emitted docs and assert single occurrence. Other docs may NAME a fact and cross-reference; never restate its value or mechanism.

**★★ TAG CLAIMS ABOUT CODE.** A line asserting what the tree does carries `[code: path]` or `[unverified]`. Untagged lines are decisions or measurements. Every checkpoint that checked has falsified some of these. **A claim of AUTOMATIC FUTURE BEHAVIOR ("self-heals", "regenerates", "X will consume Y") requires `[code: path]` naming the enforcing mechanism — else it is not written (Matt, 2026-08-05; the τ_h "self-heal" was a hand list).**

**Compression.** Telegraphic, fragments, no scaffolding. **Rewording ≠ compressing**; when a reword pass stops paying, delete whole blocks.

**★ THE REPO PRACTICE DOCS** — `docs/design/verification_practice.md` · `measurement_practice.md` · `retired.md` (append-only; a reversal is a new UN-RETIRED entry, never an edit; **a reused or re-scoped retired policy needs a new dated entry**). CC-facing: prompts CITE them, this doc set never restates them; check `retired.md` before proposing an approach.

**Self-perpetuation.** Each future Claude knows only what these docs contain → carry this document forward, amended or preserved, never eroded.

---

## TIER 0.5 — THE EXCHANGE FOLDER (2026-08-08)

**`C:\Code\fractal-drive-sync\{prompts,reports}\`** — a Drive-synced folder outside both repos, live in BOTH directions: claude.ai writes prompts into `prompts\` via the Drive connector; CC copies its reports into `reports\`. **SCRATCH, and Matt deletes freely** — empty or absent is normal, never an error. **One writer per subfolder.** `scratch/` stays the canonical home of a report; the copy is best-effort.
- **★★ THE STANDING PROMPT CONTRACT LIVES IN fractal-maker's `CLAUDE.md`** (`## Standing prompt contract`, commit `6634410`) — report shape, report delivery, runtime discipline, engine-subprocess helpers, commit gate. **Prompts no longer restate any of it**; a prompt that repeats a rule the repo already encodes is duplication, and the repo's version is the more precise one. Absorb by cross-reference, never by copy.
- **★ ALL PROMPTS GO THROUGH `prompts\`** — CC code-work prompts and session/distillation prompts alike; one channel, no exceptions.
- The controller repo's `CLAUDE.md` carries the mirror rules: read prompts from either location, **never write anywhere under the exchange folder**, and the handoff docs are single-sourced in the controller repo — never copied, synced, or mirrored anywhere.
- `matt-claude-workflow.md` (exchange-folder root) documents the whole pattern for standing up a NEW project on it.

---

## STANDING POSITIONS (Matt, firm)

- **★★ NO ARCHAEOLOGY; DELETION IS NORMAL.** Don't resurrect artifacts that don't match how things work now. Only the latest model matters. Matt holds retention outside the repo; in a genuine last-resort case ask once, otherwise move on.
- **★★ USEFULNESS BEFORE RECOVERABILITY.** First question: will anything ever want it back? If nothing will, delete the regeneration machinery with the data. **Regenerability is not per-file when builds are chained** — rebuilding needs the ORDER, which nothing in code states.
- **★★ NOTHING LOAD-BEARING LIVES IN `scratch/`, both ways.** Evidence leaves it the moment it justifies a durable decision; a proposal computed there never leaves it as a fact. Deliberate exceptions are DECLARED in the enforced allowlist (fractal-storage) with owner + expected lifetime; **Matt wipes scratch between checkpoints — every distillation states the must-preserve set AND useful-to-keep candidates (2026-08-05); default nothing necessary.**
- **★★ A DURABLE RECORD WRITTEN AFTER A FALLIBLE STEP IS NOT DURABLE IN PRACTICE.** Write the irreplaceable record first, then the work that can fail.
- **★★ LOSING HAND-LABELED DATA IS A MAJOR FAILURE/BUG (Matt, firm, 2026-08-04).** Labels are irreplaceable: nothing rewrites, deletes, or re-keys stored label rows; re-attribution is reader-side only; verify every export merged BY ROW COUNT (the reachability guard cannot see opaque-keyed exports).
- **★ `docs/design/` ADMISSION:** something in the code owns it and it stays true as the code changes. A transient measurement lives in scratch, survivors extracted into the owning doc, then deleted — **an extraction that does not delete its source is the failure; a rule nothing enforces is not a rule — name the guard.** A surviving measurement carries date + command, re-derived at commit time.
- **★ FRACTAL TYPES ARE PERMANENT DESIGN CONSTRAINTS** — phoenix and the 2% classic-phoenix case included. Retiring a generation METHOD is legitimate only when emission for that type is uncompromised.
- **★★ ENFORCING FROZEN THRESHOLDS WERE THE ROOT CAUSE OF THE IMPOSSIBLE-STATE FAILURES (Matt, 2026-08-09).** Derived per-partition cuts held as FROZEN STATE are what produced the recurring "zero supply / impossible by construction" pattern. **Prefer read-time rank + coarse semantic floors; a threshold change should be a READ-TIME CHOICE, never an event that invalidates populations.** The guard set that is explicitly KEPT: sink isolation · dedup · label-carries-its-join · seeded determinism.

---

## REASONING

**Confidence convention.** Every verdict carries **basis** (`[human n=X]`·`[machine-decode]`·`[measured]`·`[inferred]`·`[by-eye]`), **population** (most falsified verdicts were population errors wearing a number), and **overturned-by**. A verdict with no falsifier is a belief; `[machine-decode]` is evidence about the MODEL, not the world. **★ A reproducibility test must re-run the writer the artifact came from, not a plausible neighbour** — and a prompt making classification mechanical must PIN the writer (the q4-fields false-durable arc). **★★ A "BYTE-IDENTICAL REBUILD" CLAIM IS PROVEN BY RUNNING THE REAL COMMANDS, FIRST — before anything is de-tracked** (and run with the dependencies already gone, so the proof doesn't rest on them). It is also the step that finds what does NOT reproduce: a live disk probe frozen into a record has no guard and will differ. **★ Early reads of a slow-starting run: mechanism (mix conformance, queue states) is valid immediately; yield/funnel is warm-up, not the run** — this bit twice at ckpt 30.

Measurement method → `measurement_practice.md`; verification → `verification_practice.md` — cite in prompts, don't transcribe.

---

## WORKING STYLE

One CC prompt at a time; wait for results. Progress through delivery over methodological minutiae (Matt); scope narrow. Diagnosis-first is NOT a standing policy — case by case. **★ MATT'S N-HOUR BUDGET COVERS EVERYTHING** — build + shakedown + run + post done ≤N wall-clock; the run's own cap ~N−2, shaved further when build/post estimates grow; overlapping build/post with a running crawl is legitimate. Deadline form ("done by <time>") = same semantics, computed at launch: reserve for post, wall-budget = remaining − reserve, active = wall/1.15; the pre-loop draw is OUTSIDE the wall cap by construction — subtract its bound too (fractal-orchestration). **One run per budget: a follow-up run of ANY length after one completes is a NEW budget question for Matt — never launch back-to-back on inference (2026-08-04).**

- Prompts = short `.md` in `/mnt/user-data/outputs/`, presented, **never inline**. Scale length to risk; trust CC on mechanics. Prompts touching tests, guards, or measurements cite the repo practice docs by path.
- **★ CC's honest spec-deviations with stated reasons are consistently right — read before overriding.** Supply claims to be CHECKED, not text to transcribe, and ask for the corrections list back.
- **★★ SPECIFY THE REPORT (Matt, firm; softened 2026-08-07). Paste into every prompt:** *Report → `scratch/<prompt-name>_report.md` (exact filename in the prompt; never repo root — root prose fails the docs-tree guard). Target ~60 lines — SOFT, not a gate: write once, at most one trim pass, then STOP; running over is fine, NEVER iterate to squeeze under the number. Filter for every line: does it change what claude.ai decides next? If not, it goes in the repo (commit message or design doc), pointed to by path. (1) per item: outcome + commit, ≤1 line — no mechanism, no rationale for settled decisions; (2) corrections to the prompt: every one, ONE line each; (3) unrequested decisions needing attention: one line each; settled implementation choices: names/paths only; (4) results that move decisions: each number once, with population + basis; confounds; costs that change future sizing; (5) suite: two lines max — counts, newly-red vs pre-existing, "N proved red by injection, M test defects fixed"; (6) NOT done / not covered: one line each. Overflow that might matter later → appendix files beside the report (JSON preferred), one pointer line each. A deliberately comprehensive deliverable (census, certification) states its own explicit larger target in the prompt. Trivial tasks (a commit, a move): one line, no file.* **(The hard-cap era made CC burn ~20 invocations micro-shortening — the cap is the anti-padding filter, not a gate.)**
- **★ AFTER A REPORT, DO NOT SUMMARIZE IT BACK.** Say only what it CHANGES, what Claude got WRONG, and what's next.
- **★ CC WRITES ITS REPORT TO A `.md` UNDER `scratch/`, NEVER THE TERMINAL** — TUI copy-out mangles at wrap boundaries. Screenshot = fine fallback.
- **★ NEVER EDIT A PROMPT ALREADY HANDED OVER** — addendums as separate paste-able files. Not-yet-run → edit. If an outputs file diverges from what ran, restore it.
- Matt does NOT hand-edit JSON/config — he dictates values, the prompt applies them. Acceptance BY EYE except classifier/ranker evals. He commits his own work; git — commits, push, remotes, auth — is his entirely: never flag, track, or mention its state. **★ CC commits to `main` ONLY.** **★★ NO COMMIT ≥20 MB — single blob or aggregate, LFS counted — WITHOUT MATT'S EXPLICIT PRIOR CONFIRMATION (Matt, firm, 2026-08-04):** binds claude.ai prompts and CC alike; encoded in repo CLAUDE.md; stop and ask, never sanction implicitly.
- **★ A FIX WITH A SHAPE NEEDS THE PROMPT, NOT A "YES"** (derive-from-data vs hardcode, relational vs literal).
- **★ A POLICY FLIP ASKS "WHO ELSE APPLIES THIS DECISION?"** — an owner only decides for the sites that ask it; grep for private copies before declaring a flip done (deploy_tail carried its own mining report-only branch; second occurrence after the τ_h pooled fallback).
- **★ BUILD ≠ FLIP.** Built and staged in one prompt, adopted in another against a pre-registered bar. Standing exceptions bought by disasters: pre-registered eval bars · blind human reads as adjudicator of any model-selected population · reject autopsy + identity round-trips.
- **★ A SHAKEDOWN BEFORE A LONG UNATTENDED RUN PAYS FOR ITSELF.** A cap that never fired is untested, not working.
- **★ NEVER DRAFT A `docs/design/` FILE BLIND** — CC reads the tree first. Name design files after CODE ARTIFACTS; index at creation. An analysis worth keeping is committed in the SAME prompt that produces it, BEFORE the execution it describes.

**Labeling.**
- **★★ LABELING IS AFFORDABLE WHEN WE NEED IT (Matt, 2026-08-04 — replaces the retired "labeling is fast, never argue cost" framing).** Size for statistical power; spend deliberately. **Renders, not labeling, price a batch build** [measured]: ~6.3 rows/min at label fidelity (two crops/row), decelerating on deep tails — budget construction around render time and bound it.
- **★★ LABELS MUST SERVE OBJECTIVES THE NEXT RETRAIN CANNOT DEPRECATE (Matt, firm, 2026-08-05).** Until a network is believed final-stage, push back on labeling whose value dies with the next version. Passes: eval instruments, design reads, correction sittings (below). Score-unconditioned draws stay a legitimate one-time purchase but are DEMOTED to contingency (2026-08-06 — fractal-thresholds). Fails by default: training volume for the current head.
- **★★ NEVER add calibration duplicates, drift probes, repeat rows, or ANY calibration aid to a labeling batch (firm)** **"Noise is expected at all boundaries" (Matt)** — never re-raise adjacent-category disagreement or bar drift.
- **★★ THE CORRECTION LOOP IS THE LABELING METHOD (Matt, 2026-08-05/06):** heads pre-label, Matt corrects (sheet mechanics → fractal-corpus). NO blind slices, NO unbiased-eval machinery — assume proper randomization; Matt corrects what's wrong; a real distribution concern gets ≤1 line of prose, never a design. Calibration default = randomized LOCATION-GROUPED splits. Per-sitting correction rate = the head's report card and the progressive-loop convergence metric (taper to spot-checks). Reads off corrected labels are CEILINGS (anchoring) — state it; it blocks nothing.
- **★ Don't editorialize on a sheet the human is about to label blind.** Pre-labeling sheets get design commentary only; an INSPECTION sheet inverts one rule — literal cached bytes, parameters captioned, no vivid substitution.
- **★ A prompt running while Matt labels conflicts on GIT, not CPU** — commit only your own files by explicit path.

**Runs.** Detached; cap = accumulated ACTIVE time, never wall-clock; check at the finest safe boundary AND don't start a unit that can't finish; hard-kill backstop clamped to remaining budget; idempotent resume via state file. An external reaper kills long Python/GPU processes at random → per-unit checkpoint + exact resume. Halt on invariant violations; isolate+record operational failures; rate-threshold the flaky.
- **★★ AN INTERRUPTIBLE WRITE MUST BE ATOMIC OR RESUME-BY-SKIP POISONS THE OUTPUT** — `.tmp` sibling + rename, byte-identity verified. Legitimate alternative when rename-per-record is prohibitive (multi-hundred-MB stores): append-only + fsync'd index + self-healing recovery — record lands first, one index line names it, the next open recomputes position from the VALID index.
- **★ AN APPEND-ONLY LOG IS A SUPERSET OF THE CHECKPOINTED COUNTERS AFTER A KILL** — dedup before quoting any log-derived rate.
