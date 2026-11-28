# Search Holland & Barrett products

Automatically search Holland & Barrett products on hollandandbarrett.com. Search products on Holland & Barrett UK (hollandandbarrett.com, the United Kingdom store) by keywords, and get one page of results in the order the site gives for relevance: each product with its Holland & Barrett product id and sku, name, brand, link, image, price and earlier price in pounds (GBP), discount percent, promotion, price per unit, rating and review count, availability, whether a marketplace seller sells it and whether it is a sponsored listing. A page has up to 40 results: pass page for the next ones, and use pageCount to know how many there are. A search with no match, or a page after the last one, gives found false and an empty list.

- Site: hollandandbarrett.com
- Address: `reduck/hollandandbarrett.com/search-products`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hollandandbarrett.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hollandandbarrett.com/search-products
```

## Input

- `query` (string, required): Search words, as typed in the Holland & Barrett search box.
- `page` (integer, optional): The result page, from 1. Holland & Barrett shows up to 40 results on a page.

## Output

- `page` (integer, required)
- `found` (boolean, required): False when the site answered with its no result page.
- `query` (string, required)
- `total` (integer | null, required): The number of products the site gives for the search.
- `pageSize` (integer | null, required)
- `products` (array, required)
- `pageCount` (integer | null, required)
- `searchedQuery` (string | null, required): The words the site searched, after its spelling check.

## FAQ

### What does "Search Holland & Barrett products" do?

Search products on Holland & Barrett UK (hollandandbarrett.com, the United Kingdom store) by keywords, and get one page of results in the order the site gives for relevance: each product with its Holland & Barrett product id and sku, name, brand, link, image, price and earlier price in pounds (GBP), discount percent, promotion, price per unit, rating and review count, availability, whether a marketplace seller sells it and whether it is a sponsored listing. A page has up to 40 results: pass page for the next ones, and use pageCount to know how many there are. A search with no match, or a page after the last one, gives found false and an empty list.

### How do I automatically search Holland & Barrett products on hollandandbarrett.com?

Ask an AI agent connected to Reduck to run reduck/hollandandbarrett.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hollandandbarrett.com/search-products

### Is there a hollandandbarrett.com API to search Holland & Barrett products?

You do not need one. "Search Holland & Barrett products" drives the real hollandandbarrett.com pages in a browser, so it works whether or not hollandandbarrett.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, found, query, total, pageSize, products, pageCount, searchedQuery.

### Do I need to be logged in to hollandandbarrett.com?

No. It only uses pages of hollandandbarrett.com that are reachable without signing in.

### Does it change anything on hollandandbarrett.com, or only read data?

It only reads. It looks things up on hollandandbarrett.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hollandandbarrett.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hollandandbarrett.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hollandandbarrett.com/search-products
