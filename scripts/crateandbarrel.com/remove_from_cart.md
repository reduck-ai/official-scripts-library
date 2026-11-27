# Remove from Crate & Barrel cart

Automatically remove from Crate & Barrel cart on crateandbarrel.com. Remove a product from the Crate & Barrel cart (crateandbarrel.com, US) of this browser, by product id or link, whatever its quantity. A product that is not in the cart leaves the cart unchanged and returns removed false. Returns the cart after the removal.

- Site: crateandbarrel.com
- Address: `reduck/crateandbarrel.com/remove_from_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/crateandbarrel.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/crateandbarrel.com/remove_from_cart
```

## Input

- `product_id` (string, required): Product id (the number after /s in a product link, the productId of a cart line) or the product link.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required): Item subtotal in USD, without tax or shipping.
- `removed` (boolean, required): True when the product was in the cart and is no longer in it.

## FAQ

### What does "Remove from Crate & Barrel cart" do?

Remove a product from the Crate & Barrel cart (crateandbarrel.com, US) of this browser, by product id or link, whatever its quantity. A product that is not in the cart leaves the cart unchanged and returns removed false. Returns the cart after the removal.

### How do I automatically remove from Crate & Barrel cart on crateandbarrel.com?

Ask an AI agent connected to Reduck to run reduck/crateandbarrel.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crateandbarrel.com/remove_from_cart

### Is there a crateandbarrel.com API to remove from Crate & Barrel cart?

You do not need one. "Remove from Crate & Barrel cart" drives the real crateandbarrel.com pages in a browser, so it works whether or not crateandbarrel.com offers an API for this.

### What information do I need to provide?

Required: product_id.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to crateandbarrel.com?

No. It only uses pages of crateandbarrel.com that are reachable without signing in.

### Does it change anything on crateandbarrel.com, or only read data?

It makes changes on crateandbarrel.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/crateandbarrel.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crateandbarrel.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/crateandbarrel.com/remove_from_cart
