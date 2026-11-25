# Search Back Market France products

Automatically search Back Market France products on backmarket.fr. Search backmarket.fr by free text and return the first page of results: for each the product id, the offer shown (offer id, price in euros, condition grade, warranty), the seller id, rating, review count, stock, image and product page link. Also returns the total number of products found over all pages; later pages are not available. A search with no match returns an empty list. Pass a product link to Get Back Market France product, or to Add Back Market France product to cart.

- Site: backmarket.fr
- Address: `reduck/backmarket.fr/search-products`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/backmarket.fr/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/backmarket.fr/search-products
```

## Input

- `query` (string, required): Free-text search, e.g. iPhone 13 or coque iPhone

## Output

- `items` (array, required)
- `query` (string, required)
- `total_results` (integer | null, optional): Number of products the site found for the search, over all its pages.

## FAQ

### What does "Search Back Market France products" do?

Search backmarket.fr by free text and return the first page of results: for each the product id, the offer shown (offer id, price in euros, condition grade, warranty), the seller id, rating, review count, stock, image and product page link. Also returns the total number of products found over all pages; later pages are not available. A search with no match returns an empty list. Pass a product link to Get Back Market France product, or to Add Back Market France product to cart.

### How do I automatically search Back Market France products on backmarket.fr?

Ask an AI agent connected to Reduck to run reduck/backmarket.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/backmarket.fr/search-products

### Is there a backmarket.fr API to search Back Market France products?

You do not need one. "Search Back Market France products" drives the real backmarket.fr pages in a browser, so it works whether or not backmarket.fr offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns items, query, total_results.

### Do I need to be logged in to backmarket.fr?

No. It only uses pages of backmarket.fr that are reachable without signing in.

### Does it change anything on backmarket.fr, or only read data?

It only reads. It looks things up on backmarket.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/backmarket.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/backmarket.fr/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/backmarket.fr/search-products
