# Search PetSmart products

Automatically search PetSmart products on petsmart.com. Search PetSmart products by keyword and return one page of results.

- Site: petsmart.com
- Address: `reduck/petsmart.com/search-products`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/petsmart.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/petsmart.com/search-products
```

## Input

- `query` (string, required): Search words, as typed in the PetSmart search box.
- `page` (integer, optional): Results page, 1 for the first.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `total_pages` (integer | null, required)
- `has_next_page` (boolean, required)
- `total_results` (integer, required)

## FAQ

### What does "Search PetSmart products" do?

Search PetSmart products by keyword and return one page of results.

### How do I automatically search PetSmart products on petsmart.com?

Ask an AI agent connected to Reduck to run reduck/petsmart.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/petsmart.com/search-products

### Is there a petsmart.com API to search PetSmart products?

You do not need one. "Search PetSmart products" drives the real petsmart.com pages in a browser, so it works whether or not petsmart.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, total_pages, has_next_page, total_results.

### Do I need to be logged in to petsmart.com?

No. It only uses pages of petsmart.com that are reachable without signing in.

### Does it change anything on petsmart.com, or only read data?

It only reads. It looks things up on petsmart.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/petsmart.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/petsmart.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/petsmart.com/search-products
