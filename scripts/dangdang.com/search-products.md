# Search Dangdang products

Automatically search Dangdang products on dangdang.com. Search the Dangdang Chinese store (dangdang.com), books, home, fashion, electronics and more, by free text (Chinese words work best) and return one page of results in the site's own order, 60 a page, up to page 100: the total result count, has_next_page, and for each product its product id, name, link, price and list price in yuan, review count, seller (Dangdang itself or a marketplace shop, with its shop id), book details when the site shows them, the promotion line and image. Stop paging when has_next_page is false; a page past the last one returns an empty list. A search with no match returns an empty list, not the products the site suggests instead. Use a managed browser in China (country CN). Pass a product id to Get Dangdang product.

- Site: dangdang.com
- Address: `reduck/dangdang.com/search-products`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dangdang.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dangdang.com/search-products
```

## Input

- `query` (string, required): Free-text search, for example "手机" or "耳机".
- `page` (integer, optional): Result page, 60 products a page, 100 pages at most. Stop when has_next_page is false.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required)

## FAQ

### What does "Search Dangdang products" do?

Search the Dangdang Chinese store (dangdang.com), books, home, fashion, electronics and more, by free text (Chinese words work best) and return one page of results in the site's own order, 60 a page, up to page 100: the total result count, has_next_page, and for each product its product id, name, link, price and list price in yuan, review count, seller (Dangdang itself or a marketplace shop, with its shop id), book details when the site shows them, the promotion line and image. Stop paging when has_next_page is false; a page past the last one returns an empty list. A search with no match returns an empty list, not the products the site suggests instead. Use a managed browser in China (country CN). Pass a product id to Get Dangdang product.

### How do I automatically search Dangdang products on dangdang.com?

Ask an AI agent connected to Reduck to run reduck/dangdang.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dangdang.com/search-products

### Is there a dangdang.com API to search Dangdang products?

You do not need one. "Search Dangdang products" drives the real dangdang.com pages in a browser, so it works whether or not dangdang.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, has_next_page, total_results.

### Do I need to be logged in to dangdang.com?

No. It only uses pages of dangdang.com that are reachable without signing in.

### Does it change anything on dangdang.com, or only read data?

It only reads. It looks things up on dangdang.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dangdang.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dangdang.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/dangdang.com/search-products
