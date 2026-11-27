# Remove a product from the Micro Center cart

Automatically remove a product from the Micro Center cart on microcenter.com. Remove a line from the Micro Center (microcenter.com) cart of this browser, by its line id or by the product id (from List the items in the Micro Center cart), and return the whole cart afterwards with removed true. A product that is not in the cart is not an error: nothing changes and removed is false. Works as a guest, with no account. Nothing is paid or ordered.

- Site: microcenter.com
- Address: `reduck/microcenter.com/remove_from_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/microcenter.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/microcenter.com/remove_from_cart
```

## Input

- `line_id` (string, optional): Cart line id (lineId of List the items in the Micro Center cart).
- `product_id` (string, optional): Micro Center product id of the product to remove. Used when no line_id is given.

## Output

- `count` (integer, required): Number of units in the cart after the call, all lines together.
- `lines` (array, required)
- `total` (number | null, required): Cart total in US dollars as Micro Center shows it, before tax, with the shipping price of shippable items.
- `removed` (boolean, required): True when a line was removed, false when the product was not in the cart.

## FAQ

### What does "Remove a product from the Micro Center cart" do?

Remove a line from the Micro Center (microcenter.com) cart of this browser, by its line id or by the product id (from List the items in the Micro Center cart), and return the whole cart afterwards with removed true. A product that is not in the cart is not an error: nothing changes and removed is false. Works as a guest, with no account. Nothing is paid or ordered.

### How do I automatically remove a product from the Micro Center cart on microcenter.com?

Ask an AI agent connected to Reduck to run reduck/microcenter.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/microcenter.com/remove_from_cart

### Is there a microcenter.com API to remove a product from the Micro Center cart?

You do not need one. "Remove a product from the Micro Center cart" drives the real microcenter.com pages in a browser, so it works whether or not microcenter.com offers an API for this.

### What information do I need to provide?

Optional: line_id, product_id.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to microcenter.com?

No. It only uses pages of microcenter.com that are reachable without signing in.

### Does it change anything on microcenter.com, or only read data?

It makes changes on microcenter.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/microcenter.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/microcenter.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/microcenter.com/remove_from_cart
