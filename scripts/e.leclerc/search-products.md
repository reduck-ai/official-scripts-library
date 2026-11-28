# Search E.Leclerc products

Automatically search E.Leclerc products on e.leclerc. Search e.leclerc by keyword.

- Site: e.leclerc
- Address: `reduck/e.leclerc/search-products`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/e.leclerc/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/e.leclerc/search-products
```

## Input

- `query` (string, required): Search words, e.g. "lego star wars".
- `page` (integer, optional): Results page, 40 products per page.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `total_pages` (integer, required)
- `redirect_url` (string | null, required): Set when e.leclerc sends this query to a category page instead of listing products (e.g. "lego"); items is then empty
- `has_next_page` (boolean, required)
- `total_results` (integer, required)

## FAQ

### What does "Search E.Leclerc products" do?

Search e.leclerc by keyword.

### How do I automatically search E.Leclerc products on e.leclerc?

Ask an AI agent connected to Reduck to run reduck/e.leclerc/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/e.leclerc/search-products

### Is there a e.leclerc API to search E.Leclerc products?

You do not need one. "Search E.Leclerc products" drives the real e.leclerc pages in a browser, so it works whether or not e.leclerc offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, total_pages, redirect_url, has_next_page, total_results.

### Do I need to be logged in to e.leclerc?

No. It only uses pages of e.leclerc that are reachable without signing in.

### Does it change anything on e.leclerc, or only read data?

It only reads. It looks things up on e.leclerc and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/e.leclerc/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/e.leclerc/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/e.leclerc/search-products
