# Get Cultura product offers

Automatically get Cultura product offers on cultura.com. List the offers for one cultura.com product: Cultura's own (when it sells it) and the marketplace sellers', new and used.

- Site: cultura.com
- Address: `reduck/cultura.com/get-product-offers`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cultura.com/get-product-offers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cultura.com/get-product-offers
```

## Input

- `product` (string, required): A cultura.com product link or a product id from search-products.

## Output

- `id` (string, required)
- `offers` (array, required)
- `offers_count` (integer, required)
- `name` (string | null, optional)

## FAQ

### What does "Get Cultura product offers" do?

List the offers for one cultura.com product: Cultura's own (when it sells it) and the marketplace sellers', new and used.

### How do I automatically get Cultura product offers on cultura.com?

Ask an AI agent connected to Reduck to run reduck/cultura.com/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cultura.com/get-product-offers

### Is there a cultura.com API to get Cultura product offers?

You do not need one. "Get Cultura product offers" drives the real cultura.com pages in a browser, so it works whether or not cultura.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, name, offers, offers_count.

### Do I need to be logged in to cultura.com?

No. It only uses pages of cultura.com that are reachable without signing in.

### Does it change anything on cultura.com, or only read data?

It only reads. It looks things up on cultura.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cultura.com/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cultura.com/get-product-offers

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/cultura.com/get-product-offers
