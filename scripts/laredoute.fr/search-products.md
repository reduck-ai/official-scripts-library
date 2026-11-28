# Search La Redoute products

Automatically search La Redoute products on laredoute.fr. Search laredoute.fr by keyword, one results page at a time: each product's id, link, brand, name, price and former price in euros, rating, number of colours and image, along with the result count and page count.

- Site: laredoute.fr
- Address: `reduck/laredoute.fr/search-products`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/laredoute.fr/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/laredoute.fr/search-products
```

## Input

- `query` (string, required): Words to search for, as typed in La Redoute's search box (French works best, e.g. "serviette").
- `page` (integer, optional): Results page, from 1.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `has_next_page` (boolean, required)
- `total_pages` (integer | null, optional)
- `total_results` (integer | null, optional)

## FAQ

### What does "Search La Redoute products" do?

Search laredoute.fr by keyword, one results page at a time: each product's id, link, brand, name, price and former price in euros, rating, number of colours and image, along with the result count and page count.

### How do I automatically search La Redoute products on laredoute.fr?

Ask an AI agent connected to Reduck to run reduck/laredoute.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/laredoute.fr/search-products

### Is there a laredoute.fr API to search La Redoute products?

You do not need one. "Search La Redoute products" drives the real laredoute.fr pages in a browser, so it works whether or not laredoute.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, total_pages, has_next_page, total_results.

### Do I need to be logged in to laredoute.fr?

No. It only uses pages of laredoute.fr that are reachable without signing in.

### Does it change anything on laredoute.fr, or only read data?

It only reads. It looks things up on laredoute.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/laredoute.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/laredoute.fr/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/laredoute.fr/search-products
