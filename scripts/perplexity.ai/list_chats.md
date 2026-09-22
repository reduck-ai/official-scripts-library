# List Perplexity chats

Automatically list Perplexity chats on perplexity.ai. List your recent Perplexity threads (most recent first), as shown in the account's sidebar.

- Site: perplexity.ai
- Address: `reduck/perplexity.ai/list_chats`
- Updated: 2026-08-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/perplexity.ai/list_chats`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/perplexity.ai/list_chats
```

## Input

It takes no input.

## Output

- `chats` (array, required)

## FAQ

### What does "List Perplexity chats" do?

List your recent Perplexity threads (most recent first), as shown in the account's sidebar.

### How do I automatically list Perplexity chats on perplexity.ai?

Ask an AI agent connected to Reduck to run reduck/perplexity.ai/list_chats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/perplexity.ai/list_chats

### Is there a perplexity.ai API to list Perplexity chats?

You do not need one. "List Perplexity chats" drives the real perplexity.ai pages in a browser, so it works whether or not perplexity.ai offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns chats.

### Do I need to be logged in to perplexity.ai?

Yes. It acts as you on perplexity.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the perplexity.ai cookies saved by the Reduck extension.

### Does it change anything on perplexity.ai, or only read data?

It only reads. It looks things up on perplexity.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/perplexity.ai/list_chats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/perplexity.ai/list_chats

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/perplexity.ai/list_chats
