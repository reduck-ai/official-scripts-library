# Search Amazon products

Automatically search Amazon products on amazon.com. Search Amazon by free-text query and return one page of results. Returns query, page, zip, url, and items (asin, title, url, price, list_price, rating, review_count, image_url, sponsored). Organic results are stable per page but sponsored slots rotate between fetches; pagination caps around 20 pages.

- Site: amazon.com
- Address: `reduck/amazon.com/search-products`
- Updated: 2026-08-17 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.com/search-products
```

## Input

- `query` (string, required): Free-text search query.
- `page` (integer, optional): Result page (Amazon serves ~16-22 organic results per page; pagination caps around 20 pages). Pagination is deterministic per session — same page re-fetched returns the same set; sponsored slots may rotate.
- `zipCode` (string, optional): US ZIP used to pin the store location (prices, availability).

## Output

- `url` (string, required)
- `zip` (string, required)
- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)

## FAQ

### What does "Search Amazon products" do?

Search Amazon by free-text query and return one page of results. Returns query, page, zip, url, and items (asin, title, url, price, list_price, rating, review_count, image_url, sponsored). Organic results are stable per page but sponsored slots rotate between fetches; pagination caps around 20 pages.

### How do I automatically search Amazon products on amazon.com?

Ask an AI agent connected to Reduck to run reduck/amazon.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com/search-products

### Is there a amazon.com API to search Amazon products?

You do not need one. "Search Amazon products" drives the real amazon.com pages in a browser, so it works whether or not amazon.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, zipCode.

### What does it return?

It returns url, zip, page, items, query.

### Do I need to be logged in to amazon.com?

No. It only uses pages of amazon.com that are reachable without signing in.

### Does it change anything on amazon.com, or only read data?

It only reads. It looks things up on amazon.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com/search-products

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/amazon.com/search-products
