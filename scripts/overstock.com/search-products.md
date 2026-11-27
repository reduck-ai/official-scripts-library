# Search Overstock products

Automatically search Overstock products on overstock.com. Search Overstock products by keyword, one results page at a time. Gives each product's id, name, link, price, comparison price, rating, review count and image, with the number of pages. Overstock does not state the number of results. A search with no match, or a page after the last one, gives an empty items list.

- Site: overstock.com
- Address: `reduck/overstock.com/search-products`
- Updated: 2026-11-26 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/overstock.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/overstock.com/search-products
```

## Input

- `query` (string, required): The words to search for, as typed in the site's search box, e.g. "coffee table".
- `page` (integer, optional): The results page to return, from 1.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `total_pages` (integer | null, required): The number of results pages the site lets you open. Null for a page after the last one.
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required): 0 when the search has no match. Null otherwise: Overstock does not state the number of results.

## FAQ

### What does "Search Overstock products" do?

Search Overstock products by keyword, one results page at a time. Gives each product's id, name, link, price, comparison price, rating, review count and image, with the number of pages. Overstock does not state the number of results. A search with no match, or a page after the last one, gives an empty items list.

### How do I automatically search Overstock products on overstock.com?

Ask an AI agent connected to Reduck to run reduck/overstock.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/overstock.com/search-products

### Is there a overstock.com API to search Overstock products?

You do not need one. "Search Overstock products" drives the real overstock.com pages in a browser, so it works whether or not overstock.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, total_pages, has_next_page, total_results.

### Do I need to be logged in to overstock.com?

No. It only uses pages of overstock.com that are reachable without signing in.

### Does it change anything on overstock.com, or only read data?

It only reads. It looks things up on overstock.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/overstock.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/overstock.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/overstock.com/search-products
