# Search Alternate products

Automatically search Alternate products on alternate.de. Search products on Alternate Germany (alternate.de, the German store) by keywords, and get one page of results in the order the site gives for relevance: each product with its Alternate product id (Art.-Nr.), name, brand, variant line, link, image, price and currency (euros, VAT included), rating count, availability as the site shows it, and key specifications. A page has up to 24 results: pass page for the next ones, and use total to know how many pages there are. The site answers almost every search with products, close matches included. A page after the last one gives an empty list. When the site sends a search to another page (a brand or category page), redirectUrl gives that page.

- Site: alternate.de
- Address: `reduck/alternate.de/search-products`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/alternate.de/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/alternate.de/search-products
```

## Input

- `query` (string, required): Search words, as typed in the Alternate search box.
- `page` (integer, optional): The result page, from 1. Alternate shows up to 24 results on a page.

## Output

- `page` (integer, required)
- `query` (string, required)
- `total` (integer | null, required): The number of results Alternate gives for the search.
- `products` (array, required)
- `lastResult` (integer | null, required)
- `firstResult` (integer | null, required): The position of the first result of this page, from 1.
- `redirectUrl` (string | null, required): The page the site opened instead of a result list, when it sent the search elsewhere.

## FAQ

### What does "Search Alternate products" do?

Search products on Alternate Germany (alternate.de, the German store) by keywords, and get one page of results in the order the site gives for relevance: each product with its Alternate product id (Art.-Nr.), name, brand, variant line, link, image, price and currency (euros, VAT included), rating count, availability as the site shows it, and key specifications. A page has up to 24 results: pass page for the next ones, and use total to know how many pages there are. The site answers almost every search with products, close matches included. A page after the last one gives an empty list. When the site sends a search to another page (a brand or category page), redirectUrl gives that page.

### How do I automatically search Alternate products on alternate.de?

Ask an AI agent connected to Reduck to run reduck/alternate.de/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alternate.de/search-products

### Is there a alternate.de API to search Alternate products?

You do not need one. "Search Alternate products" drives the real alternate.de pages in a browser, so it works whether or not alternate.de offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, query, total, products, lastResult, firstResult, redirectUrl.

### Do I need to be logged in to alternate.de?

No. It only uses pages of alternate.de that are reachable without signing in.

### Does it change anything on alternate.de, or only read data?

It only reads. It looks things up on alternate.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/alternate.de/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alternate.de/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/alternate.de/search-products
