# Get Instacart product offers

Automatically get Instacart product offers on instacart.com. List the stores that sell one Instacart.com product in the delivery area Instacart has for this browser, with each store's price in US dollars, its regular price when discounted and the discount text. Returns the postal code used. Pass a store's slug to Search Instacart store products or Add to Instacart cart.

- Site: instacart.com
- Address: `reduck/instacart.com/get-product-offers`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instacart.com/get-product-offers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instacart.com/get-product-offers
```

## Input

- `product` (string, required): An Instacart product id (e.g. "16408559") or a product link containing /products/<id>.

## Output

- `offers` (array, required)
- `productId` (string, required)
- `postal_code` (string | null, optional)

## FAQ

### What does "Get Instacart product offers" do?

List the stores that sell one Instacart.com product in the delivery area Instacart has for this browser, with each store's price in US dollars, its regular price when discounted and the discount text. Returns the postal code used. Pass a store's slug to Search Instacart store products or Add to Instacart cart.

### How do I automatically get Instacart product offers on instacart.com?

Ask an AI agent connected to Reduck to run reduck/instacart.com/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instacart.com/get-product-offers

### Is there a instacart.com API to get Instacart product offers?

You do not need one. "Get Instacart product offers" drives the real instacart.com pages in a browser, so it works whether or not instacart.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns offers, productId, postal_code.

### Do I need to be logged in to instacart.com?

No. It only uses pages of instacart.com that are reachable without signing in.

### Does it change anything on instacart.com, or only read data?

It only reads. It looks things up on instacart.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instacart.com/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instacart.com/get-product-offers

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/instacart.com/get-product-offers
