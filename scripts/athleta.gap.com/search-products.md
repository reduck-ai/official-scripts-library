# Search Athleta products

Automatically search Athleta products on athleta.gap.com. Search the Athleta US store (athleta.gap.com) by free text, with the sort orders and filters of the site. Returns one page of up to 200 products as the site lists them: the product id, the id and link of the first color, the name, the sale and regular price range in US dollars, the rating, the review count, the number of colors, the image, the badges and offers shown on the card, and up to 5 colors with their own id, price and image. Also returns the total number of results, the page count, whether a next page exists, and the filters the site offers for this search (department, size, color, fit and more), each value with its result count. A search with no match, or a page past the last one, returns an empty list. When Athleta sends a search term to another page (for example a help page), the list is empty and redirectUrl gives that page. Pass a productId or url to Get Athleta product to see the sizes.

- Site: athleta.gap.com
- Address: `reduck/athleta.gap.com/search-products`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/athleta.gap.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/athleta.gap.com/search-products
```

## Input

- `query` (string, required): Free text to search for, for example "high rise leggings".
- `page` (integer, optional): Page of results, up to 200 products a page, starting at 1. Stop when hasNextPage is false.
- `sort` (string, optional): Sort order of the site: featured, newest first, price low to high, price high to low.
- `filters` (array, optional): Filters to apply. Each one is a filter name and one or more of its values, taken from the filters of an earlier search, for example {"name":"department","values":["Women"]}. Several values of one filter match any of them.
- `priceMax` (number | null, optional): Highest price in US dollars. Give it with priceMin.
- `priceMin` (number | null, optional): Lowest price in US dollars. Give it with priceMax.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `filters` (array, required)
- `totalPages` (integer | null, required)
- `hasNextPage` (boolean, required)
- `redirectUrl` (string | null, required)
- `totalResults` (integer | null, required)

## FAQ

### What does "Search Athleta products" do?

Search the Athleta US store (athleta.gap.com) by free text, with the sort orders and filters of the site. Returns one page of up to 200 products as the site lists them: the product id, the id and link of the first color, the name, the sale and regular price range in US dollars, the rating, the review count, the number of colors, the image, the badges and offers shown on the card, and up to 5 colors with their own id, price and image. Also returns the total number of results, the page count, whether a next page exists, and the filters the site offers for this search (department, size, color, fit and more), each value with its result count. A search with no match, or a page past the last one, returns an empty list. When Athleta sends a search term to another page (for example a help page), the list is empty and redirectUrl gives that page. Pass a productId or url to Get Athleta product to see the sizes.

### How do I automatically search Athleta products on athleta.gap.com?

Ask an AI agent connected to Reduck to run reduck/athleta.gap.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/athleta.gap.com/search-products

### Is there a athleta.gap.com API to search Athleta products?

You do not need one. "Search Athleta products" drives the real athleta.gap.com pages in a browser, so it works whether or not athleta.gap.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, filters, priceMax, priceMin.

### What does it return?

It returns page, items, query, filters, totalPages, hasNextPage, redirectUrl, totalResults.

### Do I need to be logged in to athleta.gap.com?

No. It only uses pages of athleta.gap.com that are reachable without signing in.

### Does it change anything on athleta.gap.com, or only read data?

It only reads. It looks things up on athleta.gap.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/athleta.gap.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/athleta.gap.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/athleta.gap.com/search-products
