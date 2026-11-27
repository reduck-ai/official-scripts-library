# Remove Newegg product from cart

Automatically remove Newegg product from cart on newegg.com. Remove a product from your Newegg (newegg.com) cart, whatever its quantity, and return the cart after. A product not in the cart returns removed false and changes nothing.

- Site: newegg.com
- Address: `reduck/newegg.com/remove_from_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/newegg.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/newegg.com/remove_from_cart
```

## Input

- `item` (string, required): Newegg item number of the cart line (productId from list_cart_items). The whole line goes, whatever its quantity.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `removed` (boolean, required): False when the product was not in the cart; nothing was changed then.
- `total` (number | null, optional)

## FAQ

### What does "Remove Newegg product from cart" do?

Remove a product from your Newegg (newegg.com) cart, whatever its quantity, and return the cart after. A product not in the cart returns removed false and changes nothing.

### How do I automatically remove Newegg product from cart on newegg.com?

Ask an AI agent connected to Reduck to run reduck/newegg.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/newegg.com/remove_from_cart

### Is there a newegg.com API to remove Newegg product from cart?

You do not need one. "Remove Newegg product from cart" drives the real newegg.com pages in a browser, so it works whether or not newegg.com offers an API for this.

### What information do I need to provide?

Required: item.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to newegg.com?

No. It only uses pages of newegg.com that are reachable without signing in.

### Does it change anything on newegg.com, or only read data?

It makes changes on newegg.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/newegg.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/newegg.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/newegg.com/remove_from_cart
