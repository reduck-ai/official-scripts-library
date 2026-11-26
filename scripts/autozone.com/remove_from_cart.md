# Remove a product from the AutoZone cart

Automatically remove a product from the AutoZone cart on autozone.com. Remove a product from the AutoZone cart, whatever its quantity, and return the cart after. A product that is not in the cart leaves the cart unchanged and returns removed false.

- Site: autozone.com
- Address: `reduck/autozone.com/remove_from_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/autozone.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/autozone.com/remove_from_cart
```

## Input

- `product_id` (string, required): AutoZone product id (the productId of a cart line, e.g. 663640) or a product link https://www.autozone.com/p/<name>/<id>.

## Output

- `count` (integer, required): Number of items in the cart (sum of quantities).
- `lines` (array, required)
- `total` (number | null, required): Item subtotal in USD, without tax or shipping.
- `removed` (boolean, required): True when the product was in the cart and is no longer there.

## FAQ

### What does "Remove a product from the AutoZone cart" do?

Remove a product from the AutoZone cart, whatever its quantity, and return the cart after. A product that is not in the cart leaves the cart unchanged and returns removed false.

### How do I automatically remove a product from the AutoZone cart on autozone.com?

Ask an AI agent connected to Reduck to run reduck/autozone.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/autozone.com/remove_from_cart

### Is there a autozone.com API to remove a product from the AutoZone cart?

You do not need one. "Remove a product from the AutoZone cart" drives the real autozone.com pages in a browser, so it works whether or not autozone.com offers an API for this.

### What information do I need to provide?

Required: product_id.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to autozone.com?

No. It only uses pages of autozone.com that are reachable without signing in.

### Does it change anything on autozone.com, or only read data?

It makes changes on autozone.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/autozone.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/autozone.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/autozone.com/remove_from_cart
