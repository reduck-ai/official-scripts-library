# Ask Gemini

Automatically ask Gemini on gemini.google.com. Open a new Gemini chat, send one question, and wait until Gemini has finished its answer (up to 3 min). Returns the answer as Gemini sends it, in Markdown (it can hold Gemini's own tags for images, steps and follow-up suggestions), the new conversation's id, and the citations Gemini attached, each with its sources' URL, title and publisher; citations is empty when the answer cites nothing. Needs a browser signed in to Google: signed out, the run fails with a signed-out error asking you to sign in to gemini.google.com. A Google account that has never opened Gemini fails with a message asking you to open gemini.google.com once and accept its terms. One run is one draw: the same question can be answered, searched or cited differently on the next run.

- Site: gemini.google.com
- Address: `reduck/gemini.google.com/ask`
- Updated: 2026-10-22 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/gemini.google.com/ask`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/gemini.google.com/ask
```

## Input

- `question` (string, required): The question/prompt to send as the first message of a new chat.

## Output

- `answer` (string, required): The answer as Gemini sends it, in Markdown. Never empty.
- `citations` (array, required): The citations Gemini attached to the answer, in order, each with the sources it names. Empty when the answer cites nothing.
- `conversationId` (string, required): The new conversation's id, as in its gemini.google.com/app/<id> address.

## FAQ

### What does "Ask Gemini" do?

Open a new Gemini chat, send one question, and wait until Gemini has finished its answer (up to 3 min). Returns the answer as Gemini sends it, in Markdown (it can hold Gemini's own tags for images, steps and follow-up suggestions), the new conversation's id, and the citations Gemini attached, each with its sources' URL, title and publisher; citations is empty when the answer cites nothing. Needs a browser signed in to Google: signed out, the run fails with a signed-out error asking you to sign in to gemini.google.com. A Google account that has never opened Gemini fails with a message asking you to open gemini.google.com once and accept its terms. One run is one draw: the same question can be answered, searched or cited differently on the next run.

### How do I automatically ask Gemini on gemini.google.com?

Ask an AI agent connected to Reduck to run reduck/gemini.google.com/ask, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gemini.google.com/ask

### Is there a gemini.google.com API to ask Gemini?

You do not need one. "Ask Gemini" drives the real gemini.google.com pages in a browser, so it works whether or not gemini.google.com offers an API for this.

### What information do I need to provide?

Required: question.

### What does it return?

It returns answer, citations, conversationId.

### Do I need to be logged in to gemini.google.com?

Yes. It acts as you on gemini.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the gemini.google.com cookies saved by the Reduck extension.

### Does it change anything on gemini.google.com, or only read data?

It makes changes on gemini.google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/gemini.google.com/ask, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gemini.google.com/ask

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/gemini.google.com/ask
