# List category

Automatically list category on toptex.fr. List one page of products from a toptex.fr category page (e.g. /produits/vetements/categories/t-shirts.html). Returns products (reference, name, brand, from-price, image, PDP url) with deterministic pagination; page is 0-based. No login required.

- Site: toptex.fr
- Address: `reduck/toptex.fr/list-category`
- Updated: 2026-08-24 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/toptex.fr/list-category`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/toptex.fr/list-category
```

## Input

- `url` (string, required): Category page URL, e.g. https://www.toptex.fr/produits/vetements/categories/t-shirts.html
- `page` (integer, optional): 0-based result page (deterministic pagination).
- `hitsPerPage` (integer, optional): Products per page (site default 24).

## Output

- `url` (string, required)
- `page` (integer, required)
- `nbHits` (integer, required)
- `nbPages` (integer, required)
- `products` (array, required)
- `hitsPerPage` (integer, required)
- `ruleContexts` (array, optional): Category scope token(s) applied to this page's results.

## FAQ

### What does "List category" do?

List one page of products from a toptex.fr category page (e.g. /produits/vetements/categories/t-shirts.html). Returns products (reference, name, brand, from-price, image, PDP url) with deterministic pagination; page is 0-based. No login required.

### How do I automatically list category on toptex.fr?

Ask an AI agent connected to Reduck to run reduck/toptex.fr/list-category, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/toptex.fr/list-category

### Is there a toptex.fr API to list category?

You do not need one. "List category" drives the real toptex.fr pages in a browser, so it works whether or not toptex.fr offers an API for this.

### What information do I need to provide?

Required: url. Optional: page, hitsPerPage.

### What does it return?

It returns url, page, nbHits, nbPages, products, hitsPerPage, ruleContexts.

### Do I need to be logged in to toptex.fr?

No. It only uses pages of toptex.fr that are reachable without signing in.

### Does it change anything on toptex.fr, or only read data?

It only reads. It looks things up on toptex.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/toptex.fr/list-category, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/toptex.fr/list-category

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/toptex.fr/list-category
