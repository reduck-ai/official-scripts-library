# Search Nykaa products

Automatically search Nykaa products on nykaa.com. Search products in the Nykaa India store (nykaa.com) by text. It returns up to 20 products per page with their id, brand, link, price and maximum retail price in Indian rupees, discount, rating and stock, plus the total number found. Nykaa sends some searches, for example "lipstick", to a category page: then the script returns that category's products and the category link in redirectUrl. Use page for the next pages and sort for the order Nykaa offers. A page past the last one returns an empty list. Nykaa can show a few near matches for a search with no exact match.

- Site: nykaa.com
- Address: `reduck/nykaa.com/search-products`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/nykaa.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/nykaa.com/search-products
```

## Input

- `query` (string, required): Search text, for example "lipstick" or "maybelline fit me foundation".
- `page` (integer, optional): Page of results, from 1. Nykaa shows 20 products per page.
- `sort` (string, optional): Sort value as Nykaa sends it from its sort menu: relevance (search pages only), popularity (category pages only), discount, name, customer_top_rated, new_arrival, price_desc or price_asc. Leave it out for the site's default order.

## Output

- `page` (integer, required)
- `query` (string, required)
- `products` (array, required)
- `sort` (string | null, optional): Sort that Nykaa applied.
- `banners` (array, optional): Banner tiles that the category page shows between its products.
- `hasMore` (boolean, optional): True when a next page has more products.
- `currency` (string, optional): Currency of the prices: INR.
- `totalFound` (integer | null, optional): Number of products Nykaa found.
- `redirectUrl` (string | null, optional): Category page that Nykaa sent this search to, for example lipstick goes to the lips category. Null when Nykaa showed a search result page.
- `categoryName` (string | null, optional): Title of that category page.

## FAQ

### What does "Search Nykaa products" do?

Search products in the Nykaa India store (nykaa.com) by text. It returns up to 20 products per page with their id, brand, link, price and maximum retail price in Indian rupees, discount, rating and stock, plus the total number found. Nykaa sends some searches, for example "lipstick", to a category page: then the script returns that category's products and the category link in redirectUrl. Use page for the next pages and sort for the order Nykaa offers. A page past the last one returns an empty list. Nykaa can show a few near matches for a search with no exact match.

### How do I automatically search Nykaa products on nykaa.com?

Ask an AI agent connected to Reduck to run reduck/nykaa.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nykaa.com/search-products

### Is there a nykaa.com API to search Nykaa products?

You do not need one. "Search Nykaa products" drives the real nykaa.com pages in a browser, so it works whether or not nykaa.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort.

### What does it return?

It returns page, sort, query, banners, hasMore, currency, products, totalFound, redirectUrl, categoryName.

### Do I need to be logged in to nykaa.com?

No. It only uses pages of nykaa.com that are reachable without signing in.

### Does it change anything on nykaa.com, or only read data?

It only reads. It looks things up on nykaa.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/nykaa.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nykaa.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/nykaa.com/search-products
