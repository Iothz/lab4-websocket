# Lab 4 WebSocket -- Project Report

## What I specified

[The sentence you will send and the answer you expect, as asked in the objective. Decided *before* generating or pasting code.]


## What I changed

[Files and behaviour. Not a restatement of the starter README.]

Edited the following files:
- `src/test/kotlin/websockets/ElizaServerTest.kt`
  - Removed `@Disabled` from `onChat` and `@Suppress("UNUSED_PARAMETER")` annotations from the `onMessage` method.
  - Completed the `onMessage` method 
  - Completed the `onChat` test 
## Technical decisions

[Why you chose that sentence and that answer, and what you rejected.]

- Sentence: `"always"`
- Answer: `"Can you think of a specific example?"`

Because the Eliza server is designed to respond to certain keywords in the user's input and the chosen sentence
contains the keyword `"always"`, which can only trigger the specific response `"Can you think of a specific example?"`.


## How I verified

[Commands (`./gradlew check`), what failed first, what you fixed. You remain accountable for correctness.]



## AI disclosure

Fill **either** the list **or** the no-AI line.

- **Tools / skills:** …
- **Purpose:** …
- **Representative prompts:** … (or appendix)
- **Affected files/sections:** …
- **Validation steps:** …
- **Citations:** … (external snippets you adapted)
- **Human-reviewed:** what you checked, changed, or rejected

Or: **No AI assistance** was used for this lab.
