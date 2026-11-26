# Remove from Boulanger cart

Automatically remove from Boulanger cart on boulanger.com. Remove a Boulanger.com product from the cart, whatever its quantity, by its id, and return the cart after. A product not in the cart returns removed false and changes nothing. Works as a guest: the cart lives with the browser.

- Site: boulanger.com
- Address: `reduck/boulanger.com/remove_from_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/boulanger.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/boulanger.com/remove_from_cart
```

## Input

- `id` (string, required): Boulanger product reference (productId in List Boulanger cart items).

## Output

- `cart` (object, required)
- `removed` (boolean, required)

## FAQ

### What does "Remove from Boulanger cart" do?

Remove a Boulanger.com product from the cart, whatever its quantity, by its id, and return the cart after. A product not in the cart returns removed false and changes nothing. Works as a guest: the cart lives with the browser.

### How do I automatically remove from Boulanger cart on boulanger.com?

Ask an AI agent connected to Reduck to run reduck/boulanger.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/boulanger.com/remove_from_cart

### Is there a boulanger.com API to remove from Boulanger cart?

You do not need one. "Remove from Boulanger cart" drives the real boulanger.com pages in a browser, so it works whether or not boulanger.com offers an API for this.

### What information do I need to provide?

Required: id.

### What does it return?

It returns cart, removed.

### Do I need to be logged in to boulanger.com?

No. It only uses pages of boulanger.com that are reachable without signing in.

### Does it change anything on boulanger.com, or only read data?

It makes changes on boulanger.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/boulanger.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/boulanger.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/boulanger.com/remove_from_cart
