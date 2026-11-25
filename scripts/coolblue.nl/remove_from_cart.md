# Remove from Coolblue cart

Automatically remove from Coolblue cart on coolblue.nl. Remove a product from the Coolblue Netherlands (coolblue.nl) shopping cart of this browser by its product number or product link, whatever its quantity, and return what is left in the cart: each line with its line id, product number, name, quantity, unit price and line price in euros, plus the item count and total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. Works as a guest, with no account. A link that is not a Coolblue product page fails with an error.

- Site: coolblue.nl
- Address: `reduck/coolblue.nl/remove_from_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/coolblue.nl/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/coolblue.nl/remove_from_cart
```

## Input

- `product` (string, required): Coolblue product number (the productId of List Coolblue cart items) or a product link.

## Output

- `count` (integer, required): Number of items left in the cart (quantities added up).
- `lines` (array, required)
- `total` (number | null, required): Cart total in euros, VAT included, added up from the lines.
- `removed` (boolean, required): True when the product was in the cart and is gone; false when it was not in the cart.

## FAQ

### What does "Remove from Coolblue cart" do?

Remove a product from the Coolblue Netherlands (coolblue.nl) shopping cart of this browser by its product number or product link, whatever its quantity, and return what is left in the cart: each line with its line id, product number, name, quantity, unit price and line price in euros, plus the item count and total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. Works as a guest, with no account. A link that is not a Coolblue product page fails with an error.

### How do I automatically remove from Coolblue cart on coolblue.nl?

Ask an AI agent connected to Reduck to run reduck/coolblue.nl/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/coolblue.nl/remove_from_cart

### Is there a coolblue.nl API to remove from Coolblue cart?

You do not need one. "Remove from Coolblue cart" drives the real coolblue.nl pages in a browser, so it works whether or not coolblue.nl offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to coolblue.nl?

No. It only uses pages of coolblue.nl that are reachable without signing in.

### Does it change anything on coolblue.nl, or only read data?

It makes changes on coolblue.nl, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/coolblue.nl/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/coolblue.nl/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/coolblue.nl/remove_from_cart
