# fractal-state — checkpoint 47 (2026-08-15)

## Where we are
Ckpt 47 closes the HEAD ERA: fractal-wallpapers now trains, evaluates, and ships its own judges. Landed this era — big repo: quantization recipe decided (`quant_recipe_v1`; **fp16 RATIFIED for everything, both repos, incl. pref** — Matt overrode the report's pref-fp32 exception). New repo: location head trained (`4a8e72f`, 3 seeds, BORDERLINE — ADOPTED on Matt's call: beats the incumbent's whole band at ≥4 (+0.012..+0.018), sits 0.004–0.009 under at ≥3 on a population that resolves only 0.012, against a yardstick generous to the incumbent) and both render heads (`292e3b7`: strange_render BORDERLINE-and-ahead, whole band above both prior heads; smooth_render ordering PASS / calibration-arm FAIL on an arm its own report proved unsatisfiable — sheet D is 3.95× enriched over the training distribution). **Matt: SHIP EVERYTHING** — smooth shipped as a policy call over the recorded FAIL; the bar record stays untouched. fp16 artifacts + `weights.json` entries staged for all heads; **cutting the `weights-v1` GitHub release is Matt's step**. Details, defects, lessons → fractal-tutorial §TRANSFER STATE; reports in `fractal-drive-sync\reports\`.
Backbone verdict landed and closed: keep `mobilenetv4_conv_medium` (fastest AND smallest; nothing better outside noise) — facts + the conditional-sigmoid score caveat → fractal-models.
Big-repo side: quant tooling only; **ARCHIVE TRAJECTORY (Matt): once fractal-wallpapers is operational, fractal-maker becomes an archive he won't actively maintain** — new work goes to fractal-wallpapers.

## OPEN (ordered)
1. **`weights-v1` release cut (Matt)** — artifacts + manifest staged; one release can carry all four heads.
2. **Palette-head distillation slice** — next transfer lane (design notes → fractal-tutorial §PLAN); the quantization check folds into its acceptance harness.
3. **Curation slice** → then deep-zoom demo → the site repo ("fractals-website"; hosting decided → fractal-tutorial).
4. **The ~500-row sitting — REDIRECTED to fractal-wallpapers** (Matt): output lands in the new repo's store via its rig; the accumulator list (fractal-corpus) keeps its value. Undated, Matt's schedule. Gate-passer v3→v4b repoint rides it IF it still matters under the archive trajectory.
5. **Smooth_render's ≥3 boundary has NO blind instrument** (sheet D can't referee it — 6 rows below tier 3); joins phoenix:classic's missing score-unconditioned draw as future-sitting material.
6. Run 28 / `--release-workers` first live run (big repo) — unchanged but likely mooted by the archive trajectory; Matt's call. First-100hr unknowns likewise; **the intended next long run is an 8hr TEST in fractal-wallpapers** once curation lands.

## CLOSED this era (verdict · record)
- **backbone_search_v1: keep mnv4_conv_medium** · report + `data/backbone_search/`; conditional-sigmoid caveat → fractal-models.
- **Quantization recipe: fp16 everything (Matt ratified)** · `quant_recipe_v1_report.md` + `data/quant/quant_recipe_v1.json`.
- **Location head trained in-repo, ADOPTED** · `4a8e72f` + `location_head_slice_report.md`; 11,303/11,303 label join, ZERO disagreements.
- **Both render heads trained in-repo, SHIPPED** · `292e3b7` + `render_heads_slice_report.md`.
- **Decisions batch (Matt, 2026-08-15):** prompts stay OUT of the public repo (Drive holds them) · outline v2 = Plan v2 §7 as-is (no Matt edits) · hosting = dedicated site repo + GitHub Releases for the wallpaper corpus · audience = advanced-HS-with-calculus / college CS · exemption watch RATIFIED (keep the strict no-exemption rule) · article gets an "alternative rendering modes" section (discrete integer-band opener) · anchored/correction-sheet distinction stays OUT of the article.

## Queue
Next: Matt cuts weights-v1 → palette-head distillation → curation → deep-zoom demo → site repo → rig polish. The sitting on Matt's schedule, aimed at fractal-wallpapers.

## ROSTER — soft size targets (unchanged)
operating 17k · state 6k · engine 10.5k · storage 6.5k · orchestration 5.5k · models 7k · thresholds 6k · corpus 8k · discovery 11k · emission 6.5k · tutorial 20k
