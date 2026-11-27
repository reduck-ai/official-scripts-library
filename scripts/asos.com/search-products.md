# Search ASOS products

Automatically search ASOS products on asos.com. Search the ASOS UK store (asos.com) by free text, one page of up to 72 products at a time, in the site's sort order (relevance, newest, price up or down), with the site's filters (brand, colour, size, product type and more, from facets of an earlier search) and a price range in pounds. For each product: product id, name, brand, colour, link, price in pounds, price before a reduction, promo code price, sale, outlet, selling fast and more colours flags, and image. Also gives the total number of results, the page count and the filters the site offers for the search. A query the site does not match exactly returns the site's nearest matches. A query that names a page of the site (for example gift card) returns no products and the page the site opened.

- Site: asos.com
- Address: `reduck/asos.com/search-products`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/asos.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/asos.com/search-products
```

## Input

- `query` (string, required): Words to search for, as typed in the ASOS search box.
- `page` (integer, optional): Result page, from 1. Each page holds up to 72 products.
- `sort` (string, optional): Sort order of the site.
- `filters` (array, optional): Filters to apply, each the filter value of a facet value from an earlier search (for example brand:12136 or base_colour:4). Values of one facet match any of them.
- `maxPrice` (number, optional): Highest price, in pounds.
- `minPrice` (number, optional): Lowest price, in pounds.

## Output

- `url` (string, required)
- `page` (integer, required)
- `query` (string, required)
- `facets` (array, required)
- `currency` (string | null, required)
- `products` (array, required)
- `pageCount` (integer | null, required)
- `hasNextPage` (boolean, required)
- `redirectedTo` (string | null, required): The page the site opened in place of results, for a query that names a page of the site (for example gift card). Products are then empty.
- `totalResults` (integer | null, required)

## FAQ

### What does "Search ASOS products" do?

Search the ASOS UK store (asos.com) by free text, one page of up to 72 products at a time, in the site's sort order (relevance, newest, price up or down), with the site's filters (brand, colour, size, product type and more, from facets of an earlier search) and a price range in pounds. For each product: product id, name, brand, colour, link, price in pounds, price before a reduction, promo code price, sale, outlet, selling fast and more colours flags, and image. Also gives the total number of results, the page count and the filters the site offers for the search. A query the site does not match exactly returns the site's nearest matches. A query that names a page of the site (for example gift card) returns no products and the page the site opened.

### How do I automatically search ASOS products on asos.com?

Ask an AI agent connected to Reduck to run reduck/asos.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/asos.com/search-products

### Is there a asos.com API to search ASOS products?

You do not need one. "Search ASOS products" drives the real asos.com pages in a browser, so it works whether or not asos.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, filters, maxPrice, minPrice.

### What does it return?

It returns url, page, query, facets, currency, products, pageCount, hasNextPage, redirectedTo, totalResults.

### Do I need to be logged in to asos.com?

No. It only uses pages of asos.com that are reachable without signing in.

### Does it change anything on asos.com, or only read data?

It only reads. It looks things up on asos.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/asos.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/asos.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/asos.com/search-products
