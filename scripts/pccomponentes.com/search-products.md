# Search PcComponentes products

Automatically search PcComponentes products on pccomponentes.com. Search PcComponentes Spain (pccomponentes.com) by free-text query, with the site's sort orders, a price range and the filters it offers for the search (family, brand, condition, seller type and the product's own attributes). Returns one page of up to 40 products: product id, title, link, brand, family, price and struck-through price in euros, discount, rating out of 5, review count, image, seller and whether PcComponentes sells it, shipping cost and the delivery window, plus the total count, has_next_page, the price range of the results and the filter values the site offers, each with the filter string to pass back. Texts are in Spanish. When nothing matches, items is empty.

- Site: pccomponentes.com
- Address: `reduck/pccomponentes.com/search-products`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/pccomponentes.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/pccomponentes.com/search-products
```

## Input

- `query` (string, required): Free-text search query, in Spanish or any word the shop knows.
- `page` (integer, optional): Result page, up to 40 products a page. has_next_page says when to stop.
- `sort` (string, optional): Sort order: relevance (the default), price_asc, price_desc, sales (best sellers), discount (largest discount), top_rated, activation_date (newest).
- `filters` (array, optional): Filters, each as group:id exactly as the filter of a value in facets gives it, for example "brands:38" (Sony) or "families:1067". Values of one group are alternatives; different groups all apply.
- `price_max` (number, optional): Maximum price in euros.
- `price_min` (number, optional): Minimum price in euros.

## Output

- `url` (string, required)
- `page` (integer, required)
- `items` (array, required): Products of this page in the site's order. Empty when nothing matches.
- `query` (string, required)
- `facets` (array, required): The filter values the site offers for this search, with the filter string to pass back in filters. Price is the price_min and price_max arguments.
- `page_count` (integer | null, required)
- `price_range` (object | null, required): Lowest and highest price in euros among the results.
- `has_next_page` (boolean, required)
- `total_results` (integer, required)

## FAQ

### What does "Search PcComponentes products" do?

Search PcComponentes Spain (pccomponentes.com) by free-text query, with the site's sort orders, a price range and the filters it offers for the search (family, brand, condition, seller type and the product's own attributes). Returns one page of up to 40 products: product id, title, link, brand, family, price and struck-through price in euros, discount, rating out of 5, review count, image, seller and whether PcComponentes sells it, shipping cost and the delivery window, plus the total count, has_next_page, the price range of the results and the filter values the site offers, each with the filter string to pass back. Texts are in Spanish. When nothing matches, items is empty.

### How do I automatically search PcComponentes products on pccomponentes.com?

Ask an AI agent connected to Reduck to run reduck/pccomponentes.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pccomponentes.com/search-products

### Is there a pccomponentes.com API to search PcComponentes products?

You do not need one. "Search PcComponentes products" drives the real pccomponentes.com pages in a browser, so it works whether or not pccomponentes.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, filters, price_max, price_min.

### What does it return?

It returns url, page, items, query, facets, page_count, price_range, has_next_page, total_results.

### Do I need to be logged in to pccomponentes.com?

No. It only uses pages of pccomponentes.com that are reachable without signing in.

### Does it change anything on pccomponentes.com, or only read data?

It only reads. It looks things up on pccomponentes.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/pccomponentes.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pccomponentes.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/pccomponentes.com/search-products
