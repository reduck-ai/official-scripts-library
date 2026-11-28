# Search Bershka products

Automatically search Bershka products on bershka.com. Search the products of the Bershka France store (bershka.com/fr) by words. Gives 32 products for each page, in the order of the site: the product id, name and link, and each colour with its price and old price in euros and its sizes with their offerId, length and stock state. It also gives the number of results in total and in the woman and man sections. Use nextPage to get the next page; the script gives the first 224 results, in 7 pages. A search with no result gives an empty list and a total of 0.

- Site: bershka.com
- Address: `reduck/bershka.com/search-products`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bershka.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bershka.com/search-products
```

## Input

- `query` (string, required): Words to search for, as typed in the search box of the site.
- `page` (integer, optional): Page of 32 results, 1 to 7 (the first 224 results). Use nextPage of the previous page.

## Output

- `page` (integer, required)
- `query` (string, required)
- `total` (integer | null, required): Number of results the site gives for the search.
- `currency` (string, required): Currency of the prices, as an ISO code (euro).
- `manItems` (integer | null, required): Number of results in the man section.
- `nextPage` (integer | null, required): Page to ask for next, or null when this page is the last one the script can give.
- `products` (array, required): Results in the order of the site, 32 per page.
- `womanItems` (integer | null, required): Number of results in the woman section.

## FAQ

### What does "Search Bershka products" do?

Search the products of the Bershka France store (bershka.com/fr) by words. Gives 32 products for each page, in the order of the site: the product id, name and link, and each colour with its price and old price in euros and its sizes with their offerId, length and stock state. It also gives the number of results in total and in the woman and man sections. Use nextPage to get the next page; the script gives the first 224 results, in 7 pages. A search with no result gives an empty list and a total of 0.

### How do I automatically search Bershka products on bershka.com?

Ask an AI agent connected to Reduck to run reduck/bershka.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bershka.com/search-products

### Is there a bershka.com API to search Bershka products?

You do not need one. "Search Bershka products" drives the real bershka.com pages in a browser, so it works whether or not bershka.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, query, total, currency, manItems, nextPage, products, womanItems.

### Do I need to be logged in to bershka.com?

No. It only uses pages of bershka.com that are reachable without signing in.

### Does it change anything on bershka.com, or only read data?

It only reads. It looks things up on bershka.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bershka.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bershka.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/bershka.com/search-products
