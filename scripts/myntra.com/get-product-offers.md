# Get Myntra product offers

Automatically get Myntra product offers on myntra.com. List the sellers' offers for one myntra.com product, size by size: sku, size, seller id and name, price and MRP in rupees, and how many are available. Takes the link Search Myntra products returns.

- Site: myntra.com
- Address: `reduck/myntra.com/get-product-offers`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/myntra.com/get-product-offers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/myntra.com/get-product-offers
```

## Input

- `url` (string, required): The product's link as Search Myntra products returns it (https://www.myntra.com/.../<id>/buy).

## Output

- `offers` (array, required)
- `product_id` (string, required)

## FAQ

### What does "Get Myntra product offers" do?

List the sellers' offers for one myntra.com product, size by size: sku, size, seller id and name, price and MRP in rupees, and how many are available. Takes the link Search Myntra products returns.

### How do I automatically get Myntra product offers on myntra.com?

Ask an AI agent connected to Reduck to run reduck/myntra.com/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/myntra.com/get-product-offers

### Is there a myntra.com API to get Myntra product offers?

You do not need one. "Get Myntra product offers" drives the real myntra.com pages in a browser, so it works whether or not myntra.com offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns offers, product_id.

### Do I need to be logged in to myntra.com?

No. It only uses pages of myntra.com that are reachable without signing in.

### Does it change anything on myntra.com, or only read data?

It only reads. It looks things up on myntra.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/myntra.com/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/myntra.com/get-product-offers

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/myntra.com/get-product-offers
