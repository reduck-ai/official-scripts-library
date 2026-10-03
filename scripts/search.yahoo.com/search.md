# Yahoo web search

Search the web with Yahoo Search and get one page of organic results: each result's position, title, link, displayed site and snippet. Sponsored results are left out. Page through results with the page number.

- Site: search.yahoo.com
- Address: `reduck/search.yahoo.com/search`
- Updated: 2026-10-02 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/search.yahoo.com/search`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/search.yahoo.com/search
```

## Input

- `query` (string, required): What to search for. Yahoo's operators work, e.g. site:example.com or "exact phrase".
- `page` (integer, optional): Results page, 1-based.

## Output

- `page` (integer, required)
- `query` (string, required)
- `results` (array, required): Organic results in page order. Empty when Yahoo has no results for the query.
- `hasNextPage` (boolean, optional)

## FAQ

### What does "Yahoo web search" do?

Search the web with Yahoo Search and get one page of organic results: each result's position, title, link, displayed site and snippet. Sponsored results are left out. Page through results with the page number.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, query, results, hasNextPage.

### Do I need to be logged in to search.yahoo.com?

No. It only uses pages of search.yahoo.com that are reachable without signing in.

### Does it change anything on search.yahoo.com, or only read data?

It only reads. It looks things up on search.yahoo.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/search.yahoo.com/search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/search.yahoo.com/search

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/search.yahoo.com/search
