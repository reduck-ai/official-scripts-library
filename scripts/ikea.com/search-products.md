# Search IKEA France products

Automatically search IKEA France products on ikea.com. Search the IKEA France shop (ikea.com/fr/fr, prices in euros) by free text, with the site's own sort order. Returns one page of 24 results: the total number of products, whether another page exists, and for each product its article number, name, type, size, link, price, rating, colors, number of other variants and whether it can be bought online. Stop paging when has_next_page is false. A search with no match returns an empty list. Pass the article number to Get IKEA France product.

- Site: ikea.com
- Address: `reduck/ikea.com/search-products`
- Updated: 2026-11-24 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ikea.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ikea.com/search-products
```

## Input

- `query` (string, required): Free-text search, in French, for example "bougie" or "étagère blanche".
- `page` (integer, optional): Page of results, 24 products per page, starting at 1.
- `sort` (string, optional): Sort order of the site.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `has_next_page` (boolean, required)
- `sort` (string | null, optional)
- `total_results` (integer | null, optional)

## FAQ

### What does "Search IKEA France products" do?

Search the IKEA France shop (ikea.com/fr/fr, prices in euros) by free text, with the site's own sort order. Returns one page of 24 results: the total number of products, whether another page exists, and for each product its article number, name, type, size, link, price, rating, colors, number of other variants and whether it can be bought online. Stop paging when has_next_page is false. A search with no match returns an empty list. Pass the article number to Get IKEA France product.

### How do I automatically search IKEA France products on ikea.com?

Ask an AI agent connected to Reduck to run reduck/ikea.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ikea.com/search-products

### Is there a ikea.com API to search IKEA France products?

You do not need one. "Search IKEA France products" drives the real ikea.com pages in a browser, so it works whether or not ikea.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort.

### What does it return?

It returns page, sort, items, query, has_next_page, total_results.

### Do I need to be logged in to ikea.com?

No. It only uses pages of ikea.com that are reachable without signing in.

### Does it change anything on ikea.com, or only read data?

It only reads. It looks things up on ikea.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ikea.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ikea.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/ikea.com/search-products
