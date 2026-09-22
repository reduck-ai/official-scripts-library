# Search Claude chats

Automatically search Claude chats on claude.ai. Search your Claude.ai chats (the "Search chats…" box): server-side full-text over titles + message bodies. Each hit carries the matched snippet and match offsets the UI bolds.

- Site: claude.ai
- Address: `reduck/claude.ai/search_chats`
- Updated: 2026-07-20 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/claude.ai/search_chats`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/claude.ai/search_chats
```

## Input

- `query` (string, required): Free-text query, same as the site's search box.
- `n` (integer, optional): Max results (the site requests 200).
- `snippet_size` (integer, optional): Target length of each matched snippet, in chars.

## Output

- `results` (array, required)
- `next_page_token` (string | null, optional)

## FAQ

### What does "Search Claude chats" do?

Search your Claude.ai chats (the "Search chats…" box): server-side full-text over titles + message bodies. Each hit carries the matched snippet and match offsets the UI bolds.

### How do I automatically search Claude chats on claude.ai?

Ask an AI agent connected to Reduck to run reduck/claude.ai/search_chats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/search_chats

### Is there a claude.ai API to search Claude chats?

You do not need one. "Search Claude chats" drives the real claude.ai pages in a browser, so it works whether or not claude.ai offers an API for this.

### What information do I need to provide?

Required: query. Optional: n, snippet_size.

### What does it return?

It returns results, next_page_token.

### Do I need to be logged in to claude.ai?

Yes. It acts as you on claude.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the claude.ai cookies saved by the Reduck extension.

### Does it change anything on claude.ai, or only read data?

Unknown: its author has not declared whether it changes anything on claude.ai, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/claude.ai/search_chats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/search_chats

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/claude.ai/search_chats
