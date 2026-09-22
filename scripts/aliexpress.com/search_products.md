# Search AliExpress products

Automatically search AliExpress products on aliexpress.com. Search AliExpress products by keyword and page. Returns each result's item id, title, price, rating, sold-count text, product image and url. The item id pairs with aliexpress.com/get_product, and is resolved for bundle-deal results too, which link through a different url shape. Scrolls the results so every card's image loads, and reports an image as absent rather than returning a placeholder. Anonymous, read-only. Prices and the sold-count text appear in whatever currency and locale AliExpress resolves the session to. Fails with a clear message rather than returning an empty list, since AliExpress returns results even for nonsense queries.

- Site: aliexpress.com
- Address: `reduck/aliexpress.com/search_products`
- Updated: 2026-09-18 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/aliexpress.com/search_products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/aliexpress.com/search_products
```

## Input

- `query` (string, required): Search keywords, e.g. "phone case".
- `page` (integer, optional): Results page number.

## Output

- `url` (string, required)
- `page` (integer, required)
- `query` (string, required)
- `products` (array, required)

## FAQ

### What does "Search AliExpress products" do?

Search AliExpress products by keyword and page. Returns each result's item id, title, price, rating, sold-count text, product image and url. The item id pairs with aliexpress.com/get_product, and is resolved for bundle-deal results too, which link through a different url shape. Scrolls the results so every card's image loads, and reports an image as absent rather than returning a placeholder. Anonymous, read-only. Prices and the sold-count text appear in whatever currency and locale AliExpress resolves the session to. Fails with a clear message rather than returning an empty list, since AliExpress returns results even for nonsense queries.

### How do I automatically search AliExpress products on aliexpress.com?

Ask an AI agent connected to Reduck to run reduck/aliexpress.com/search_products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/aliexpress.com/search_products

### Is there a aliexpress.com API to search AliExpress products?

You do not need one. "Search AliExpress products" drives the real aliexpress.com pages in a browser, so it works whether or not aliexpress.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns url, page, query, products.

### Do I need to be logged in to aliexpress.com?

No. It only uses pages of aliexpress.com that are reachable without signing in.

### Does it change anything on aliexpress.com, or only read data?

It only reads. It looks things up on aliexpress.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/aliexpress.com/search_products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/aliexpress.com/search_products

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/aliexpress.com/search_products
