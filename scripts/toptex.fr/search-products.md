# Search TopTex products

Automatically search TopTex products on toptex.fr. Search toptex.fr for products by free-text query. Returns one page of products (reference, name, brand, color, from-price, image, PDP url); page is 0-based. Catalogue prices are public, so no login is required.

- Site: toptex.fr
- Address: `reduck/toptex.fr/search-products`
- Updated: 2026-07-20 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/toptex.fr/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/toptex.fr/search-products
```

## Input

- `query` (string, required): Free-text query (product name, brand, or reference, e.g. "t-shirt bio", "IB297").
- `page` (integer, optional): 0-based result page (Algolia pagination; deterministic — same page re-fetched returns the same set).
- `hitsPerPage` (integer, optional): Products per page (site default 24).

## Output

- `page` (integer, required)
- `query` (string, required)
- `nbHits` (integer, required): Total matching products across all pages.
- `nbPages` (integer, required)
- `products` (array, required)
- `hitsPerPage` (integer, required)

## FAQ

### What does "Search TopTex products" do?

Search toptex.fr for products by free-text query. Returns one page of products (reference, name, brand, color, from-price, image, PDP url); page is 0-based. Catalogue prices are public, so no login is required.

### How do I automatically search TopTex products on toptex.fr?

Ask an AI agent connected to Reduck to run reduck/toptex.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/toptex.fr/search-products

### Is there a toptex.fr API to search TopTex products?

You do not need one. "Search TopTex products" drives the real toptex.fr pages in a browser, so it works whether or not toptex.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, hitsPerPage.

### What does it return?

It returns page, query, nbHits, nbPages, products, hitsPerPage.

### Do I need to be logged in to toptex.fr?

No. It only uses pages of toptex.fr that are reachable without signing in.

### Does it change anything on toptex.fr, or only read data?

Unknown: its author has not declared whether it changes anything on toptex.fr, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/toptex.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/toptex.fr/search-products

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/toptex.fr/search-products
