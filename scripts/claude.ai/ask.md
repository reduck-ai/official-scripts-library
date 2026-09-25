# Ask Claude

Automatically ask Claude on claude.ai. Open a new Claude.ai chat, send one question, and wait for the answer to finish (up to 3 minutes). Returns the answer as the markdown the model emitted, the message and conversation ids, why generation stopped, which model answered, the web_search queries it issued, every source its web_search and web_fetch tools surfaced, and — separately — the sources the answer actually cited. Requires a signed-in session: claude.ai has no anonymous chat. Avoid running many of these at once: claude.ai limits how many chats one account may hold concurrently and refuses the extras, so a refused send comes back quickly carrying Claude's own message and only needs to be retried at a slower pace.

- Site: claude.ai
- Address: `reduck/claude.ai/ask`
- Updated: 2026-09-24 (v15)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/claude.ai/ask`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/claude.ai/ask
```

## Input

- `question` (string, required): The question/prompt to send as the first message of a new chat.

## Output

- `url` (string, required): Address of the new chat on claude.ai, opening it for the account that asked: https://claude.ai/chat/<conversationId>.
- `model` (string | null, required): Which model answered, as the conversation records it (e.g. "claude-opus-5") — the server's own name for what ran, not the composer's display label. Null when the conversation carried no model.
- `answer` (string, required): The assistant's full answer as the markdown source the model emitted (the turn's `text` blocks, concatenated in order). Not the rendered text: the reasoning card and tool-call cards are separate block types and are excluded. It carries NO citation markup — a cited sentence is plain text here, and which sources it cited is `citations`.
- `sources` (array, required): Every source the model's tools surfaced: each result web_search returned and each page web_fetch loaded, deduped by url. This is the CANDIDATE POOL the model could read, NOT what the answer cited — a one-line answer routinely carries a dozen. See `citations` for what it actually attributed. Empty when no tool ran.
- `searches` (array, required): One entry per web search call, in call order, each with the tool that ran it and the results it returned. Empty when the model didn't search. This is the per-query view; `sources` is the same pages as one deduped pool together with what web_fetch loaded.
- `citations` (array, required): The sources the ANSWER ATTRIBUTED a sentence to — the citation pills rendered under the text — in first-cited order, deduped by url. A strict reading of what the answer stood on, as opposed to `sources`, which is everything the tools put in front of it. Empty when the answer cited nothing, which is a real outcome and not a failure: a model answering from training data cites nobody. The span each citation covers is not reported — only which sources were cited.
- `messageId` (string, required): uuid of the assistant message.
- `stopReason` (string, required): Why generation ended: "end_turn" for a complete answer, anything else (e.g. "max_tokens") means the answer is truncated.
- `conversationId` (string, required): Conversation uuid, read off the completion endpoint's own URL (never null — claude.ai has no anonymous chat).
- `webSearchQueries` (array, required): Search queries the model issued during this answer, with either search tool, in order. Empty when it didn't search. The same calls, each with its tool and result list, are `searches`.

## FAQ

### What does "Ask Claude" do?

Open a new Claude.ai chat, send one question, and wait for the answer to finish (up to 3 minutes). Returns the answer as the markdown the model emitted, the message and conversation ids, why generation stopped, which model answered, the web_search queries it issued, every source its web_search and web_fetch tools surfaced, and — separately — the sources the answer actually cited. Requires a signed-in session: claude.ai has no anonymous chat. Avoid running many of these at once: claude.ai limits how many chats one account may hold concurrently and refuses the extras, so a refused send comes back quickly carrying Claude's own message and only needs to be retried at a slower pace.

### How do I automatically ask Claude on claude.ai?

Ask an AI agent connected to Reduck to run reduck/claude.ai/ask, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/ask

### Is there a claude.ai API to ask Claude?

You do not need one. "Ask Claude" drives the real claude.ai pages in a browser, so it works whether or not claude.ai offers an API for this.

### What information do I need to provide?

Required: question.

### What does it return?

It returns url, model, answer, sources, searches, citations, messageId, stopReason, conversationId, webSearchQueries.

### Do I need to be logged in to claude.ai?

Yes. It acts as you on claude.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the claude.ai cookies saved by the Reduck extension.

### Does it change anything on claude.ai, or only read data?

It only reads. It looks things up on claude.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/claude.ai/ask, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/ask

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/claude.ai/ask
