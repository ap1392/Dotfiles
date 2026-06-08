---
name: cleanup
description: My personal pre-PR cleanup pass over the current working changes — strip debugging leftovers and scratch before I open a pull request. Use when I say "clean up," "clean up my changes," "tidy this up before the PR," or similar. Hygiene only — it does not hunt for bugs (use /code-review) or refactor for quality (use /simplify).
allowed-tools: Bash(git diff:*) Bash(git status:*) Read Edit
---

# Cleanup pass

Tidy the *changes I'm about to ship* — not the whole repo. Scope to the working diff.

## Steps
1. Run `git status` and `git diff` (and `git diff --staged`) to see exactly what I've touched. Only act on changed/added lines.
2. Within those changes, remove or flag:
   - Debug output left behind: `console.log`, `print`, `println!`, `dbg!`, `debugger`, etc. — anything that was for my own debugging, not real logging.
   - Commented-out code and dead scratch blocks.
   - Stray `TODO` / `FIXME` / `XXX` I added — resolve it or call it out so I can decide.
   - Leftover test scaffolding: `.only`, `.skip`, hardcoded test values not meant to ship.
   - Obvious accidents: trailing whitespace I introduced, an unintended file, a committed secret or `.env`.
3. Leave real, intentional logging and pre-existing comments alone.
4. When done, give me a short list of what you removed and anything you left for me to decide. Don't commit.

<!-- Personalize: language-specific patterns, a lint/format command to run, files to always ignore. -->
