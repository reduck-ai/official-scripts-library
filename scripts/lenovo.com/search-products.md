# Search Lenovo products

Automatically search Lenovo products on lenovo.com. Search the Lenovo US store (lenovo.com/us/en) by free text and get one page of products, 20 per page, in the order of Lenovo's default sort (recommended). For each product: the product code (pass it to Get a Lenovo product), name, model name, link, price, list price and saving in US dollars, rating, review count, sales status, stock flag, shipping message, outlet flag and image. Also gives the total number of products, the number of pages and whether a next page exists. Lenovo can answer a query it does not understand with loosely related products. A page after the last page gives an empty list. When Lenovo shows its "Access Denied" page, the run fails and says so.

- Site: lenovo.com
- Address: `reduck/lenovo.com/search-products`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/lenovo.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/lenovo.com/search-products
```

## Input

- `query` (string, required): Free-text search, for example "thinkpad x1 carbon".
- `page` (integer, optional): Results page, 20 products per page. Stop when has_next_page is false.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `page_count` (integer | null, required)
- `total_count` (integer | null, required): Number of products that match, all pages together.
- `has_next_page` (boolean, required)

## FAQ

### What does "Search Lenovo products" do?

Search the Lenovo US store (lenovo.com/us/en) by free text and get one page of products, 20 per page, in the order of Lenovo's default sort (recommended). For each product: the product code (pass it to Get a Lenovo product), name, model name, link, price, list price and saving in US dollars, rating, review count, sales status, stock flag, shipping message, outlet flag and image. Also gives the total number of products, the number of pages and whether a next page exists. Lenovo can answer a query it does not understand with loosely related products. A page after the last page gives an empty list. When Lenovo shows its "Access Denied" page, the run fails and says so.

### How do I automatically search Lenovo products on lenovo.com?

Ask an AI agent connected to Reduck to run reduck/lenovo.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lenovo.com/search-products

### Is there a lenovo.com API to search Lenovo products?

You do not need one. "Search Lenovo products" drives the real lenovo.com pages in a browser, so it works whether or not lenovo.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, page_count, total_count, has_next_page.

### Do I need to be logged in to lenovo.com?

No. It only uses pages of lenovo.com that are reachable without signing in.

### Does it change anything on lenovo.com, or only read data?

It only reads. It looks things up on lenovo.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/lenovo.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lenovo.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/lenovo.com/search-products
