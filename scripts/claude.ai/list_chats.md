# List Claude chats

Automatically list Claude chats on claude.ai. List your recent Claude.ai chats (the /recents + sidebar list), newest first. Paginate with limit+offset.

- Site: claude.ai
- Address: `reduck/claude.ai/list_chats`
- Updated: 2026-07-20 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/claude.ai/list_chats`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/claude.ai/list_chats
```

## Input

- `limit` (integer, optional): Max conversations to return (default 30).
- `offset` (integer, optional): How many to skip. The site's infinite scroll is a growing offset; order is updated_at desc and stable, so offset paging is safe.

## FAQ

### What does "List Claude chats" do?

List your recent Claude.ai chats (the /recents + sidebar list), newest first. Paginate with limit+offset.

### How do I automatically list Claude chats on claude.ai?

Ask an AI agent connected to Reduck to run reduck/claude.ai/list_chats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/list_chats

### Is there a claude.ai API to list Claude chats?

You do not need one. "List Claude chats" drives the real claude.ai pages in a browser, so it works whether or not claude.ai offers an API for this.

### What information do I need to provide?

Optional: limit, offset.

### Do I need to be logged in to claude.ai?

Yes. It acts as you on claude.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the claude.ai cookies saved by the Reduck extension.

### Does it change anything on claude.ai, or only read data?

Unknown: its author has not declared whether it changes anything on claude.ai, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/claude.ai/list_chats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/list_chats

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/claude.ai/list_chats
