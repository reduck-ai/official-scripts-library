# List Carrefour product offers

Automatically list Carrefour product offers on carrefour.fr. List every offer Carrefour.fr shows for one product, from its barcode number or product link: Carrefour's own offers and each marketplace seller's, with offer id, seller name and id, price in euros, shipping price and days, availability, purchase limit and the seller's rating. Pass an offer id to Add Carrefour product to cart to buy from that seller. An unknown barcode number fails with an error that says so.

- Site: carrefour.fr
- Address: `reduck/carrefour.fr/get-product-offers`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/carrefour.fr/get-product-offers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/carrefour.fr/get-product-offers
```

## Input

- `product` (string, required): Barcode number of the product (8 to 14 digits), or a carrefour.fr/p/... link.

## Output

- `id` (string, required)
- `title` (string, required)
- `offers` (array, required)

## FAQ

### What does "List Carrefour product offers" do?

List every offer Carrefour.fr shows for one product, from its barcode number or product link: Carrefour's own offers and each marketplace seller's, with offer id, seller name and id, price in euros, shipping price and days, availability, purchase limit and the seller's rating. Pass an offer id to Add Carrefour product to cart to buy from that seller. An unknown barcode number fails with an error that says so.

### How do I automatically list Carrefour product offers on carrefour.fr?

Ask an AI agent connected to Reduck to run reduck/carrefour.fr/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/carrefour.fr/get-product-offers

### Is there a carrefour.fr API to list Carrefour product offers?

You do not need one. "List Carrefour product offers" drives the real carrefour.fr pages in a browser, so it works whether or not carrefour.fr offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, title, offers.

### Do I need to be logged in to carrefour.fr?

No. It only uses pages of carrefour.fr that are reachable without signing in.

### Does it change anything on carrefour.fr, or only read data?

It only reads. It looks things up on carrefour.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/carrefour.fr/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/carrefour.fr/get-product-offers

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/carrefour.fr/get-product-offers
