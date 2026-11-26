# Search B&H products

Automatically search B&H products on bhphotovideo.com. Search B&H Photo Video for products with a keyword, one results page at a time. Returns the total number of results, the page count and, for each product, its B&H item id, name, link, price, price before discount, star rating, review count, image, stock status and B&H and maker part numbers.

- Site: bhphotovideo.com
- Address: `reduck/bhphotovideo.com/search-products`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bhphotovideo.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bhphotovideo.com/search-products
```

## Input

- `query` (string, required): Search keywords, for example "sd card".
- `page` (integer, optional): Results page number, starting at 1.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `has_next_page` (boolean, required)
- `total_pages` (integer | null, optional)
- `redirect_url` (string | null, optional): Set when B&H sends the search to a store or category page instead of a results list; items is then empty.
- `total_results` (integer | null, optional)

## FAQ

### What does "Search B&H products" do?

Search B&H Photo Video for products with a keyword, one results page at a time. Returns the total number of results, the page count and, for each product, its B&H item id, name, link, price, price before discount, star rating, review count, image, stock status and B&H and maker part numbers.

### How do I automatically search B&H products on bhphotovideo.com?

Ask an AI agent connected to Reduck to run reduck/bhphotovideo.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bhphotovideo.com/search-products

### Is there a bhphotovideo.com API to search B&H products?

You do not need one. "Search B&H products" drives the real bhphotovideo.com pages in a browser, so it works whether or not bhphotovideo.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, total_pages, redirect_url, has_next_page, total_results.

### Do I need to be logged in to bhphotovideo.com?

No. It only uses pages of bhphotovideo.com that are reachable without signing in.

### Does it change anything on bhphotovideo.com, or only read data?

It only reads. It looks things up on bhphotovideo.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bhphotovideo.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bhphotovideo.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/bhphotovideo.com/search-products
