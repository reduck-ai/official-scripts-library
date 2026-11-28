# Search Samsung products

Automatically search Samsung products on samsung.com. Search products on the Samsung US store (samsung.com/us), 15 results a page. Returns each result with its model code (SKU), name, link, sale and regular price in US dollars, stock status, rating, review count, category, badge, image and the model codes of the other configurations on its card, plus the result tabs (product, accessory, other) with their counts, the total and whether a next page exists. Pass tab to read another tab and page to go to the next page. Samsung's search is semantic: a query with no close match can still return popular products, and showingResultsFor gives the words Samsung searched for. A page after the last one returns an empty list.

- Site: samsung.com
- Address: `reduck/samsung.com/search-products`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/samsung.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/samsung.com/search-products
```

## Input

- `query` (string, required): Search words, as typed in the Samsung US search box, e.g. "galaxy buds" or "monitor".
- `tab` (string, optional): Result tab to read, as listed in tabs of an earlier search (for example "product" or "accessory"). Omit to get the tab Samsung opens first.
- `page` (integer, optional): Results page, 15 results a page. hasMore says if a next page exists.

## Output

- `page` (integer, required)
- `tabs` (array, required)
- `items` (array, required)
- `query` (string, required)
- `total` (integer | null, required): Number of results in the tab shown, as Samsung counts them.
- `hasMore` (boolean, required): True when a next page of results exists.
- `resultType` (string | null, required): The tab Samsung shows, for example Product or Accessory.
- `redirectUrl` (string | null, optional): The page Samsung sends this query to instead of a result list, if any.
- `searchState` (string | null, optional): The search state Samsung gives for this query, as the site writes it.
- `showingResultsFor` (string | null, optional): The words Samsung searched for, which can differ from the query when Samsung corrected it.

## FAQ

### What does "Search Samsung products" do?

Search products on the Samsung US store (samsung.com/us), 15 results a page. Returns each result with its model code (SKU), name, link, sale and regular price in US dollars, stock status, rating, review count, category, badge, image and the model codes of the other configurations on its card, plus the result tabs (product, accessory, other) with their counts, the total and whether a next page exists. Pass tab to read another tab and page to go to the next page. Samsung's search is semantic: a query with no close match can still return popular products, and showingResultsFor gives the words Samsung searched for. A page after the last one returns an empty list.

### How do I automatically search Samsung products on samsung.com?

Ask an AI agent connected to Reduck to run reduck/samsung.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/samsung.com/search-products

### Is there a samsung.com API to search Samsung products?

You do not need one. "Search Samsung products" drives the real samsung.com pages in a browser, so it works whether or not samsung.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: tab, page.

### What does it return?

It returns page, tabs, items, query, total, hasMore, resultType, redirectUrl, searchState, showingResultsFor.

### Do I need to be logged in to samsung.com?

No. It only uses pages of samsung.com that are reachable without signing in.

### Does it change anything on samsung.com, or only read data?

It only reads. It looks things up on samsung.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/samsung.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/samsung.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/samsung.com/search-products
