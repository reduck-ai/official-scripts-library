# List Grok Chats

Automatically list Grok Chats on grok.com. List recent Grok conversations (newest first): id, title, and a human-readable last-activity label as Grok itself displays it.

- Site: grok.com
- Address: `reduck/grok.com/list_chats`
- Updated: 2026-08-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/grok.com/list_chats`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/grok.com/list_chats
```

## Input

It takes no input.

## Output

- `chats` (array, required)

## FAQ

### What does "List Grok Chats" do?

List recent Grok conversations (newest first): id, title, and a human-readable last-activity label as Grok itself displays it.

### How do I automatically list Grok Chats on grok.com?

Ask an AI agent connected to Reduck to run reduck/grok.com/list_chats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/grok.com/list_chats

### Is there a grok.com API to list Grok Chats?

You do not need one. "List Grok Chats" drives the real grok.com pages in a browser, so it works whether or not grok.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns chats.

### Do I need to be logged in to grok.com?

Yes. It acts as you on grok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the grok.com cookies saved by the Reduck extension.

### Does it change anything on grok.com, or only read data?

It only reads. It looks things up on grok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/grok.com/list_chats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/grok.com/list_chats

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/grok.com/list_chats
