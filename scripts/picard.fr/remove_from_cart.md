# Remove a product from the Picard cart

Automatically remove a product from the Picard cart on picard.fr. Remove a product from the Picard France (picard.fr) cart of this browser by its product id, whatever its quantity, and return what is left in the cart: each line with its line id, product id, name, seller (always Picard), quantity, unit price and line price in euros, plus the item count and the total of the products. Give the line id from List Picard cart items to pick one line when the product is on several lines. Works as a guest, with no account. A product that is not in the cart gives removed false, and nothing is changed.

- Site: picard.fr
- Address: `reduck/picard.fr/remove_from_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/picard.fr/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/picard.fr/remove_from_cart
```

## Input

- `productId` (string, required): The product id from List Picard cart items (leading zeros optional).
- `lineId` (string, optional): The line id from List Picard cart items, to remove one line only.

## Output

- `count` (integer, required): Units left in the cart.
- `lines` (array, required)
- `total` (number | null, required): Total of the products in euros, delivery and loyalty discounts not included.
- `removed` (boolean, required): False when the product was not in the cart.
- `currency` (string, required)

## FAQ

### What does "Remove a product from the Picard cart" do?

Remove a product from the Picard France (picard.fr) cart of this browser by its product id, whatever its quantity, and return what is left in the cart: each line with its line id, product id, name, seller (always Picard), quantity, unit price and line price in euros, plus the item count and the total of the products. Give the line id from List Picard cart items to pick one line when the product is on several lines. Works as a guest, with no account. A product that is not in the cart gives removed false, and nothing is changed.

### How do I automatically remove a product from the Picard cart on picard.fr?

Ask an AI agent connected to Reduck to run reduck/picard.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/picard.fr/remove_from_cart

### Is there a picard.fr API to remove a product from the Picard cart?

You do not need one. "Remove a product from the Picard cart" drives the real picard.fr pages in a browser, so it works whether or not picard.fr offers an API for this.

### What information do I need to provide?

Required: productId. Optional: lineId.

### What does it return?

It returns count, lines, total, removed, currency.

### Do I need to be logged in to picard.fr?

No. It only uses pages of picard.fr that are reachable without signing in.

### Does it change anything on picard.fr, or only read data?

It makes changes on picard.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/picard.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/picard.fr/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/picard.fr/remove_from_cart
