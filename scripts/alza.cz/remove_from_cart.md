# Remove Alza.cz product from cart

Automatically remove Alza.cz product from cart on alza.cz. Remove a product from the Alza.cz cart of this browser by its product id, whatever its quantity, and return what is left in the cart: each line with its product id, name, quantity, unit price and line price in Czech crowns, plus the item count and total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure.

- Site: alza.cz
- Address: `reduck/alza.cz/remove_from_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/alza.cz/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/alza.cz/remove_from_cart
```

## Input

- `productId` (string, required): Product id of the cart line, as List Alza.cz cart items gives it (for example 13308667).

## Output

- `count` (integer, required): Units in the cart after the removal.
- `lines` (array, required)
- `total` (number | null, required): Cart total in Czech crowns, taxes included. Null when the cart is empty.
- `removed` (boolean, required): True when a line was removed, false when the product was not in the cart.

## FAQ

### What does "Remove Alza.cz product from cart" do?

Remove a product from the Alza.cz cart of this browser by its product id, whatever its quantity, and return what is left in the cart: each line with its product id, name, quantity, unit price and line price in Czech crowns, plus the item count and total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure.

### How do I automatically remove Alza.cz product from cart on alza.cz?

Ask an AI agent connected to Reduck to run reduck/alza.cz/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alza.cz/remove_from_cart

### Is there a alza.cz API to remove Alza.cz product from cart?

You do not need one. "Remove Alza.cz product from cart" drives the real alza.cz pages in a browser, so it works whether or not alza.cz offers an API for this.

### What information do I need to provide?

Required: productId.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to alza.cz?

No. It only uses pages of alza.cz that are reachable without signing in.

### Does it change anything on alza.cz, or only read data?

It makes changes on alza.cz, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/alza.cz/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alza.cz/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/alza.cz/remove_from_cart
