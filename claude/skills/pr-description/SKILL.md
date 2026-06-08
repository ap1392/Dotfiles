---
name: pr-description
description: How I want pull-request descriptions worded — the voice, tone, and phrasing of the English prose, NOT the git/gh mechanics. Use when writing or rewording a PR description, summary, or body. In the Notability repo this complements create-pr (which handles branching, labels, and the template); this skill governs the wording that goes inside it.
---

# How to word my PR descriptions

This is about the *prose*, not the process. When you draft or reword a PR description for me, follow these.

Please follow the following format for PR descriptions.
"
Fixes #(ticket issue number associated with the PR)

A clean, to the point description. Covers all bases, is not overly wordy, NO semicolons or em dashes, clear and easy to understand sentences

Test steps
Thorough test steps for developers to follow when testing the app. Also clear and to the point.

Dev QA
Leave blank but add the title in

Here are some example PR descriptions for you to follow:

------------------------
Fixes #41309

This PR adds provisioning logic for Mix and Match as well as initializes the `MixAndMatchView` in `LearnHomeView` and `StudyView`

Provisioning works by creating a `MixAndMatchSet` from the 20 flashcards, after the set is created a single `MixAndMatchSet` object is added to the `flashcardQueue` (redux thinks it's only one question but the `MixAndMatchSet` object stores all of the questions). Full provisioning documentation can be found [here](https://docs.google.com/document/d/1GyW6iJyjlFjToAqXhyxGpfwjg0ahfl3XArD8fNJohjs/edit?tab=t.0#heading=h.n293yxb3e36k)

I also hardcoded logic to fetch 20 questions for the server for a mix and match quiz, since we aren't going to launch it as a part of automatic study flow this should be fine for now

<details>
<summary>Screenshots</summary>
<img width="2752" height="2064" alt="image" src="https://github.com/user-attachments/assets/bd7c49a8-332e-4a9a-b88f-f631b6aaa23f" />
<img width="2752" height="2064" alt="image" src="https://github.com/user-attachments/assets/eaffcb08-04bc-4036-a1f3-16e11128cdb2" />
</details>

<!-- Summarize what changed and why. Link issue if one exists, and add relevant context. -->
<!-- Before requesting review, review your own code. If this includes UI changes, please add screenshots/video and tag a designer for review. -->

### Test Steps
<!-- What to test and how to test it. The tests you ran, big picture impact, and edge cases. Include instructions on setup process and version information, if needed. -->
<!-- Don't send to QA with this empty! QA will check these off as they test. -->
- [x] Turn `learnMixAndMatch` FF off, open a note w Smart Notes, go to quiz and make sure mix and match doesn't show up in the quiz picker
- [x] Close learn, turn the `learnMixAndMatch` FF on, open learn, select "Mix and Match" in the quiz picker and ensure it looks as it does in the screenshots

### Dev QA
<!-- If not a Skip QA ticket, please request a reviewer to Dev QA here -->
------------------------

Note, add the screenshot/media only if I tell you. Usually I will just add them myself on Github but if you have any feel free to add
