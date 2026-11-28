# Search J.Crew products

Automatically search J.Crew products on jcrew.com. Search J.Crew (jcrew.com, US) products by keywords, 60 a page: code, name, link, list price, lowest and highest sale price of its colors in US dollars, largest discount in percent, fit, badge, rating, review count and colors of each, plus the total count and the number of pages. A search with no match gives an empty list and a zero total, and a page past the last one gives an empty list. When J.Crew sends the keywords to another page instead of search results, redirected_to gives that page.

- Site: jcrew.com
- Address: `reduck/jcrew.com/search-products`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/jcrew.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/jcrew.com/search-products
```

## Input

- `query` (string, required): Keywords, for example "oxford shirt".
- `page` (integer, optional): Results page, 60 products a page.

## Output

- `page` (integer, required)
- `pages` (integer | null, required): Number of result pages.
- `query` (string, required)
- `total` (integer | null, required): Number of products that match, on all pages.
- `products` (array, required)
- `redirected_to` (string | null, required): The page J.Crew sent these keywords to, when it is not a search results page.

## FAQ

### What does "Search J.Crew products" do?

Search J.Crew (jcrew.com, US) products by keywords, 60 a page: code, name, link, list price, lowest and highest sale price of its colors in US dollars, largest discount in percent, fit, badge, rating, review count and colors of each, plus the total count and the number of pages. A search with no match gives an empty list and a zero total, and a page past the last one gives an empty list. When J.Crew sends the keywords to another page instead of search results, redirected_to gives that page.

### How do I automatically search J.Crew products on jcrew.com?

Ask an AI agent connected to Reduck to run reduck/jcrew.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/jcrew.com/search-products

### Is there a jcrew.com API to search J.Crew products?

You do not need one. "Search J.Crew products" drives the real jcrew.com pages in a browser, so it works whether or not jcrew.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, pages, query, total, products, redirected_to.

### Do I need to be logged in to jcrew.com?

No. It only uses pages of jcrew.com that are reachable without signing in.

### Does it change anything on jcrew.com, or only read data?

It only reads. It looks things up on jcrew.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/jcrew.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/jcrew.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/jcrew.com/search-products
