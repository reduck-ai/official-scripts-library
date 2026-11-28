# Remove a product from the Sam's Club cart

Automatically remove a product from the Sam's Club cart on samsclub.com. Remove a product from the Sam's Club (samsclub.com, US) cart of this browser, by its item id (productId of List Sam's Club cart items), whatever its quantity, and return what is left in the cart: each line with its line id, product id, offer id, name, seller, quantity, unit price and line price in US dollars, plus the item count and the subtotal. A product that is not in the cart is reported with removed false, and nothing is changed. Works as a guest, with no account.

- Site: samsclub.com
- Address: `reduck/samsclub.com/remove_from_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/samsclub.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/samsclub.com/remove_from_cart
```

## Input

- `item_id` (string, required): Item id of the product to remove (productId of List Sam's Club cart items).

## Output

- `count` (integer, required): Number of items left in the cart, all lines together.
- `lines` (array, required)
- `total` (number | null, required): Subtotal of the cart in US dollars, before shipping and tax.
- `removed` (boolean, required): True when the product was in the cart and is removed; false when it was not in the cart.
- `productId` (string, required)

## FAQ

### What does "Remove a product from the Sam's Club cart" do?

Remove a product from the Sam's Club (samsclub.com, US) cart of this browser, by its item id (productId of List Sam's Club cart items), whatever its quantity, and return what is left in the cart: each line with its line id, product id, offer id, name, seller, quantity, unit price and line price in US dollars, plus the item count and the subtotal. A product that is not in the cart is reported with removed false, and nothing is changed. Works as a guest, with no account.

### How do I automatically remove a product from the Sam's Club cart on samsclub.com?

Ask an AI agent connected to Reduck to run reduck/samsclub.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/samsclub.com/remove_from_cart

### Is there a samsclub.com API to remove a product from the Sam's Club cart?

You do not need one. "Remove a product from the Sam's Club cart" drives the real samsclub.com pages in a browser, so it works whether or not samsclub.com offers an API for this.

### What information do I need to provide?

Required: item_id.

### What does it return?

It returns count, lines, total, removed, productId.

### Do I need to be logged in to samsclub.com?

No. It only uses pages of samsclub.com that are reachable without signing in.

### Does it change anything on samsclub.com, or only read data?

It makes changes on samsclub.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/samsclub.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/samsclub.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/samsclub.com/remove_from_cart
