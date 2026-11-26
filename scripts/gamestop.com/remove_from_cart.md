# Remove from GameStop cart

Automatically remove from GameStop cart on gamestop.com. Remove a product from the GameStop cart of the browser, whatever its quantity, and return the cart. A product that is not in the cart leaves it unchanged.

- Site: gamestop.com
- Address: `reduck/gamestop.com/remove_from_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/gamestop.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/gamestop.com/remove_from_cart
```

## Input

- `product_id` (string, required): GameStop product id (the variant id of the cart line, or its product id) or product link.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required)
- `removed` (boolean, required)

## FAQ

### What does "Remove from GameStop cart" do?

Remove a product from the GameStop cart of the browser, whatever its quantity, and return the cart. A product that is not in the cart leaves it unchanged.

### How do I automatically remove from GameStop cart on gamestop.com?

Ask an AI agent connected to Reduck to run reduck/gamestop.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gamestop.com/remove_from_cart

### Is there a gamestop.com API to remove from GameStop cart?

You do not need one. "Remove from GameStop cart" drives the real gamestop.com pages in a browser, so it works whether or not gamestop.com offers an API for this.

### What information do I need to provide?

Required: product_id.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to gamestop.com?

No. It only uses pages of gamestop.com that are reachable without signing in.

### Does it change anything on gamestop.com, or only read data?

It makes changes on gamestop.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/gamestop.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gamestop.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/gamestop.com/remove_from_cart
