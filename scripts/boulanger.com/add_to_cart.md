# Add to Boulanger cart

Automatically add to Boulanger cart on boulanger.com. Add 1 to 10 units of a Boulanger.com product to the cart, from its id (the reference Search Boulanger products returns), and return the cart after the add. Works as a guest: the cart lives with the browser. Nothing is paid or ordered. An unknown id, or a product with no offer to buy, is refused with a clear message.

- Site: boulanger.com
- Address: `reduck/boulanger.com/add_to_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/boulanger.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/boulanger.com/add_to_cart
```

## Input

- `id` (string, required): Boulanger product reference, for example 1204873.
- `quantity` (integer, optional)

## Output

- `id` (string, required)
- `cart` (object, required)
- `added` (integer, required)
- `offer_id` (string, required)

## FAQ

### What does "Add to Boulanger cart" do?

Add 1 to 10 units of a Boulanger.com product to the cart, from its id (the reference Search Boulanger products returns), and return the cart after the add. Works as a guest: the cart lives with the browser. Nothing is paid or ordered. An unknown id, or a product with no offer to buy, is refused with a clear message.

### How do I automatically add to Boulanger cart on boulanger.com?

Ask an AI agent connected to Reduck to run reduck/boulanger.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/boulanger.com/add_to_cart

### Is there a boulanger.com API to add to Boulanger cart?

You do not need one. "Add to Boulanger cart" drives the real boulanger.com pages in a browser, so it works whether or not boulanger.com offers an API for this.

### What information do I need to provide?

Required: id. Optional: quantity.

### What does it return?

It returns id, cart, added, offer_id.

### Do I need to be logged in to boulanger.com?

No. It only uses pages of boulanger.com that are reachable without signing in.

### Does it change anything on boulanger.com, or only read data?

It makes changes on boulanger.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/boulanger.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/boulanger.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/boulanger.com/add_to_cart
