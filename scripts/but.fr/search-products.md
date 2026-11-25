# Search BUT.fr products

Automatically search BUT.fr products on but.fr. Search BUT.fr (furniture, mattresses, home appliances, TV and hi-fi) by free-text query and return one page of 40 results, in euros: the total result and page counts, has_next_page, and for each product its id, title, link, brand, price, struck-through list price, discount, rating, review count, image and seller. Pass page to read further. A very generic query that BUT.fr treats as a product category (for example a plain product type) is refused with an error that asks for a more specific query. Pass the id or link to Get BUT product.

- Site: but.fr
- Address: `reduck/but.fr/search-products`
- Updated: 2026-11-24 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/but.fr/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/but.fr/search-products
```

## Input

- `query` (string, required): Free-text search, for example table basse noire.
- `page` (integer, optional): Page of results, starting at 1. Stop when has_next_page is false.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `page_count` (integer | null, required)
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required)

## FAQ

### What does "Search BUT.fr products" do?

Search BUT.fr (furniture, mattresses, home appliances, TV and hi-fi) by free-text query and return one page of 40 results, in euros: the total result and page counts, has_next_page, and for each product its id, title, link, brand, price, struck-through list price, discount, rating, review count, image and seller. Pass page to read further. A very generic query that BUT.fr treats as a product category (for example a plain product type) is refused with an error that asks for a more specific query. Pass the id or link to Get BUT product.

### How do I automatically search BUT.fr products on but.fr?

Ask an AI agent connected to Reduck to run reduck/but.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/but.fr/search-products

### Is there a but.fr API to search BUT.fr products?

You do not need one. "Search BUT.fr products" drives the real but.fr pages in a browser, so it works whether or not but.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, page_count, has_next_page, total_results.

### Do I need to be logged in to but.fr?

No. It only uses pages of but.fr that are reachable without signing in.

### Does it change anything on but.fr, or only read data?

It only reads. It looks things up on but.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/but.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/but.fr/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/but.fr/search-products
