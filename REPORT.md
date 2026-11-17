# Lab 4 WebSocket -- Project Report

## What I specified

Looking at the code, you can see that certain keywords trigger only one specific answer. For example, the sentence
`"always"` can trigger the specific response `"Can you think of a specific example?"`.

That is why the sentence I will send is `"always"`, and the answer I expect is
`"Can you think of a specific example?"`.

## What I changed

Edited the following files:

- `src/test/kotlin/websockets/ElizaServerTest.kt`
  - Removed `@Disabled` from `onChat` and `@Suppress("UNUSED_PARAMETER")` annotations from the `onMessage` method.
  - Completed the `onMessage` method.
  - Completed the `onChat` test.

## Technical decisions

- Sentence: `"always"`
- Answer: `"Can you think of a specific example?"`

The Eliza server is designed to respond to certain keywords in the user's input, and the chosen sentence contains the
keyword `"always"`, which can trigger the specific response `"Can you think of a specific example?"`. You could
complicate the sentence with more words, but as long as the keyword `"always"` is present, it will trigger the same
response.

`"always"` is the perfect choice because it is the first keyword that Eliza checks for in the input sentence and has a
unique response.

There were other options, such as `"because"` or `"sorry"`, but all options with multiple answers were discarded.

## How I verified

I ran `./gradlew check` after fixing the tests.

The first run resulted in `BUILD FAILED` because `import org.junit.jupiter.api.Disabled` was unused. I removed the
import and re-ran `./gradlew check`, resulting in `BUILD SUCCESSFUL`.

During the build, a warning stating `"A terminally deprecated method in sun.misc.Unsafe has been called"` appeared,
but it did not affect the successful build.

Also executed `./gradlew ktlintCheck` to ensure that the code style was correct, and it passed successfully.

## AI disclosure

- **Tools / skills:** GitHub Copilot through the IntelliJ IDEA add-on and Gemini AI through chat.
- **Purpose:** Exploring the code, explaining and redacting.
- **Representative prompts:**
  - "How important is the deprecated method warning in the build?"
  - "Check the redaction of the report without changing the meaning of the text."
- **Affected files/sections:** All edited files were affected by AI to some extent, but the final implementation was
reviewed by the author, and all suggestions were either accepted, modified, or rejected.
- **Validation steps:** All suggestions were reviewed by the author and either accepted, modified, or rejected. The
final implementation was tested and manually verified to ensure correctness.
- **Citations:** No external sources were used for this lab, apart from the Eliza server code provided in the starter project.
- **Human-reviewed:** All code and the report were reviewed by the author to ensure correctness and clarity. If any
code was unclear or not understandable, I would have asked for clarification or rejected the suggestion.