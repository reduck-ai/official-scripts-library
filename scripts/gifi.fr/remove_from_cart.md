# Remove from Gifi cart

Automatically remove from Gifi cart on gifi.fr. Remove a product from the Gifi.fr guest cart of this browser by its product id or link, whatever its quantity, and return removed and the cart after: the unit count, the item subtotal in euros and each line with its product id, name, seller, quantity, unit price and line price. A product that is not in the cart gives removed false and the cart unchanged, not an error.

- Site: gifi.fr
- Address: `reduck/gifi.fr/remove_from_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/gifi.fr/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/gifi.fr/remove_from_cart
```

## Input

- `product_id` (string, required): Gifi product id of the line (productId of List Gifi cart items) or its product page link.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required)
- `removed` (boolean, required): False when the product was not in the cart; nothing was changed then.

## FAQ

### What does "Remove from Gifi cart" do?

Remove a product from the Gifi.fr guest cart of this browser by its product id or link, whatever its quantity, and return removed and the cart after: the unit count, the item subtotal in euros and each line with its product id, name, seller, quantity, unit price and line price. A product that is not in the cart gives removed false and the cart unchanged, not an error.

### How do I automatically remove from Gifi cart on gifi.fr?

Ask an AI agent connected to Reduck to run reduck/gifi.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gifi.fr/remove_from_cart

### Is there a gifi.fr API to remove from Gifi cart?

You do not need one. "Remove from Gifi cart" drives the real gifi.fr pages in a browser, so it works whether or not gifi.fr offers an API for this.

### What information do I need to provide?

Required: product_id.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to gifi.fr?

No. It only uses pages of gifi.fr that are reachable without signing in.

### Does it change anything on gifi.fr, or only read data?

It makes changes on gifi.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/gifi.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gifi.fr/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/gifi.fr/remove_from_cart
