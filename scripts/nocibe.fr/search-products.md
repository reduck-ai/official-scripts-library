# Search Nocibé products

Automatically search Nocibé products on nocibe.fr. Search the Nocibé French beauty store (nocibe.fr, prices in euros) by free text, with the site's sort orders. Returns one page of 48 products: the total number of results, the page count and has_next_page, then for each product its product id, the code of the size shown (offer_id), brand, line, name, size, category, link, price, list price and discount, rating and review count, whether it is in stock, the seller (Nocibé or a partner seller, marketplace true) and image. Stop paging when has_next_page is false; a page past the last one returns an empty list. A search with no match returns an empty list. Pass product_id to Get Nocibé product for every size. Works in your own browser (the extension); Nocibé refuses cloud browsers.

- Site: nocibe.fr
- Address: `reduck/nocibe.fr/search-products`
- Updated: 2026-11-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/nocibe.fr/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/nocibe.fr/search-products
```

## Input

- `query` (string, required): Free text, as typed in the Nocibé search box (French works best), e.g. "parfum femme" or a brand.
- `page` (integer, optional): Result page, from 1. 48 products a page.
- `sort` (string, optional): The site's sort orders.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `total_pages` (integer, optional)
- `has_next_page` (boolean, optional)
- `total_results` (integer, optional)

## FAQ

### What does "Search Nocibé products" do?

Search the Nocibé French beauty store (nocibe.fr, prices in euros) by free text, with the site's sort orders. Returns one page of 48 products: the total number of results, the page count and has_next_page, then for each product its product id, the code of the size shown (offer_id), brand, line, name, size, category, link, price, list price and discount, rating and review count, whether it is in stock, the seller (Nocibé or a partner seller, marketplace true) and image. Stop paging when has_next_page is false; a page past the last one returns an empty list. A search with no match returns an empty list. Pass product_id to Get Nocibé product for every size. Works in your own browser (the extension); Nocibé refuses cloud browsers.

### How do I automatically search Nocibé products on nocibe.fr?

Ask an AI agent connected to Reduck to run reduck/nocibe.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nocibe.fr/search-products

### Is there a nocibe.fr API to search Nocibé products?

You do not need one. "Search Nocibé products" drives the real nocibe.fr pages in a browser, so it works whether or not nocibe.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort.

### What does it return?

It returns page, items, query, total_pages, has_next_page, total_results.

### Do I need to be logged in to nocibe.fr?

No. It only uses pages of nocibe.fr that are reachable without signing in.

### Does it change anything on nocibe.fr, or only read data?

It only reads. It looks things up on nocibe.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/nocibe.fr/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nocibe.fr/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/nocibe.fr/search-products
