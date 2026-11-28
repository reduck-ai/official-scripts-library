# Get Kaufland product offers

Automatically get Kaufland product offers on kaufland.de. List every seller's offer for one kaufland.de product, new and used: offer id, price and shipping fee in euros, delivery window, who ships it, and the seller with its return period. Pass an offer id to Add to Kaufland cart to buy from that seller. Takes the link Search Kaufland products returns.

- Site: kaufland.de
- Address: `reduck/kaufland.de/get-product-offers`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/kaufland.de/get-product-offers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/kaufland.de/get-product-offers
```

## Input

- `url` (string, required): The product's link as Search Kaufland products returns it (https://www.kaufland.de/product/<id>/).

## Output

- `offers` (array, required)
- `product_id` (string, required)

## FAQ

### What does "Get Kaufland product offers" do?

List every seller's offer for one kaufland.de product, new and used: offer id, price and shipping fee in euros, delivery window, who ships it, and the seller with its return period. Pass an offer id to Add to Kaufland cart to buy from that seller. Takes the link Search Kaufland products returns.

### How do I automatically get Kaufland product offers on kaufland.de?

Ask an AI agent connected to Reduck to run reduck/kaufland.de/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kaufland.de/get-product-offers

### Is there a kaufland.de API to get Kaufland product offers?

You do not need one. "Get Kaufland product offers" drives the real kaufland.de pages in a browser, so it works whether or not kaufland.de offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns offers, product_id.

### Do I need to be logged in to kaufland.de?

No. It only uses pages of kaufland.de that are reachable without signing in.

### Does it change anything on kaufland.de, or only read data?

It only reads. It looks things up on kaufland.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/kaufland.de/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kaufland.de/get-product-offers

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/kaufland.de/get-product-offers
