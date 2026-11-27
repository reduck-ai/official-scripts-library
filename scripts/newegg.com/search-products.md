# Search Newegg products

Automatically search Newegg products on newegg.com. Search Newegg (newegg.com) products by keyword, one results page at a time, with sort. Returns item numbers, titles, prices, sellers and the total count; a search with no match or a page past the last returns an empty list.

- Site: newegg.com
- Address: `reduck/newegg.com/search-products`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/newegg.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/newegg.com/search-products
```

## Input

- `query` (string, required): Free-text search query, e.g. "ssd 1tb".
- `page` (integer, optional): Result page (1-based).
- `sort` (string, optional): Newegg's own sort options.

## Output

- `page` (integer, required)
- `items` (array, required): The products of this page, in Newegg's order, sponsored ones included and flagged. Empty when nothing matches.
- `query` (string, required)
- `url` (string, optional)
- `sort` (string, optional)
- `total_count` (integer | null, optional): Newegg's count of matches for the query.
- `corrected_query` (string | null, optional)

## FAQ

### What does "Search Newegg products" do?

Search Newegg (newegg.com) products by keyword, one results page at a time, with sort. Returns item numbers, titles, prices, sellers and the total count; a search with no match or a page past the last returns an empty list.

### How do I automatically search Newegg products on newegg.com?

Ask an AI agent connected to Reduck to run reduck/newegg.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/newegg.com/search-products

### Is there a newegg.com API to search Newegg products?

You do not need one. "Search Newegg products" drives the real newegg.com pages in a browser, so it works whether or not newegg.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort.

### What does it return?

It returns url, page, sort, items, query, total_count, corrected_query.

### Do I need to be logged in to newegg.com?

No. It only uses pages of newegg.com that are reachable without signing in.

### Does it change anything on newegg.com, or only read data?

It only reads. It looks things up on newegg.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/newegg.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/newegg.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/newegg.com/search-products
