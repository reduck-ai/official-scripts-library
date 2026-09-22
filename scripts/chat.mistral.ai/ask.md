# Ask Le Chat

Automatically ask Le Chat on chat.mistral.ai. Open a new Le Chat conversation, send one question, wait for the answer, and return the answer text plus any web-search source domains cited.

- Site: chat.mistral.ai
- Address: `reduck/chat.mistral.ai/ask`
- Updated: 2026-08-26 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/chat.mistral.ai/ask`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/chat.mistral.ai/ask
```

## Input

- `question` (string, required): The question or prompt to send to Le Chat

## Output

- `answer` (string, required): The assistant's answer text (markdown as rendered)
- `chatId` (string, required): Id of the newly created conversation
- `question` (string, required)
- `citations` (array, required): Web-search source domains Le Chat cited inline, if any. Le Chat's UI does not expose full source URLs, only the source domain.
- `messageId` (string, required): Id of the assistant's answer message

## FAQ

### What does "Ask Le Chat" do?

Open a new Le Chat conversation, send one question, wait for the answer, and return the answer text plus any web-search source domains cited.

### How do I automatically ask Le Chat on chat.mistral.ai?

Ask an AI agent connected to Reduck to run reduck/chat.mistral.ai/ask, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chat.mistral.ai/ask

### Is there a chat.mistral.ai API to ask Le Chat?

You do not need one. "Ask Le Chat" drives the real chat.mistral.ai pages in a browser, so it works whether or not chat.mistral.ai offers an API for this.

### What information do I need to provide?

Required: question.

### What does it return?

It returns answer, chatId, question, citations, messageId.

### Do I need to be logged in to chat.mistral.ai?

Yes. It acts as you on chat.mistral.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the chat.mistral.ai cookies saved by the Reduck extension.

### Does it change anything on chat.mistral.ai, or only read data?

It makes changes on chat.mistral.ai, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/chat.mistral.ai/ask, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chat.mistral.ai/ask

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/chat.mistral.ai/ask
