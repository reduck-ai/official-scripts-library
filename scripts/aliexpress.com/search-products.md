# Search AliExpress products

Automatically search AliExpress products on aliexpress.com. Search AliExpress by free-text query, one page of about 60 results at a time. Returns the total result count, the result type AliExpress gives (normal_result, few_result or zero_result), has_next_page, then for each product its id, title, link, price and struck-through original price with currency, discount, rating, sold-count text, image and whether it is sponsored. When nothing matches, AliExpress shows unrelated top-selling products with result_type few_result; a page past the last one gives an empty list. Prices are in the currency AliExpress picks for the browser. Pass an id or link to Get AliExpress product or Add AliExpress product to cart.

- Site: aliexpress.com
- Address: `reduck/aliexpress.com/search-products`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/aliexpress.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/aliexpress.com/search-products
```

## Input

- `query` (string, required): Free-text search, e.g. "usb cable".
- `page` (integer, optional): Results page, from 1. AliExpress shows at most 60 pages.

## Output

- `url` (string, required)
- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `result_type` (string | null, required): AliExpress's own result type: normal_result, few_result (few or no matches: AliExpress fills the page with other top-selling products) or zero_result.
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required)
- `currency` (string | null, optional)

## FAQ

### What does "Search AliExpress products" do?

Search AliExpress by free-text query, one page of about 60 results at a time. Returns the total result count, the result type AliExpress gives (normal_result, few_result or zero_result), has_next_page, then for each product its id, title, link, price and struck-through original price with currency, discount, rating, sold-count text, image and whether it is sponsored. When nothing matches, AliExpress shows unrelated top-selling products with result_type few_result; a page past the last one gives an empty list. Prices are in the currency AliExpress picks for the browser. Pass an id or link to Get AliExpress product or Add AliExpress product to cart.

### How do I automatically search AliExpress products on aliexpress.com?

Ask an AI agent connected to Reduck to run reduck/aliexpress.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/aliexpress.com/search-products

### Is there a aliexpress.com API to search AliExpress products?

You do not need one. "Search AliExpress products" drives the real aliexpress.com pages in a browser, so it works whether or not aliexpress.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns url, page, items, query, currency, result_type, has_next_page, total_results.

### Do I need to be logged in to aliexpress.com?

No. It only uses pages of aliexpress.com that are reachable without signing in.

### Does it change anything on aliexpress.com, or only read data?

It only reads. It looks things up on aliexpress.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/aliexpress.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/aliexpress.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/aliexpress.com/search-products
