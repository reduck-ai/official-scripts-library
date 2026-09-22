# List Klarstein category products

Automatically list Klarstein category products on klarstein.fr. List products in a Klarstein category page (e.g. "Chauffage", "Climatisation"), 20 per page, server-ranked (top-seller order). Returns totalArticles, page, and products with sku, title, url, price_eur, imageUrl, rating (0-5 filled stars), and stock status.

- Site: klarstein.fr
- Address: `reduck/klarstein.fr/list_category_products`
- Updated: 2026-09-18 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/klarstein.fr/list_category_products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/klarstein.fr/list_category_products
```

## Input

- `category` (string, required): Category path segment as it appears in Klarstein's own nav/URL, e.g. 'Chauffage', 'Climatisation', 'Qualite-de-l-air'. Case as shown in the URL.
- `page` (integer, optional): 1-based page number, mirroring the site's own pagination. 20 products per page.

## Output

- `page` (integer, required)
- `products` (array, required)
- `totalArticles` (integer, required): Total products in this category, as shown by the site's own result-count element — not just this page's count.

## FAQ

### What does "List Klarstein category products" do?

List products in a Klarstein category page (e.g. "Chauffage", "Climatisation"), 20 per page, server-ranked (top-seller order). Returns totalArticles, page, and products with sku, title, url, price_eur, imageUrl, rating (0-5 filled stars), and stock status.

### How do I automatically list Klarstein category products on klarstein.fr?

Ask an AI agent connected to Reduck to run reduck/klarstein.fr/list_category_products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/klarstein.fr/list_category_products

### Is there a klarstein.fr API to list Klarstein category products?

You do not need one. "List Klarstein category products" drives the real klarstein.fr pages in a browser, so it works whether or not klarstein.fr offers an API for this.

### What information do I need to provide?

Required: category. Optional: page.

### What does it return?

It returns page, products, totalArticles.

### Do I need to be logged in to klarstein.fr?

No. It only uses pages of klarstein.fr that are reachable without signing in.

### Does it change anything on klarstein.fr, or only read data?

It only reads. It looks things up on klarstein.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/klarstein.fr/list_category_products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/klarstein.fr/list_category_products

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/klarstein.fr/list_category_products
