# Search Myntra products

Automatically search Myntra products on myntra.com. Search myntra.com by keyword, one results page at a time: each product's id, link, name, brand, price and MRP in rupees, discount, rating, rating count, sizes, gender, category, colour and image, with the result count and whether more pages follow.

- Site: myntra.com
- Address: `reduck/myntra.com/search-products`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/myntra.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/myntra.com/search-products
```

## Input

- `query` (string, required): Words to search for, as typed in Myntra's search box (e.g. "tshirts" or "puma running shoes").
- `page` (integer, optional): Results page, from 1.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `has_next_page` (boolean, required)
- `total_results` (integer | null, optional)

## FAQ

### What does "Search Myntra products" do?

Search myntra.com by keyword, one results page at a time: each product's id, link, name, brand, price and MRP in rupees, discount, rating, rating count, sizes, gender, category, colour and image, with the result count and whether more pages follow.

### How do I automatically search Myntra products on myntra.com?

Ask an AI agent connected to Reduck to run reduck/myntra.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/myntra.com/search-products

### Is there a myntra.com API to search Myntra products?

You do not need one. "Search Myntra products" drives the real myntra.com pages in a browser, so it works whether or not myntra.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, has_next_page, total_results.

### Do I need to be logged in to myntra.com?

No. It only uses pages of myntra.com that are reachable without signing in.

### Does it change anything on myntra.com, or only read data?

It only reads. It looks things up on myntra.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/myntra.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/myntra.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/myntra.com/search-products
