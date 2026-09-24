# Ask ChatGPT

Automatically ask ChatGPT on chatgpt.com. Open a new ChatGPT chat, send one question, wait for the answer to finish (up to 3 min), and return what the model answered, the sources it cited, the searches it ran, and what ChatGPT itself reports about how it searched.

- Site: chatgpt.com
- Address: `reduck/chatgpt.com/ask`
- Updated: 2026-09-23 (v31)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/chatgpt.com/ask`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/ask
```

## Input

- `question` (string, required): The question to send as the first message of a new chat.

## Output

- `calls` (array, required): One entry per search call, as the page numbers them. A call often runs a whole round of queries at once (measured 2026-09-23: 9 queries in 2 calls) and answers one list for all of them. What the page does not receive: which query returned which result, the call's arguments, and which search backend answered it. Empty when it did not search, and signed out.
- `model` (string | null, required): Which model answered, by ChatGPT's own id (e.g. "gpt-5-6"). Null when the app does not say.
- `answer` (string | null, required): The answer as markdown, as ChatGPT's own Copy gives it: each citation is a markdown link to its source. Null signed out.
- `answers` (array, required): One entry per assistant turn, as rendered. Usually one; ChatGPT sometimes serves a paired-response variant that answers twice and asks which reply you prefer, and neither entry is more official than the other — read the length before reading answers[0]. Inline citation chips appear as their publisher's name in the text, and mathematical notation linearizes lossily.
- `sources` (array, required): Every page the searches put in front of the model, once each, in the order it got them — the pool the answer could draw on, as opposed to `references`, what it cited. Empty signed out.
- `searches` (array, required): One entry per round of web searches, in order: what the model typed and the results put in front of it. Empty when it did not search, and signed out.
- `references` (array, required): Every source the answer CITED — not everything the search retrieved (that is `sources`) — deduplicated by url and in the order the answer surfaced them. Empty when the answer did not search, which is a fact about that reply rather than a failure: the same question searches on one run and not the next.
- `stopReason` (string | null, required): Why generation ended, as ChatGPT records it: "stop" for an answer the model finished. Null signed out. A finished answer can still be only a sentence announcing work it never did; that is what the model returned, not a truncation.
- `searchContext` (object, required): What the server says about this turn's search, as sent to the page. Sent signed in, and by one of ChatGPT's two signed-out applications; the other one (the one that opens a /uc/ chat) does not put it in the page, so every field is null there whether or not the reply searched. A field is also null when the app did not send it.
- `conversationId` (string | null, required): The conversation's id, from the /c/<id> or /uc/<id> URL. Null if the app did not navigate.
- `webSearchQueries` (array, required): The searches ChatGPT issued, in order, as its answer stream names them. Sent signed in, and by one of ChatGPT's two signed-out applications; the one that opens a /uc/ chat does not put them in the page, so the list is empty there even when `references` shows the reply searched. Empty also when the reply did not search.

## FAQ

### What does "Ask ChatGPT" do?

Open a new ChatGPT chat, send one question, wait for the answer to finish (up to 3 min), and return what the model answered, the sources it cited, the searches it ran, and what ChatGPT itself reports about how it searched.

### How do I automatically ask ChatGPT on chatgpt.com?

Ask an AI agent connected to Reduck to run reduck/chatgpt.com/ask, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/ask

### Is there a chatgpt.com API to ask ChatGPT?

You do not need one. "Ask ChatGPT" drives the real chatgpt.com pages in a browser, so it works whether or not chatgpt.com offers an API for this.

### What information do I need to provide?

Required: question.

### What does it return?

It returns calls, model, answer, answers, sources, searches, references, stopReason, searchContext, conversationId, webSearchQueries.

### Do I need to be logged in to chatgpt.com?

No. It only uses pages of chatgpt.com that are reachable without signing in.

### Does it change anything on chatgpt.com, or only read data?

It makes changes on chatgpt.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/chatgpt.com/ask, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/ask

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/chatgpt.com/ask
