# Search Kaufland products

Automatically search Kaufland products on kaufland.de. Search kaufland.de by keyword, one results page at a time: each product's id, link, name, price and shipping fee in euros, rating, review count, seller, delivery window and image, along with the result count the site states.

- Site: kaufland.de
- Address: `reduck/kaufland.de/search-products`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/kaufland.de/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/kaufland.de/search-products
```

## Input

- `query` (string, required): Words to search for, as typed in Kaufland's search box (German works best, e.g. "handtuch").
- `page` (integer, optional): Results page, from 1.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `has_next_page` (boolean, required)
- `total_results` (integer | null, optional): The result count the site states; it caps large counts (e.g. 10000 for "10.000+").

## FAQ

### What does "Search Kaufland products" do?

Search kaufland.de by keyword, one results page at a time: each product's id, link, name, price and shipping fee in euros, rating, review count, seller, delivery window and image, along with the result count the site states.

### How do I automatically search Kaufland products on kaufland.de?

Ask an AI agent connected to Reduck to run reduck/kaufland.de/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kaufland.de/search-products

### Is there a kaufland.de API to search Kaufland products?

You do not need one. "Search Kaufland products" drives the real kaufland.de pages in a browser, so it works whether or not kaufland.de offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, has_next_page, total_results.

### Do I need to be logged in to kaufland.de?

No. It only uses pages of kaufland.de that are reachable without signing in.

### Does it change anything on kaufland.de, or only read data?

It only reads. It looks things up on kaufland.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/kaufland.de/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kaufland.de/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/kaufland.de/search-products
