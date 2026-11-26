# Search Geizhals products

Automatically search Geizhals products on geizhals.de. Search the Geizhals.de price comparison by free text, with the site's filters: category, manufacturers, price range and sort order (relevance, lowest price first, highest price first). Returns one page of 30 results, with the offers of merchants in Germany and Austria (the site's default for geizhals.de). For each result: whether it is one product or a group of variants, the product id (the input of Get Geizhals price history; null for a group of variants), title, link, image, lowest price in euros, the price 30 days ago and the change in percent when the site shows them, whether the site marks the price as the lowest so far, availability, number of offers, user rating and review count, and the main specifications. The answer also gives the last page number and the categories and manufacturers the site offers as filters, with their ids. A search with no match, or a page past the last one, returns an empty list.

- Site: geizhals.de
- Address: `reduck/geizhals.de/search_products`
- Updated: 2026-11-25 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/geizhals.de/search_products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/geizhals.de/search_products
```

## Input

- `query` (string, required): Search words.
- `page` (integer, optional): Result page, 30 results a page. has_next_page says when to stop.
- `sort` (string, optional): Sort order, as the site offers it: relevance (the default), lowest price first, highest price first.
- `category` (string | null, optional): Search inside this category, by an id from the categories field of an earlier answer, for example hfritteuse. Null searches all categories.
- `price_max` (number | null, optional): Highest price, in euros. Null for no upper limit.
- `price_min` (number | null, optional): Lowest price, in euros. Null for no lower limit.
- `manufacturer_ids` (array, optional): Only these manufacturers, by ids from the manufacturers field of an earlier answer.

## Output

- `url` (string, required): The result page on Geizhals.
- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `last_page` (integer | null, required)
- `categories` (array, required): Categories the site offers as filters for this search. Pass an id as category.
- `has_next_page` (boolean, required)
- `manufacturers` (array, required): Manufacturers the site offers as filters. Pass ids in manufacturer_ids.

## FAQ

### What does "Search Geizhals products" do?

Search the Geizhals.de price comparison by free text, with the site's filters: category, manufacturers, price range and sort order (relevance, lowest price first, highest price first). Returns one page of 30 results, with the offers of merchants in Germany and Austria (the site's default for geizhals.de). For each result: whether it is one product or a group of variants, the product id (the input of Get Geizhals price history; null for a group of variants), title, link, image, lowest price in euros, the price 30 days ago and the change in percent when the site shows them, whether the site marks the price as the lowest so far, availability, number of offers, user rating and review count, and the main specifications. The answer also gives the last page number and the categories and manufacturers the site offers as filters, with their ids. A search with no match, or a page past the last one, returns an empty list.

### How do I automatically search Geizhals products on geizhals.de?

Ask an AI agent connected to Reduck to run reduck/geizhals.de/search_products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/geizhals.de/search_products

### Is there a geizhals.de API to search Geizhals products?

You do not need one. "Search Geizhals products" drives the real geizhals.de pages in a browser, so it works whether or not geizhals.de offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, category, price_max, price_min, manufacturer_ids.

### What does it return?

It returns url, page, items, query, last_page, categories, has_next_page, manufacturers.

### Do I need to be logged in to geizhals.de?

No. It only uses pages of geizhals.de that are reachable without signing in.

### Does it change anything on geizhals.de, or only read data?

It only reads. It looks things up on geizhals.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/geizhals.de/search_products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/geizhals.de/search_products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/geizhals.de/search_products
