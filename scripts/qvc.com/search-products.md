# Search QVC products

Automatically search QVC products on qvc.com. Search QVC products by keyword, one results page at a time: id, name, link, price, QVC reference price, rating, image, brand and availability.

- Site: qvc.com
- Address: `reduck/qvc.com/search-products`
- Updated: 2026-11-26 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/qvc.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/qvc.com/search-products
```

## Input

- `query` (string, required): Search keywords, as typed in the QVC search box.
- `page` (integer, optional): Results page, from 1.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `total_pages` (integer | null, required)
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required)

## FAQ

### What does "Search QVC products" do?

Search QVC products by keyword, one results page at a time: id, name, link, price, QVC reference price, rating, image, brand and availability.

### How do I automatically search QVC products on qvc.com?

Ask an AI agent connected to Reduck to run reduck/qvc.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/qvc.com/search-products

### Is there a qvc.com API to search QVC products?

You do not need one. "Search QVC products" drives the real qvc.com pages in a browser, so it works whether or not qvc.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, total_pages, has_next_page, total_results.

### Do I need to be logged in to qvc.com?

No. It only uses pages of qvc.com that are reachable without signing in.

### Does it change anything on qvc.com, or only read data?

It only reads. It looks things up on qvc.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/qvc.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/qvc.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/qvc.com/search-products
