# Search Sam's Club products

Automatically search Sam's Club products on samsclub.com. Search Sam's Club (samsclub.com, US) by free text and return one page of results, as the search page lists them: for each product its item id, offer id, name, link, image, price, previous price, unit price, rating, review count, availability, whether it has options (size, color) and whether it is sponsored, plus the result count Sam's Club gives, the last page and the corrected query. Carousels of suggestions under the results are not included. Sam's Club answers most queries with its nearest products, also a query that matches nothing exactly. Pages past the last page hold only sponsored products: stop at maxPage. Prices and availability are for the club and address Sam's Club gives to the browser. No account is needed.

- Site: samsclub.com
- Address: `reduck/samsclub.com/search-products`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/samsclub.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/samsclub.com/search-products
```

## Input

- `query` (string, required): Free text to search for, for example "paper towels".
- `page` (integer, optional): Result page, from 1. maxPage in the result is the last page.
- `sort` (string, optional): Order of the results, as the search page offers it.

## Output

- `url` (string, required): The search page that was read.
- `page` (integer, required)
- `sort` (string, required)
- `items` (array, required)
- `query` (string, required)
- `total` (integer | null, required): Number of results Sam's Club gives for the query.
- `maxPage` (integer | null, required): Last result page.
- `correctedQuery` (string | null, required): The query Sam's Club searched instead, when it corrected the spelling.

## FAQ

### What does "Search Sam's Club products" do?

Search Sam's Club (samsclub.com, US) by free text and return one page of results, as the search page lists them: for each product its item id, offer id, name, link, image, price, previous price, unit price, rating, review count, availability, whether it has options (size, color) and whether it is sponsored, plus the result count Sam's Club gives, the last page and the corrected query. Carousels of suggestions under the results are not included. Sam's Club answers most queries with its nearest products, also a query that matches nothing exactly. Pages past the last page hold only sponsored products: stop at maxPage. Prices and availability are for the club and address Sam's Club gives to the browser. No account is needed.

### How do I automatically search Sam's Club products on samsclub.com?

Ask an AI agent connected to Reduck to run reduck/samsclub.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/samsclub.com/search-products

### Is there a samsclub.com API to search Sam's Club products?

You do not need one. "Search Sam's Club products" drives the real samsclub.com pages in a browser, so it works whether or not samsclub.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort.

### What does it return?

It returns url, page, sort, items, query, total, maxPage, correctedQuery.

### Do I need to be logged in to samsclub.com?

No. It only uses pages of samsclub.com that are reachable without signing in.

### Does it change anything on samsclub.com, or only read data?

It only reads. It looks things up on samsclub.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/samsclub.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/samsclub.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/samsclub.com/search-products
