# Search Monoprix products

Automatically search Monoprix products on monoprix.fr. Search monoprix.fr by keyword.

- Site: monoprix.fr
- Address: `reduck/monoprix.fr/search-products`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/monoprix.fr/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/monoprix.fr/search-products
```

## Input

- `query` (string, required): Search words, as typed in the Monoprix search box, e.g. "lait".
- `page` (integer, optional): Results page, 50 products per page.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `total_pages` (integer, required)
- `has_next_page` (boolean, required)
- `total_results` (integer, required)

## FAQ

### What does "Search Monoprix products" do?

Search monoprix.fr by keyword.

### How do I automatically search Monoprix products on monoprix.fr?

Ask an AI agent connected to Reduck to run reduck/monoprix.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/monoprix.fr/search-products

### Is there a monoprix.fr API to search Monoprix products?

You do not need one. "Search Monoprix products" drives the real monoprix.fr pages in a browser, so it works whether or not monoprix.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, total_pages, has_next_page, total_results.

### Do I need to be logged in to monoprix.fr?

No. It only uses pages of monoprix.fr that are reachable without signing in.

### Does it change anything on monoprix.fr, or only read data?

It only reads. It looks things up on monoprix.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/monoprix.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/monoprix.fr/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/monoprix.fr/search-products
