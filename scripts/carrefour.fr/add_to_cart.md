# Add Carrefour product to cart

Automatically add Carrefour product to cart on carrefour.fr. Add a Carrefour.fr product to this browser's cart from its barcode number or product link, with an optional offer id (Carrefour's or a marketplace seller's, from List Carrefour product offers) and a quantity from 1 to 10, and return the cart afterwards. Without an offer id, the offer the product page shows first is added. Works as a guest. Nothing is paid or ordered. An unknown product, an unknown or unavailable offer, or a quantity above the offer's limit fails with an error.

- Site: carrefour.fr
- Address: `reduck/carrefour.fr/add_to_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/carrefour.fr/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/carrefour.fr/add_to_cart
```

## Input

- `product` (string, required): Barcode number of the product, or a carrefour.fr/p/... link.
- `offer_id` (string, optional): Offer to buy from, from List Carrefour product offers. Leave out for the offer the product page shows first.
- `quantity` (integer, optional)

## Output

- `added` (integer, required)
- `count` (integer, required)
- `lines` (array, required)
- `total` (number, required)
- `offerId` (string, required)
- `productId` (string, required)

## FAQ

### What does "Add Carrefour product to cart" do?

Add a Carrefour.fr product to this browser's cart from its barcode number or product link, with an optional offer id (Carrefour's or a marketplace seller's, from List Carrefour product offers) and a quantity from 1 to 10, and return the cart afterwards. Without an offer id, the offer the product page shows first is added. Works as a guest. Nothing is paid or ordered. An unknown product, an unknown or unavailable offer, or a quantity above the offer's limit fails with an error.

### How do I automatically add Carrefour product to cart on carrefour.fr?

Ask an AI agent connected to Reduck to run reduck/carrefour.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/carrefour.fr/add_to_cart

### Is there a carrefour.fr API to add Carrefour product to cart?

You do not need one. "Add Carrefour product to cart" drives the real carrefour.fr pages in a browser, so it works whether or not carrefour.fr offers an API for this.

### What information do I need to provide?

Required: product. Optional: offer_id, quantity.

### What does it return?

It returns added, count, lines, total, offerId, productId.

### Do I need to be logged in to carrefour.fr?

No. It only uses pages of carrefour.fr that are reachable without signing in.

### Does it change anything on carrefour.fr, or only read data?

It makes changes on carrefour.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/carrefour.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/carrefour.fr/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/carrefour.fr/add_to_cart
