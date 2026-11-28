# Search Electro Dépôt products

Automatically search Electro Dépôt products on electrodepot.fr. Search the Electro Dépôt French store (electrodepot.fr) by free text and return one page of results as the site shows them, in its own order. For each product: product id, reference, name, link, price and former price in euros (taxes included), eco-participation, brand, condition, rating, review count, tag, key features, categories, image and a last items flag. When the text matches one of its categories, the site shows that category page instead: the result then gives the category name and the page link. Stop paging when has_next_page is false; a page past the last one returns an empty list. A search with no match returns an empty list. Prices are those the site shows to a new guest. Pass a product id to Get Electro Dépôt product.

- Site: electrodepot.fr
- Address: `reduck/electrodepot.fr/search-products`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/electrodepot.fr/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/electrodepot.fr/search-products
```

## Input

- `query` (string, required): Free-text search, for example "micro-ondes" or "samsung".
- `page` (integer, optional): Result page. Stop when has_next_page is false.

## Output

- `url` (string, required): The page the site showed for the search.
- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `category` (string | null, required): Name of the category page the site showed when the text matches a category; null on a plain search results page.
- `has_next_page` (boolean, required)

## FAQ

### What does "Search Electro Dépôt products" do?

Search the Electro Dépôt French store (electrodepot.fr) by free text and return one page of results as the site shows them, in its own order. For each product: product id, reference, name, link, price and former price in euros (taxes included), eco-participation, brand, condition, rating, review count, tag, key features, categories, image and a last items flag. When the text matches one of its categories, the site shows that category page instead: the result then gives the category name and the page link. Stop paging when has_next_page is false; a page past the last one returns an empty list. A search with no match returns an empty list. Prices are those the site shows to a new guest. Pass a product id to Get Electro Dépôt product.

### How do I automatically search Electro Dépôt products on electrodepot.fr?

Ask an AI agent connected to Reduck to run reduck/electrodepot.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/electrodepot.fr/search-products

### Is there a electrodepot.fr API to search Electro Dépôt products?

You do not need one. "Search Electro Dépôt products" drives the real electrodepot.fr pages in a browser, so it works whether or not electrodepot.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns url, page, items, query, category, has_next_page.

### Do I need to be logged in to electrodepot.fr?

No. It only uses pages of electrodepot.fr that are reachable without signing in.

### Does it change anything on electrodepot.fr, or only read data?

It only reads. It looks things up on electrodepot.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/electrodepot.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/electrodepot.fr/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/electrodepot.fr/search-products
