# Vinted — search item listings

Automatically search item listings on vinted.com. Search Vinted listings by keyword and return one page of results with each item's title, brand, size, condition, price, total price with Buyer Protection, favourite count, photo and link. Supports sorting, a price range and paging.

- Site: vinted.com
- Address: `reduck/vinted.com/search_items`
- Updated: 2026-09-25 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/vinted.com/search_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/vinted.com/search_items
```

## Input

- `query` (string, required): Free-text search, e.g. "levis 501" or "nike air max".
- `page` (integer, optional): Result page, 96 items per page. Pages are near-disjoint but not a frozen snapshot: newly listed items shift the window, so consecutive pages fetched minutes apart can repeat a couple of items.
- `order` (string, optional): Sort order. Omit for the site default (relevance).
- `price_to` (number, optional): Maximum item price, in the currency the run's session resolves to.
- `price_from` (number, optional): Minimum item price, in the currency the run's session resolves to.

## Output

- `page` (integer, required)
- `items` (array, required)
- `search_url` (string, required)

## FAQ

### What does "Vinted — search item listings" do?

Search Vinted listings by keyword and return one page of results with each item's title, brand, size, condition, price, total price with Buyer Protection, favourite count, photo and link. Supports sorting, a price range and paging.

### How do I automatically search item listings on vinted.com?

Ask an AI agent connected to Reduck to run reduck/vinted.com/search_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/vinted.com/search_items

### Is there a vinted.com API to search item listings?

You do not need one. "Vinted — search item listings" drives the real vinted.com pages in a browser, so it works whether or not vinted.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, order, price_to, price_from.

### What does it return?

It returns page, items, search_url.

### Do I need to be logged in to vinted.com?

No. It only uses pages of vinted.com that are reachable without signing in.

### Does it change anything on vinted.com, or only read data?

It only reads. It looks things up on vinted.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/vinted.com/search_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/vinted.com/search_items

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/vinted.com/search_items
