# Search Bed Bath & Beyond products

Automatically search Bed Bath & Beyond products on bedbathandbeyond.com. Search Bed Bath & Beyond products by keyword, one results page at a time. Gives each product's id, name, link, price, comparison price, rating, review count and image, with the total number of results and pages. A search with no match, or a page after the last one, gives an empty items list.

- Site: bedbathandbeyond.com
- Address: `reduck/bedbathandbeyond.com/search-products`
- Updated: 2026-11-26 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bedbathandbeyond.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bedbathandbeyond.com/search-products
```

## Input

- `query` (string, required): The words to search for, as typed in the site's search box, e.g. "coffee table".
- `page` (integer, optional): The results page to return, from 1.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `total_pages` (integer, required): The number of results pages the site lets you open.
- `has_next_page` (boolean, required)
- `total_results` (integer, required): The number of matching products the site states.

## FAQ

### What does "Search Bed Bath & Beyond products" do?

Search Bed Bath & Beyond products by keyword, one results page at a time. Gives each product's id, name, link, price, comparison price, rating, review count and image, with the total number of results and pages. A search with no match, or a page after the last one, gives an empty items list.

### How do I automatically search Bed Bath & Beyond products on bedbathandbeyond.com?

Ask an AI agent connected to Reduck to run reduck/bedbathandbeyond.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bedbathandbeyond.com/search-products

### Is there a bedbathandbeyond.com API to search Bed Bath & Beyond products?

You do not need one. "Search Bed Bath & Beyond products" drives the real bedbathandbeyond.com pages in a browser, so it works whether or not bedbathandbeyond.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, total_pages, has_next_page, total_results.

### Do I need to be logged in to bedbathandbeyond.com?

No. It only uses pages of bedbathandbeyond.com that are reachable without signing in.

### Does it change anything on bedbathandbeyond.com, or only read data?

It only reads. It looks things up on bedbathandbeyond.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bedbathandbeyond.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bedbathandbeyond.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/bedbathandbeyond.com/search-products
