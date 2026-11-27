# Search Nike products

Automatically search Nike products on nike.com. Search Nike.com (US, prices in USD) by free-text query, 24 products per page: style-color id, title, subtitle, link, price, list price, color, type, badge and image, plus the total result and page counts. A page past the last returns an empty list.

- Site: nike.com
- Address: `reduck/nike.com/search-products`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/nike.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/nike.com/search-products
```

## Input

- `query` (string, required)
- `page` (integer, optional)

## FAQ

### What does "Search Nike products" do?

Search Nike.com (US, prices in USD) by free-text query, 24 products per page: style-color id, title, subtitle, link, price, list price, color, type, badge and image, plus the total result and page counts. A page past the last returns an empty list.

### How do I automatically search Nike products on nike.com?

Ask an AI agent connected to Reduck to run reduck/nike.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nike.com/search-products

### Is there a nike.com API to search Nike products?

You do not need one. "Search Nike products" drives the real nike.com pages in a browser, so it works whether or not nike.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### Do I need to be logged in to nike.com?

No. It only uses pages of nike.com that are reachable without signing in.

### Does it change anything on nike.com, or only read data?

It only reads. It looks things up on nike.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/nike.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nike.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/nike.com/search-products
