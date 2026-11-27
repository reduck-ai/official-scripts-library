# Search Micro Center products

Automatically search Micro Center products on microcenter.com. Search Micro Center (microcenter.com) by free-text query and return one page of results (24 per page) at one store: query, page, sort, the store the prices are for, total_count, page_count, has_next_page and items (product_id, sku, name, brand, url, price, original_price when a saving is shown, currency, category, availability text, image_url). Sort by relevance, price_low, price_high, top_rated, most_reviewed or newest. Prices and stock depend on the store: pass store_id (three digits from the site's store picker, for example 081 for Fairfax, VA) or omit it for the web store 029 (shippable items) that Micro Center sets for a new guest; a store lists the items in stock there. Micro Center answers a query it does not match with a list of other products, not with an empty list. A page past page_count returns an empty list.

- Site: microcenter.com
- Address: `reduck/microcenter.com/search-products`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/microcenter.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/microcenter.com/search-products
```

## Input

- `query` (string, required): Free-text search, for example "ssd" or "RTX 5070".
- `page` (integer, optional): Results page, 24 items per page. Stop when has_next_page is false.
- `sort` (string, optional): Sort order. Omit for Micro Center's closest match order.
- `store_id` (string, optional): Micro Center store whose prices and stock to show, as three digits from the site's store picker, for example 081 (Fairfax, VA) or 029 (the web store, shippable items). Omit for the store Micro Center sets for a new guest, which is the web store 029.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `has_next_page` (boolean, required)
- `url` (string, optional)
- `sort` (string | null, optional)
- `store_id` (string | null, optional): The store whose prices and stock the results show.
- `page_count` (integer | null, optional)
- `store_name` (string | null, optional)
- `total_count` (integer | null, optional)

## FAQ

### What does "Search Micro Center products" do?

Search Micro Center (microcenter.com) by free-text query and return one page of results (24 per page) at one store: query, page, sort, the store the prices are for, total_count, page_count, has_next_page and items (product_id, sku, name, brand, url, price, original_price when a saving is shown, currency, category, availability text, image_url). Sort by relevance, price_low, price_high, top_rated, most_reviewed or newest. Prices and stock depend on the store: pass store_id (three digits from the site's store picker, for example 081 for Fairfax, VA) or omit it for the web store 029 (shippable items) that Micro Center sets for a new guest; a store lists the items in stock there. Micro Center answers a query it does not match with a list of other products, not with an empty list. A page past page_count returns an empty list.

### How do I automatically search Micro Center products on microcenter.com?

Ask an AI agent connected to Reduck to run reduck/microcenter.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/microcenter.com/search-products

### Is there a microcenter.com API to search Micro Center products?

You do not need one. "Search Micro Center products" drives the real microcenter.com pages in a browser, so it works whether or not microcenter.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, store_id.

### What does it return?

It returns url, page, sort, items, query, store_id, page_count, store_name, total_count, has_next_page.

### Do I need to be logged in to microcenter.com?

No. It only uses pages of microcenter.com that are reachable without signing in.

### Does it change anything on microcenter.com, or only read data?

It only reads. It looks things up on microcenter.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/microcenter.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/microcenter.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/microcenter.com/search-products
