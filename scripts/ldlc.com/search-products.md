# Search LDLC products

Automatically search LDLC products on ldlc.com. Search LDLC.com by free-text query with LDLC's own sort order, one page at a time (about 48 products per page, promoted ones included). Returns the page and page counts, has_next_page and the items: product id (the input of Get LDLC product and Add LDLC product to cart), offer id, title, short description, link, price and struck-through list price in euros, review count, image, stock code, whether the offer comes from a marketplace seller and the badges LDLC shows on the card (promotion, best seller, new). Stop paging when has_next_page is false. A search that matches nothing returns an empty list.

- Site: ldlc.com
- Address: `reduck/ldlc.com/search-products`
- Updated: 2026-11-24 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ldlc.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ldlc.com/search-products
```

## Input

- `query` (string, required): Free-text search query.
- `page` (integer, optional): Result page. has_next_page and total_pages say when to stop.
- `sort` (string, optional): Sort order: relevance (LDLC's default), price_asc (lowest price first), price_desc (highest first), newest, best_sellers.

## Output

- `url` (string, required)
- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `total_pages` (integer | null, required)
- `has_next_page` (boolean, required)

## FAQ

### What does "Search LDLC products" do?

Search LDLC.com by free-text query with LDLC's own sort order, one page at a time (about 48 products per page, promoted ones included). Returns the page and page counts, has_next_page and the items: product id (the input of Get LDLC product and Add LDLC product to cart), offer id, title, short description, link, price and struck-through list price in euros, review count, image, stock code, whether the offer comes from a marketplace seller and the badges LDLC shows on the card (promotion, best seller, new). Stop paging when has_next_page is false. A search that matches nothing returns an empty list.

### How do I automatically search LDLC products on ldlc.com?

Ask an AI agent connected to Reduck to run reduck/ldlc.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ldlc.com/search-products

### Is there a ldlc.com API to search LDLC products?

You do not need one. "Search LDLC products" drives the real ldlc.com pages in a browser, so it works whether or not ldlc.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort.

### What does it return?

It returns url, page, items, query, total_pages, has_next_page.

### Do I need to be logged in to ldlc.com?

No. It only uses pages of ldlc.com that are reachable without signing in.

### Does it change anything on ldlc.com, or only read data?

It only reads. It looks things up on ldlc.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ldlc.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ldlc.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/ldlc.com/search-products
