# Ask Grok

Automatically ask Grok on grok.com. Open a new Grok conversation, send one question, wait for the answer, and return the answer text plus any cited web sources. If the account has never confirmed Grok's one-time age gate, sending will hang and time out rather than silently confirming it on the caller's behalf.

- Site: grok.com
- Address: `reduck/grok.com/ask`
- Updated: 2026-08-27 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/grok.com/ask`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/grok.com/ask
```

## Input

- `question` (string, required): The question to ask Grok

## Output

- `answer` (string, required): The assistant's answer text
- `sources` (array, required): Inline-cited web sources referenced in the answer, if any (empty when Grok answered without citing sources)
- `conversationId` (string, required): The Grok conversation id, from the resulting /c/<id> URL

## FAQ

### What does "Ask Grok" do?

Open a new Grok conversation, send one question, wait for the answer, and return the answer text plus any cited web sources. If the account has never confirmed Grok's one-time age gate, sending will hang and time out rather than silently confirming it on the caller's behalf.

### How do I automatically ask Grok on grok.com?

Ask an AI agent connected to Reduck to run reduck/grok.com/ask, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/grok.com/ask

### Is there a grok.com API to ask Grok?

You do not need one. "Ask Grok" drives the real grok.com pages in a browser, so it works whether or not grok.com offers an API for this.

### What information do I need to provide?

Required: question.

### What does it return?

It returns answer, sources, conversationId.

### Do I need to be logged in to grok.com?

Yes. It acts as you on grok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the grok.com cookies saved by the Reduck extension.

### Does it change anything on grok.com, or only read data?

It makes changes on grok.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/grok.com/ask, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/grok.com/ask

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/grok.com/ask
