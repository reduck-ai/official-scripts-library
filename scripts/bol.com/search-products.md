# Search bol.com products

Automatically search bol.com products on bol.com. Search bol.com (Netherlands, Dutch site) by free text and get one page of results: for each product its id, title, link, brand, seller, price in euros, rating, review count, whether it is sponsored and whether it has an offer to buy now. Also returns the number of the last page and the product categories the search offers, each with the id to pass back as category_id to narrow the search. Page 1 is the default; stop paging at the last page. A search with no result returns an empty list. Pass a product id to Get bol.com product.

- Site: bol.com
- Address: `reduck/bol.com/search-products`
- Updated: 2026-11-24 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bol.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bol.com/search-products
```

## Input

- `query` (string, required): Free-text search, as typed in the bol.com search box (Dutch terms give the best results).
- `page` (integer, optional): Result page, starting at 1. The last page number is returned as max_page.
- `category_id` (string, optional): Category id taken from the categories of an earlier search, to keep only that category.

## Output

- `page` (integer, required)
- `query` (string, required)
- `max_page` (integer | null, required)
- `products` (array, required)
- `categories` (array, required)
- `has_next_page` (boolean, required)

## FAQ

### What does "Search bol.com products" do?

Search bol.com (Netherlands, Dutch site) by free text and get one page of results: for each product its id, title, link, brand, seller, price in euros, rating, review count, whether it is sponsored and whether it has an offer to buy now. Also returns the number of the last page and the product categories the search offers, each with the id to pass back as category_id to narrow the search. Page 1 is the default; stop paging at the last page. A search with no result returns an empty list. Pass a product id to Get bol.com product.

### How do I automatically search bol.com products on bol.com?

Ask an AI agent connected to Reduck to run reduck/bol.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bol.com/search-products

### Is there a bol.com API to search bol.com products?

You do not need one. "Search bol.com products" drives the real bol.com pages in a browser, so it works whether or not bol.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, category_id.

### What does it return?

It returns page, query, max_page, products, categories, has_next_page.

### Do I need to be logged in to bol.com?

No. It only uses pages of bol.com that are reachable without signing in.

### Does it change anything on bol.com, or only read data?

It only reads. It looks things up on bol.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bol.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bol.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/bol.com/search-products
