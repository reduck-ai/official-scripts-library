# Search notebooksbilliger.de products

Automatically search notebooksbilliger.de products on notebooksbilliger.de. Search notebooksbilliger.de by free-text query, 48 products a page. Returns the total result count, whether there is a next page, and for each product its id, article number, link, name, brand, category, price and recommended price (UVP) in euros, the campaign label and discount it shows, availability text, rating, review count, highlights and image. A query with no match, or a page past the last, returns an empty list. Pass a product id to Get notebooksbilliger.de product.

- Site: notebooksbilliger.de
- Address: `reduck/notebooksbilliger.de/search-products`
- Updated: 2026-11-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/notebooksbilliger.de/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/notebooksbilliger.de/search-products
```

## Input

- `query` (string, required): Free-text search, e.g. "ssd".
- `page` (integer, optional): Result page, 48 products each.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `has_next_page` (boolean, required)
- `total_results` (integer, required)

## FAQ

### What does "Search notebooksbilliger.de products" do?

Search notebooksbilliger.de by free-text query, 48 products a page. Returns the total result count, whether there is a next page, and for each product its id, article number, link, name, brand, category, price and recommended price (UVP) in euros, the campaign label and discount it shows, availability text, rating, review count, highlights and image. A query with no match, or a page past the last, returns an empty list. Pass a product id to Get notebooksbilliger.de product.

### How do I automatically search notebooksbilliger.de products on notebooksbilliger.de?

Ask an AI agent connected to Reduck to run reduck/notebooksbilliger.de/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/notebooksbilliger.de/search-products

### Is there a notebooksbilliger.de API to search notebooksbilliger.de products?

You do not need one. "Search notebooksbilliger.de products" drives the real notebooksbilliger.de pages in a browser, so it works whether or not notebooksbilliger.de offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, has_next_page, total_results.

### Do I need to be logged in to notebooksbilliger.de?

No. It only uses pages of notebooksbilliger.de that are reachable without signing in.

### Does it change anything on notebooksbilliger.de, or only read data?

It only reads. It looks things up on notebooksbilliger.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/notebooksbilliger.de/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/notebooksbilliger.de/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/notebooksbilliger.de/search-products
