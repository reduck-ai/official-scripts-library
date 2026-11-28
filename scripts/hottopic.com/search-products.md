# Search Hot Topic products

Automatically search Hot Topic products on hottopic.com. Search Hot Topic (hottopic.com, US) products by keywords, 20 a page: id, name, link, price shown and price before the discount in US dollars, whether the price is a starting price, promotion labels and image of each, plus the total count and the number of pages. A search with no match gives an empty list and a zero total, and a page past the last one gives an empty list. When Hot Topic sends the keywords to another page instead of results, redirected_to gives that page.

- Site: hottopic.com
- Address: `reduck/hottopic.com/search-products`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hottopic.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hottopic.com/search-products
```

## Input

- `query` (string, required): Keywords, for example "band tee".
- `page` (integer, optional): Results page, 20 products a page.

## Output

- `page` (integer, required)
- `pages` (integer | null, required): Number of result pages.
- `query` (string, required)
- `total` (integer | null, required): Number of products that match, on all pages.
- `products` (array, required)
- `redirected_to` (string | null, required): The page Hot Topic sent these keywords to, when it is not a search results page.

## FAQ

### What does "Search Hot Topic products" do?

Search Hot Topic (hottopic.com, US) products by keywords, 20 a page: id, name, link, price shown and price before the discount in US dollars, whether the price is a starting price, promotion labels and image of each, plus the total count and the number of pages. A search with no match gives an empty list and a zero total, and a page past the last one gives an empty list. When Hot Topic sends the keywords to another page instead of results, redirected_to gives that page.

### How do I automatically search Hot Topic products on hottopic.com?

Ask an AI agent connected to Reduck to run reduck/hottopic.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hottopic.com/search-products

### Is there a hottopic.com API to search Hot Topic products?

You do not need one. "Search Hot Topic products" drives the real hottopic.com pages in a browser, so it works whether or not hottopic.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, pages, query, total, products, redirected_to.

### Do I need to be logged in to hottopic.com?

No. It only uses pages of hottopic.com that are reachable without signing in.

### Does it change anything on hottopic.com, or only read data?

It only reads. It looks things up on hottopic.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hottopic.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hottopic.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hottopic.com/search-products
