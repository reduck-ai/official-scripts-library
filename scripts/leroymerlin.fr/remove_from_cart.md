# Remove product from Leroy Merlin cart

Automatically remove product from Leroy Merlin cart on leroymerlin.fr. Remove a product from the Leroy Merlin cart of this browser by its product reference, whatever its quantity, and return what is left in the cart: each line with its product reference, offer id, name, seller, quantity, unit price and line price in euros, plus the item count and the items total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. When the same product is in the cart from several offers, pass the offer id to pick the line.

- Site: leroymerlin.fr
- Address: `reduck/leroymerlin.fr/remove_from_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/leroymerlin.fr/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/leroymerlin.fr/remove_from_cart
```

## Input

- `productId` (string, required): Product reference as the cart lists it (productId of List Leroy Merlin cart items), for example 82231854.
- `offerId` (string, optional): Offer id of the line, only needed when the same product is in the cart from several offers.

## Output

- `count` (integer, required): Units in the cart after the removal.
- `lines` (array, required)
- `total` (number | null, required): Items total in euros, taxes included, delivery excluded.
- `removed` (boolean, required): False when the product was not in the cart.
- `productId` (string, required)

## FAQ

### What does "Remove product from Leroy Merlin cart" do?

Remove a product from the Leroy Merlin cart of this browser by its product reference, whatever its quantity, and return what is left in the cart: each line with its product reference, offer id, name, seller, quantity, unit price and line price in euros, plus the item count and the items total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. When the same product is in the cart from several offers, pass the offer id to pick the line.

### How do I automatically remove product from Leroy Merlin cart on leroymerlin.fr?

Ask an AI agent connected to Reduck to run reduck/leroymerlin.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leroymerlin.fr/remove_from_cart

### Is there a leroymerlin.fr API to remove product from Leroy Merlin cart?

You do not need one. "Remove product from Leroy Merlin cart" drives the real leroymerlin.fr pages in a browser, so it works whether or not leroymerlin.fr offers an API for this.

### What information do I need to provide?

Required: productId. Optional: offerId.

### What does it return?

It returns count, lines, total, removed, productId.

### Do I need to be logged in to leroymerlin.fr?

No. It only uses pages of leroymerlin.fr that are reachable without signing in.

### Does it change anything on leroymerlin.fr, or only read data?

It makes changes on leroymerlin.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/leroymerlin.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leroymerlin.fr/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/leroymerlin.fr/remove_from_cart
