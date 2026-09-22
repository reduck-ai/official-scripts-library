# Search Crunchbase News

Automatically search Crunchbase News on news.crunchbase.com. List recent Crunchbase News articles, either by topic section or by a search query, with pagination.

- Site: news.crunchbase.com
- Address: `reduck/news.crunchbase.com/search_news`
- Updated: 2026-07-31 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/news.crunchbase.com/search_news`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/news.crunchbase.com/search_news
```

## Input

- `page` (integer, optional): 1-based page number for pagination.
- `query` (string, optional): Full-text search query, e.g. "biotech". Mutually exclusive with section.
- `section` (string, optional): Topic section path as it appears in the site nav, e.g. "fintech", "ai", "seed", "public/ipo". Mutually exclusive with query.

## FAQ

### What does "Search Crunchbase News" do?

List recent Crunchbase News articles, either by topic section or by a search query, with pagination.

### How do I automatically search Crunchbase News on news.crunchbase.com?

Ask an AI agent connected to Reduck to run reduck/news.crunchbase.com/search_news, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/news.crunchbase.com/search_news

### Is there a news.crunchbase.com API to search Crunchbase News?

You do not need one. "Search Crunchbase News" drives the real news.crunchbase.com pages in a browser, so it works whether or not news.crunchbase.com offers an API for this.

### What information do I need to provide?

Optional: page, query, section.

### Do I need to be logged in to news.crunchbase.com?

No. It only uses pages of news.crunchbase.com that are reachable without signing in.

### Does it change anything on news.crunchbase.com, or only read data?

Unknown: its author has not declared whether it changes anything on news.crunchbase.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/news.crunchbase.com/search_news, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/news.crunchbase.com/search_news

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/news.crunchbase.com/search_news
