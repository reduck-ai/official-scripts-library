# Remove a product from the Auchan cart

Automatically remove a product from the Auchan cart on auchan.fr. Remove a product from the Auchan France (auchan.fr) cart of this browser by its product id, whatever its quantity, and return what is left in the cart: each line with its line id, product id, offer id, name, seller, quantity, unit price and line price in euros, plus the item count and the cart total. Give the offer id or the line id from List Auchan cart items to remove one seller's line only when the product is in the cart from several sellers. Works as a guest, with no account. A product that is not in the cart gives removed false, and nothing is changed.

- Site: auchan.fr
- Address: `reduck/auchan.fr/remove_from_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/auchan.fr/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/auchan.fr/remove_from_cart
```

## Input

- `productId` (string, required): The product id from List Auchan cart items.
- `lineId` (string, optional): The line id from List Auchan cart items, to remove that line only.
- `offerId` (string, optional): The offer id from List Auchan cart items, to remove one seller's line only.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required)
- `removed` (boolean, required): False when the product was not in the cart.
- `currency` (string, required)

## FAQ

### What does "Remove a product from the Auchan cart" do?

Remove a product from the Auchan France (auchan.fr) cart of this browser by its product id, whatever its quantity, and return what is left in the cart: each line with its line id, product id, offer id, name, seller, quantity, unit price and line price in euros, plus the item count and the cart total. Give the offer id or the line id from List Auchan cart items to remove one seller's line only when the product is in the cart from several sellers. Works as a guest, with no account. A product that is not in the cart gives removed false, and nothing is changed.

### How do I automatically remove a product from the Auchan cart on auchan.fr?

Ask an AI agent connected to Reduck to run reduck/auchan.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/auchan.fr/remove_from_cart

### Is there a auchan.fr API to remove a product from the Auchan cart?

You do not need one. "Remove a product from the Auchan cart" drives the real auchan.fr pages in a browser, so it works whether or not auchan.fr offers an API for this.

### What information do I need to provide?

Required: productId. Optional: lineId, offerId.

### What does it return?

It returns count, lines, total, removed, currency.

### Do I need to be logged in to auchan.fr?

No. It only uses pages of auchan.fr that are reachable without signing in.

### Does it change anything on auchan.fr, or only read data?

It makes changes on auchan.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/auchan.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/auchan.fr/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/auchan.fr/remove_from_cart
