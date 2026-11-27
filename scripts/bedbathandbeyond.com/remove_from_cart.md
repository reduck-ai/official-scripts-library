# Remove from Bed Bath & Beyond cart

Automatically remove from Bed Bath & Beyond cart on bedbathandbeyond.com. Remove a Bed Bath & Beyond product from the cart of this browser, from its id or page link: every option of it, whatever the quantity. Gives the cart after the removal and removed: true, or removed: false when the product was not in the cart.

- Site: bedbathandbeyond.com
- Address: `reduck/bedbathandbeyond.com/remove_from_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bedbathandbeyond.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bedbathandbeyond.com/remove_from_cart
```

## Input

- `product` (string, required): The product id (from list_cart_items or search-products) or the link of its page on bedbathandbeyond.com.

## Output

- `count` (integer, required): The number of items in the cart after the removal.
- `lines` (array, required)
- `total` (number | null, required): The cart total in US dollars.
- `removed` (boolean, required): False when the product was not in the cart.

## FAQ

### What does "Remove from Bed Bath & Beyond cart" do?

Remove a Bed Bath & Beyond product from the cart of this browser, from its id or page link: every option of it, whatever the quantity. Gives the cart after the removal and removed: true, or removed: false when the product was not in the cart.

### How do I automatically remove from Bed Bath & Beyond cart on bedbathandbeyond.com?

Ask an AI agent connected to Reduck to run reduck/bedbathandbeyond.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bedbathandbeyond.com/remove_from_cart

### Is there a bedbathandbeyond.com API to remove from Bed Bath & Beyond cart?

You do not need one. "Remove from Bed Bath & Beyond cart" drives the real bedbathandbeyond.com pages in a browser, so it works whether or not bedbathandbeyond.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to bedbathandbeyond.com?

No. It only uses pages of bedbathandbeyond.com that are reachable without signing in.

### Does it change anything on bedbathandbeyond.com, or only read data?

It makes changes on bedbathandbeyond.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bedbathandbeyond.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bedbathandbeyond.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/bedbathandbeyond.com/remove_from_cart
