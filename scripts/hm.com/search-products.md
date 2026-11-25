# Search H&M France products

Automatically search H&M France products on hm.com. Search the H&M France shop (hm.com/fr_fr, prices in euros) by free text and return one page of results of about 36 products: id, name, price, colors, sizes with their variant ids and stock, image and link, plus the total count, the page count and the filters the site offers. Page through with page; stop when has_next_page is false. Pass a product id to Get H&M France product, or a variant id (product id plus size code) to Add H&M France product to cart.

- Site: hm.com
- Address: `reduck/hm.com/search-products`
- Updated: 2026-11-24 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hm.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hm.com/search-products
```

## Input

- `query` (string, required): Free-text search, for example "t-shirt blanc".
- `page` (integer, optional): Result page, 1-based. Stop when has_next_page is false.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `filters` (array, required)
- `has_next_page` (boolean, required)
- `total_pages` (integer | null, optional)
- `total_results` (integer | null, optional)

## FAQ

### What does "Search H&M France products" do?

Search the H&M France shop (hm.com/fr_fr, prices in euros) by free text and return one page of results of about 36 products: id, name, price, colors, sizes with their variant ids and stock, image and link, plus the total count, the page count and the filters the site offers. Page through with page; stop when has_next_page is false. Pass a product id to Get H&M France product, or a variant id (product id plus size code) to Add H&M France product to cart.

### How do I automatically search H&M France products on hm.com?

Ask an AI agent connected to Reduck to run reduck/hm.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hm.com/search-products

### Is there a hm.com API to search H&M France products?

You do not need one. "Search H&M France products" drives the real hm.com pages in a browser, so it works whether or not hm.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, filters, total_pages, has_next_page, total_results.

### Do I need to be logged in to hm.com?

No. It only uses pages of hm.com that are reachable without signing in.

### Does it change anything on hm.com, or only read data?

It only reads. It looks things up on hm.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hm.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hm.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hm.com/search-products
