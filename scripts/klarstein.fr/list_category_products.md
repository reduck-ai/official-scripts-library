# List Klarstein category products

Automatically list Klarstein category products on klarstein.fr. List products in a Klarstein category page (e.g. "Chauffage", "Climatisation"), 20 per page, server-ranked (top-seller order). Returns totalArticles, page, and products with sku, title, url, price_eur, imageUrl, rating (0-5 filled stars), and stock status.

- Site: klarstein.fr
- Address: `reduck/klarstein.fr/list_category_products`
- Updated: 2026-10-28 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/klarstein.fr/list_category_products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/klarstein.fr/list_category_products
```

## Input

- `category` (string, required): Category path segment as it appears in Klarstein's own nav/URL, e.g. 'Chauffage', 'Climatisation'. Case does not matter. A landing page that only groups sub-categories (e.g. 'Qualite-de-l-air') is refused: pass one of its sub-categories.
- `cursor` (string, optional): nextCursor from a previous run on the same category, to get the next 20 products. Omit for the first 20. Klarstein's list is forward-only, so there is no jumping to page N.

## Output

- `products` (array, required): Up to 20 products, in Klarstein's own top-seller order.
- `nextCursor` (string | null, required): Pass as cursor (with the same category) for the next 20 products. Null when this was the last batch.
- `totalArticles` (integer, required): Total products in this category, as shown by the site's own result-count element, not just this batch's count.

## FAQ

### What does "List Klarstein category products" do?

List products in a Klarstein category page (e.g. "Chauffage", "Climatisation"), 20 per page, server-ranked (top-seller order). Returns totalArticles, page, and products with sku, title, url, price_eur, imageUrl, rating (0-5 filled stars), and stock status.

### How do I automatically list Klarstein category products on klarstein.fr?

Ask an AI agent connected to Reduck to run reduck/klarstein.fr/list_category_products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/klarstein.fr/list_category_products

### Is there a klarstein.fr API to list Klarstein category products?

You do not need one. "List Klarstein category products" drives the real klarstein.fr pages in a browser, so it works whether or not klarstein.fr offers an API for this.

### What information do I need to provide?

Required: category. Optional: cursor.

### What does it return?

It returns products, nextCursor, totalArticles.

### Do I need to be logged in to klarstein.fr?

No. It only uses pages of klarstein.fr that are reachable without signing in.

### Does it change anything on klarstein.fr, or only read data?

It only reads. It looks things up on klarstein.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/klarstein.fr/list_category_products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/klarstein.fr/list_category_products

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/klarstein.fr/list_category_products
