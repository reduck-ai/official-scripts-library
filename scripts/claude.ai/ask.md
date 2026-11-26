# Ask Claude on claude.ai

Automatically ask Claude on claude.ai on claude.ai. Open a new Claude.ai chat, send one question, and wait for the answer to finish (up to 100 s). Returns the answer as the markdown the model emitted, the message and conversation ids, why generation stopped, which model answered, each web search it made with the results it was shown, and every source its search and fetch tools surfaced. Citation links are returned when claude.ai attaches them to the answer; answers that searched the web now carry their links in the markdown instead, and the citation list is then empty. Requires a signed-in session: claude.ai has no anonymous chat, and a signed-out browser fails at once with an error that says so. When the account has used up its 5-hour or weekly allowance, it fails at once with the time the allowance resets, without sending anything. Avoid running many of these at once: claude.ai limits how many chats one account may hold concurrently and refuses the extras, so a refused send comes back quickly carrying Claude's own message and only needs to be retried at a slower pace.

- Site: claude.ai
- Address: `reduck/claude.ai/ask`
- Updated: 2026-11-25 (v33)
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
- `answer` (string, required): The assistant's full answer as the markdown source the model emitted (the turn's `text` blocks, concatenated in order). Not the rendered text: the reasoning card and tool-call cards are separate block types and are excluded. Links the model wrote into its answer stay in the markdown.
- `sources` (array, required): Every source the model's tools surfaced: each result a web search returned and each page a fetch loaded, deduped by url. This is the candidate pool the model could read, not what the answer cited. Empty when no tool ran.
- `searches` (array, required): One entry per web search call, in call order, each with its mode and the results it returned. Empty when the model didn't search.
- `citations` (array, required): One entry per citation link claude.ai attaches to the answer, when it attaches them as citation data. Since Nov 2026 claude.ai answers with web searches carry none (the model writes its links into the markdown of `answer`), so this is empty then; it is also empty when the answer cited nothing.
- `messageId` (string, required): uuid of the assistant message.
- `stopReason` (string, required): Why generation ended: "end_turn" for a complete answer, anything else (e.g. "max_tokens") means the answer is truncated.
- `conversationId` (string, required): Conversation uuid, read off the chat's own URL (/chat/<conversationId>) once the server holds the conversation.
- `webSearchQueries` (array, required): Search queries the model issued during this answer, in order. Empty when it didn't search.

## FAQ

### What does "Ask Claude on claude.ai" do?

Open a new Claude.ai chat, send one question, and wait for the answer to finish (up to 100 s). Returns the answer as the markdown the model emitted, the message and conversation ids, why generation stopped, which model answered, each web search it made with the results it was shown, and every source its search and fetch tools surfaced. Citation links are returned when claude.ai attaches them to the answer; answers that searched the web now carry their links in the markdown instead, and the citation list is then empty. Requires a signed-in session: claude.ai has no anonymous chat, and a signed-out browser fails at once with an error that says so. When the account has used up its 5-hour or weekly allowance, it fails at once with the time the allowance resets, without sending anything. Avoid running many of these at once: claude.ai limits how many chats one account may hold concurrently and refuses the extras, so a refused send comes back quickly carrying Claude's own message and only needs to be retried at a slower pace.

### How do I automatically ask Claude on claude.ai on claude.ai?

Ask an AI agent connected to Reduck to run reduck/claude.ai/ask, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/ask

### Is there a claude.ai API to ask Claude on claude.ai?

You do not need one. "Ask Claude on claude.ai" drives the real claude.ai pages in a browser, so it works whether or not claude.ai offers an API for this.

### What information do I need to provide?

Required: question.

### What does it return?

It returns url, model, answer, sources, searches, citations, messageId, stopReason, conversationId, webSearchQueries.

### Do I need to be logged in to claude.ai?

Yes. It acts as you on claude.ai: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for claude.ai.

### Does it change anything on claude.ai, or only read data?

It makes changes on claude.ai, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/claude.ai/ask, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/ask

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/claude.ai/ask
