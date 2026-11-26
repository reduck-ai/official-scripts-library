# Remove from Cdiscount cart

Automatically remove from Cdiscount cart on cdiscount.com. Remove a Cdiscount.com product from the cart, whatever its quantity (every line of that sku, or only the line of one offer_id), and return the cart after. A product not in the cart returns removed false and changes nothing. Works as a guest: the cart lives with the browser.

- Site: cdiscount.com
- Address: `reduck/cdiscount.com/remove_from_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cdiscount.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cdiscount.com/remove_from_cart
```

## Input

- `sku` (string, required): Cdiscount product id (productId in List Cdiscount cart items).
- `offer_id` (string, optional): Only remove the line of this offer. Omit to remove every line of the sku.

## Output

- `cart` (object, required)
- `removed` (boolean, required)

## FAQ

### What does "Remove from Cdiscount cart" do?

Remove a Cdiscount.com product from the cart, whatever its quantity (every line of that sku, or only the line of one offer_id), and return the cart after. A product not in the cart returns removed false and changes nothing. Works as a guest: the cart lives with the browser.

### How do I automatically remove from Cdiscount cart on cdiscount.com?

Ask an AI agent connected to Reduck to run reduck/cdiscount.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cdiscount.com/remove_from_cart

### Is there a cdiscount.com API to remove from Cdiscount cart?

You do not need one. "Remove from Cdiscount cart" drives the real cdiscount.com pages in a browser, so it works whether or not cdiscount.com offers an API for this.

### What information do I need to provide?

Required: sku. Optional: offer_id.

### What does it return?

It returns cart, removed.

### Do I need to be logged in to cdiscount.com?

No. It only uses pages of cdiscount.com that are reachable without signing in.

### Does it change anything on cdiscount.com, or only read data?

It makes changes on cdiscount.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cdiscount.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cdiscount.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/cdiscount.com/remove_from_cart
