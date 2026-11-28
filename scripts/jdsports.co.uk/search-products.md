# Search JD Sports products

Automatically search JD Sports products on jdsports.co.uk. Search products on JD Sports UK (jdsports.co.uk, the United Kingdom store) by keywords, and get one page of results in the order the site recommends: each product with its JD Sports product id, name, brand, colour, link, image, price and currency (pounds, GBP), whether it is on sale and its discount percent, whether it is in stock, its sizes and its badge. A page has up to 72 results: pass page for the next ones, and use pageCount to know how many there are. A search with no match, or a page after the last one, gives an empty list. When the site opens a brand or category page for the words, redirectUrl gives that page.

- Site: jdsports.co.uk
- Address: `reduck/jdsports.co.uk/search-products`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/jdsports.co.uk/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/jdsports.co.uk/search-products
```

## Input

- `query` (string, required): Search words, as typed in the JD Sports search box.
- `page` (integer, optional): The result page, from 1. JD Sports shows up to 72 results on a page.

## Output

- `page` (integer, required)
- `query` (string, required)
- `total` (integer | null, required): The number of results the site gives for the search.
- `pageSize` (integer | null, required)
- `products` (array, required)
- `pageCount` (integer | null, required)
- `redirectUrl` (string | null, required): The page the site opened instead of a search, when it sent the words to a brand or category page.

## FAQ

### What does "Search JD Sports products" do?

Search products on JD Sports UK (jdsports.co.uk, the United Kingdom store) by keywords, and get one page of results in the order the site recommends: each product with its JD Sports product id, name, brand, colour, link, image, price and currency (pounds, GBP), whether it is on sale and its discount percent, whether it is in stock, its sizes and its badge. A page has up to 72 results: pass page for the next ones, and use pageCount to know how many there are. A search with no match, or a page after the last one, gives an empty list. When the site opens a brand or category page for the words, redirectUrl gives that page.

### How do I automatically search JD Sports products on jdsports.co.uk?

Ask an AI agent connected to Reduck to run reduck/jdsports.co.uk/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/jdsports.co.uk/search-products

### Is there a jdsports.co.uk API to search JD Sports products?

You do not need one. "Search JD Sports products" drives the real jdsports.co.uk pages in a browser, so it works whether or not jdsports.co.uk offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, query, total, pageSize, products, pageCount, redirectUrl.

### Do I need to be logged in to jdsports.co.uk?

No. It only uses pages of jdsports.co.uk that are reachable without signing in.

### Does it change anything on jdsports.co.uk, or only read data?

It only reads. It looks things up on jdsports.co.uk and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/jdsports.co.uk/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/jdsports.co.uk/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/jdsports.co.uk/search-products
