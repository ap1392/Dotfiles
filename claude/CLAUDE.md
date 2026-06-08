# Personal Claude instructions

These apply to every project I work in. Each repo's own CLAUDE.md is loaded *after*
this file and takes precedence, so project rules win on any conflict.

## How to communicate
- Be concise and direct. Lead with the answer, then the reasoning.
- When you change code, tell me what changed and why in a sentence or two — don't narrate every step.
- If you're unsure or making an assumption, say so explicitly instead of guessing silently.
- Push back when you think I'm wrong; I'd rather hear it.

## How to write code
- Match the conventions of the surrounding file over any general "best practice."
- Prefer the smallest change that solves the problem. No drive-by refactors unless I ask.
- Comment the "why," not the "what." Don't add comments that just restate the code.
- Never leave debugging scratch (console.log / print / commented-out code) in anything you hand back.

## Workflow
- Don't commit or push unless I ask.
- When a task is done, say what you actually verified (tests run, app launched). Don't claim it works if you didn't check.

<!-- Edit freely. Keep this short and high-signal — a long file dilutes the rules that matter. -->
