# Remove product from emag.ro cart

Automatically remove product from emag.ro cart on emag.ro. Remove a product from the emag.ro cart of this browser by its product id, whatever its quantity, and return what is left in the cart: each line with its product id, offer id, name, seller, quantity, unit price and line price in lei (RON), plus the item count and products total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. When the same product is in the cart from several sellers, pass the offer id to pick the line.

- Site: emag.ro
- Address: `reduck/emag.ro/remove_from_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/emag.ro/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/emag.ro/remove_from_cart
```

## Input

- `productId` (string, required): Product id of the cart line, as List emag.ro cart items gives it (for example 54764942).
- `offerId` (string, optional): Offer id of the line, as List emag.ro cart items gives it. Needed only when the same product is in the cart from several sellers.

## Output

- `count` (integer, required): Units in the cart after the removal.
- `lines` (array, required)
- `total` (number | null, required): Products total in lei, taxes included.
- `removed` (boolean, required): True when a line was removed, false when the product was not in the cart.

## FAQ

### What does "Remove product from emag.ro cart" do?

Remove a product from the emag.ro cart of this browser by its product id, whatever its quantity, and return what is left in the cart: each line with its product id, offer id, name, seller, quantity, unit price and line price in lei (RON), plus the item count and products total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. When the same product is in the cart from several sellers, pass the offer id to pick the line.

### How do I automatically remove product from emag.ro cart on emag.ro?

Ask an AI agent connected to Reduck to run reduck/emag.ro/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/emag.ro/remove_from_cart

### Is there a emag.ro API to remove product from emag.ro cart?

You do not need one. "Remove product from emag.ro cart" drives the real emag.ro pages in a browser, so it works whether or not emag.ro offers an API for this.

### What information do I need to provide?

Required: productId. Optional: offerId.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to emag.ro?

No. It only uses pages of emag.ro that are reachable without signing in.

### Does it change anything on emag.ro, or only read data?

It makes changes on emag.ro, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/emag.ro/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/emag.ro/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/emag.ro/remove_from_cart
