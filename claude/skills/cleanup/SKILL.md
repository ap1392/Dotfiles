---
name: cleanup
description: My personal pre-PR cleanup pass over the current working changes — strip debugging leftovers and scratch before I open a pull request. Use when I say "clean up," "clean up my changes," "tidy this up before the PR," or similar. Hygiene only — it does not hunt for bugs (use /code-review) or refactor for quality (use /simplify).
allowed-tools: Bash(git diff:*) Bash(git status:*) Read Edit
---


# Code comments

For any comments you have make sure to simplify them completely. No semi-colons, no em dashes. Straight and to the point, simply describing what the code does. Examples (with code):

-------------------------------------------------------------------------
// Questions on screen is never empty, rather we mark items as blank so the view knows when to display a blank card. The number of questions left on screen is the number of non blank questions left and the number of questions left in the queue is the full length of the queue (nothing in the queue is blank)
questionsOnScreen.filter{ !$0.isBlank }.count + questionQueue.count
-------------------------------------------------------------------------

-------------------------------------------------------------------------
// Text being nil represents a case where we've run out of cards to show on screen so we need to show a blank space where the previous pairs were
RoundedRectangle(cornerRadius: personality.comfy)
   .opacity(0)
-------------------------------------------------------------------------

-------------------------------------------------------------------------
// Fills the area inside the cell with a lighter selection color to match figma
RoundedRectangle(cornerRadius: personality.comfy)
   .fill(selectionColor.opacity(0.12))
-------------------------------------------------------------------------


If you think you need a more verbose description, use something like this:
// Checks to make sure questions on screen and question queue are the appropriate length, we multiply by 2 because the consts
// represents a pair and we split up each pair into individual values in the 2 queues. We have a min check in place in case
// there's less questions being provisioned than we have slots on screen (ex: we only have 3 questions provisioned so it's
// not possible to fill all 4 slots on screen)
let expectedQuestionsOnScreenCount: Int = min(MixAndMatchSet.Consts.pairsOnScreenCount * 2, questionCount * 2)
#expect(mixAndMatchQueue.questionsOnScreen.count == expectedQuestionsOnScreenCount)

