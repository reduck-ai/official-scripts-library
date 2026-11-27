# Search HP products

Automatically search HP products on hp.com. Search the HP US store (hp.com/us-en/shop) by free-text query and return one page of results (24 per page): query, page, sort, total_count, page_count, has_next_page and items (product_id, which is the HP part number, name, url, price after instant savings, list_price, currency, image_url, rating, review_count, stock_status, product_class, category). Sort by relevance, price_low, price_high, newest or top_rated. A query with no match returns an empty list. A page past page_count returns an empty list. Prices are in US dollars, as HP shows them to a guest.

- Site: hp.com
- Address: `reduck/hp.com/search-products`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hp.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hp.com/search-products
```

## Input

- `query` (string, required): Free-text search, for example "laptop" or "OmniBook 5".
- `page` (integer, optional): Results page, 24 items per page. Stop when has_next_page is false.
- `sort` (string, optional): Sort order. Omit for HP's default order (relevance).

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `has_next_page` (boolean, required)
- `url` (string, optional): The HP search page of the query.
- `sort` (string | null, optional)
- `page_count` (integer | null, optional)
- `total_count` (integer | null, optional): Number of products HP finds for the query.

## FAQ

### What does "Search HP products" do?

Search the HP US store (hp.com/us-en/shop) by free-text query and return one page of results (24 per page): query, page, sort, total_count, page_count, has_next_page and items (product_id, which is the HP part number, name, url, price after instant savings, list_price, currency, image_url, rating, review_count, stock_status, product_class, category). Sort by relevance, price_low, price_high, newest or top_rated. A query with no match returns an empty list. A page past page_count returns an empty list. Prices are in US dollars, as HP shows them to a guest.

### How do I automatically search HP products on hp.com?

Ask an AI agent connected to Reduck to run reduck/hp.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hp.com/search-products

### Is there a hp.com API to search HP products?

You do not need one. "Search HP products" drives the real hp.com pages in a browser, so it works whether or not hp.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort.

### What does it return?

It returns url, page, sort, items, query, page_count, total_count, has_next_page.

### Do I need to be logged in to hp.com?

No. It only uses pages of hp.com that are reachable without signing in.

### Does it change anything on hp.com, or only read data?

It only reads. It looks things up on hp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hp.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hp.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hp.com/search-products
