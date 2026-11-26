# Search Etsy products

Automatically search Etsy products on etsy.com. Search Etsy (etsy.com) listings by keyword, one results page (about 60 listings, ads included as Etsy shows them) at a time. Returns Etsy's match total, whether a next page exists, and for each listing its id (the productId other Etsy scripts take), title, link, price, original price when on sale, currency, shop and image. Digital downloads are excluded, as Etsy does by default. A query with no match returns an empty list; Etsy often shows near matches instead. A page past the last one returns an empty list.

- Site: etsy.com
- Address: `reduck/etsy.com/search-products`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/etsy.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/etsy.com/search-products
```

## Input

- `query` (string, required): Search keywords, e.g. "ceramic mug".
- `page` (integer, optional): Result page, 1-based. has_next_page says when to stop.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `has_next_page` (boolean, required)
- `total` (integer | null, optional): Etsy's count of matching listings.

## FAQ

### What does "Search Etsy products" do?

Search Etsy (etsy.com) listings by keyword, one results page (about 60 listings, ads included as Etsy shows them) at a time. Returns Etsy's match total, whether a next page exists, and for each listing its id (the productId other Etsy scripts take), title, link, price, original price when on sale, currency, shop and image. Digital downloads are excluded, as Etsy does by default. A query with no match returns an empty list; Etsy often shows near matches instead. A page past the last one returns an empty list.

### How do I automatically search Etsy products on etsy.com?

Ask an AI agent connected to Reduck to run reduck/etsy.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/etsy.com/search-products

### Is there a etsy.com API to search Etsy products?

You do not need one. "Search Etsy products" drives the real etsy.com pages in a browser, so it works whether or not etsy.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, total, has_next_page.

### Do I need to be logged in to etsy.com?

No. It only uses pages of etsy.com that are reachable without signing in.

### Does it change anything on etsy.com, or only read data?

It only reads. It looks things up on etsy.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/etsy.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/etsy.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/etsy.com/search-products
