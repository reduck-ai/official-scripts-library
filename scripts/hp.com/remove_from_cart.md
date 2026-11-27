# Remove a product from the HP cart

Automatically remove a product from the HP cart on hp.com. Remove a line from the HP US store (hp.com/us-en/shop) cart of this browser, by its line id or by the product's HP part number (from List the items in the HP cart), and return the whole cart afterwards with removed true. A product that is not in the cart is not an error: nothing changes and removed is false. Works as a guest, with no account. Nothing is paid or ordered.

- Site: hp.com
- Address: `reduck/hp.com/remove_from_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hp.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hp.com/remove_from_cart
```

## Input

- `line_id` (string, optional): Cart line id (lineId of List the items in the HP cart).
- `product_id` (string, optional): HP part number of the product to remove, for example 7P8K6AV_1. Used when no line_id is given.

## Output

- `count` (integer, required): Number of units in the cart after the call, all lines together.
- `lines` (array, required)
- `total` (number | null, required): Total of the products in US dollars, before tax and shipping.
- `removed` (boolean, required): True when a line was removed, false when the product was not in the cart.

## FAQ

### What does "Remove a product from the HP cart" do?

Remove a line from the HP US store (hp.com/us-en/shop) cart of this browser, by its line id or by the product's HP part number (from List the items in the HP cart), and return the whole cart afterwards with removed true. A product that is not in the cart is not an error: nothing changes and removed is false. Works as a guest, with no account. Nothing is paid or ordered.

### How do I automatically remove a product from the HP cart on hp.com?

Ask an AI agent connected to Reduck to run reduck/hp.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hp.com/remove_from_cart

### Is there a hp.com API to remove a product from the HP cart?

You do not need one. "Remove a product from the HP cart" drives the real hp.com pages in a browser, so it works whether or not hp.com offers an API for this.

### What information do I need to provide?

Optional: line_id, product_id.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to hp.com?

No. It only uses pages of hp.com that are reachable without signing in.

### Does it change anything on hp.com, or only read data?

It makes changes on hp.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hp.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hp.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hp.com/remove_from_cart
