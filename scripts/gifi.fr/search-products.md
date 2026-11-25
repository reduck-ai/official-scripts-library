# Search Gifi products

Automatically search Gifi products on gifi.fr. Search Gifi.fr (home, decoration, toys) by free text and return one page of results of about 48 items: id, name, link, price in euros, availability label, category path, image and seller, plus the total number of results, the page number and whether another page follows. Stop paging when has_next_page is false. A search with no match returns an empty list. Pass an item's url to Get Gifi product.

- Site: gifi.fr
- Address: `reduck/gifi.fr/search-products`
- Updated: 2026-11-24 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/gifi.fr/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/gifi.fr/search-products
```

## Input

- `query` (string, required): Free-text search, in French, e.g. bougie parfumée.
- `page` (integer, optional): Page number, starting at 1.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `has_next_page` (boolean, required)
- `last_page` (integer | null, optional)
- `total_results` (integer | null, optional)

## FAQ

### What does "Search Gifi products" do?

Search Gifi.fr (home, decoration, toys) by free text and return one page of results of about 48 items: id, name, link, price in euros, availability label, category path, image and seller, plus the total number of results, the page number and whether another page follows. Stop paging when has_next_page is false. A search with no match returns an empty list. Pass an item's url to Get Gifi product.

### How do I automatically search Gifi products on gifi.fr?

Ask an AI agent connected to Reduck to run reduck/gifi.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gifi.fr/search-products

### Is there a gifi.fr API to search Gifi products?

You do not need one. "Search Gifi products" drives the real gifi.fr pages in a browser, so it works whether or not gifi.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, last_page, has_next_page, total_results.

### Do I need to be logged in to gifi.fr?

No. It only uses pages of gifi.fr that are reachable without signing in.

### Does it change anything on gifi.fr, or only read data?

It only reads. It looks things up on gifi.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/gifi.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gifi.fr/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/gifi.fr/search-products
