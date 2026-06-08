---
name: pr-description
description: How I want pull-request descriptions worded — the voice, tone, and phrasing of the English prose, NOT the git/gh mechanics. Use when writing or rewording a PR description, summary, or body. In the Notability repo this complements create-pr (which handles branching, labels, and the template); this skill governs the wording that goes inside it.
---

# How to word my PR descriptions

This is about the *prose*, not the process. When you draft or reword a PR description for me, follow these.

## Voice
- Plain, direct English. Write like a senior engineer explaining the change to a busy reviewer, not like marketing.
- Active voice, present tense: "Adds retry logic," not "Retry logic was added."
- No filler or hype — drop "simply," "just," "basically," "various improvements," "as you can see."
- Don't restate the diff line by line. Summarize intent; the reviewer can read the code.

## Structure
- **Open with the why.** First 1–2 sentences: what problem this solves and why it matters. A reviewer should get the point before reading any detail.
- Then **what changed** — a short summary or a tight bullet list of the meaningful changes (skip the trivial ones).
- Call out **risk / blast radius** honestly: migrations, perf, anything reviewers should scrutinize. If it's low-risk, say why.
- Note **how it was tested** when relevant.

## Length
- Short by default. A small fix gets 2–3 sentences. Match the description size to the change.
- Don't pad to look thorough. Reviewers skim — make every line earn its place.

<!-- Personalize: pet phrases to ban, sections you always want, ticket-link format, etc. -->
