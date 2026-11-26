# Get Cdiscount product offers

Automatically get Cdiscount product offers on cdiscount.com. List every seller's offer for one Cdiscount.com product by its sku, cheapest first, one page at a time: offer id (pass it to Add to Cdiscount cart), seller with id, rating, sales count and ships-from country, price and struck-through list price in euros, condition and minimum quantity. Read further pages while has_next_page is true. An unknown sku fails with an error that says so.

- Site: cdiscount.com
- Address: `reduck/cdiscount.com/get-product-offers`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cdiscount.com/get-product-offers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cdiscount.com/get-product-offers
```

## Input

- `sku` (string, required): Cdiscount product id, as Search Cdiscount products returns it, for example aaaqy27804.
- `page` (integer, optional): Page of the offer list, cheapest first. Read further while has_next_page is true.

## Output

- `sku` (string, required)
- `page` (integer, required)
- `count` (integer, required): Offers on this page.
- `title` (string | null, required)
- `offers` (array, required)
- `has_next_page` (boolean, required)

## FAQ

### What does "Get Cdiscount product offers" do?

List every seller's offer for one Cdiscount.com product by its sku, cheapest first, one page at a time: offer id (pass it to Add to Cdiscount cart), seller with id, rating, sales count and ships-from country, price and struck-through list price in euros, condition and minimum quantity. Read further pages while has_next_page is true. An unknown sku fails with an error that says so.

### How do I automatically get Cdiscount product offers on cdiscount.com?

Ask an AI agent connected to Reduck to run reduck/cdiscount.com/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cdiscount.com/get-product-offers

### Is there a cdiscount.com API to get Cdiscount product offers?

You do not need one. "Get Cdiscount product offers" drives the real cdiscount.com pages in a browser, so it works whether or not cdiscount.com offers an API for this.

### What information do I need to provide?

Required: sku. Optional: page.

### What does it return?

It returns sku, page, count, title, offers, has_next_page.

### Do I need to be logged in to cdiscount.com?

No. It only uses pages of cdiscount.com that are reachable without signing in.

### Does it change anything on cdiscount.com, or only read data?

It only reads. It looks things up on cdiscount.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cdiscount.com/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cdiscount.com/get-product-offers

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/cdiscount.com/get-product-offers
