# Remove a product from the Micromania cart

Automatically remove a product from the Micromania cart on micromania.fr. Remove a product from the Micromania cart of this browser by its product id, whatever its quantity, and return what is left in the cart: each line with its product id, name, quantity, unit price and line price in euros, plus the item count and the total of the items. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. Works as a guest, with no account.

- Site: micromania.fr
- Address: `reduck/micromania.fr/remove_from_cart`
- Updated: 2026-11-24 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/micromania.fr/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/micromania.fr/remove_from_cart
```

## Input

- `productId` (string, required): Micromania product id of the line to remove, as List Micromania cart items returns it in productId (for example 158402).

## Output

- `count` (integer, required): Units left in the cart.
- `lines` (array, required)
- `total` (number | null, required): Total of the items left, in euros, delivery not included.
- `removed` (boolean, required): True when the product was in the cart and is now gone, false when it was not in the cart.
- `productId` (string, required)

## FAQ

### What does "Remove a product from the Micromania cart" do?

Remove a product from the Micromania cart of this browser by its product id, whatever its quantity, and return what is left in the cart: each line with its product id, name, quantity, unit price and line price in euros, plus the item count and the total of the items. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. Works as a guest, with no account.

### How do I automatically remove a product from the Micromania cart on micromania.fr?

Ask an AI agent connected to Reduck to run reduck/micromania.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/micromania.fr/remove_from_cart

### Is there a micromania.fr API to remove a product from the Micromania cart?

You do not need one. "Remove a product from the Micromania cart" drives the real micromania.fr pages in a browser, so it works whether or not micromania.fr offers an API for this.

### What information do I need to provide?

Required: productId.

### What does it return?

It returns count, lines, total, removed, productId.

### Do I need to be logged in to micromania.fr?

No. It only uses pages of micromania.fr that are reachable without signing in.

### Does it change anything on micromania.fr, or only read data?

It makes changes on micromania.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/micromania.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/micromania.fr/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/micromania.fr/remove_from_cart
