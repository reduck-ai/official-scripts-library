# Search Instacart store products

Automatically search Instacart store products on instacart.com. Search one store on Instacart.com (by its store slug, such as "wegmans" or "costco") for a free-text query, 40 results a page, at the delivery area Instacart has for this browser. Returns the total result count, the store's shop id and the postal code used, and for each product its item id, product id, link, name, brand, size, price in US dollars, regular price when on sale, unit price text, stock level and image. A query with no match, or a page past the last, returns an empty list.

- Site: instacart.com
- Address: `reduck/instacart.com/search-products`
- Updated: 2026-11-26 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instacart.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instacart.com/search-products
```

## Input

- `query` (string, required)
- `store` (string, required): The store's Instacart slug, as in instacart.com/store/<slug> (e.g. "wegmans").
- `page` (integer, optional)

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `store` (string, required)
- `total_results` (integer, required)
- `shop_id` (string | null, optional)
- `postal_code` (string | null, optional)
- `has_next_page` (boolean, optional)

## FAQ

### What does "Search Instacart store products" do?

Search one store on Instacart.com (by its store slug, such as "wegmans" or "costco") for a free-text query, 40 results a page, at the delivery area Instacart has for this browser. Returns the total result count, the store's shop id and the postal code used, and for each product its item id, product id, link, name, brand, size, price in US dollars, regular price when on sale, unit price text, stock level and image. A query with no match, or a page past the last, returns an empty list.

### How do I automatically search Instacart store products on instacart.com?

Ask an AI agent connected to Reduck to run reduck/instacart.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instacart.com/search-products

### Is there a instacart.com API to search Instacart store products?

You do not need one. "Search Instacart store products" drives the real instacart.com pages in a browser, so it works whether or not instacart.com offers an API for this.

### What information do I need to provide?

Required: store, query. Optional: page.

### What does it return?

It returns page, items, query, store, shop_id, postal_code, has_next_page, total_results.

### Do I need to be logged in to instacart.com?

No. It only uses pages of instacart.com that are reachable without signing in.

### Does it change anything on instacart.com, or only read data?

It only reads. It looks things up on instacart.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instacart.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instacart.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/instacart.com/search-products
