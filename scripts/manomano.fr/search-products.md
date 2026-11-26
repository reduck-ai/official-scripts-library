# Search ManoMano products

Automatically search ManoMano products on manomano.fr. Search ManoMano.fr (DIY, home and garden marketplace) by free-text query and return one page of results as the site shows them: for each product its product id, article id, title, link, brand, price and struck-through price in euros, discount, rating, review count, image, the seller that sells the offer, and whether it is sponsored. Also returns the total number of results, the page count and has_next_page. Some queries make ManoMano open a category page instead of a result list, and the category is then named in the answer. A page past the last one fails with an error that says so. Pass the link to Get ManoMano product or Add ManoMano product to cart.

- Site: manomano.fr
- Address: `reduck/manomano.fr/search-products`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/manomano.fr/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/manomano.fr/search-products
```

## Input

- `query` (string, required): What to search for, as typed in the ManoMano search box, for example "vis à bois" or "perceuse visseuse makita".
- `page` (integer, optional): Result page, starting at 1. Stop when has_next_page is false.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `page_count` (integer | null, required)
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required)
- `category` (string | null, optional): Name of the category ManoMano opened instead of a result list, when it did.
- `per_page` (integer | null, optional)

## FAQ

### What does "Search ManoMano products" do?

Search ManoMano.fr (DIY, home and garden marketplace) by free-text query and return one page of results as the site shows them: for each product its product id, article id, title, link, brand, price and struck-through price in euros, discount, rating, review count, image, the seller that sells the offer, and whether it is sponsored. Also returns the total number of results, the page count and has_next_page. Some queries make ManoMano open a category page instead of a result list, and the category is then named in the answer. A page past the last one fails with an error that says so. Pass the link to Get ManoMano product or Add ManoMano product to cart.

### How do I automatically search ManoMano products on manomano.fr?

Ask an AI agent connected to Reduck to run reduck/manomano.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/manomano.fr/search-products

### Is there a manomano.fr API to search ManoMano products?

You do not need one. "Search ManoMano products" drives the real manomano.fr pages in a browser, so it works whether or not manomano.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, category, per_page, page_count, has_next_page, total_results.

### Do I need to be logged in to manomano.fr?

No. It only uses pages of manomano.fr that are reachable without signing in.

### Does it change anything on manomano.fr, or only read data?

It only reads. It looks things up on manomano.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/manomano.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/manomano.fr/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/manomano.fr/search-products
