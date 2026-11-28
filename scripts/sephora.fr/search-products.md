# Search Sephora France products

Automatically search Sephora France products on sephora.fr. Search sephora.fr by keyword, one results page at a time: each product's sku, link, name, brand, price in euros, stock state, rating, review count and image, and whether more pages follow.

- Site: sephora.fr
- Address: `reduck/sephora.fr/search-products`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/sephora.fr/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/sephora.fr/search-products
```

## Input

- `query` (string, required): Words to search for, as typed in Sephora's search box (e.g. "mascara").
- `page` (integer, optional): Results page, from 1.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `has_next_page` (boolean, required)

## FAQ

### What does "Search Sephora France products" do?

Search sephora.fr by keyword, one results page at a time: each product's sku, link, name, brand, price in euros, stock state, rating, review count and image, and whether more pages follow.

### How do I automatically search Sephora France products on sephora.fr?

Ask an AI agent connected to Reduck to run reduck/sephora.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sephora.fr/search-products

### Is there a sephora.fr API to search Sephora France products?

You do not need one. "Search Sephora France products" drives the real sephora.fr pages in a browser, so it works whether or not sephora.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, has_next_page.

### Do I need to be logged in to sephora.fr?

No. It only uses pages of sephora.fr that are reachable without signing in.

### Does it change anything on sephora.fr, or only read data?

It only reads. It looks things up on sephora.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/sephora.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sephora.fr/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/sephora.fr/search-products
