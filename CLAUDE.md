# CLAUDE.md — handoff-docs folder

## What this folder is
The 10 `fractal-*.md` files are claude.ai's cross-session working memory for the
fractal-wallpaper project. Their SOLE AUTHOR is claude.ai. They are written for a future
claude.ai instance, in deliberately compressed, telegraphic style. They are not
documentation, not yours to improve, and their apparent errors, terseness, or oddities
are usually deliberate.

## Your role: mechanical applier. Nothing else.
- You edit these files ONLY when given a `DISTILL_`-prefixed prompt, and only by
  executing its wholesale replacements and exact hunks.
- A hunk applies only on a VERBATIM, unique match (whitespace included). No match, or
  multiple matches → apply nothing further to that file; report which hunk failed.
- NEVER fix typos, normalize formatting, correct grammar, update numbers, or improve
  wording — anywhere, ever, including inside content you are pasting.
- NEVER create, delete, or rename `fractal-*.md` files unless a DISTILL_ prompt says so.

## Size targets
Size targets are SOFT (Matt, 2026-08-02): small justified overage = apply and note;
dramatic overage or padding = stop and report; targets move only with Matt. No
measured-size or line-count bookkeeping.

## Wrong-instance check
If a prompt references source code, Cargo.toml, tests, `tools/`, `scratch/`, or asks you
to build or run anything beyond git/wc/grep — it belongs to a different repository.
Stop and say so.

## Git
Working tree clean before applying. One commit per distillation, message `ckpt N`.
Never rebase, amend, or rewrite history.

## Reports
Short: per file applied/failed + final `wc -c` vs ceiling, failed hunks verbatim,
check outcomes. Nothing else.

## `prompts/` — ignored, never edited
`prompts/` is gitignored and outside your write scope. Read prompts from it; never
create, edit, delete, or rename anything inside it, and never commit it. Matt deletes
prompts there once applied — only the `*.md` files at this folder's root matter.
