# Remove from Overstock cart

Automatically remove from Overstock cart on overstock.com. Remove an Overstock product from the cart of this browser, from its id or page link: every option of it, whatever the quantity. Gives the cart after the removal and removed: true, or removed: false when the product was not in the cart.

- Site: overstock.com
- Address: `reduck/overstock.com/remove_from_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/overstock.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/overstock.com/remove_from_cart
```

## Input

- `product` (string, required): The product id (from list_cart_items or search-products) or the link of its page on overstock.com.

## Output

- `count` (integer, required): The number of items in the cart after the removal.
- `lines` (array, required)
- `total` (number | null, required): The estimated cart total in US dollars, before taxes.
- `removed` (boolean, required): False when the product was not in the cart.

## FAQ

### What does "Remove from Overstock cart" do?

Remove an Overstock product from the cart of this browser, from its id or page link: every option of it, whatever the quantity. Gives the cart after the removal and removed: true, or removed: false when the product was not in the cart.

### How do I automatically remove from Overstock cart on overstock.com?

Ask an AI agent connected to Reduck to run reduck/overstock.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/overstock.com/remove_from_cart

### Is there a overstock.com API to remove from Overstock cart?

You do not need one. "Remove from Overstock cart" drives the real overstock.com pages in a browser, so it works whether or not overstock.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to overstock.com?

No. It only uses pages of overstock.com that are reachable without signing in.

### Does it change anything on overstock.com, or only read data?

It makes changes on overstock.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/overstock.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/overstock.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/overstock.com/remove_from_cart
