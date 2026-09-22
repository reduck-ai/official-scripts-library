# Search Gemini chats

Automatically search Gemini chats on gemini.google.com. Search your Gemini conversations (the "Search chats" box): server-side full-text over titles and message bodies.

- Site: gemini.google.com
- Address: `reduck/gemini.google.com/search_chats`
- Updated: 2026-08-26 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/gemini.google.com/search_chats`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/gemini.google.com/search_chats
```

## Input

- `query` (string, required): Free-text query, same as the site's "Search chats" box.

## Output

- `results` (array, required)

## FAQ

### What does "Search Gemini chats" do?

Search your Gemini conversations (the "Search chats" box): server-side full-text over titles and message bodies.

### How do I automatically search Gemini chats on gemini.google.com?

Ask an AI agent connected to Reduck to run reduck/gemini.google.com/search_chats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gemini.google.com/search_chats

### Is there a gemini.google.com API to search Gemini chats?

You do not need one. "Search Gemini chats" drives the real gemini.google.com pages in a browser, so it works whether or not gemini.google.com offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns results.

### Do I need to be logged in to gemini.google.com?

Yes. It acts as you on gemini.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the gemini.google.com cookies saved by the Reduck extension.

### Does it change anything on gemini.google.com, or only read data?

It only reads. It looks things up on gemini.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/gemini.google.com/search_chats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gemini.google.com/search_chats

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/gemini.google.com/search_chats
