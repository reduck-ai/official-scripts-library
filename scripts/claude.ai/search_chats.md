# Search Claude chats

Automatically search Claude chats on claude.ai. Search all your Claude chats by words in their titles and messages, as Claude's Search box does. Returns up to 25 chats with uuid, title, dates, the excerpt that matched and where the words match. Claude's search also returns related chats, so a result does not always contain the words.

- Site: claude.ai
- Address: `reduck/claude.ai/search_chats`
- Updated: 2026-11-09 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/claude.ai/search_chats`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/claude.ai/search_chats
```

## Input

- `query` (string, required): Words to look for, as typed in Claude's Search box.

## Output

- `results` (array, required)
- `next_page_token` (string | null, optional): Claude's own page token; null when it gives none (the Search box shows at most 25 results).

## FAQ

### What does "Search Claude chats" do?

Search all your Claude chats by words in their titles and messages, as Claude's Search box does. Returns up to 25 chats with uuid, title, dates, the excerpt that matched and where the words match. Claude's search also returns related chats, so a result does not always contain the words.

### How do I automatically search Claude chats on claude.ai?

Ask an AI agent connected to Reduck to run reduck/claude.ai/search_chats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/search_chats

### Is there a claude.ai API to search Claude chats?

You do not need one. "Search Claude chats" drives the real claude.ai pages in a browser, so it works whether or not claude.ai offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns results, next_page_token.

### Do I need to be logged in to claude.ai?

Yes. It acts as you on claude.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the claude.ai cookies saved by the Reduck extension.

### Does it change anything on claude.ai, or only read data?

It only reads. It looks things up on claude.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/claude.ai/search_chats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/search_chats

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/claude.ai/search_chats
