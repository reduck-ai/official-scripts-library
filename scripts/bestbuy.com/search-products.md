# Search Best Buy products

Automatically search Best Buy products on bestbuy.com. Search Best Buy (US) by free-text query, with its own filters: price range, sort order, every left-column refinement (sold and shipped by Best Buy, brand, condition, rating, deals, the product's own attributes) whose values List Best Buy search filters gives, and whether to search all categories instead of the one Best Buy picks for the query. Returns one page of 18 results: total_results, the category Best Buy narrowed to, has_next_page, and per product its SKU, title, link, image, brand, model, price, regular price, savings, rating, review count, condition, whether Best Buy sells it or a Marketplace seller does, and whether it is a sponsored slot. A query with no match returns an empty list; a page past the last one returns an empty list with has_next_page false.

- Site: bestbuy.com
- Address: `reduck/bestbuy.com/search-products`
- Updated: 2026-11-18 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bestbuy.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bestbuy.com/search-products
```

## Input

- `query` (string, required): Free-text search query.
- `page` (integer, optional): Result page, 18 products a page. has_next_page says when to stop.
- `sort` (string, optional): Sort order.
- `price_max` (number, optional): Highest price in US dollars.
- `price_min` (number, optional): Lowest price in US dollars.
- `refinements` (array, optional): Filters from Best Buy's left column, each as the refinement string List Best Buy search filters returns, e.g. "bbyonly_facet=Sold & shipped by~Best Buy". Values of one filter are alternatives; different filters all apply.
- `all_categories` (boolean, optional): Best Buy narrows most queries to one category (category in the result). True searches every category instead.

## Output

- `url` (string, required): The Best Buy search page for these arguments.
- `page` (integer, required)
- `items` (array, required): The products in page order, sponsored slots included. A product can appear twice: once sponsored, once as a result.
- `query` (string, required)
- `category` (string | null, required): The category Best Buy narrowed the search to on its own, null when it searched all categories.
- `has_next_page` (boolean, required)
- `total_results` (integer, required): Products matching the search, sponsored slots excluded.

## FAQ

### What does "Search Best Buy products" do?

Search Best Buy (US) by free-text query, with its own filters: price range, sort order, every left-column refinement (sold and shipped by Best Buy, brand, condition, rating, deals, the product's own attributes) whose values List Best Buy search filters gives, and whether to search all categories instead of the one Best Buy picks for the query. Returns one page of 18 results: total_results, the category Best Buy narrowed to, has_next_page, and per product its SKU, title, link, image, brand, model, price, regular price, savings, rating, review count, condition, whether Best Buy sells it or a Marketplace seller does, and whether it is a sponsored slot. A query with no match returns an empty list; a page past the last one returns an empty list with has_next_page false.

### How do I automatically search Best Buy products on bestbuy.com?

Ask an AI agent connected to Reduck to run reduck/bestbuy.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bestbuy.com/search-products

### Is there a bestbuy.com API to search Best Buy products?

You do not need one. "Search Best Buy products" drives the real bestbuy.com pages in a browser, so it works whether or not bestbuy.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, price_max, price_min, refinements, all_categories.

### What does it return?

It returns url, page, items, query, category, has_next_page, total_results.

### Do I need to be logged in to bestbuy.com?

No. It only uses pages of bestbuy.com that are reachable without signing in.

### Does it change anything on bestbuy.com, or only read data?

It only reads. It looks things up on bestbuy.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bestbuy.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bestbuy.com/search-products

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/bestbuy.com/search-products
