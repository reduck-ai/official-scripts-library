# Remove BUT.fr product from cart

Automatically remove BUT.fr product from cart on but.fr. Remove a product from the BUT.fr cart of this browser by its product id, whatever its quantity, and return what is left in the cart: each line with its product id, name, seller, quantity, unit price and line price in euros, plus the item count and total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure.

- Site: but.fr
- Address: `reduck/but.fr/remove_from_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/but.fr/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/but.fr/remove_from_cart
```

## Input

- `productId` (string, required): Product id of the cart line, as List BUT cart items gives it (for example 4894223246194).

## Output

- `count` (integer, required): Units in the cart after the removal.
- `lines` (array, required)
- `total` (number | null, required): Cart total in euros, taxes included.
- `removed` (boolean, required): True when a line was removed, false when the product was not in the cart.

## FAQ

### What does "Remove BUT.fr product from cart" do?

Remove a product from the BUT.fr cart of this browser by its product id, whatever its quantity, and return what is left in the cart: each line with its product id, name, seller, quantity, unit price and line price in euros, plus the item count and total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure.

### How do I automatically remove BUT.fr product from cart on but.fr?

Ask an AI agent connected to Reduck to run reduck/but.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/but.fr/remove_from_cart

### Is there a but.fr API to remove BUT.fr product from cart?

You do not need one. "Remove BUT.fr product from cart" drives the real but.fr pages in a browser, so it works whether or not but.fr offers an API for this.

### What information do I need to provide?

Required: productId.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to but.fr?

No. It only uses pages of but.fr that are reachable without signing in.

### Does it change anything on but.fr, or only read data?

It makes changes on but.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/but.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/but.fr/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/but.fr/remove_from_cart
