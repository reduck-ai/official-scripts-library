# Search Harbor Freight products

Automatically search Harbor Freight products on harborfreight.com. Search the Harbor Freight catalogue by keyword and return one page of results (36 per page) with price, rating and stock status.

- Site: harborfreight.com
- Address: `reduck/harborfreight.com/search-products`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/harborfreight.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/harborfreight.com/search-products
```

## Input

- `query` (string, required): Search words, as typed in the site search box.
- `page` (integer, optional): Results page, 36 products per page.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `has_next_page` (boolean, required)
- `total_results` (integer, required)
- `total_pages` (integer | null, optional)
- `redirect_url` (string | null, optional): The page the site opens instead of results, for example when the query is an exact SKU.

## FAQ

### What does "Search Harbor Freight products" do?

Search the Harbor Freight catalogue by keyword and return one page of results (36 per page) with price, rating and stock status.

### How do I automatically search Harbor Freight products on harborfreight.com?

Ask an AI agent connected to Reduck to run reduck/harborfreight.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/harborfreight.com/search-products

### Is there a harborfreight.com API to search Harbor Freight products?

You do not need one. "Search Harbor Freight products" drives the real harborfreight.com pages in a browser, so it works whether or not harborfreight.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, total_pages, redirect_url, has_next_page, total_results.

### Do I need to be logged in to harborfreight.com?

No. It only uses pages of harborfreight.com that are reachable without signing in.

### Does it change anything on harborfreight.com, or only read data?

It only reads. It looks things up on harborfreight.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/harborfreight.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/harborfreight.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/harborfreight.com/search-products
