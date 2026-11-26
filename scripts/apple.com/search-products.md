# Search Apple Store products

Automatically search Apple Store products on apple.com. Search the Apple Store (US) for products and accessories with a keyword, one results page at a time. Returns the total number of results, the page count and, for each product, its part number, name, link, price, image and colors.

- Site: apple.com
- Address: `reduck/apple.com/search-products`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/apple.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/apple.com/search-products
```

## Input

- `query` (string, required): Search keywords, for example "usb-c cable".
- `page` (integer, optional): Results page number, starting at 1. The site shows up to 30 products per page.

## Output

- `page` (integer, required)
- `items` (array, required)
- `query` (string, required)
- `has_next_page` (boolean, required)
- `total_pages` (integer | null, optional)
- `total_results` (integer | null, optional)

## FAQ

### What does "Search Apple Store products" do?

Search the Apple Store (US) for products and accessories with a keyword, one results page at a time. Returns the total number of results, the page count and, for each product, its part number, name, link, price, image and colors.

### How do I automatically search Apple Store products on apple.com?

Ask an AI agent connected to Reduck to run reduck/apple.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/apple.com/search-products

### Is there a apple.com API to search Apple Store products?

You do not need one. "Search Apple Store products" drives the real apple.com pages in a browser, so it works whether or not apple.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, items, query, total_pages, has_next_page, total_results.

### Do I need to be logged in to apple.com?

No. It only uses pages of apple.com that are reachable without signing in.

### Does it change anything on apple.com, or only read data?

It only reads. It looks things up on apple.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/apple.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/apple.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/apple.com/search-products
