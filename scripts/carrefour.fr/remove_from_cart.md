# Remove Carrefour product from cart

Automatically remove Carrefour product from cart on carrefour.fr. Remove a product's line from this browser's Carrefour.fr cart by barcode number, whatever its quantity, and return the cart left. Takes the line's review_hash from List Carrefour cart items: when it is missing or the line changed since, nothing is removed and the error gives the line as it is now and its hash. When the product is in the cart from several offers, pass the offer id. A product not in the cart returns removed false.

- Site: carrefour.fr
- Address: `reduck/carrefour.fr/remove_from_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/carrefour.fr/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/carrefour.fr/remove_from_cart
```

## Input

- `product` (string, required): Barcode number as List Carrefour cart items gives it, or a carrefour.fr/p/... link.
- `offer_id` (string, optional): Offer id of the line, only needed when the product is in the cart from several offers.
- `review_hash` (string, optional): review_hash of the line, from List Carrefour cart items.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number, required)
- `removed` (boolean, required)

## FAQ

### What does "Remove Carrefour product from cart" do?

Remove a product's line from this browser's Carrefour.fr cart by barcode number, whatever its quantity, and return the cart left. Takes the line's review_hash from List Carrefour cart items: when it is missing or the line changed since, nothing is removed and the error gives the line as it is now and its hash. When the product is in the cart from several offers, pass the offer id. A product not in the cart returns removed false.

### How do I automatically remove Carrefour product from cart on carrefour.fr?

Ask an AI agent connected to Reduck to run reduck/carrefour.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/carrefour.fr/remove_from_cart

### Is there a carrefour.fr API to remove Carrefour product from cart?

You do not need one. "Remove Carrefour product from cart" drives the real carrefour.fr pages in a browser, so it works whether or not carrefour.fr offers an API for this.

### What information do I need to provide?

Required: product. Optional: offer_id, review_hash.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to carrefour.fr?

No. It only uses pages of carrefour.fr that are reachable without signing in.

### Does it change anything on carrefour.fr, or only read data?

It makes changes on carrefour.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/carrefour.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/carrefour.fr/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/carrefour.fr/remove_from_cart
