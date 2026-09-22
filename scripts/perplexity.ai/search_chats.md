# Search Perplexity chats

Automatically search Perplexity chats on perplexity.ai. Search your Perplexity thread history by keyword, via the Sessions library's search box.

- Site: perplexity.ai
- Address: `reduck/perplexity.ai/search_chats`
- Updated: 2026-08-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/perplexity.ai/search_chats`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/perplexity.ai/search_chats
```

## Input

- `query` (string, required): Search term, matched against thread titles and answer text.

## Output

- `chats` (array, required)
- `query` (string, required)
- `hasMore` (boolean, required): Whether more matching threads exist beyond the ones returned here.

## FAQ

### What does "Search Perplexity chats" do?

Search your Perplexity thread history by keyword, via the Sessions library's search box.

### How do I automatically search Perplexity chats on perplexity.ai?

Ask an AI agent connected to Reduck to run reduck/perplexity.ai/search_chats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/perplexity.ai/search_chats

### Is there a perplexity.ai API to search Perplexity chats?

You do not need one. "Search Perplexity chats" drives the real perplexity.ai pages in a browser, so it works whether or not perplexity.ai offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns chats, query, hasMore.

### Do I need to be logged in to perplexity.ai?

Yes. It acts as you on perplexity.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the perplexity.ai cookies saved by the Reduck extension.

### Does it change anything on perplexity.ai, or only read data?

It only reads. It looks things up on perplexity.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/perplexity.ai/search_chats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/perplexity.ai/search_chats

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/perplexity.ai/search_chats
