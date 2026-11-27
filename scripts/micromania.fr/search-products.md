# Search Micromania products

Automatically search Micromania products on micromania.fr. Search Micromania.fr (video games, trading cards and gaming goods, in euros) by free-text query, with the site's own sort orders, one page of about 20 results at a time. Returns the page number, has_next_page, the total number of results when the site states it, and the items: sku, title, url, price, struck-through list_price, rating, review_count, image_url, brand, ean, availability, condition and whether the product can be added to the cart. Stop paging when has_next_page is false. Pass the url of an item to Get Micromania product and Add a product to the Micromania cart.

- Site: micromania.fr
- Address: `reduck/micromania.fr/search-products`
- Updated: 2026-11-24 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/micromania.fr/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/micromania.fr/search-products
```

## Input

- `query` (string, required): Free-text search, for example booster pokemon or zelda switch.
- `page` (integer, optional): Result page, starting at 1. Stop when has_next_page is false.
- `sort` (string, optional): Sort order of the site: relevance is the site's default order.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required): Number of results the site states for the whole search, null when the page does not state it.

## FAQ

### What does "Search Micromania products" do?

Search Micromania.fr (video games, trading cards and gaming goods, in euros) by free-text query, with the site's own sort orders, one page of about 20 results at a time. Returns the page number, has_next_page, the total number of results when the site states it, and the items: sku, title, url, price, struck-through list_price, rating, review_count, image_url, brand, ean, availability, condition and whether the product can be added to the cart. Stop paging when has_next_page is false. Pass the url of an item to Get Micromania product and Add a product to the Micromania cart.

### How do I automatically search Micromania products on micromania.fr?

Ask an AI agent connected to Reduck to run reduck/micromania.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/micromania.fr/search-products

### Is there a micromania.fr API to search Micromania products?

You do not need one. "Search Micromania products" drives the real micromania.fr pages in a browser, so it works whether or not micromania.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort.

### What does it return?

It returns page, items, query, has_next_page, total_results.

### Do I need to be logged in to micromania.fr?

No. It only uses pages of micromania.fr that are reachable without signing in.

### Does it change anything on micromania.fr, or only read data?

It only reads. It looks things up on micromania.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/micromania.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/micromania.fr/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/micromania.fr/search-products
