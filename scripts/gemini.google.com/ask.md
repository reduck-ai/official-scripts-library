# Ask Gemini

Automatically ask Gemini on gemini.google.com. Open a new Gemini chat, send one question, and wait for the answer to finish generating (up to 3 min), then return the answer as rendered, the conversation id, and the citation labels Gemini attached to it. Requires a signed-in Google session: gemini.google.com has no anonymous chat, and signed out it serves the marketing page and never mounts a composer. An account that has never opened Gemini also has to accept its first-run terms once in a normal browser; until then the app stays on that same page and the script fails with a descriptive error rather than hanging. The answer is always read in English, whatever language the account is set to. Citations are publisher labels, not links: Gemini renders each grounded claim as an inline chip naming the source ("FIFA", "aimagazine.com +1") and keeps the target URL behind a dialog that only opens on click, so `citations` tells you whether the answer was grounded and on whom, but is not a URL list, and an ungrounded answer returns an empty one. Treat one run as a single draw rather than a measurement: the model may search differently, or not search at all, on the next run of the same question, so repeat a question before concluding anything from it.

- Site: gemini.google.com
- Address: `reduck/gemini.google.com/ask`
- Updated: 2026-09-21 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/gemini.google.com/ask`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/gemini.google.com/ask
```

## Input

- `question` (string, required): The question/prompt to send as the first message of a new chat.

## Output

- `answer` (string, required): The reply as rendered (innerText of the response's message-content). Inline widget labels appear as they do on screen and KaTeX math linearizes lossily. Never empty: a response that rendered no text is breakage, not an answer.
- `citations` (array, required): The inline citation chips as rendered, in order — a publisher label per grounded claim ("FIFA", "aimagazine.com +1"), not a URL: Gemini keeps each chip's target behind a click-only dialog. Empty when the answer cited nothing.
- `conversationId` (string, required): Conversation id from the /app/<id> URL, which the send creates. Required: a chat that never got one did not happen.

## FAQ

### What does "Ask Gemini" do?

Open a new Gemini chat, send one question, and wait for the answer to finish generating (up to 3 min), then return the answer as rendered, the conversation id, and the citation labels Gemini attached to it. Requires a signed-in Google session: gemini.google.com has no anonymous chat, and signed out it serves the marketing page and never mounts a composer. An account that has never opened Gemini also has to accept its first-run terms once in a normal browser; until then the app stays on that same page and the script fails with a descriptive error rather than hanging. The answer is always read in English, whatever language the account is set to. Citations are publisher labels, not links: Gemini renders each grounded claim as an inline chip naming the source ("FIFA", "aimagazine.com +1") and keeps the target URL behind a dialog that only opens on click, so `citations` tells you whether the answer was grounded and on whom, but is not a URL list, and an ungrounded answer returns an empty one. Treat one run as a single draw rather than a measurement: the model may search differently, or not search at all, on the next run of the same question, so repeat a question before concluding anything from it.

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

It makes changes on gemini.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/gemini.google.com/ask, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gemini.google.com/ask

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/gemini.google.com/ask
