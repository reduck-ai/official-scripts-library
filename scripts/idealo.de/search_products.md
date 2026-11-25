# Search idealo.de products

Automatically search idealo.de products on idealo.de. Search the idealo.de price comparison by free text, with the site's filters: category, the attribute filters of a category (brand, size, color and others), price range, fast delivery, short-term deals, bargains, and the sort order (relevance, price, biggest saving, newest). Returns one page of results: for each, whether it is a product idealo compares across shops or the offer of one shop, the product id (the input of get_price_history), title, characteristics, link, image, lowest price in euros, number of offers, user rating and review count, test grade, bargain saving, energy class, and for an offer the shop and its delivery. Sponsored results come first and are marked. The answer also gives the total number of results, the categories of a search in all categories and the filters of the category, with their ids. For some searches the site chooses a category itself: the answer says which. A search with no match, or a page past the last one, returns an empty list.

- Site: idealo.de
- Address: `reduck/idealo.de/search_products`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/idealo.de/search_products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/idealo.de/search_products
```

## Input

- `query` (string, required): Search words.
- `page` (integer, optional): Result page. has_next_page says when to stop.
- `sort` (string, optional): Sort order, as the site offers it: relevance (the default), lowest price first, highest price first, biggest saving first, newest first.
- `filters` (array, optional): Filter ids from the filter_groups field of an earlier answer in the same category (brand, size, color and the other attributes of the category). Needs category_id. Values of one group are alternatives; values of different groups all apply.
- `bargains` (boolean, optional): Only bargains: products whose price is lower than usual.
- `price_max` (number | null, optional): Highest price, in euros. Null for no upper limit.
- `price_min` (number | null, optional): Lowest price, in euros. Null for no lower limit.
- `category_id` (string | null, optional): Search inside this category, by an id from the categories field of an earlier answer, or the category_id of an earlier answer. Null searches all categories; the site can then choose a category itself, which category_id in the answer says.
- `fast_delivery` (boolean, optional): Only results the shops deliver in 1 to 7 working days.
- `short_term_deals` (boolean, optional): Only short-term deals (shown as Black Friday offers during that sales event).

## Output

- `url` (string, required): The result page on idealo.
- `page` (integer, required)
- `site` (string, required)
- `items` (array, required): Sponsored results first, then the results in the order of the sort.
- `query` (string, required)
- `categories` (array, required): Categories the results are in, with how many each has, for a search in all categories. Pass an id as category_id.
- `category_id` (string | null, required): The category the results are in. Null for a search in all categories.
- `filter_groups` (array, required): Filters the site offers for these results, by group. Pass filter ids in filters, with the category_id.
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required)

## FAQ

### What does "Search idealo.de products" do?

Search the idealo.de price comparison by free text, with the site's filters: category, the attribute filters of a category (brand, size, color and others), price range, fast delivery, short-term deals, bargains, and the sort order (relevance, price, biggest saving, newest). Returns one page of results: for each, whether it is a product idealo compares across shops or the offer of one shop, the product id (the input of get_price_history), title, characteristics, link, image, lowest price in euros, number of offers, user rating and review count, test grade, bargain saving, energy class, and for an offer the shop and its delivery. Sponsored results come first and are marked. The answer also gives the total number of results, the categories of a search in all categories and the filters of the category, with their ids. For some searches the site chooses a category itself: the answer says which. A search with no match, or a page past the last one, returns an empty list.

### How do I automatically search idealo.de products on idealo.de?

Ask an AI agent connected to Reduck to run reduck/idealo.de/search_products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/idealo.de/search_products

### Is there a idealo.de API to search idealo.de products?

You do not need one. "Search idealo.de products" drives the real idealo.de pages in a browser, so it works whether or not idealo.de offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, filters, bargains, price_max, price_min, category_id, fast_delivery, short_term_deals.

### What does it return?

It returns url, page, site, items, query, categories, category_id, filter_groups, has_next_page, total_results.

### Do I need to be logged in to idealo.de?

No. It only uses pages of idealo.de that are reachable without signing in.

### Does it change anything on idealo.de, or only read data?

It only reads. It looks things up on idealo.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/idealo.de/search_products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/idealo.de/search_products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/idealo.de/search_products
