# Search Crate & Barrel products

Automatically search Crate & Barrel products on crateandbarrel.com. Search the Crate & Barrel catalogue (crateandbarrel.com, US) for a query and return one page of products (100 a page, in the site's order): id, name, link, price, regular price, rating, review count, image and color variants, with the total number of results.

- Site: crateandbarrel.com
- Address: `reduck/crateandbarrel.com/search-products`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/crateandbarrel.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/crateandbarrel.com/search-products
```

## Input

- `query` (string, required): Words to search for, as typed in the site's search box (for example "table lamp").
- `page` (integer, optional): Page of results, 100 products a page.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `total_pages` (integer | null, required)
- `has_next_page` (boolean, required)
- `total_results` (integer, required): Number of products the site found for the query.

## FAQ

### What does "Search Crate & Barrel products" do?

Search the Crate & Barrel catalogue (crateandbarrel.com, US) for a query and return one page of products (100 a page, in the site's order): id, name, link, price, regular price, rating, review count, image and color variants, with the total number of results.

### How do I automatically search Crate & Barrel products on crateandbarrel.com?

Ask an AI agent connected to Reduck to run reduck/crateandbarrel.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crateandbarrel.com/search-products

### Is there a crateandbarrel.com API to search Crate & Barrel products?

You do not need one. "Search Crate & Barrel products" drives the real crateandbarrel.com pages in a browser, so it works whether or not crateandbarrel.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, total_pages, has_next_page, total_results.

### Do I need to be logged in to crateandbarrel.com?

No. It only uses pages of crateandbarrel.com that are reachable without signing in.

### Does it change anything on crateandbarrel.com, or only read data?

It only reads. It looks things up on crateandbarrel.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/crateandbarrel.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crateandbarrel.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/crateandbarrel.com/search-products
