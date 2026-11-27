# Search Rossmann products

Automatically search Rossmann products on rossmann.de. Search the Rossmann Germany online shop (rossmann.de) by free text, one page of up to 24 products at a time, in the site's sort order (relevance, price up or down, newest, rating), with the site's filters (brand, category and more, from facets of an earlier search). For each product: barcode number (the product id), Rossmann article number, name, brand, link, pack size, price and struck-through earlier price in euros, base price text, badges, sponsored flag, online stock status, sales channel, rating, review count and image. Also gives the total number of results, the page count and the filters the site offers. A query that names a category opens that category, and the result says which. A query with no exact match returns the site's nearest matches.

- Site: rossmann.de
- Address: `reduck/rossmann.de/search-products`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/rossmann.de/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/rossmann.de/search-products
```

## Input

- `query` (string, required): Words to search for, as typed in the Rossmann search box.
- `page` (integer, optional): Result page, from 1. Each page holds up to 24 products.
- `sort` (string, optional): Sort order of the site.
- `filters` (array, optional): Filters to apply, each the filter value of a facet value from an earlier search (for example brand:"NIVEA").

## Output

- `url` (string, required)
- `page` (integer, required)
- `query` (string, required)
- `facets` (array, required)
- `category` (string | null, required): The category page the site opened in place of a search, when the query names a category.
- `products` (array, required)
- `pageCount` (integer | null, required)
- `hasNextPage` (boolean, required)
- `totalResults` (integer | null, required)

## FAQ

### What does "Search Rossmann products" do?

Search the Rossmann Germany online shop (rossmann.de) by free text, one page of up to 24 products at a time, in the site's sort order (relevance, price up or down, newest, rating), with the site's filters (brand, category and more, from facets of an earlier search). For each product: barcode number (the product id), Rossmann article number, name, brand, link, pack size, price and struck-through earlier price in euros, base price text, badges, sponsored flag, online stock status, sales channel, rating, review count and image. Also gives the total number of results, the page count and the filters the site offers. A query that names a category opens that category, and the result says which. A query with no exact match returns the site's nearest matches.

### How do I automatically search Rossmann products on rossmann.de?

Ask an AI agent connected to Reduck to run reduck/rossmann.de/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/rossmann.de/search-products

### Is there a rossmann.de API to search Rossmann products?

You do not need one. "Search Rossmann products" drives the real rossmann.de pages in a browser, so it works whether or not rossmann.de offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, filters.

### What does it return?

It returns url, page, query, facets, category, products, pageCount, hasNextPage, totalResults.

### Do I need to be logged in to rossmann.de?

No. It only uses pages of rossmann.de that are reachable without signing in.

### Does it change anything on rossmann.de, or only read data?

It only reads. It looks things up on rossmann.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/rossmann.de/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/rossmann.de/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/rossmann.de/search-products
