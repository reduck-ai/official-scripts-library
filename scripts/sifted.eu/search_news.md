# Search Sifted News

Automatically search Sifted News on sifted.eu. Search Sifted's European tech news articles by keyword, with optional sector, category, and country filters.

- Site: sifted.eu
- Address: `reduck/sifted.eu/search_news`
- Updated: 2026-07-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/sifted.eu/search_news`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/sifted.eu/search_news
```

## Input

- `query` (string, required): Full-text search query, e.g. "biotech" or a company name.
- `page` (integer, optional): 1-based page number for pagination.
- `sector` (string, optional): Restrict to one of Sifted's top-level sectors.
- `category` (string, optional): Restrict to one article format/category.

## FAQ

### What does "Search Sifted News" do?

Search Sifted's European tech news articles by keyword, with optional sector, category, and country filters.

### How do I automatically search Sifted News on sifted.eu?

Ask an AI agent connected to Reduck to run reduck/sifted.eu/search_news, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sifted.eu/search_news

### Is there a sifted.eu API to search Sifted News?

You do not need one. "Search Sifted News" drives the real sifted.eu pages in a browser, so it works whether or not sifted.eu offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sector, category.

### Do I need to be logged in to sifted.eu?

No. It only uses pages of sifted.eu that are reachable without signing in.

### Does it change anything on sifted.eu, or only read data?

Unknown: its author has not declared whether it changes anything on sifted.eu, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/sifted.eu/search_news, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sifted.eu/search_news

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/sifted.eu/search_news
